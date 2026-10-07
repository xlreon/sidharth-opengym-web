# Sidharth — openGym plan import

Plan file: `/workspace/sidharth-opengym-plan.json`  
Demo: https://opengym.duarte-santos.ch/demo/

## 1. How to import

1. Open https://opengym.duarte-santos.ch/demo/ and **create a profile** (kg units).
2. Set **week starts Monday** in profile/settings (`weekStart` Monday). Week keys in the file are already Mon=1 … Sat=6; Sunday is omitted (rest).
3. Plan → Share / Import → import `sidharth-opengym-plan.json`.
4. When prompted, **accept the custom exercises** (`cx_*`) — they are not in the library and will be dropped if you skip them.
5. Enable **replace schedule** (or assign routines manually) so the week becomes:
   - Mon `Push + Abs`
   - Tue `Pull + Abs`
   - Wed `Legs`
   - Thu `Upper leftovers + Abs`
   - Fri `Plyo + Abs`
   - Sat `Sport (pick one)`
   - Sun empty (rest)
6. One routine per day after import. Fill missing weights as you go (most lifts leave weight empty; bench starts at **50 kg** as a working suggestion under your 60 kg best).

## 2. Library search names vs your names

| Your name | Library id | Library search name (`n`) |
|---|---|---|
| Barbell bench press | `0025` | barbell bench press |
| Smith shoulder press | `0766` | smith shoulder press |
| Low cable chest fly | `0179` | cable low fly |
| Dumbbell lateral raise | `0334` | dumbbell lateral raise |
| Cable pushdown | `0201` | cable pushdown |
| Overhead triceps (rope) | `0194` | cable overhead triceps extension (rope attachment) |
| Hanging leg raise | `0472` | hanging leg raise |
| Bicycle crunch | `0003` | air bike |
| Flutter kicks | `0459` | flutter kicks |
| Lat pulldown | `0150` | cable bar lateral pulldown |
| One-arm DB row | `0292` | dumbbell one arm bent-over row |
| Dumbbell pullover | `0375` | dumbbell pullover |
| Face pull | `0203` | cable rear delt row (with rope) |
| EZ-bar curl | `0447` | ez barbell curl |
| Preacher curl | `0070` | barbell preacher curl |
| Smith squat | `0770` | smith squat |
| Romanian deadlift | `0085` | barbell romanian deadlift |
| Walking lunge | `1460` | walking lunge |
| Lying leg curl | `0586` | lever lying leg curl |
| Standing calf raise | `0605` | lever standing calf raise |
| Leg press | `0739` | sled 45° leg press |
| Incline bench | `0047` | barbell incline bench press |
| Seated cable row | `0861` | cable seated row |
| High-to-low cable fly | `0227` | cable standing fly |
| Reverse pec deck | `0602` | lever seated reverse fly |
| Skull crushers | `0060` | barbell lying triceps extension skull crusher |
| Cable curl | `0868` | cable curl |
| Decline crunch | `0277` | decline crunch |
| Russian twist | `0687` | russian twist |
| Mountain climbers | `0630` | mountain climber |
| Quick feet | `3552` | quick feet v. 2 |
| Jump squat | `0514` | jump squat |
| Skater hops | `3361` | skater hops |
| High knees | `3636` | high knee against wall |
| Broad / low box jump | `1472` | forward jump |
| Dead bug | `0276` | dead bug |
| Easy bike | `2138` | stationary bike run v. 3 |

Upright rows are **not** in this plan (intentionally omitted).

## 3. Custom exercises to accept on import (missing from library)

| id | Name | bp | Notes |
|---|---|---|---|
| `cx_forearm_plank` | Forearm plank | waist | Tue abs — time 60 s |
| `cx_bird_dog` | Bird dog | back | Tue abs — 10/side |
| `cx_superman_hold` | Superman hold | back | Tue abs — time 15 s |
| `cx_pogo_hops` | Pogo hops | cardio | Fri plyo — tiny bounce |
| `cx_side_plank` | Side plank | waist | Fri abs — 30 s each side |
| `cx_plank_hip_dip` | Plank hip dip | waist | Fri abs — time 45 s |
| `cx_pickleball` | Pickleball | cardio | Sat — pick **one** sport; ~50 min |
| `cx_swim` | Easy swim | cardio | Sat — pick **one** sport; 30 min |

## 4. Reminders

- **Cardio** (pickleball, swim, bike): use `mode: cardio` / `min` (minutes), not reps.
- **Timed abs / holds** (air bike, flutter kicks, planks, Superman, Russian twist, mountain climbers, etc.): use `mode: time` / `sec` — never put seconds in `reps`.
- **Abs progression note** (on ab exercises): 60 s between rounds; after main session. Week 2 +5 sec or +2 reps; Week 3 same again; Week 4 hold. `restSec` 30 is between exercises within a round.
- **Shin rules**: no run on leg day; if shins heat up, drop jumps and mountain climbers (keep quick feet); Friday abs only if shins quiet — else move abs to Saturday.
- **Abs from this plan only** — do not stack another ab program.
- **Unilateral lifts** (one-arm row, walking lunge, skater hops, bird dog, dead bug): `side: true` with **total** reps across both sides (e.g. 16 = 8/side). Notes say each side.
- Most lift **weights are empty** for you to fill; bench suggests **50 kg** under your 60 kg best — leave 1–2 reps in reserve and add a little each set.
