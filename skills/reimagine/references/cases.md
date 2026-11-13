# Worked cases

Five real reimagines, anonymized. Each shows the request, what was measured, the diagnosis, the move
and how the user reacted. The user reacted best to concrete structures, measured numbers, reasoned
changes to their own sketch, and a clear "no, because" when an idea would hurt.

## 1. Long-form video pipeline

- **Request**: "Fastest, easiest, least chaotic way to make these videos. Impeccable, almost on the
  first try."
- **Measured**: the channel's manual, the taste log, the style guide, the editing code, and the
  history of the first three videos. About 15 new rules appeared after review in video 3; four docs
  (~300 lines) contradicted each other; a pause change redrew 91 of 94 scenes; 519 lines of scene code
  were written per video; three generations of the tool coexisted.
- **Diagnosis**: rules born at review; contradictory sources; expensive (voice, render) before cheap
  (rhythm); the agent can't hear, so the human was the audio QA; every video designed from scratch.
- **Move**: one channel bible with rules as numbers; a library of ~12 approved scene parts; a free
  preview with computer voice before paying for voice; an automatic "robot ear" for silences,
  overlaps and loudness; every rejection becomes a check; human stops at 2 points.

## 2. Personal finance dashboard

- **Request**: "Still confusing. I need to glance and know: how much came in, how much went out, am I
  making or losing money, where do I cut, how much reserve do I have."
- **Measured**: the existing page (10 sections stacked) and the data files.
- **Move**: 6 tabs, one question each; the summary obeys only the filter and opens with a one-line
  verdict and three numbers; costs tagged "cut / cap / required".
- **Lesson**: the user validated the redesign by interrogating its numbers ("where is that money
  now?"). That exposed a reserve that was really sales revenue still sitting in a payment platform.
  Always reconcile the headline numbers against reality.

## 3. WhatsApp bot for farm records

- **Request**: "Too many guards are hurting. Simplest model with maximum efficiency."
- **Diagnosis**: guard on top of guard; the AI did four jobs at once (understand, calculate, decide
  what to ask, write), and the guards only caught errors after the fact.
- **Move**: the AI fills a fixed form, the system validates and calculates, and the user sees the
  calculation ("10 bags × 180 = 1,800") and answers yes/fix/cancel. Ask when an error is costly,
  assume and show when it is cheap. An explicit list of deleted guards. Metric: a normal entry takes
  2 messages. Approved and implemented.

## 4. Client folders across Git and Drive

- **Request**: "All clients must have EXACTLY the same folders, so the agent always knows where each
  file goes."
- **Measured**: 10 clients had 7 different folder sets in Git, and 8 had 7 different sets in Drive.
  The docs claimed uniformity; nothing checked it.
- **Move**: one 9-folder tree mirrored on both sides (file weight decides the side), one
  machine-readable spec, three checks reading it (merge, pre-commit, Drive audit), and the owners
  migrate their own files. Said no to "move everything to Drive", with reasons. Approved; it became a
  skill consulted before every merge.

## 5. Node-based creative studio

- **Request**: "Wireframe it completely and reimagine it so it's universal with the site."
- **Measured**: a code map plus the live app. 11 nodes mirrored retired apps and had 0 uses; a panel
  did nothing; 628 generations were unlabeled; 11 buttons had no label.
- **Diagnosis**: the same product built twice.
- **Move**: a thesis, cheap fixes first, then deleting 3,560 dead lines, and exporting the studio's
  best feature (its cost bar) to the rest of the site.
- **Lesson**: the user corrected missing visual detail ("draw all the nodes, not just the ones you
  saw") and wrong assumptions about features they know better. Open everything before drawing.
