# Confetti: Play the show

Step through one episode of Confetti, Facebook's first interactive game show, in the screens I designed. I led product design for it at Meta, on Facebook Watch, from 2018 to 2019.

**Live:** https://isaakhayes.github.io/confetti-demo/

## How it is built

Every interface layer is drawn in code at the size of the original screens (676 by 1171 pixels), so it stays sharp and matches the original layout: the LIVE badge and viewer count, the chat, the INVITE and comment bar, the reactions, the question card and answer rows, the status pills, the friend circles at the top, the scoreboard, the end-of-game result cards, the Facebook post and the Android navigation bar. The chat names, friend names and winners are made up. The fonts are embedded, so nothing loads from outside.

The video behind the interface is a separate image for each screen, so I can drop in frames from the raw files.

## Adding the raw frames

Put these images in a folder named `assets` next to `index.html`. Use the exact names. Each should be a portrait frame of the whole phone screen, taken from the show with no interface on it (no LIVE badge, no chat, no question card). JPG. The page fits each frame to the screen and keeps the top, so frames with the same proportions as the original screens (676 by 1171) fit best.

| File | The frame behind |
|---|---|
| `bg-feed-media.jpg` | The countdown graphic in the Facebook post |
| `bg-countdown.jpg` | The countdown, "The game starts in" |
| `bg-open-s.jpg` | The neon S title card |
| `bg-open-logo.jpg` | The Confetti logo |
| `bg-host-1.jpg` | The host arrives |
| `bg-host-2.jpg` | The host sets the room |
| `bg-host-wide.jpg` | The wide shot of the stage |
| `bg-q1.jpg` | Question 1 |
| `bg-timesup.jpg` | Time's up |
| `bg-right.jpg` | Right answer |
| `bg-inrunning.jpg` | Players in the running |
| `bg-scoreboard.jpg` | The video strip above the scoreboard |
| `bg-partyfoul.jpg` | Party foul |
| `bg-final.jpg` | The final question |
| `bg-end.jpg` | The dimmed frame behind the end-of-game result cards |
| `bg-tune.jpg` | The "Tune in tomorrow" graphic |

Any file that is missing falls back to a built-in background, so you can add them one at a time.

## Using it

Press Play the show to watch it run like a short film, or tap one of the five chapters on the right to jump to that part: The invitation, The show opens, The question, The scoreboard and The end. The arrows (or the arrow keys) step one screen at a time. Start over returns to the first screen. On the question, you have 10 seconds: tap an answer, and tap another to change it until the clock hits zero. A right answer pops confetti, keeps you in, and fills the trophy at the top. Your free lives sit in the center of the top bar as a heart. It animates in as an outlined heart with a plus, and a heartbeat nudges you to tap it until you first do. Finishing the game earns your first life: the heart fills and shows 1 with a +1. Tap the heart any time to open the scoreboard: the heart flies into the Free Lives tile, and once you have earned a life, a Free Lives card shows where it came from. The X or a tap on the video closes it. A wrong one puts you out, and the show carries on without you. Start over returns to the first screen. It works on desktop and phone.
