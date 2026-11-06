# PLAN.md: T1 – Chị Trang + My

## Pitch (one sentence)
You are the night cook, trying to keep the 11 secret herbs & spices in the vault, before the 60-second shift change ends your watch.

## Theme and limitation
The secret recipe: KFC's 11 herbs & spices recipe card, locked in the kitchen vault. The player protects it; each spy that reaches the vault steals one herb.
Limitation: 60-Second Run. How it shapes the core mechanic: one run is one 60-second night shift, so holding the vault until 0:00 is the win. Spies speed up every 15 s and the last 10 s is a RUSH.

## Core loop
What the player does every 5 seconds: spot the spies running from 6 doors toward the vault and tap each one before it gets in.

## Controls
Tap (phone) or click (laptop) a spy. Space or Enter starts and restarts a run.

## Win, lose and score
Win: at least 1 herb left at 0:00. Lose: all 11 herbs stolen before 0:00. Score: herbs left × 100 + spies caught × 10.

## MVP: must ship (5 items max, in build order; playable after item 3)
| # | Item | Owner | Minutes | Done when |
|---|------|-------|---------|-----------|
| 1 | Title screen ("Tap to start" + fan-made notice), 60 s countdown, end screen with restart | Trang | 8 | Start → 60 → 0 → end screen → restart works |
| 2 | Vault + recipe card with 11 herbs; spies walk from 6 doors to the vault; each arrival steals 1 herb; 0 herbs = lose | My | 10 | Doing nothing loses herbs one by one and ends in "Recipe stolen!" |
| 3 | Tap/click a spy to catch it (big hit area), score, win/lose screens | Trang | 7 | A playtester wins one run on a phone and on a laptop |
| 4 | Difficulty ramp every 15 s; last 10 s RUSH (red pulse) | My | 5 | Spies at 0:50 are clearly faster than at 0:05 |
| 5 | Web Audio sounds (catch, steal, last-10 s tick), catch burst, best score in localStorage | Trang | 8 | Every catch and steal has a sound; best score survives a reload |

## Stretch: only after MVP (cut from the bottom)
1. Golden drumstick: tap it to freeze all spies for 2 s.
2. Disguised spy (delivery driver) that needs 2 taps.
3. "Herb #7 stolen!" floating text.

## Risks and fallbacks (top 2)
- Risk: taps miss on phones (canvas scaling, small targets) / Fallback: spies as DOM elements with large hit areas instead of canvas hit-testing.
- Risk: GitHub Pages fails or lags before the 0:55 link / Fallback: publish the same folder to Netlify.

## Milestones
- 0:55 First playable: MVP items 1 to 3
- Final: all MVP items

## Change log (fill in while you build)
| Time | Change | Why |
|------|--------|-----|
| 0:10 | Picked Vault Guard over Sauce Memory Rush and Spice Heist 60 | Lowest build risk for 2 people; one tap input works on phone and laptop |
