# 🧠 Math-Bee Championship — C Programming Project 🎮

## 📌 Overview

**Math-Bee Championship** is a console-based math quiz game developed in **C**. The program generates random math questions from different topics and difficulty levels, evaluates user answers, and calculates a score based on performance.

This project demonstrates core **C programming**, **problem-solving**, and **mathematical logic implementation**.

---

## ✨ Features

* Four difficulty levels: **Easy, Medium, Difficult, Expert**
* Randomly generated questions each time the program runs 🔄
* Multiple math topics covered:

  * ➕ Basic Arithmetic
  * 📘 Linear Equations
  * 📈 AP & GP
  * 🔺 Quadratic Equations
  * 📐 Geometry (Area problems)
  * 🔁 Unit Conversions
  * 🧩 Logical Riddles
  * 🎲 Probability
  * 📉 Differentiation
  * ∫ Integration
* 🏆 Score calculation system
* ⌨️ User input-based interactive gameplay
* 🔷 ASCII shape drawing for geometry questions
* 🔊 **Beep sound alert for incorrect answers** using `Beep()` from `windows.h`

---

## 💻 Programming Concepts Used

| Concept                  | Description                                       |
| ------------------------ | ------------------------------------------------- |
| Functions                | Separate functions for each type of question      |
| Pointers                 | Score updated using pointer variables             |
| Arrays                   | Used for storing questions, answers, coefficients |
| Strings                  | Used for player name and level selection          |
| Random Numbers           | `rand()` used to generate random questions        |
| Math Functions           | `pow()`, `sqrt()`, `roundf()`                     |
| Conditional Statements   | `if`, `switch`                                    |
| Loops                    | `for`, `while`                                    |
| Modular Programming      | Large program divided into smaller functions      |
| Floating Point Precision | EPSILON used for decimal comparison               |

---

## 🎯 Difficulty Levels

### 🟢 Easy Level

* Addition, subtraction, multiplication
* Division
* Simple linear equations

### 🟡 Medium Level

* Arithmetic expressions
* System of equations
* Geometry area problems
* Unit conversions
* Logical riddles

### 🔴 Difficult Level

* Arithmetic Progression (AP)
* Geometric Progression (GP)
* Quadratic equations
* Logical riddles

### ⚫ Expert Level

* Probability
* Last digit of powers
* Polynomial differentiation
* Polynomial integration

---

## ▶️ How to Compile and Run

### Compile

```bash
gcc math_bee.c -o math_bee -lm
```

### Run

```bash
./math_bee
```

> ⚠️ Note: The program uses `windows.h` for sound (`Beep()`), so it works best on Windows.

---

## 🧠 Skills Demonstrated

* C Programming
* Problem Solving
* Mathematical Algorithm Implementation
* Modular Programming
* Use of Pointers and Arrays
* Random Number Logic
* User Interaction via Console

---

## 🏁 Conclusion

**Math-Bee Championship** is a multi-level math quiz game that demonstrates strong fundamentals in **C programming, logic building, and mathematical computation**. This project is suitable for academic submission and placement portfolio as it shows structured programming and problem-solving ability.

