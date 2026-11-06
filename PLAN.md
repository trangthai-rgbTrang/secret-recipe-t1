# PLAN.md: T1 – Chị Trang + My

## Pitch (one sentence)
You are the night cook, trying to stop sneaky spies from stealing KFC's secret recipe, before the 60-second shift ends.

## Theme and limitation
The secret recipe: KFC's 11 herbs & spices, kept as a recipe card in the kitchen vault. Each spy that reaches the vault grabs one herb and runs; lose all 11 and the recipe is gone.
Limitation: 60-Second Run. How it shapes the core mechanic: one run is one 60-second night shift, so holding the vault until 0:00 is the win. A new wave every 15 s brings faster spies, and the last 10 s is a RUSH.

## Core loop
What the player does every 5 seconds: tap the spies sneaking from the doors toward the vault; when one gets through, a herb flies off the card and a hole opens, so leave the 🔧 cook alone while he walks over and patches it.

## Controls
Tap (phone) or click (laptop). Space or Enter starts and restarts. Type your name on the title screen.

## Win, lose and score
Win: at least 1 herb left at 0:00. Lose: all 11 herbs stolen before 0:00. Score: herbs left × 100 + spies caught × 10 + holes patched × 5 − cooks hit × 50. Each name's best score goes into a top 10 on the device.

## MVP: must ship (5 items max, in build order; playable after item 3)
| # | Item | Owner | Minutes | Done when |
|---|------|-------|---------|-----------|
| 1 | ✅ Title screen told in pictures, no sentences: 🕵️ ➜ 🔐📜 ❌ · 👆🕵️ ✅ · 👆🧑‍🍳 ❌ · ⏱ 60; name field with 👤; big ▶ button; fan-made notice; 60 s countdown; end screen with ↻ restart | Trang | 9 | A first-time player can say what the game is about from the pictures alone, without reading |
| 2 | ✅ Vault labelled "SECRET RECIPE" + card with 11 herbs; spies walk from 6 doors; on arrival a herb flies from the card to the spy, who runs back out; 0 herbs = lose | My | 10 | Doing nothing shows herbs flying away one by one and ends in "Recipe stolen!" |
| 3 | ✅ Tap a spy +10. Each spy that gets in leaves a hole 🕳️ in the vault; a cook carrying 🔧 walks from a door to the hole (green dotted line) and patches it (green progress ring), +5. Tapping a cook = −50 and the hole stays open. First 5 s are a guided wave in pictures: a bouncing 👆 over one slow spy, then a 🚫 over the first cook | Trang | 11 | A first-time player catches a spy, leaves the 🔧 cook alone and sees the hole close, without anyone explaining and without reading |
| 4 | ✅ A new wave every 15 s with an icon banner (⚡🕵️🕵️); last 10 s RUSH (red pulse, big ⏱) | My | 3 | Banners show at 0:45, 0:30, 0:15 and spies are clearly faster each time |
| 5 | ✅ Local top 10 by name; end screen in icons (🌿 × 100, 🕵️ × 10, 🧑‍🍳 −50) with the rank as 🏆 #2 | Trang | 6 | Two different names both appear in the top 10 after a reload, in score order |

## Stretch: only after MVP (cut from the bottom)
1. Web Audio sounds: catch pop, steal alarm, oops buzz, RUSH tick.
2. Combo ×2 / ×3 for catches within 1 s (a cook tap resets it); Perfect shift +500 when no herb is lost.
3. Desktop layout (≥ 900 px): how-to-play panel left, live top 10 right; "Copy score" button to challenge others in chat.

## Risks and fallbacks (top 2)
- Risk: newcomers don't get what to tap or why herbs disappear / Fallback: keep the guided first wave and the flying-herb animation even if other items slip; cut wave banners first.
- Risk: cooks and spies both walk toward the vault and get mixed up / Fallback: cooks always carry a 🔧 badge, have a green ring and a green dotted line to their hole; spies have a red ring and red trail.

## Milestones
- 0:55 First playable: MVP items 1 to 3
- Final: all MVP items

## Change log (fill in while you build)
| Time | Change | Why |
|------|--------|-----|
| 0:10 | Picked Vault Guard over Sauce Memory Rush and Spice Heist 60 | Lowest build risk for 2 people; one tap input works on phone and laptop |
| 0:39 | Added night-crew cooks to MVP 3 (tap = −50); added a local top 10 by name; combo and Perfect shift added as stretch | Tapping only spies could be spammed; names and ranks make it competitive |
| 0:41 | Added a picture story on the title screen, a guided first wave, flying-herb steal feedback and wave banners; sounds moved to stretch 1, combo to stretch 2 | A stranger couldn't tell what the game was about; learning by playing beats a rules screen; MVP kept at 39 min |
| 0:43 | All hints and banners use icons instead of sentences (the only fixed text is the required fan-made notice) | Players read little; pictures work for everyone, on a phone, at a glance |
| 0:45 | Cooks now have a job: each spy that gets in leaves a hole, a 🔧 cook walks over and patches it (+5); tapping him costs −50 and leaves the hole open. MVP 3 to 11 min, MVP 4 to 3 min | Gives the "don't tap" rule a visible reason; patching rewards patience, but less than catching spies |
| 0:50 | Built MVP 1–3 in one pass and published the first playable | The plan ran long; one pass was the fastest way to a link that runs |
| 0:50 | Catching a spy that is running out with a herb sends the herb back to the card | Clear cause and effect in pictures; a few lines of code |
| 0:51 | Playtest: an idle run lost all 11 herbs in about 25 s, so wave 1 is gentler (a spy every 2 s, 0.8× speed) | Too hard for first-timers |
| 0:53 | MVP 4 and 5 done. The vault shows 📜 instead of a "SECRET RECIPE" text label | Pictures over words |
| 0:56 | Playtest (Trang): the end screen only had Play again. Added 🏠 home and 🏆 buttons and a full top 10 screen, also reachable from the title | Players want to see the ranking and go back without starting a new run |
| 0:59 | Playtest (Trang): too easy. Waves 2–4 faster; from 0:30 left a quarter of spies are disguised as cooks (no 🔧, no green line, +20); a spy carrying a herb runs twice as fast; combo ×2/×3 for catches within 1 s, lost on a missed tap or a cook tap; Perfect shift +500; HUD shows the 👑 device leader with ▲/▼ | Players should feel pressure and want another go; stretch 2 pulled in, desktop layout (stretch 3) and sounds (stretch 1) still cut |
| 1:09 | Added v2 at /v2/: same game, but you steer a 🍳 pan with WASD/arrow keys (or tap where to go) and catch spies by touching them; bumping a 🔧 cook costs −50. Own top 10. v1 (tap) stays the main link | Trang asked for a farm-style keyboard version; kept as a separate page so the tap version stays safe |
