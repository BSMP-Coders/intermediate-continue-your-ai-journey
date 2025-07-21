# 🎮 Week 3, Lesson 2: Build a Pygame Using GitHub Copilot Inline Editor

## 💻 Step 1: Choose How to Run Your Game

You have two options for running your game. We encourage you to try the local setup for a smoother experience, but you can continue in the browser if you prefer.

### 🖥️ Option 1: Run Locally with VS Code

Want to build a more advanced game on your own computer?

Working locally gives you faster performance and full control — a great option for your coding challenge project!

👉 Follow our [📋 Local Setup Guide](local-setup.md) to get started on Windows.

---

### 🌐 Option 2: Run in the Browser with GitHub Codespaces

If you don't want to set things up locally, you can continue using **GitHub Codespaces** right in your browser — just like in previous lessons. It’s pre-configured and ready to go!

> ⏳ *Heads up:* When your Codespace starts, it may take a minute to finish setting everything up. Wait until it’s ready before writing code.

> 💡 *If you're using GitHub Codespaces, you need to add the following lines at the top of your file to enable graphics display in the browser.*

```python
# Only needed if you're running in GitHub Codespaces
import os
os.environ["DISPLAY"] = ":1"
```

---

## Welcome to Your First Game with Pygame and Copilot Inline

In this lesson, you’ll build a simple interactive game using **GitHub Copilot’s inline chat editor** in Visual Studio Code. Instead of writing out full code or comments, you'll use **natural language prompts directly in the inline editor** to ask Copilot for help — step by step.

## 🧠 How It Works

1. Open your Python file: `app.py`
2. Place your cursor where you want code to appear
3. Press `Ctrl + I` or right-click and choose **Copilot: Open Inline Chat**
4. Type your request in natural language (e.g., “create a game loop that quits when you close the window”)
5. Review and insert the Copilot-generated code

## 🛠️ First: Set Up Your Game File

Add this starter block at the top of your file:

```python
# Only needed if you're using GitHub Codespaces
import os
os.environ["DISPLAY"] = ":1"

import pygame
import sys
pygame.init()
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("My Game")
clock = pygame.time.Clock()
running = True
```

---

## 💬 Step-by-Step Copilot Tasks Using the Inline Editor

### 🎯 Step 1: Create the Game Loop

Use Copilot Inline Chat:

> “Create a game loop that handles events and fills the screen white”

Place your cursor under `running = True` and run the inline prompt. Accept the suggested code.

---

### 🟦 Step 2: Draw a Player Block

Use Copilot Inline Chat:

> “Create a blue square at the bottom of the screen called player”

Ask Copilot to create a `pygame.Rect` for the player and draw it in the game loop.

---

### 🕹️ Step 3: Add Arrow Key Movement

Use Copilot Inline Chat:

> “Move the player left and right using the arrow keys”

Have Copilot generate code to check for key presses and update the player position.

---

### 🔻 Step 4: Create a Falling Obstacle

Use Copilot Inline Chat:

> “Add a red block that falls from the top and resets when off screen”

Ask Copilot to create an obstacle `pygame.Rect`, update its position, and reset it when it goes past the screen.

---

### 💥 Step 5: Add Collision Detection

Use Copilot Inline Chat:

> “Check if the player collides with the obstacle and end the game”

Have Copilot generate collision logic using `.colliderect()` and stop the loop.

---

### 💡 Bonus Copilot Tasks

Use inline chat to explore any of these features:

> “Add score and display it on screen”
> “Play a sound when the player wins”
> “Spawn multiple falling obstacles”
> “Show a start screen with a play button”
> “Restart the game when spacebar is pressed”

---

## ▶️ Run Your Game

### Option 1: Use the Run Button

* Open `app.py`
* Click the green **Run** button in the top-right corner of VS Code

### Option 2: Use the Terminal

```bash
cd lesson-2
python app.py
```

---

## 📚 Learn More

Want to get creative? Explore [Pygame Docs](https://www.pygame.org/docs/) to find ways to add images, sounds, animation, or multiple levels.

> ✅ Build your game step by step — test as you go, ask Copilot for help, and have fun making it your own!