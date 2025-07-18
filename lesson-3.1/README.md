# 🐢 Week 3, Lesson 1: Build a Python Turtle Game with GitHub Copilot

## Welcome to Your First Game with Turtle!

You're about to explore **Turtle**, a simple yet powerful Python library that helps you create fun, graphical games using code. This lesson will guide you step-by-step from basics to building and sharing your very own game!

## 🎯 Lesson Objectives

By the end of this lesson, you'll be able to:

* **Create an animated Turtle game** using Python and GitHub Copilot.
* **Collaborate on GitHub** by sharing your project and giving constructive feedback.

## 🚀 Getting Started

**Recommended:** Use GitHub Codespaces for the best experience - it's pre-configured and ready to go!

## 🐢 Turtle Basics

Open `app.py` and practice these foundational steps:

### 🐢 Step 1: Import and Create a Turtle

```python
import turtle

wn = turtle.Screen()  # Creates the game window
player = turtle.Turtle()  # Creates a turtle

wn.mainloop()  # Keeps the window open
```

### 🎨 Step 2: Customize the Turtle

Paste the following code just before the `wn.mainloop()` line:

```python
player.shape("turtle")     # Changes the shape
player.color("blue")       # Changes the color
player.speed(1)            # Sets movement speed
```

### 🔄 Step 3: Move the Turtle Around

Paste the following code just before the `wn.mainloop()` line:

```python
player.forward(100)  # Move forward
player.right(90)     # Turn right
player.forward(100)
```

### 🧠 Step 4: Use Functions and Loops

Paste the following code just before the `wn.mainloop()` line:

```python
for _ in range(4):
    player.forward(100)
    player.right(90)  # Draws a square
```

### 🕹️ Step 5: Add User Input

Paste the following code just before the `wn.mainloop()` line:

```python
def move_up():
    player.setheading(90)
    player.forward(10)

wn.listen()
wn.onkey(move_up, "Up")
```

## 🚀 GitHub Copilot Editor Suggestions

To use GitHub Copilot’s inline suggestions in VS Code:

1. Open your Python file (`app.py`) in VS Code.
2. Press `Ctrl + I` to open the GitHub Copilot inline editor.
3. Type one of these prompts into the inline editor to generate code:

* "Make the turtle move smoothly with arrow keys"
* "Draw random objects on the screen"
* "Detect collision between objects"
* "Keep score in the game"
* "End game when a condition is met"

> These suggestions will help Copilot generate useful functions for your game!

## 🕹️ Choose Your Turtle Game!

Open [app.py](/lesson-2/app.py). Use these Copilot prompts to build your game step by step:

| 🐢 Game                | 🎯 What You'll Build                        | 🚀 Step-by-Step Prompts                                                                                 |
| ---------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **🏃 Dodge the Dots**  | Move your turtle to avoid falling obstacles | 1. "Draw turtle and falling dots" 2. "Move turtle with arrow keys" 3. "End game when turtle hits a dot" |
| **🍎 Catch the Apple** | Catch apples using your turtle as a basket  | 1. "Draw turtle and falling apple" 2. "Move turtle left/right" 3. "Detect when turtle catches apple"    |
| **💥 Turtle Chase**    | Chase and tag a moving target               | 1. "Draw two turtles" 2. "Make one move randomly" 3. "Control player turtle and detect collision"       |
| **🧱 Simple Breakout** | Break bricks with a bouncing turtle ball    | 1. "Draw bricks, paddle, and ball" 2. "Bounce ball off paddle" 3. "Remove bricks when hit"              |

> **💡 Pro Tip:** Turtle is great for beginners. Always run your game after each prompt to check progress!

## ▶️ Running Your Game

You have two options to run your game:

### Option 1: VS Code Play Button

* Open `app.py`.
* Click the green **Run** button in the top right.

### Option 2: Terminal

```bash
cd lesson-2
python app.py
```

## 🔎 Share & Collaborate with GitHub

Use GitHub to improve your game through collaboration:

### Commit and Push

* Open **Source Control** in VS Code.
* Type a commit message (e.g., "First Turtle game version").
* Commit and sync your changes.

### Try Another Game

* Clone a classmate's GitHub repository.
* Open and play their game.
* Note what you like and suggest improvements.

### Leave Feedback

* Go to their GitHub page, click **Issues** → **New Issue**.
* Provide specific, helpful feedback.

> Great collaboration makes great games. Be kind, honest, and specific!

### Running VSCode Locally

**Alternative:** If you prefer to work locally, see our [📋 Local VS Code Setup Guide](local-setup.md) for Windows installation instructions.
