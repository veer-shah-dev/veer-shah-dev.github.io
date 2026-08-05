---
layout: page
title: Terminal Tic-Tac-Toe Game
description: Interactive two-player command-line Tic-Tac-Toe game with ASCII rendering and win-checking logic in C.
img: assets/img/3.jpg
importance: 2
category: Games & Algorithms
giscus_comments: false
---

## Overview

A terminal-based **Tic-Tac-Toe** implementation built in **C**, demonstrating key concepts in 2D array representation, matrix state checking algorithms, and robust CLI user interaction.

---

## Key Features

- **Interactive ASCII Interface**: Displays a clean 3x3 game board grid directly in the terminal interface.
- **Turn-based Logic**: Multi-player turn switching with input validation to prevent overwriting occupied slots or out-of-bounds coordinates.
- **Win & Draw Condition Algorithms**: Evaluates rows, columns, and diagonal matrices after every move to detect immediate game-ending states.
- **Error Handling**: Friendly error prompts for invalid grid choices, ensuring seamless playability.

---

## Tech Stack & Concepts Applied

- **Language**: C
- **Data Structures**: 2D Character Matrix Array (`char board[3][3]`)
- **Core Concepts**: Nested loops, conditional logic, modular state functions, input sanitization
