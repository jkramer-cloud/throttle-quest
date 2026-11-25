# Throttle Quest v3.3 — Technical Terrain / Batch 4

Cumulative replacement for v3.2. Copy `index.html` and `README.md` to the existing repository root. The game remains a single offline-ready HTML file. Back up your current career and repository before replacing it. No GitHub or PlayForge changes have been made.

## Batch 4 changes

- 14 technical-riding badge milestones for successful manual jumps, jump height, airtime, distance, clean landing streaks, distinct clean obstacle clearances and qualified retro/technical finishes. Technical badges appear under Records > Achievements > Technical riding. Existing badge milestones remain available.
- New technical progress is credited only after a completed career course with at least one correct in-ride answer. Only manual landings with at least 2 m forward displacement and 10 cm clearance count, once per 8 m landing zone per run. A collision or crash resets the current clean streak. Distinct obstacle badges track course ID and obstacle location across rides; replaying one log does not count as a new obstacle. Local duels do not contribute. New badges use the existing one-time tier payouts of 50–500 coins (new technical tiers currently 50–250). No automatic coins for each manual jump. Ramp landing rewards remain capped at three per ride and require forward distance and a distinct landing zone. Repeated normal course finishes still earn existing finish rewards.
- Fixed duplicate finish-time achievement payouts by routing them through the existing paid-badge ledger. Achievement rewards are shown separately in the results. Previous balances are not confiscated. Old saves initialize the technical statistics to zero; historical manual jumps cannot be reconstructed from prior records.
- Fuel recovery still requires the configured number of correct answers. Optional question skips can no longer bypass termination of a ride flagged for repeated rapid wrong answers. Existing escalating local restrictions remain; no career deletion. Browser-local state is not tamper-proof.
- Made the early Meadow Ridge/Pine Summit obstacles more forgiving; widened and lowered Pine Summit's three solid obstacles, without removing them. Assisted low-speed uphill traction receives a bounded boost; automatic downshifting better handles slow climbs. Advanced obstacles and the straightaway layout remain unchanged. Course intro shows setup recommendations. Hard-landings and obstacle crashes now take priority over a simultaneous finish.
- All 32 course IDs, 129 terrain features and 64 catalog models are retained. Existing purchases, records and unlocks remain. Prior course times may not be directly comparable after terrain changes.

## Verification and limits

JavaScript syntax passed. Eleven Chromium checks passed with a simulated localStorage object and temporary test hooks: catalog/course/feature counts, old-save initialization, manual jump and no double jump, qualified ride and unique obstacle tracking, 14 technical badges and single payout, ride start, wrong-answer fuel gate, correct-answer fuel recovery, finish accounting and career validation, technical badge filter, and rapid-guessing optional-skip protection. No page errors in these checks. Test hooks are NOT in the delivered HTML.

A separate deterministic physics sweep attempted all 32 tracks using the starter and two higher-end bikes with terrain-selected tires and shorter gearing. The controller brakes before obstacles but does not manually jump; it simulates refueling/recovery and is not a human playthrough. 27/32 tracks finished with at least one of the three setups (70/96 attempts). The starter finished Meadow Ridge, Pine Summit, Retro Ramp Rally, and several additional tracks without crashes. Black Rock Peak, Skybridge, Everest, Timber Trials and Ironwood Extreme Enduro did not finish in this sweep; manual riding, alternative setups, and additional difficulty tuning may be required. This is not proof that those tracks are impossible or fully balanced. Real Chromebook performance, storage persistence, actual keyboard/touch playthroughs on school devices and full course solvability remain to be checked before classroom rollout. The existing question bank was not independently re-fact-checked in this batch.

### Physics sweep (each cell: outcome / meters / seconds / crashes)

```text
Course | CRF110F stock | CRF450X tuned | KTM 500 EXC-F tuned
tq-meadow Course complete/350/25/0 Course complete/350/22/0 Course complete/350/21/0
tq-pines Course complete/425/38/0 Course complete/425/28/0 Course complete/425/28/0
tq-dunes Course complete/470/32/0 Course complete/470/26/0 Course complete/470/26/0
tq-bog Course complete/490/36/0 Course complete/490/27/0 Course complete/490/26/0
tq-jumps Course complete/510/32/0 Course complete/510/27/0 Course complete/510/26/0
tq-enduro stalled/155/43/1 stalled/305/56/2 stalled/307/63/3
tq-road Course complete/600/29/0 Course complete/600/21/0 Course complete/600/21/0
tq-canyon Course complete/490/36/0 Course complete/490/30/0 Course complete/490/29/0
tq-coast stalled/335/44/0 Course complete/520/30/0 Course complete/520/30/0
tq-rain stalled/289/42/0 Course complete/540/34/1 Course complete/540/34/1
tq-quarry stalled/140/48/2 Course complete/515/43/2 Course complete/515/43/2
tq-stadium Course complete/465/31/0 Course complete/465/26/0 Course complete/465/26/0
tq-volcano Course complete/550/43/0 Course complete/550/34/0 Course complete/550/36/0
tq-crown Course complete/600/56/1 stalled/244/45/1 stalled/244/45/1
tq-orchard Course complete/500/36/1 Course complete/500/25/0 Course complete/500/24/0
tq-alpine Course complete/500/34/0 Course complete/500/26/0 Course complete/500/26/0
tq-oasis Course complete/500/36/0 Course complete/500/31/0 Course complete/500/31/0
tq-marsh Course complete/500/40/1 Course complete/500/29/0 Course complete/500/29/0
tq-redmesa Course complete/500/36/0 Course complete/500/29/0 Course complete/500/29/0
tq-final stalled/204/35/1 Course complete/500/28/0 Course complete/500/27/0
tq-arena-night Course complete/550/33/0 Course complete/550/28/0 Course complete/550/27/0
tq-stadium-finals Course complete/650/40/0 Course complete/650/33/0 Course complete/650/33/0
tq-frostline stalled/629/76/4 Course complete/780/44/1 Course complete/780/45/1
tq-mesa-endurance stalled/280/42/1 Course complete/1000/58/1 Course complete/1000/57/1
tq-marsh-endurance Course complete/920/80/2 Obstacle collision/401/55/9 stalled/410/48/1
tq-skybridge Obstacle collision/380/56/9 Obstacle collision/947/80/9 Obstacle collision/947/79/9
tq-dune-marathon stalled/671/63/0 Course complete/1350/63/0 Course complete/1350/62/0
tq-everest Obstacle collision/445/56/9 Obstacle collision/1140/75/9 Obstacle collision/1140/74/9
tq-retro Course complete/530/30/0 Course complete/530/23/0 Course complete/530/23/0
tq-trials-garden Obstacle collision/68/57/9 Obstacle collision/68/48/9 Obstacle collision/67/48/9
tq-hard-enduro Time limit/355/120/7 Obstacle collision/127/69/9 Obstacle collision/127/69/9
tq-super-rhythm Course complete/636/37/0 Course complete/636/27/0 Course complete/636/27/0
```

---

# Previous development notes

# Throttle Quest v3.2 — Course Expansion, Batch 3

Cumulative build based on v3.1 Batch 2. Replace `index.html` and `README.md` in the existing repository when ready; export a career backup first. No live GitHub or PlayForge changes have been made.

## Course expansion

- 32 total courses (28 retained, four new), 129 authored technical features across 31 courses. Redline Straightaway is unchanged. All 28 original course IDs, base segment geometry, lengths, unlock thresholds, finish rewards and medal targets are preserved. The 28 pilot features from v3.1 are unchanged; 20 previously unmodified courses now have technical features. Previous personal bests and medals are retained, but times from before terrain changes are not directly comparable. New courses count toward the same career unlock progression. The existing 84-cache achievement milestone is retained; the course collection book now includes 96 caches. New milestone/reward balancing is deferred to Batch 4.

| New course | Length | Unlock | Focus |
|---|---:|---|---|
| Retro Ramp Rally | 530 m | Immediately | Classic 8-bit-inspired side-view time attack with two repeated ramp sequences, flat runs, tabletop, paired jumps and whoops. Pixel-inspired stadium backdrop, existing rider and physics. |
| Timber Trials | 475 m | 3 unique career finishes | Low-speed logs, rock gardens, short ledges and balance. |
| Thunder Dome Supercross | 636 m | 8 unique career finishes | Triples, tabletop sections and extended rhythm bumps. |
| Ironwood Extreme Enduro | 750 m | 12 unique career finishes | Rock, roots, mud, steep climbs and solid hazards. |

Retro is an original course inspired by classic motocross games, not an Excitebike recreation. The repeated sections form a single continuous point-to-point time attack; no separate lap system, lane switching, AI competitors, overheating redesign, or track editor has been implemented. The existing simulator's temperature, educational questions, jumping, crash recovery, anti-guessing controls, unlocks and garage remain intact. Use the Tracks filter to choose Retro motocross, Trials, Enduro / hill climb, MX / stadium, Technical terrain or Speed testing. New course art reuses appropriate world scenery and existing motorcycle/rider artwork.

## Verification

- Chromium loaded all 32 courses with no uncaught page errors in the test. Geometry checks passed: segments are contiguous, feature spans within bounds and non-overlapping; original course metadata and v3.1 pilot features match exactly. A fresh v3.1 career object validated in v3.2.
- 386 terrain-render checks (standard and low graphics; starts, midpoints, and every obstacle location). Retro course filter returned exactly Retro Ramp Rally.
- 17 solid obstacles on the two new technical courses passed isolated low-speed crossing simulations using a factory YZ450F. These tests start near each obstacle, not a full course.
- A controlled starter-bike simulation finished all 530 m of Retro Ramp Rally in 44.03 seconds, with six natural jumps. This is a physics test with automated throttle/lean, not a human classroom playthrough or proof of all jump timing/medal targets.
- Full course completion, achievement and reward balancing, existing record comparability, educational end-to-end regression testing and real Chromebook/touchscreen performance remain outstanding. Batch 4 is intended to address balancing and testing. No test hooks shipped.

---

# Throttle Quest v3.1 — Technical Terrain, Batch 2

Cumulative update based on the recovered v3.0 Batch 1 ZIP. Extract and replace `index.html` and `README.md` in the existing repository only when ready. Export a career backup first. No GitHub or PlayForge changes have been made.

## What's new

- 28 authored terrain features on seven existing courses: Meadow Ridge (3), Pine Summit (4), Copper Dunes (3), Thunder Bog (4), Skyline MX (3), Black Rock Peak (6), and Granite Quarry (5). The other 21 courses remain unchanged for Batch 3. All 28 courses retain their IDs, lengths, gates and reward definitions.
- Fallen logs, boulders, rock ledges, deep ruts, rolling slopes and rhythm bumps change the actual ground profile. Logs, boulders and ledges have front- and rear-wheel contact tests, speed loss, suspension compression, and a speed/impact-dependent crash condition. A front-wheel lift reduces impact; a correctly timed jump can avoid contact. Ruts and bumps alter slope, surface grip and suspension motion.
- Upcoming-obstacle warnings appear within 45 meters and yellow trailside warning signs mark obstacles. The course renderer uses the same terrain profile as the physics. Both graphics quality modes show hazards.
- Hard obstacle strikes use the existing crash recovery question and checkpoint. If a checkpoint is too close to an obstacle, recovery moves the bike back to a clear approach. No new obstacle coin rewards, achievement unlocks, or learning-integrity changes. Existing jump reward path ignores a natural-jump touchdown that hits a physical obstacle.
- Spacebar hold/release, A/D lean, touch controls, existing garage, all 64 motorcycle designs, career save key and question systems are retained. Technical features also appear in local duels.

## Verification and limitations

- JavaScript syntax checked. Chromium tests used inline page loading and simulated local storage because direct file/site navigation was blocked by the test environment. All 28 terrain profiles passed boundary/finite-height checks; all 28 features rendered in both graphics modes (56 renders). No page errors in the final independent-page regression tests.
- Seeded simulation: small starter-bike log crossings passed at low speed; a sweep of manual-jump timings found 38 speed/launch-position combinations that cleared the first log with zero wheel contacts; a 15 m/s boulder strike triggered an obstacle collision. Tests used precharged suspension for launch timing, not a full live keyboard ride. All 16 solid obstacle features passed isolated low-to-moderate-speed crossing tests on a factory YZ450F after repositioning five difficult obstacles; these are not full course completion tests.
- Straightaway simulation trace matched v3.0 exactly over 1,200 physics steps, including manual jump input. Career structure and 64-model/28-course counts retained. The terrain system is a simplified two-wheel height-profile simulation rather than rigid-body dynamics.
- Classroom Chromebook performance, real touchscreen input, full-course traversal, timing targets and reward balancing are not yet verified. Batch 3 will expand technical layouts and Batch 4 will balance difficulty, achievements and rewards. Prior v3.0 and older verification notes follow.

---

# Throttle Quest v3.0 — Technical Terrain Batch 1

Based on the recovered v2.9.1 full motorcycle reconstruction. Install by replacing only `index.html` and `README.md` in the existing repository; export career backup first. No GitHub or PlayForge changes made.

## Manual jumping
- W/Up throttle, S/Down brake, A/Left lean back, D/Right lean forward. Hold Space (or hold the Jump touch button), then release while rolling on both wheels. Charge is shown on the button. Charge takes approximately 0.48 seconds to fill; very short presses are ignored. Airborne presses cannot queue a jump. A brief landing cooldown prevents repeated impulses.
- Suspension springs, travel, rebound, bike mass, grip and slope affect launch. Rider crouches during preload, extends in the air and absorbs landing. The original natural ramp flight and suspension system remain in use. Manual impacts and poor landing angles use the existing crash recovery quiz.
- Manual jumps consume a small amount of fuel/energy. Successful forward jumps of at least 2 m and 0.10 m terrain-relative clearance count toward existing jump metrics. No new direct manual-jump coin reward; existing course, career, learning and natural ramp reward systems remain. New achievements and economy balancing are deferred to Batch 4.
- Existing 28 course profiles are unchanged. Logs, boulders and new slopes are deferred to Batch 2. This is a game approximation, not real riding advice.

# Throttle Quest v2.9.1 — Full 64-Motorcycle Reconstruction

**Status: Complete manually installable review release.** Based directly on the v2.9 three-bike pilot and the corrected v2.8 cumulative game. GitHub and PlayForge have not been changed.

## What has been built

- Extended the approved structural drawing system to **all 64 catalog motorcycles**: seven trail, 42 motocross, 11 enduro, two cross-country and two electric.
- The three approved reference designs — Honda CRF110F, Yamaha YZ450F and Sur-Ron Light Bee X — are **unchanged at the pixel level** for normal riding, dealership and side-profile views. All 61 other catalog motorcycles use the new reconstructed artwork.
- Correct component attachment points for wheel axles, engine and motor casings, swingarms, frame rails, steering heads, seats and handlebars. Reduced the oversized/floating fairings and plastic-on-fork overlaps of v2.8.
- Proportions now respond to the real catalog's engine-size classes and riding disciplines; beginner bikes are compact, full motocross bikes are taller, enduro bikes carry appropriate guards and bodywork, cross-country bikes combine racing stance and fuel-bodywork styling, and a small vintage subset has more period-appropriate panels.
- Two-stroke and four-stroke engines have different visible header/expansion details. Electric motorcycles have a visible battery, electric motor and controller/upgrade markings, and **no exhaust manifold, header, muffler or pipe**.
- Uses the same redesigned motorcycle rendering for **racing, garage, shop, thumbnails and detailed inspections**, including wheel animation and rider placement.
- All existing bike catalog entries, gameplay physics, learning safeguards, reward systems, 28 courses, purchases and local career saves remain from v2.8. This is an artwork-focused update, not a motorcycle balance pass.

**Artwork scope:** These are original, stylized family-aware procedural graphics, not exact factory drawings. Individual motorcycles in the same family share some body-panel shapes; engine class, tire/frame geometry, powertrain, brand colors and certain details differentiate them. Further hand-authored model-by-model art refinement remains possible after classroom visual review.

## Download / install — you control GitHub

1. Export a career backup from Settings in the existing game before replacing anything.
2. Extract this ZIP. The **only two files to upload** to the existing `jkramer-cloud/throttle-quest` repository root are `index.html` and `README.md`.
3. Replace those two existing files, committing the changes yourself. **Do not upload or replace the `REVIEW/` folder.**
4. Refresh the game in a Chromebook, inspect a trail, MX, enduro, cross-country and electric bike, run a short race, and confirm your career/settings still load. The PlayForge launch link does not need updating.

The career save key remains `throttle-quest-career-v04`. The v2.6 separate learning-integrity local state is preserved. Data lives in each browser/profile and is not remotely synced.

## Visual evidence supplied

- `REVIEW/catalog-sheet-1.png` to `catalog-sheet-4.png`: all **64** catalog motorcycles, clearly labeled with riding family and cycle.
- `REVIEW/QA_REPORT.json`: structural/screenshot testing and counts.
- `REVIEW/v29-approved-three-bikes.png`: the three previously approved reference bikes.

## Verification

- Eight embedded JavaScript scripts pass `node --check` syntax validation.
- Catalog remains at 64 models, with 28 courses, and the nonvisual JavaScript sections are byte-identical to the v2.9 pilot (which inherited v2.8 cumulative).
- Headless Chromium successfully rendered **all 64 models** in normal, rider/pose, dealership and thumbnail modes, with no page errors.
- All three approved prototype motorcycles are pixel-identical to the pilot build; all 61 other catalog motorcycles produced changed side-profile drawings.
- Electric battery/controller/motor upgrades show visual differences; engine/exhaust cosmetic configurations still affect gasoline bikes.
- ZIP integrity and its file SHA-256s were checked after creation.

**Limits:** A passing browser-render test is not a substitute for direct Chromebook gameplay, save/import regression, long-race performance, and review of every art interaction at classroom resolution. Do not overwrite a student's career without a backup.

---

## Earlier releases (historical documentation)

# Throttle Quest v2.9 — Motorcycle Reconstruction Pilot (3 Bikes)

**Development review build, not yet a full 64-bike visual overhaul.** Based on the complete v2.8 ZIP. GitHub and PlayForge were not changed.

## This build fixes three reference motorcycles first

| Motorcycle | Category | What changed |
| --- | --- | --- |
| Honda CRF110F | Beginner trail | Shorter rounded plastics, lower stance, correctly positioned small engine, slimmer frame and swingarm, wheel-mounted fender and fork |
| Yamaha YZ450F | Full-size motocross | Taller stance, sharper but restrained radiator shrouds, separated fuel tank and number panel, exposed four-stroke engine and slim header, coherent front fork |
| Sur-Ron Light Bee X | Electric | Compact battery-and-motor layout, small top cover, exposed triangle frame, short rear/fender profile, **no combustion engine, fuel tank, header pipe or muffler** |

These are original stylized game interpretations, not licensed factory technical drawings or validated physical measurements.

### What the reconstruction changes

- Uses model-specific *attachment points* for seat, steering head, bars, footpeg, swingarm pivot, fork, and wheels.
- Groups the rendering into deliberate layers: wheels and drivetrain, rear suspension and frame, powertrain, limited body panels, seating, steering/fender, controls and rider.
- Restrains plastic panel extents so the radiator shroud does not reach across the fork or hide the entire engine.
- Draws both unoccupied showrooms and active riding from the same motorcycle geometry; the rider's hand and foot attachment points follow the reconstructed frame.
- Preserves colors, available upgrades, wheel animations, tire treads and suspension poses.

**61 other motorcycle models still use their v2.8 rendering**, intentionally unchanged. They are not yet endorsed for visual quality. The completed game still contains all 64 bikes and 28 courses.

## How to review — no publishing required

1. Open `REVIEW/v29-before-after.png` to compare the three motorcycles with their v2.8 predecessors.
2. Open `REVIEW/v29-silhouette-review.png` to inspect the new silhouettes without the distraction of colors.
3. Open `REVIEW/v29-pilot-contact.png` for dealership, side profile and simulated riding views.
4. To try the complete prototype game, open `index.html` locally in a browser that permits local files, or test it in a private staging environment. The starter Honda CRF110F is visible immediately; the other two models can be inspected through the dealership without purchase.
5. If you choose to publish later, **only `index.html` and `README.md` replace the repository-root files.** Do not upload `REVIEW/`. Export a career backup first (Settings), then perform a Chromebook check.

## Preservation and tests

- All eight inline JavaScript sections: syntax checked.
- 64/64 motorcycles: headless browser drawing with rider, pose changes and thumbnail rendering passed.
- Source catalog and non-visual JavaScript code: identical to v2.8.
- Non-pilot bitmap spot checks: byte-identical output to the same models under v2.8.
- Academic integrity restrictions, academic practice, badge claims, backup/export and career ID/storage logic: preserved at source level.
- Save key remains `throttle-quest-career-v04`, alongside the v2.6 separate integrity storage.
- No terrain physics, handling, rewards, course difficulty, purchases or motorcycles were added/removed.

**Outstanding before classroom release:** Chromebook real-device riding tests, garage selection and purchase/preview checks, save/export/import checks against realistic fictional existing careers, and subjective art review. Rendering tests are not proof that every game interaction has been tested end-to-end.

---

## v2.8 cumulative documentation (preserved)

# Throttle Quest v2.8 — Motorcycle Visual Identity Update

## Installation (you upload)

This is a **complete cumulative release** built directly from the corrected v2.7.1 release. To install it, first export a career backup from **Settings → Export** in Throttle Quest. Then replace **both `index.html` and `README.md`** in the root of your existing `jkramer-cloud/throttle-quest` GitHub repository. Keep other files and PlayForge links unchanged.

## New in v2.8

- Different vehicle silhouettes: compact trail, aggressive motocross, enlarged enduro, cross-country, vintage and slender electric.
- Different tank/shroud, tail, seat profile, headlight and front-fender shapes tied to vehicle type, power class and historical model.
- Electric motorcycles show a battery enclosure and sealed electric motor with **no muffler, header or exhaust system**. The garage inspector identifies their battery/motor rather than describing them as a combustion engine.
- Updated rider posture according to the family of motorcycle.
- The same rendered bike design is used in rides, the garage, shop, thumbnails and inspections.

The change is primarily visual. Wheel centers, gameplay physics, purchases, achievements, educational questions, local saves, v2.6 learning-integrity safeguards, v2.7 courses, helmet accessories and tire trails remain as before. The unchanged save key is `throttle-quest-career-v04`, and the separate integrity state is retained.

**Note:** Only the existing motorcycle disciplines are represented in the catalog. Vintage is a subset of existing motocross/enduro models, not a new shop class. This update does not add a new trials, supermoto or special hill-climb motorcycle catalog.

## Testing

The cumulative source was checked against the original v2.7.1 file. Browser tests were run using representative trail, motocross, enduro, cross-country and electric previews, and the original source catalog and physics were kept unchanged. Please verify in a school Chromebook before rolling it out to students.

---

## Prior release details (v2.7.1)

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
