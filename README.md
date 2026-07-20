# Selfection

A tool that helps you reflect on yourself and understand yourself more deeply in the present moment.

## Night Flight

Night Flight is a private guided reflection designed for a quiet period without reliable internet. It helps a user turn one live question into a working hypothesis, a boundary and one seven day behaviour experiment.

## Deploy on GitHub Pages

1. Create a repository and copy the contents of this folder into its root.
2. In the repository settings, open Pages and deploy from the main branch root.
3. Open the published page once while online.
4. Wait until the boarding screen says `Ready for offline use` before relying on it without a connection.

The service worker caches the complete app shell. Update `CACHE_NAME` in `sw.js` whenever a deployed release must replace the existing offline copy.

## Install on iPhone

1. Open the published page in Safari while online.
2. Tap Share, then choose Add to Home Screen.
3. Launch Night Flight once from the Home Screen and wait for the offline readiness message.
4. When installed, file exports use the iPhone share sheet so the user can save them to Files, Notes or another chosen destination.

The interface accounts for display cutouts, the Home indicator, Safari text scaling, short landscape screens and the changing viewport while the keyboard is visible. Fixed navigation is hidden during text entry so it does not cover the active field.

## Privacy

The app has no analytics, account, remote fonts or content processing. Reflection text stays in the browser unless the user explicitly exports or shares it.

The default storage option uses `sessionStorage`, which survives a refresh in the current tab session. Optional device storage uses `localStorage` and persists in the same browser profile. Device storage is convenient but is not encrypted and may be visible to anyone who can access that profile.

## Evidence boundaries

This is an evidence informed reflection tool, not therapy, diagnosis or a validated psychological assessment. The combined Night Flight sequence has not been clinically validated.

The psychological needs section is a short custom reflection inspired by Self Determination Theory. It is not the validated Basic Psychological Need Satisfaction and Frustration Scale.

The difficult signal section treats envy, strong reactions and guilt as possible sources of information rather than proof of a hidden trait or motive.

The action section uses implementation intention principles while first checking that the selected goal matters to the user.

## Release checks

Before publishing a new version, check:

1. The whole session on a narrow phone screen and a desktop screen.
2. Refresh recovery in both temporary and device storage modes.
3. Offline loading after the service worker reports readiness.
4. Keyboard navigation and visible focus on every control.
5. Reduced motion and low power visual modes.
6. Markdown, JSON and calendar downloads.
7. Copy, Share and Print in at least one current Chromium browser and Safari.
8. Erasing a saved session without removing previously downloaded files.
