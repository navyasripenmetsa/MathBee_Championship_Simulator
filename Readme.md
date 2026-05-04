# Math-Bee Championship

A console-based mathematics quiz application built in C that tests players across four progressive difficulty levels - from basic arithmetic to calculus. The game covers a broad range of mathematical topics and is designed to challenge students at multiple stages of learning.

---

## Overview

Math-Bee Championship presents randomized math problems to a single player and evaluates answers in real time. Each difficulty level targets a distinct set of mathematical concepts, and the scoring system reflects the complexity of each level. The application runs entirely in the terminal with no external dependencies beyond the standard C libraries and the Windows API.

---

## Features

- Four difficulty levels with distinct question categories
- Randomized problem generation to ensure a unique experience on every run
- Real-time answer validation with score tracking
- Explanations provided for incorrect answers in select question types
- Named player session with a final score reported at the end of each level

---

## Difficulty Levels

### Easy
Intended for foundational arithmetic practice.

- Addition, subtraction, and multiplication of two-digit integers
- Integer division with guaranteed whole-number results
- Single-variable linear equations

### Medium
Covers applied mathematics and introduces multi-step reasoning.

- Order of operations (BODMAS) with mixed arithmetic expressions
- Simultaneous linear equations with two unknowns
- Area calculation for six geometric shapes: square, rectangle, triangle, parallelogram, rhombus, and hexagon
- Unit conversion problems across time, length, mass, volume, and currency
- Mathematical riddles requiring logical deduction

### Difficult
Targets secondary-school level topics.

- Arithmetic progressions: finding the nth term given the first term and common difference
- Geometric progressions: finding the nth term given the first term and common ratio
- Quadratic equations: solving for both real roots
- Multi-step mathematical riddles

### Expert
Designed for advanced problem-solving.

- Combinatorics-based probability problems with pre-computed answers
- Last-digit problems using modular exponentiation
- Polynomial differentiation: evaluating the derivative of a degree-5 polynomial at a given point
- Polynomial integration: computing the definite integral of a degree-5 polynomial

---

## Technical Details

| Property | Detail |
|---|---|
| Language | C (C99 standard) |
| Platform | Windows (uses `windows.h` for audio feedback) |
| Compiler | GCC / MinGW recommended |
| Dependencies | `stdio.h`, `stdlib.h`, `math.h`, `string.h`, `time.h`, `stdbool.h`, `windows.h` |

### Problem Generation

All numerical parameters are generated using seeded pseudorandom number generation via `srand(time(NULL))`. For questions involving algebra, the application constructs the problem by working backwards from a known answer — for example, quadratic problems are built from two randomly selected roots, and simultaneous equations are built from a known solution pair. This guarantees that every generated problem has a valid, integer solution.

### Scoring

| Level | Points per Correct Answer |
|---|---|
| Easy | 30 per arithmetic question, up to 150 total |
| Medium | 50 per question, up to 250 total |
| Difficult | 65 per question, up to 260 total |
| Expert | 85 per question, up to 340 total |

---

## Getting Started

### Prerequisites

- A C compiler with Windows API support (GCC via MinGW or MSVC)
- Windows operating system (required for `Beep()` and `windows.h`)

### Build

```bash
gcc mathbee.c -o mathbee -lm
```

### Run

```bash
./mathbee
```

On launch, enter the player name and select a difficulty level by typing one of the following:

```
EASY
MEDIUM
DIFFICULT
EXPERT
```

---

## Project Structure

```
mathbee.c           # Single-file application containing all logic
```

All question generation, answer evaluation, score management, and output are contained within a single source file. Functions are organized by category: arithmetic, geometry, unit conversion, sequences, equations, probability, and calculus.

---

## Known Limitations

- Windows-only due to the use of `Beep()` from `windows.h`. Removing or stubbing out the `Beep()` calls makes the code portable to Linux and macOS.
- The riddle question bank is static. Adding new riddles requires modifying the source arrays directly.
- The probability question bank uses pre-computed floating-point answers matched with a tolerance of 0.001, which may require adjustment for edge cases.

---

## License

This project is protected under "All Rights Reserved".
Unauthorized copying, modification, or distribution is strictly prohibited.
