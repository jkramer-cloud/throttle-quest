# Throttle Quest v2.7.1 — Corrected Cumulative Release (v2.6 + v2.7 Phases 1–3)

A self-contained educational motorcycle hill-climb arcade game for grades 5–8, with a career garage, 64 motorcycles, 28 courses (27 career courses plus the practice road) and optional local two-player practice. No account, external libraries, or network assets required.

## Status and recommended installation

**This is the corrected cumulative ZIP.** It restores the v2.6 learning-integrity, achievement reward, detailed garage and per-bike protection systems that were absent from the first reconstructed v2.7 ZIP, while retaining v2.7's eight added courses, stoppie mechanic, helmet graphics and tire trails. No previous version needs to be installed first.

**Before publishing:** export your career from **Settings → Export**. Extract the ZIP and replace both repository-root files (`index.html`, `README.md`) only when ready; do not merge fragments from older versions. Existing career storage and JSON backups remain `throttle-quest-career-v04`. In the same browser profile, the v2.6 separate learning-integrity storage is also read and retained. The original v2.7 ZIP should **not** be uploaded.

**No GitHub or PlayForge changes were made by this build.** This archive is for review and later manual publication.

## Install or update

Replace **index.html** and **README.md** in the root of your existing `throttle-quest` GitHub Pages repository. Keep its name and Pages URL unchanged. No PlayForge/Learning Hub changes are needed if its existing card already links to the game. Students should export a career backup first (Settings). Existing careers use the same local storage key (`throttle-quest-career-v04`). Data is browser-local, does not sync between devices, and can be lost if browser data is cleared. Students can restore their own exported backup.

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
| v2.1 | Deen the fictional workshop mechanic, equipped motorcycle/rider artwork, wheelie balance HUD and progressive achievements, smoother terrain-relative pitch, single-question balance rescue |
| v2.2 | Distinct animated landmark scenes for all 20 courses, additional deterministic trailside props and ambient effects, reduced-detail mode preserved |
| v2.3 | Seven motorcycle classes, steeper price bands, sequential ownership prerequisites, visible class ladder and purchase restrictions, existing garage grandfathered |
| v2.4 | Manufacturer collection achievements, one-time reward claims, 5–10% brand-specific finish bonuses, unlockable paid sponsor graphics and factory team gear |
| v2.5 | Original 60 permanent trail caches, collection book, optional one-attempt academic trail challenge, distinct ride reward breakdown |
| v2.6 | Learning-integrity warnings and temporary non-destructive riding restrictions; academic practice; tiered badge coin rewards with a one-time ledger; five detailed garage inspection views; per-bike configuration guards |
| v2.7 Phase 1 | More layered bike/rider art, eight paid helmet finishes, four introductory tire trails and bike-specific appearance |
| v2.7 Phase 2 | Eight helmet decals, five premium tire trails, expanded stadium lighting/stands/banners, updated workshop controls and free previews |
| v2.7 Phase 3 | Eight new longer courses (550–1,600 m), tougher late-career routes and timed targets, stoppie/nose-wheelie physics and separate balance meter, crash/question recovery, stored ride records and stoppie milestones |
| v2.7.1 | Restores and validates the missing v2.6 systems in the cumulative v2.7 game, updates achievement display and corrects the front-wheel rescue panel |

Factory starter configuration is included. New bikes, upgrades and cosmetics cost coins; previously purchased parts can be reinstalled without further charge. Duels are practice and do not grant career rewards. Sound is optional even after unlocking; the unlock is not a tamper-proof administrative control.

## v2.6 systems restored in this corrected release

### Academic practice and learning integrity

- Students can use **Home → Academic practice** at any time, including during a career restriction. Practice draws from the selected grade (5–8) and subjects, provides explanations and a running session score, and **does not award coins or alter career question totals**.
- During paid career racing, the response timer looks for repeated unusually fast **incorrect** submissions (under 1.8 seconds). Three rapid wrong answers among the most recent 10 responses on that local day trigger a warning; five cause a temporary career pause. Four ordinary wrong answers in a row prompt supportive review guidance **without a strike**.
- Flagged days within the rolling 14-day period escalate to **10 minutes, 24 hours, 72 hours, then seven days**, without deleting motorcycles, coins, achievements or saved progress. A flagged in-progress ride ends without pending ride earnings; ordinary learning and purchases remain available. Subsequent rapid wrong attempts after the same day has already been flagged do not create extra strikes for that day.
- Restrictions are saved inside the career and separately in browser-local storage under `throttle-quest-career-v04-integrity-v26`. Importing an older backup on the same browser profile does not erase an active restriction. This is **not tamper-proof or suitable as an official disciplinary system**: switching devices, clearing browser data or modifying the browser can bypass it. The intent is to encourage careful academic engagement, not to penalize genuine mistakes.

### Achievement coin rewards

- Each ordinary achievement awards coins once at its tier: **Bronze 50, Silver 100, Gold 175, Jade 250, Platinum 350, Legend 500**. The `badgeCoinsPaid` ledger is retained in career saves and backups; repeated page loads, revisiting Records, and repeated saves do not duplicate a claimed reward.
- Achievements already satisfied in a prior saved career receive any **previously unpaid** one-time catch-up awards on the first updated save. Manufacturer Collector / Factory Team rewards remain on their separate reward paths and are excluded from these badge payouts to prevent double payment.
- The first successful career stoppie still carries its separate 45-coin one-time bonus. Rewards are triggered by progress and saved career activity, including garage milestones; they do not require finishing a ride after reaching a milestone.

### Detailed, independent motorcycle garage

- **My Garage → Detailed motorcycle inspection** provides larger zoomed component views: entire motorcycle, front tread, rear tread, engine/exhaust, and front suspension, using the installed or previewed mechanical setup. This remains stylized artwork rather than photographic/OEM-accurate geometry.
- Mechanical and cosmetic purchases remain tied to each separately owned motorcycle. Reinstalling a previously purchased part for the same motorcycle costs nothing; the same premium change on another motorcycle still costs coins. Workshop previews do not deduct coins until purchased.

## v2.7: new content and controls

### New courses (28 total)

The 20 existing courses and their unlocks, segments and original medal times are retained. These eight additions are progressively tougher, have explicitly longer time limits and are added after the existing courses in the career listing. All course previews and scenery are drawn locally in Canvas.

| Added course | Distance | Time limit | Environment |
|---|---:|---:|---|
| Neon Arena MX | 550 m | 150 s | Floodlit stadium |
| Grand Prix Supercross | 650 m | 190 s | Championship stadium |
| Frostline Traverse | 780 m | 210 s | Alpine terrain |
| Red Mesa 1000 | 1,000 m | 245 s | Canyon endurance |
| Endless Wetlands | 920 m | 245 s | Mud / grass endurance |
| Skybridge Quarry | 1,200 m | 275 s | Rock quarry endurance |
| Duststorm Marathon | 1,350 m | 310 s | Sand marathon |
| Evercrest 1600 | 1,600 m | 350 s | Final mixed-terrain test |

The three collectibles per added course increase the full trail collection from 60 to 84, with collection milestones at 75 and 84. The 20 original routes still behave as before. Course time limits are game-clock limits, not real-world speed targets. Late routes are intended for progressively upgraded bikes; starter motorcycles may struggle.

### Stunts and balance

- **W / up arrow**: throttle. **S / down arrow**: brake. **A / left arrow**: lean back. **D / right arrow**: lean forward. Touchscreen buttons remain available.
- To try a **stoppie (nose wheelie)**, build speed on suitable ground, then hold **S + D** briefly. As the back lifts, use **A** to keep from going over the bars. This is deliberately difficult. The front-wheel balance meter shows a separate safe and danger range; it does not replace the established rear-wheelie meter.
- The first successful career stoppie earns **45 bonus coins once per career**. Later successes are recorded but do not repeat that reward. One-question balance rescue may be offered within the existing per-ride limits; the question itself does not award coins. Local two-player races remain non-rewarding practice.
- Best front-wheel stoppie duration is recorded with the ride and on the Records page, including achievements. Existing wheelie records and reward logic are retained.

### Motorcycle appearance

Under **My Garage → Custom graphics & rider gear**, preview and unlock new helmet colors (180 coins), helmet emblems (200 coins) and tire effects (240–420 coins). The factory color, unadorned helmet and no tire effect are free. Cosmetic purchases attach to the selected motorcycle, can be reinstalled on that motorcycle without paying again, and are saved inside the existing career backup. The effects are visual only, without speed or traction boosts. Low graphics mode skips tire effect particles. Existing paid upgrades and brand sponsor designs are preserved.

### Achievement awards

Ordinary achievement tiers pay the fixed one-time rewards listed in the v2.6 section above, and the 45-coin first-stoppie reward is separate. `badgeCoinsPaid`, earned badge IDs, and academic progress are included in saved careers. Repeated rapid incorrect guesses can temporarily restrict riding, **but never automatically reset a career**. Normal incorrect answers do not create penalty strikes.

### Verification performed for v2.7.1

- **Source checks:** all eight inline JavaScript blocks passed Node.js syntax validation; HTML element IDs are unique. No external libraries or network requests are required for gameplay.
- **Headless Chromium (25 targeted regression assertions):** clean startup, 28 courses, 64 catalog motorcycles, seven bike price tiers, 140+ achievement milestones, exact 50/100-coin Bronze/Silver test payouts, zero repeat claims, retention of existing v2.6 integrity and badge fields through career validation, first-time paid helmet color and free re-equipping, separate purchases on a second bike, independent mechanical setup changes, slow wrong answers never causing a strike, warning after three rapid wrong responses and a ten-minute pause after five, independently stored restrictions and preservation during an old backup import, practice during restriction, and baseline physics stability on each course. No browser JavaScript exceptions in those flows.
- **Real in-race quiz flow:** a five-response rapid guessing scenario invoked the actual question UI and pause flow; the ride exited without pending coin payout and the saved career remained intact.
- **Stoppie rescue:** separate front-wheel rescue banner, correct balance-station artwork and no-coin reward were verified.
- **The test harness was not included in the ZIP.** These checks are simulated and do not replace hands-on, full-course playtesting or real district Chromebook performance/graphics testing. Existing student career files were not provided; simulated v2.6-profile data was used for migration tests.
- **Provenance:** the playable content is built from the archived v2.5 game plus reconstructed v2.7 additions and restored v2.6 functionality inspected against the source currently available in the linked Throttle Quest GitHub repository. It is a feature-level integration, not a byte-for-byte copy of every prior unreleased development file.

## Learning coverage

| Grade | Math | ELA | Science | Social studies | Geography | Technology | Total |
|---|---:|---:|---:|---:|---:|---:|---:|
| 5 | 2692 | 778 | 261 | 55 | 258 | 118 | 4162 |
| 6 | 3125 | 775 | 245 | 156 | 204 | 163 | 4668 |
| 7 | 3125 | 775 | 245 | 155 | 184 | 154 | 4638 |
| 8 | 2729 | 647 | 245 | 156 | 246 | 146 | 4169 |
| Total | 11671 | 2975 | 996 | 522 | 892 | 581 | 17637 |

Counts include generated variations, not individually authored lessons. Some prompts overlap grades. Questions do not repeat within an individual grade/subject deck cycle; smaller decks exhaust sooner. Question practice is not a formal standards-aligned assessment. Non-math factual banks can be expanded in future versions.

## v2.2–v2.5 gameplay notes

### World and scenery

Every track retains its original terrain, physics, routing and gates. Authored landmarks include orchards and barns, windmills, watchtowers, camps, waterfalls, coastal ships and lighthouses, quarry cranes, bridges, ruins, castles, volcanic ridges, steampunk foundries and airships. Decorative objects are non-colliding. Landmarks and trail props are seeded per course; animation is lightweight and lower graphics quality reduces minor detail. They do not move the actual racing surface.

### Career motorcycle classes

| Class | Models | Approximate coin price band |
|---|---:|---:|
| Starter | 1 | Initial CRF110F free; additional copies 1,800 |
| Junior | 16 | 1,500–3,000 |
| Amateur | 10 | 3,500–6,000 |
| Competition | 17 | 8,000–15,000 |
| Expert | 7 | 18,000–28,000 |
| Professional | 10 | 35,000–50,000 |
| Legend | 3 | 65,000–85,000 |

Prices within each class depend on the game's normalized power estimate and are rounded to 50 coins. The player must own at least one motorcycle from every earlier class before buying a new bike in a higher class. Already owned bikes, parts, cosmetics, wallet balances, course unlocks, and statistics are not revoked, even when older careers skipped a class. The class ladder and inspection screen explain what is locked. Existing coin rewards are retained, supplemented by sponsor rewards and exploration bonuses. These initial price bands require classroom balancing; especially the Legend class is a long-term target.

### Manufacturer sponsorship

The Records collection book tracks distinct models, not duplicate purchases. Claim each milestone once: Collector (three models, or the full set if the brand has fewer) and Factory Team (all models). Collector awards 150 coins per required model and unlocks brand-themed sponsor paint (600 coins to purchase per bike). Factory Team awards at least 500 coins or 250 per catalog model, whichever is larger, and unlocks matching rider gear (450 coins per bike). Qualified brands add 5% to the base course finish reward, or 10% for a complete brand collection, when riding a bike made by that brand. Bonuses do not multiply other rewards. Brand rewards and exclusive designs are fictional game mechanics, not sponsored or endorsed by manufacturers.

### Trail explorer

- The original 20 courses contain 60 caches; v2.7 adds 24 more across the new eight courses, for 84 total.
- Each course contains three consistently positioned collectible caches worth 80, 120 and 160 coins. Ride past a gold marker to collect it. The cache is not a hazard; it does not affect physics.
- Each cache can be collected once per career, including across replays, and is committed with its coin reward when the ride ends. Leaving the page mid-ride before the results are saved does not commit that ride's caches or pending coins.
- Records includes an 84-cache collection tracker, plus achievements at 5, 15, 30, 45, 60, 75 and 84.
- Around two-thirds of a course, an optional Deen trail challenge offers one randomly drawn grade/subject-appropriate question for 60 coins. A wrong answer or skip simply resumes the ride; no crash or penalty. One opportunity per career ride. Local duels remain practice-only and do not grant trail or sponsor rewards.

### Verification

- JavaScript syntax validated. Chromium tests verified all 64 catalog assignments, rejection of skipped tiers, sequential unlocks through Legend, duplicate sponsor claim rejection, sponsor paint unlock and paid purchase, old career loading and retention of an equipped high-tier motorcycle, all 20 track world renders at three positions, first-time cache rewards and repeat rejection, and the correct-answer trail challenge path.
- v2.1 regression checks: equipped-bike rider art, Deen's advice button, sustained starter wheelie, correct rescue, incorrect rescue and crash recovery. Tests used browser-local simulated storage and temporary balances; no test hooks are included in the shipped file.
- Real Chromebook frame rate, long-term economy progression and edge cases on complete rides still need classroom playtesting. No live repository changes were made.

## v2.1 gameplay notes

- Meet the Crew and rider selection now show the active bike with its installed setup, paint, rider kit and number rather than a fixed CRF110F. Each alternative rider is previewed on that same equipped bike. Unpurchased workshop previews do not change the showcase.
- Deen appears in My Garage, with original stylized steampunk portrait and rotating tips. The character is fictional; obtain school-appropriate consent before using a student name publicly.
- Hold A (or left arrow) to lift the front wheel; use D (or right arrow) to correct a high wheelie. The balance bar appears during wheelies, with green, warning and danger ranges. Lowering the front wheel normally is safe. Riding assist is more forgiving than manual mode.
- A sustained dangerous angle may offer a one-question rescue in career mode: 65% chance when eligible, at most two per ride, at least 18 simulated seconds apart. A correct answer restores balance without bonus coins; an incorrect answer leads to normal crash recovery. Rescues are disabled in local two-player practice to keep conditions comparable. Questions use the existing grade/subject decks.
- Wheelie milestones: 2, 5, 10, 20, 30 and 67 seconds; existing achievements and the original one-time ride reward are retained. Longer runs require suitable terrain, speed and balance. No new paid mechanical parts in v2.1; v2.3 subsequently changes motorcycle purchase prices.

## v2.1 verification

- Base ZIP files matched the published GitHub v2.0 Git blob hashes before modification. JavaScript syntax checked.
- Chromium interface test with simulated browser storage: active bike/rider art changed after purchase and selection; workshop tip button worked; a real starter-bike simulation sustained a wheelie for more than five seconds without crashing; forced red-zone tests verified correct-answer rescue and incorrect-answer crash followed by standard recovery; no uncaught page errors.
- Physics is still illustrative, and rare terrain/landing cases and real Chromebook performance require classroom playtesting. The test harness was not included in the release.

## Previous release verification (v2.0 baseline)

- JavaScript syntax checked; five original catalog/physics/mechanics/ledger/career script blocks were byte-identical to v1.0 after text decoding in the v2.0 release. The v2.1 physics changes are intentional; the learning engine is unchanged.
- All 24 complete grade/subject question-deck cycles (17,637 questions), distinct answer options, correct-answer placement, mixed-subject rotation and serialized history tested.
- Local Chromium interface tests: fresh setup, older save migration using simulated storage, balance and history retention, garage purchase/reinstall/affordability checks, 64 bike model renders, riding, pit refuel/recovery/sponsor, HUD, mobile/low graphics, medal and personal-best payout, championship claim, archived badges, practice duel isolation, muted startup, audio unlock and opt-in, volume, blur mute and ride reset.
- Award tests use simulated finish outcomes; some transaction tests seed a temporary test balance. Test harness code is not included in the published file.
- Direct file/site navigation was blocked by the test environment. Real hosted storage, school Chromebook performance, natural full runs of every course, and factual content review remain recommended before broad classroom deployment.

Artwork is original stylized 2D canvas rendering and not factory-accurate. This is a game with estimated vehicle characteristics, not real motorcycle tuning or riding guidance.
