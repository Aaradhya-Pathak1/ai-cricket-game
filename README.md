# 🏏 AI Adaptive Cricket

A fast-paced, browser-based cricket timing game built with plain HTML5 Canvas and JavaScript — no libraries, no build step. Time your swing perfectly to hit the ball and rack up runs, but watch out: the better you do, the harder it gets.

**▶️ [Play it live](https://aaradhya-pathak1.github.io/ai-cricket-game/)**

## How to Play

- Press **SPACE** to swing the bat as the ball reaches the hit zone.
- Hit the ball within **30px of the red center line** to score a run.
- Each successful hit adds **+1** to your score and launches the ball off the bat with physics-based trajectory.
- Miss the timing, swing at air, or let the ball pass and your score resets to 0.

## Mechanics

The ball pitches in along a curved (swinging) path that always lands dead-center at the hit line, so success comes down to pure timing. A few details that make each delivery different:

- **Adaptive difficulty** — ball speed increases with your score (`baseSpeed = 5 + score × 0.6`), so the game gets progressively faster the better you play.
- **Variable swing** — each delivery curves up or down by a random amount, keeping the line unpredictable.
- **Hit physics** — struck balls fly backward and upward with gravity pulling them down, angled slightly by your timing.
- **Score history** — the side panel tracks your last 10 game scores so you can see how you're improving.

## Outcomes

| Result | Message |
|--------|---------|
| Hit within 30px of center | CRACK! GREAT HIT! (+1 run) |
| Hit inside zone but off-center | OFF CENTER! Score Reset. |
| Swing too early / at nothing | SWUNG AT AIR! Score Reset. |
| Ball passes without a swing | TOO LATE! Score Reset. |

## Tech

Single self-contained `index.html` — HTML, CSS, and JavaScript in one file, rendered on an 800×300 Canvas using `requestAnimationFrame`. Runs in any modern browser with no setup.

## Run Locally

Just open `index.html` in your browser, or clone the repo:

```bash
git clone https://github.com/Aaradhya-Pathak1/ai-cricket-game.git
cd ai-cricket-game
open index.html
```
