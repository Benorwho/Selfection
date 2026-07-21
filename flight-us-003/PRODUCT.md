# Flight US 003

## Product description

Flight US 003 is a private anniversary reflection and planning experience for two people. It turns a relationship review into a cinematic, cooperative ritual rather than a form, a test or a therapy exercise.

The experience is designed primarily for one laptop or iPad passed between two partners. It also adapts to iPhone and desktop. Private answers are collected in separate sealed capsules, followed by shared reveals, playful prediction comparisons, a future planning sequence and a generated anniversary presentation.

The third anniversary edition uses the number three as a recurring structure: three words, three memories, three predictions, three future directions and one shared ninety day experiment.

## Core promise

In one guided session, a couple should leave with:

1. A richer shared story of their previous year.
2. A clearer understanding of what each person experienced differently.
3. A safe way to name what they want more of, less of and protected.
4. A small set of shared priorities rather than an overwhelming wish list.
5. One realistic relationship experiment for the next ninety days.
6. A beautiful landing card and time capsule for their next anniversary.

## What the experience is not

Flight US 003 is not a compatibility score, diagnostic assessment, conflict resolution system or substitute for couples therapy. It does not determine who is right. Differences are treated as discoveries, not failures.

## Primary use case

The recommended setup is one laptop or iPad, a quiet room, drinks or snacks, and sixty to ninety minutes without interruptions. Each partner completes a private capsule while the other person looks away or leaves briefly. The device is then passed across a privacy curtain before the shared reveal begins.

The interface also works on iPhone. Touch targets, safe areas, keyboard resizing, internal scrolling and swipe navigation are designed for small screens.

## Experience principles

1. Private before shared. Each person needs space to identify their own experience before adapting it to their partner.
2. Curiosity before response. Reveal moments invite questions before explanation or defence.
3. Similarity is not the goal. A surprising answer earns as much attention as an accurate prediction.
4. Celebration and honesty can coexist. Positive memories and difficult material are both included, but the emotional intensity remains bounded.
5. Plans stay small. The session ends with rituals, support and one experiment rather than a complete relationship overhaul.
6. Privacy is visible. The app explains where answers are stored and offers a temporary tab mode by default.
7. The aesthetic carries meaning. Two flight paths gradually converge as the session moves from separate reflection to shared direction.

## Session structure

### Boarding

The couple enters their names, anniversary date, preferred pace and storage choice. They agree to listen without interrupting, avoid scoring the relationship, use the Talk Later option when needed and pause if the conversation becomes unconstructive.

### Private capsule for each partner

Each partner completes the same seven short chapters:

1. Three words for the year.
2. Three memories: joyful, difficult and beautifully ordinary.
3. Moments of love, difficulty and pride.
4. More, less, protect, support and a personal dream.
5. Three predictions about their partner.
6. What to leave behind, take responsibility for or forgive.
7. Three future destinations selected from ten life directions.

Answers in the baggage chapter can be marked Share Now, Talk Later or Keep Private. Keep Private answers never appear in the shared presentation.

### Device pass

After the first capsule is sealed, a full screen privacy curtain asks the couple to pass the device. The second partner cannot see the first partner’s answers while completing their capsule.

### Shared reveal

The couple reunites for five presentation chapters:

1. Their year in words and memories.
2. Prediction cards comparing what one person expected with what the other actually said.
3. More, less and protect cards shown side by side.
4. Share Now baggage, with Talk Later items represented only as sealed conversation cards.
5. Future destinations, highlighting overlaps without treating differences as disagreement.

Prediction cards use three reactions: You Knew Me, Close and Plot Twist. These create curiosity stars for the couple as a team. They are not points awarded to individuals.

### Shared flight plan

The couple chooses:

1. One weekly ritual.
2. One monthly date rhythm.
3. One shared adventure.
4. One practical improvement.
5. One way to support each person’s individual dream.
6. One promise about what to protect during stressful periods.
7. One ninety day experiment with a cue, action, minimum version and fallback.
8. A review date.

### Time capsule and landing

The couple writes one shared letter to their fourth anniversary selves. The app compiles a cinematic landing card and presentation containing memories, discoveries, chosen directions and plans.

The result can be copied, printed, downloaded as Markdown, downloaded as JSON or added to a calendar as a review reminder.

## Interaction model

The interface uses one scene per viewport. There is no long page scroll. Content that exceeds the available height scrolls only inside its scene card.

Navigation supports:

1. Large Next and Back controls.
2. Arrow keys when a text field is not active.
3. Horizontal swipe gestures on touch devices.
4. Direct Continue controls after private sealing and reveal interactions.

GSAP controls scene entrances, exits, depth shifts, constellation movement, flight path convergence and reveal animations. Reduced Motion removes nonessential movement without removing content.

## Visual direction

The visual world begins with two separate twilight routes. Private chapters use slightly different warm and cool accents for each partner. During reunion, the paths bend toward each other. The final planning and landing chapters share a dawn palette.

The desired atmosphere is intimate, elegant and slightly magical. It should feel closer to an interactive title sequence than a productivity dashboard.

## Privacy model

The default mode stores text in the current browser tab. Optional device storage uses local browser storage. No answers, names, images or analytics are transmitted.

Selected photos remain in browser memory for the current session and are not written into saved text data. Reloading may remove them. Exported JSON and Markdown contain text only.

## Emotional safety

Every private baggage answer has a visibility choice. Both partners can open a pause overlay at any time. The overlay offers breathing guidance, a Talk Later option and a route directly to shared planning.

The interface avoids diagnostic language, hidden personality claims and relationship scoring. It reminds users that a memory, prediction or unmet want is one person’s experience, not objective proof about the other person.

## Technical shape

Flight US 003 is a static offline web application suitable for GitHub Pages. It contains no server, account, analytics or remote font dependency. GSAP is included locally. A service worker caches the complete app shell after the first online visit.

The project can later support additional anniversary editions, encrypted device transfer, optional QR based pairing, audio memories and richer presentation exports without changing the core private then shared structure.
