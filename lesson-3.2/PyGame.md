Here's an edited and polished version of your lesson, with tightened language, clarified instructions, and improved flow, while keeping your engaging tone:

---

# 🎮 Week 3, Lesson 2: Build a Python Pygame with GitHub Copilot

## Welcome to Your First Game with Pygame!

You're about to explore **Pygame**, a beginner-friendly Python library that lets you create fun, interactive games with graphics, sound, and keyboard controls. In this lesson, you'll go from zero to a working game, using GitHub Copilot as your coding sidekick.

## 🎯 Lesson Objectives

By the end of this lesson, you'll be able to:

* 🎮 **Create an interactive Pygame project** using Python and GitHub Copilot.
* 🤝 **Collaborate on GitHub** by sharing your project and giving feedback.

---

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

### 🖥️ View Your Game in the Browser (Codespaces)

Once your Codespace is set up and running:

1. Click the **Ports** tab (bottom or side of the Codespace).
2. Find the row labeled **Pygame desktop**.
3. Click the 🌐 **Open in Browser** icon.
4. In the new tab, click on **vnc.html**, then hit the **Connect** button.

This opens a virtual desktop where your Pygame window will appear!

---

## 🎮 Pygame Basics

> 🧭 *Explore more:* Visit the official [Pygame documentation](https://www.pygame.org/docs/) for examples on sprites, input handling, collision detection, and sound.

Open `app.py` and follow these steps:

---

### 🛠️ Step 2: Setup a Game Window

Add this code to start your Pygame window:

```python
import os
os.environ["DISPLAY"] = ":1"

import pygame
import sys

pygame.init()
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("My First Pygame")

clock = pygame.time.Clock()
```

This creates a window that’s 800x600 pixels. Now let’s keep the window running!

---

### 🔄 Step 3: Game Loop

Add this after your setup code:

```python
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    screen.fill((255, 255, 255))  # Fills the screen with white
    pygame.display.flip()        # Updates the screen
    clock.tick(60)               # Limits to 60 FPS

pygame.quit()
sys.exit()
```

Now when you run the file, a window will open and stay responsive.

---

### 🐧 Step 4: Draw a Character

Add this above your game loop:

```python
player = pygame.Rect(375, 500, 50, 50)  # x, y, width, height
```

Then inside your game loop, after `screen.fill(...)`:

```python
pygame.draw.rect(screen, (0, 0, 255), player)  # Blue rectangle
```

---

### 🕹️ Step 5: Move with Arrow Keys

Inside your game loop, before `pygame.display.flip()`:

```python
keys = pygame.key.get_pressed()
if keys[pygame.K_LEFT]:
    player.x -= 5
if keys[pygame.K_RIGHT]:
    player.x += 5
```

Run your game and move the block left/right!

---

### 🎯 Step 6: Add an Obstacle

Above your loop:

```python
obstacle = pygame.Rect(375, 0, 50, 50)
```

Inside your game loop, after drawing the player:

```python
obstacle.y += 5
pygame.draw.rect(screen, (255, 0, 0), obstacle)  # Red falling block

# Reset obstacle if it leaves screen
if obstacle.y > 600:
    obstacle.y = 0
```

---

### 💥 Step 7: Collision Detection

Inside the game loop, after updating the obstacle:

```python
if player.colliderect(obstacle):
    print("Game Over!")
    running = False
```

---

## 🤖 GitHub Copilot Prompts

Use GitHub Copilot to add new features:

* “Add score and display it on screen”
* “Play a sound when the player wins”
* “Spawn multiple obstacles randomly”
* “Restart the game after losing”
* “Create a start screen with a play button”

> ✅ Run your game after each change to test it live!

---

## 🕹️ Start Your Own Game!

Create a new file: `MyGame.py`, and paste this starter code:

```python
import os
os.environ["DISPLAY"] = ":1"

import pygame
import sys

pygame.init()
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("My Game")

clock = pygame.time.Clock()
running = True

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    screen.fill((255, 255, 255))
    pygame.display.flip()
    clock.tick(60)

pygame.quit()
sys.exit()
```

Use this as your blank slate and start prompting Copilot to build your full game!

---