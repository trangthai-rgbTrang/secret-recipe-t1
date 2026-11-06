# PLAN.md: T1 – Chị Trang + My

**Game: Vault Guard** · KFC · Limitation card: **60-Second Run**

## Pitch (one sentence)
You are the night cook, trying to keep the 11 secret herbs & spices in the vault, before the 60-second shift change ends your watch.

## Theme and limitation
The secret recipe: the 11 herbs & spices recipe card locked in the kitchen vault (KFC). It is the thing the player protects, and it is also the health bar: 11 herb slots on the card, each spy that reaches the vault steals one.
Limitation: **60-Second Run** – a full run lasts 60 seconds or less. How it shapes the core mechanic: the run *is* one 60-second night shift. The player only has to hold the vault until 0:00, so the clock is the win condition. Pressure is built around the 60 s: spies get faster every 15 s, and the last 10 s is a RUSH. A run ends early if all 11 herbs are stolen, so it never goes over 60 s.

## Core loop
What the player does every 5 seconds: spies pop out of 6 kitchen doors and run toward the vault in the middle → the player taps/clicks each spy before it gets in → a caught spy pops (sound + burst); a spy that gets in steals one herb from the recipe card (alarm + card shakes).

## Controls
- Phone: tap a spy.
- Desktop: click a spy. Space or Enter starts and restarts a run.
- One input only. No keyboard movement, so it plays the same on phone and laptop.

## Win, lose and score
- **Win:** the clock reaches 0:00 with at least 1 herb still in the vault.
- **Lose:** all 11 herbs are stolen before 0:00.
- **Score:** herbs left × 100 + spies caught × 10. Best score is kept on the device.

## MVP: must ship (5 items max, in build order; playable after item 3)
| # | Item | Owner | Minutes | Done when |
|---|------|-------|---------|-----------|
| 1 | Title screen with "Tap to start" and the fan-made notice, 60 s countdown, end screen with restart | Trang (drive) | 8 | Start → clock runs 60 → 0 → end screen → restart starts a new 60 s run |
| 2 | Vault + recipe card with 11 herb slots; spies spawn from 6 doors and walk to the vault; a spy that arrives removes 1 herb; 0 herbs = lose | My (drive) | 10 | Doing nothing loses herbs one by one and ends in "Recipe stolen!" before 0:00 |
| 3 | Tap/click a spy to catch it (hit area ≥ 44 px), score, win/lose screens with the score | Trang (drive) | 7 | A playtester can win one run on a phone and on a laptop; score shows on the end screen |
| 4 | Difficulty ramp: spies faster and more frequent every 15 s; last 10 s RUSH (red pulse, clock grows) | My (drive) | 5 | Spawns at 0:50 are clearly faster than at 0:05; RUSH visible from 0:10 |
| 5 | Feel: Web Audio sounds (catch pop, steal alarm, last-10 s tick), catch burst, card shake, best score in localStorage | Trang (drive) | 8 | Every catch and steal has a sound and a visual; best score survives a reload |

Total: 38 minutes.

## Stretch: only after MVP (cut from the bottom)
1. Golden drumstick power-up: tap it to freeze all spies for 2 s.
2. Disguised spy (dressed as a delivery driver) that needs 2 taps.
3. "Herb #7 stolen!" floating text when a herb is stolen.

## Risks and fallbacks (top 2)
- Risk: taps miss on phones (canvas scaling, small targets, touch vs click) / Fallback: draw each spy as an absolutely-positioned DOM element with a large hit area instead of hit-testing on the canvas.
- Risk: the first GitHub Pages deploy is slow or fails, and we miss the 0:55 link / Fallback: publish the hello-world page at plan lock to prove the link early; if Pages still fails, publish the same folder to Netlify with the CLI.

## Team roles
Only two of us, so roles are shared. **Trang:** producer (owns this file, the clock and the cut list) and driver. **My:** playtester and designer, and driver for items 2 and 4. We swap the keyboard about every 20 minutes. One MVP item per prompt; whoever didn't write the prompt plays the build.

## Milestones
- 0:30 Plan link (this file)
- 0:55 First playable: MVP items 1 to 3
- 1:35 Final: all MVP items

## Change log (fill in while you build)
| Time | Change | Why |
|------|--------|-----|
| 0:16 | Plan locked: Vault Guard picked over Sauce Memory Rush and Spice Heist 60 | Lowest build risk for a 2-person team; one tap input works the same on phone and laptop; Spice Heist was too close to the host's example |
