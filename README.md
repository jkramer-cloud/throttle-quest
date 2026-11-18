# Throttle Quest v2.0 — Arcade Edition

A self-contained educational motorcycle hill-climb arcade game for grades 5–8, with a career garage, 64 motorcycles, 20 courses and optional local two-player practice. No account, external libraries, or network assets required.

## Install or update

Replace **index.html** and **README.md** in the root of your existing `throttle-quest` GitHub Pages repository. Keep its name and Pages URL unchanged. No Learning Hub changes are needed. Students should export a career backup first (Settings). Existing careers use the same local storage key (`throttle-quest-career-v04`). Data is browser-local, does not sync between devices, and can be lost if browser data is cleared. Students can restore their own exported backup.

To test locally, extract the ZIP and open `index.html` in a supported browser that permits local files. GitHub Pages is recommended for classroom deployment.

## Cumulative release contents

| Build | Included features |
|---|---|
| v1.0 | Career progression, original game-estimated physics, 64-bike catalog, 20 courses, paid upgrades and cosmetics, local duel, records and backup |
| v1.1 | Grade 5–8 selection, six selectable subjects, three question frequencies, 17,637 question variants, persistent shuffled decks, balanced topic/subject rotation, randomized answer positions, learning records and export |
| v1.2 | Individually styled courses, parallax scenery, terrain textures, tire marks, surface particles, atmospheric effects, smoothed camera |
| v1.3 | Articulated motorcycle rig, distinct model families, eight tire treads, animated suspension and drivetrain, rider posture, visible customization and grime |
| v1.4 | Workshop, live previews, itemized work orders, showroom for all 64 bikes, inspection screens and purchase/delivery animations |
| v1.5 | Compact racing HUD, speed/RPM/gear, fuel, traction, course elevation, checkpoints, jump notifications, illustrated fuel/repair/sponsor questions |
| v1.6 | Course briefings, victory podium and achievements, 20 course medals, four championship trophies, 101 collectible milestones |
| v1.7 | Sound locked until three completed career rides AND 25 correct answers; each ride starts muted, manual opt-in, 25% default volume, mute on focus loss, no music; idle and low-graphics optimizations |
| v2.0 | Cumulative release, updated branding and corrected obsolete development information; regression review |

Factory starter configuration is included. New bikes, upgrades and cosmetics cost coins; previously purchased parts can be reinstalled without further charge. Duels are practice and do not grant career rewards. Sound is optional even after unlocking; the unlock is not a tamper-proof administrative control.

## Learning coverage

| Grade | Math | ELA | Science | Social studies | Geography | Technology | Total |
|---|---:|---:|---:|---:|---:|---:|---:|
| 5 | 2692 | 778 | 261 | 55 | 258 | 118 | 4162 |
| 6 | 3125 | 775 | 245 | 156 | 204 | 163 | 4668 |
| 7 | 3125 | 775 | 245 | 155 | 184 | 154 | 4638 |
| 8 | 2729 | 647 | 245 | 156 | 246 | 146 | 4169 |
| Total | 11671 | 2975 | 996 | 522 | 892 | 581 | 17637 |

Counts include generated variations, not individually authored lessons. Some prompts overlap grades. Questions do not repeat within an individual grade/subject deck cycle; smaller decks exhaust sooner. Question practice is not a formal standards-aligned assessment. Non-math factual banks can be expanded in future versions.

## Release verification

- JavaScript syntax checked; five original catalog/physics/mechanics/ledger/career script blocks remain byte-identical to v1.0 after text decoding. Learning engine remains identical to v1.1.
- All 24 complete grade/subject question-deck cycles (17,637 questions), distinct answer options, correct-answer placement, mixed-subject rotation and serialized history tested.
- Local Chromium interface tests: fresh setup, older save migration using simulated storage, balance and history retention, garage purchase/reinstall/affordability checks, 64 bike model renders, riding, pit refuel/recovery/sponsor, HUD, mobile/low graphics, medal and personal-best payout, championship claim, archived badges, practice duel isolation, muted startup, audio unlock and opt-in, volume, blur mute and ride reset.
- Award tests use simulated finish outcomes; some transaction tests seed a temporary test balance. Test harness code is not included in the published file.
- Direct file/site navigation was blocked by the test environment. Real hosted storage, school Chromebook performance, natural full runs of every course, and factual content review remain recommended before broad classroom deployment.

Artwork is original stylized 2D canvas rendering and not factory-accurate. This is a game with estimated vehicle characteristics, not real motorcycle tuning or riding guidance.
