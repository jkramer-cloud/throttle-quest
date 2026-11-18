# Throttle Quest v1.1 — Learning Expansion

A self-contained, account-free educational hill-climb game for grades 5–8. Open `index.html` in Chrome or host it on GitHub Pages. No dependencies or external assets are needed.

## Update an existing GitHub Pages site

Replace the repository's **index.html** and **README.md** with these two files. Keep the repository name and Pages URL unchanged. Existing career saves use the same local-storage key and save format, so they can carry forward on the same browser and site. Export a career backup before updating as a precaution.

## New in v1.1

- First-launch learning setup with grade 5 as the default, grades 5–8, any combination of six subjects, and three learning-event frequencies. Change preferences anytime from Settings.
- **17,637 grade-specific question variants**, including procedural mathematics and ELA, science, social studies, geography, technology and digital citizenship. Banks are deliberately unequal in size.
- Persistent, without-replacement question decks for each grade and subject; recently asked questions are avoided when the deck cycles, and eligible missed questions are prioritized on later deck cycles. Mixed subjects are shuffled in balanced rounds. Answer order is randomized independently on each encounter.
- Fuel stops, crash recovery and optional challenge bonuses now share the same career question engine. Local duels do not award career learning credit and use separate session history.
- Records include grade and subject accuracy, topic-level accuracy, explored-bank counts, streaks, learning achievements, and CSV/print reports.
- Riding physics, courses, rider controls, garage, bike catalog, paid parts, cosmetics, and coin rewards are retained from v1.0.

## Question coverage

| Grade | Math | ELA | Science | Social studies | Geography | Technology | Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 5 | 2692 | 778 | 261 | 55 | 258 | 118 | 4162 |
| 6 | 3125 | 775 | 245 | 156 | 204 | 163 | 4668 |
| 7 | 3125 | 775 | 245 | 155 | 184 | 154 | 4638 |
| 8 | 2729 | 647 | 245 | 156 | 246 | 146 | 4169 |
| Total | 11671 | 2975 | 996 | 522 | 892 | 581 | 17637 |

Counts are generated, grade-specific prompt variants, not individually authored lessons. Some skills and prompts overlap grades. This is practice content, not a formal standards-aligned assessment. Smaller non-math banks should be expanded with additional original questions in future releases.

## Local data

All career history and learning preferences remain on the browser/device; they do not sync between Chromebooks. Career backups include the new question history. Older subject totals are retained separately, and detailed grade/topic records start in v1.1. Clearing browser data removes local history unless a backup is restored.

## Testing

Question generation, all 24 complete subject/grade deck cycles, answer-option uniqueness and position variation, state serialization and mixed-subject rotation were checked programmatically. Local Chromium smoke testing covered startup, settings, restored saved state, records, and entering a ride. Classroom Chromebook playtesting is still recommended. The game remains an illustrative simulation, not real vehicle tuning guidance.
