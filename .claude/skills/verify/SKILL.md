---
name: verify
description: Build-free runtime verification recipe for the Night Flight single-file PWA. Use when verifying changes to index.html or sw.js by driving the app in a browser.
user-invocable: false
---

# Verifying Night Flight

Single-file vanilla PWA — no build step. Serve the repo root and drive it in a real browser.

## Serve

```bash
cd <repo-root> && python3 -m http.server 8124 &
```

## Drive (remote CCR environment)

Chromium is pre-installed at `/opt/pw-browsers/chromium` (a symlink to the real binary — pass it as `executablePath`, do NOT run `playwright install`). Install `playwright-core` in the scratchpad, not the repo:

```js
import { chromium } from 'playwright-core';
const browser = await chromium.launch({ executablePath: '/opt/pw-browsers/chromium', args: ['--no-sandbox'] });
const ctx = await browser.newContext({ viewport: {width:1440,height:900}, colorScheme: 'dark' });
```

Use a fresh `browser.newContext()` per scenario — the app saves to session/localStorage and the service worker caches aggressively, so shared contexts leak state between checks.

## Flows worth driving

- Boarding → `#beginBtn` → walk legs with `#nextBtn` (7 clicks reaches the landing card). At landing, `#hudTime` must read `Landed` and `#progressTrack.value` must be 7.
- Theme: `#themeBtn` toggles `html.light`, updates `meta[name=theme-color]`, persists via `localStorage['nightFlight.theme.v1']`. No stored key → follows `prefers-color-scheme`.
- Resume: fill `#mentalDump`, wait ≥600ms (debounced save), reload → `#resumeBox.show`, `#resumeBtn` restores step + text.
- Emulate `colorScheme: 'light'`, `reducedMotion: 'reduce'`, and a 390×844 `isMobile` context; check `document.documentElement.scrollWidth - clientWidth === 0` for overflow.
- Screenshot both themes — most regressions here are visual, not functional.

## Gotchas

- The atmosphere layers (`.sky`, `#stars`, `.cloud`) are fixed elements with negative z-index. `body` background MUST stay `transparent` — an opaque body background paints over negative-z children and silently hides the entire sky system (this shipped broken once).
- Bump `CACHE_NAME` in `sw.js` for any user-visible change, or returning clients get the cache-first stale copy.
- Headless Chromium via raw `--window-size=390,...` clamps to a wider min width; use Playwright viewport emulation for real mobile rendering.
- `--virtual-time-budget` screenshots catch panels mid `panelIn` animation; prefer Playwright with a ~700ms settle wait.
