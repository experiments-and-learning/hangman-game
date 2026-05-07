# Hangman Game

[![Type](https://img.shields.io/badge/Type-Personal_Project-blue)](https://github.com/experiments-and-learning/hangman-game)
[![Status](https://img.shields.io/badge/Status-Completed-green)](https://github.com/experiments-and-learning/hangman-game)
[![Stack](https://img.shields.io/badge/Stack-Python%20%7C%20Pygame%20%7C%20Figma-informational)](https://github.com/experiments-and-learning/hangman-game)

A desktop Hangman game built with Python and Pygame. All visual assets — screens, hangman stage illustrations, and UI buttons — were designed in Figma and exported as PNGs. Word lists for animals and fruits are loaded from text files at runtime.

---

## How It Works

1. A random word is selected from the word list (`animals.txt` or `fruits.txt`)
2. The player sees blank slots representing each letter
3. The player clicks letter buttons to guess
4. Correct guesses reveal letters in their positions; incorrect guesses draw the hangman figure one stage at a time through the OpenHead → OpenHeadBody → … → OpenFullBody sequence
5. The game ends when the word is fully revealed (win) or all stages are drawn (loss)
6. The player is prompted with a yes/no screen to play again

---

## Directory Structure

    hangman-game/
    ├── assets/
    │   ├── BG.png                          ← game background
    │   ├── CloseTitleScreen.png            ← title screen (closed/start state)
    │   ├── Dashca.png                      ← dash/blank tile graphic
    │   ├── Exit Screen.png                 ← exit confirmation screen
    │   ├── Game Over Screen.png            ← game over screen
    │   ├── Open.png                        ← gallows (no figure yet)
    │   ├── OpenFullBody.png                ← hangman stage 6 (full body)
    │   ├── OpenHead.png                    ← hangman stage 1 (head only)
    │   ├── OpenHeadBody.png                ← hangman stage 2 (head + body)
    │   ├── OpenHeadBodyBothArmsLLegs.png   ← hangman stage 5
    │   ├── OpenHeadBodyBothArms.png        ← hangman stage 4
    │   ├── OpenHeadBodyLArm.png            ← hangman stage 3
    │   ├── Splash.png                      ← splash/loading screen
    │   ├── animals.txt                     ← animal word list
    │   ├── assets.txt                      ← asset manifest
    │   ├── fruits.txt                      ← fruit word list
    │   ├── no_button.png                   ← no button graphic
    │   └── yes_button.png                  ← yes button graphic
    ├── hangman.py
    ├── LICENSE.txt
    └── README.md

---

## Prerequisites

- Python 3.8+
- Pygame

---

## Setup and Run

     1. Clone the repository
    git clone https://github.com/experiments-and-learning/hangman-game.git
    cd hangman-game

     2. Install Pygame
    pip install pygame

     3. Run the game
    python hangman.py

---

## Controls

| Input | Action |
|---|---|
| Mouse click on letter | Guess that letter |
| Click Yes | Play again |
| Click No | Quit |

---

## Design Notes

All UI assets were created in Figma before implementation. The hangman figure is rendered progressively using the stage PNGs (`OpenHead` → `OpenHeadBody` → `OpenHeadBodyLArm` → `OpenHeadBodyBothArms` → `OpenHeadBodyBothArmsLLegs` → `OpenFullBody`), each loaded and swapped in at the corresponding wrong-guess count.

---

## License

MIT License
