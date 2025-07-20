# 🐢 Week 3, Lesson 1: Build a Python Turtle Game with GitHub Copilot

## Welcome to Your First Game with Turtle!

You're about to explore **Turtle**, a simple yet powerful Python library that helps you create fun, graphical games using code. This lesson will guide you step-by-step from basics to building and sharing your very own game!

## 🎯 Lesson Objectives

By the end of this lesson, you'll be able to:

* **Create an animated Turtle game** using Python and GitHub Copilot.
* **Collaborate on GitHub** by sharing your project and giving constructive feedback.

## 🚀 Getting Started

**Recommended:** Use GitHub Codespaces for the best experience - it's pre-configured and ready to go!

> **Note:** When you start your GitHub Codespace, it may take a few moments for all dependencies and tools to finish installing. Wait until setup completes before you begin coding.

### 🖥️ View Your Game in the Browser

Once setup is complete and you run your game, look for a "Pygame desktop" entry in the **Ports** tab (usually at the bottom or side of your Codespace window).

1. Click the **Ports** tab.
2. Find the row labeled **Pygame desktop**.
3. Click the **Open in Browser** button (usually a globe icon) next to the port.
4. After you've opened it in the browser, you will see a list of files and directories. Click on the file labeled **"vnc.html"**. Once that opens, you'll see a big button that says **Connect**—click that button.

## 🐢 Turtle Basics

> 🧭 Want to explore more Turtle commands? Check out the official [Turtle documentation](https://docs.python.org/3/library/turtle.html) to see everything you can do — from drawing shapes and handling events to animation tricks!

Open `app.py` and practice these foundational steps:

### 🐢 Step 1: Import and Create a Turtle

Make sure to include the following lines at the very top of your file to enable Turtle to display in the browser window:

> If you're using VS Code locally (not Codespaces), you can skip the `import os` line — it's only needed for browser display in Codespaces.

```python
import os
os.environ["DISPLAY"] = ":1"
```

Then, add your Turtle code:

```python
import turtle

wn = turtle.Screen()  # Creates the game window
player = turtle.Turtle()  # Creates a turtle

wn.mainloop()  # Keeps the window open
```

> This will open the Turtle graphics window in your browser so you can see your turtle in action.
> To run your Python app, simply click the **Run** (green play) button directly above the `app.py` file in VS Code.

### 🎨 Step 2: Customize the Turtle

Paste the following code just before the `wn.mainloop()` line:

```python
player.shape("turtle")     # Changes the shape
player.color("blue")       # Changes the color
player.speed(1)            # Sets movement speed
```

> **Note:** To apply your latest changes, just click the **Run** (green play) button again above your file. In the browser, you may need to move your mouse over the Turtle window to refresh the display.

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

### 🌐 Step 6: Make Your Game Port Public

To share your running Turtle game with others, you need to make the port public in GitHub Codespaces:

1. Click the **Ports** tab in your Codespace.
2. Find the row labeled **Pygame desktop**.
3. **Right-click the lock icon** next to the word "private" in the Visibility column for the port.
4. Go down to **Port Visibility** and select **Public**.

> Now, anyone with the link can view your game in their browser!

## 🚀 GitHub Copilot Editor Suggestions

To use GitHub Copilot’s inline suggestions in VS Code:

1. Open your Python file (`app.py`) in VS Code.
2. Press `Ctrl + I` (or `Cmd + I` on Mac) to open the GitHub Copilot inline chat.
3. In the prompt area that appears, type one of these requests:

* "Make the turtle move smoothly with arrow keys"
* "Draw random objects on the screen"
* "Detect collision between objects"
* "Keep score in the game"
* "End game when a condition is met"

> These suggestions will help Copilot generate useful functions for your game!

## 🕹️ Choose Your Turtle Game!

Create a new Python file called `MyGame.py`. Then copy and paste this full example to get started:

```python
# If you're using GitHub Codespaces, include these two lines to enable Turtle graphics in the browser:
import os
os.environ["DISPLAY"] = ":1"

import turtle

wn = turtle.Screen()  # Creates the game window
player = turtle.Turtle()  # Creates a turtle

wn.mainloop()  # Keeps the window open
```

If you're working locally, you can skip the `import os` lines.

> Here are some prompts you can try in the Copilot inline agent to help build your full game:

| 🐢 Game                | 🎯 What You'll Build                        | 🚀 Step-by-Step Prompts                                                                                 |
| ---------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **🏃 Dodge the Dots**  | Move your turtle to avoid falling obstacles | 1. "Draw turtle and falling dots" 2. "Move turtle with arrow keys" 3. "End game when turtle hits a dot" |
| **🍎 Catch the Apple** | Catch apples using your turtle as a basket  | 1. "Draw turtle and falling apple" 2. "Move turtle left/right" 3. "Detect when turtle catches apple"    |
| **💥 Turtle Chase**    | Chase and tag a moving target               | 1. "Draw two turtles" 2. "Make one move randomly" 3. "Control player turtle and detect collision"       |
| **🧱 Simple Breakout** | Break bricks with a bouncing turtle ball    | 1. "Draw bricks, paddle, and ball" 2. "Bounce ball off paddle" 3. "Remove bricks when hit"              |

> **💡 Pro Tip:** Turtle is great for beginners. Always run your game after each prompt to check progress!

### 💻 Running VS Code Locally

**Want to build a game on your own computer?** Working locally is a great option—especially if you're building a more advanced project or working on your coding challenge project. You'll have full control, faster performance, and no need to rely on the cloud.

Check out our [📋 Local VS Code Setup Guide](local-setup.md) to get started on Windows. It's a solid choice if you want to level up your game development setup!