# Rock-Paper-Scissors (Two-Player) — Logic Plan

## Project Goal
Build a two-player **Rock–Paper–Scissors** game in **Python** (JupyterLab/Jupyter Notebook).  
The game will:
- Ask Player 1 and Player 2 for their choices
- Validate input (only rock/paper/scissors allowed)
- Determine the winner based on the rules
- Ask if they want to play again (loop until they stop)

---

## Game Rules

| Choice    | Beats     |
|----------|-----------|
| Rock     | Scissors  |
| Scissors | Paper     |
| Paper    | Rock      |

If both players choose the same option, the result is a **tie**.

---

## Program Flow (Step-by-Step)

1. Ask Player 1 to enter: `rock`, `paper`, or `scissors`
2. Ask Player 2 to enter: `rock`, `paper`, or `scissors`
3. Validate both inputs  
   - If invalid, show an error and ask again
4. Compare choices and determine the winner
5. Print the result (tie / Player 1 wins / Player 2 wins)
6. Ask: “Play again? (yes/no)”
7. If **yes**, repeat steps 1–6  
   If **no**, end the program

---

## Concepts Used (and Why)

| Concept | Purpose |
|--------|---------|
| `input()` | Collect player choices |
| `while` loop | Keep the game running until players quit |
| `if / elif / else` | Compare player choices and decide winner |
| `in` operator | Validate input is one of the allowed options |
| `break` | Exit the loop when the players say no |
| `def` (functions) | Keep code organized and readable |

---

## Input Validation Plan
Allowed inputs: `rock`, `paper`, `scissors`

Validation idea:
- Convert input to lowercase using `.lower()`
- Check membership using:
  - `choice in ["rock", "paper", "scissors"]`
- If invalid:
  - Print: “Invalid choice. Try again.”
  - Re-prompt the player

---

## Winner Logic Plan

- If choices are the same → **Tie**
- Player 1 wins if:
  - `rock` beats `scissors`
  - `scissors` beats `paper`
  - `paper` beats `rock`
- Otherwise → **Player 2 wins**

---

## Author
Amber Martin — Healthfirst Data Analytics Academy (Cohort 6)
