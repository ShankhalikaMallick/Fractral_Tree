# 🌿 Recursive Fractal Tree (Animated)

A dynamic visualization of a fractal tree built with **Processing.js**. This project uses recursive algorithms and trigonometric functions to create a "breathing" effect, where the branches open and close smoothly.

## 🚀 Overview

This project was developed and tested on [CodePen](https://codepen.io). It demonstrates how simple mathematical rules can generate complex, organic-looking patterns. The tree's branches oscillate between a closed state and a 180-degree total spread.

## 🛠️ Technical Breakdown

### 1. Recursion
The tree is built using a recursive function `drawFractal()`. Each branch renders a line, moves to the end of that line, and then calls itself twice to create two new, smaller branches. 

### 2. Smooth Oscillation (The "Breathing" Effect)
Instead of a simple linear rotation, I used a **Cosine Wave** to control the movement:
* **Function**: `cos(frameCount * 0.02)`
* **Effect**: This creates an "easing" effect where the tree slows down as it reaches its widest and narrowest points, making the animation feel organic.

### 3. Trigonometric Mapping
To ensure the tree stays within a specific range, the cosine wave is mapped to a radian range:
* **Range**: `0` to `PI/2` (90 degrees) per side.
* **Total Spread**: Since both the left and right branches rotate, the tree reaches a maximum opening of **180 degrees**.

## 🎨 How to Customize

You can modify the following parameters in the code to change the tree's appearance:

| Variable | Description |
| :--- | :--- |
| `startSize` | Adjusts the initial height of the trunk. |
| `len * 0.7` | Controls the "shrink factor" of each new branch level. |
| `depth < 10` | Defines how many generations of branches are drawn. |
| `stroke(r, g, b)` | Changes the color of the tree. |

## 💻 How to Run
1. Clone this repository.
2. Open `index.html` in any web browser.
3. The project uses the `processing.min.js` CDN, so an internet connection is required to load the library.

---
*Created as an exploration into creative coding and recursive geometry.*
