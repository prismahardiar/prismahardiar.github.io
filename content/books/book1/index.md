---
title: "The Living Equation: Art of Mathematical Animation with Python" 
date: 2026-01-07
tags: ["mathematics","Python","animation"]
author: ["Prismahardi Aji Riyantoko"]
description: "A comprehensive guide to entering the world of programmatic animation using Python and the Manim library. This book bridges the gap between abstract mathematical concepts and dynamic visual storytelling. Readers will master the essentials of the Manim engine—from setting up the environment and understanding coordinate systems to animating geometric proofs and functions. The journey culminates in a practical mini-project focused on visualizing fundamental Calculus concepts like limits and derivatives."
summary: "The ultimate starter guide to the Manim library, teaching you how to use Python code to create stunning mathematical animations and bring equations to life."
cover:
    image: "manim.png"
    alt: "The Living Equation: Art of Mathematical Animation with Python"
    relative: true
editPost:
    URL: "https://prismahardiar.github.io/"
    Text: "UPNVJT Press"
showToc: false
disableAnchoredHeadings: false

---

---

#### Description
<div style="text-align: justify">
This book bridges the gap between abstract mathematical concepts and visual storytelling using Python. It provides a comprehensive guide to the <strong>Manim</strong> engine, allowing readers to programmatically generate precise and stunning animations.[^1] The text emphasizes not just the "how-to" of coding, but the "why" of visualization, ensuring that every animation serves a pedagogical purpose.[^2] From setting up the environment to visualizing complex Calculus theorems, this book transforms the way educators and students perceive mathematical proofs.

[^1]: The book focuses on the Community Edition of Manim (ManimCE), which is the most stable version.
[^2]: Readers are expected to have a basic understanding of Python syntax and OOP concepts.

---

#### Praise

> “Mathematics is the art of giving the same name to different things.” — Henri Poincaré

---

#### View

+ [Chapter 1: Introduction to the World of Manimation]()
+ [Chapter 2: Python Fundamentals for Animation]()
+ [Chapter 3: Getting Started with Manim]()
+ [Chapter 4: Basic Mathematical Animations]()
+ [Chapter 5: Fundamental Animation Techniques]()
+ [Chapter 6: Mini Project: Calculus Visualization]()

---

#### Excerpt from Chapter 6: Mini Project: Calculus Visualization

Calculus often intimidates students due to its reliance on abstract concepts like limits and infinitesimals. However, Manim allows us to make these concepts tangible. In this chapter, we focus on visualizing the **Riemann Sum**, which approximates the area under a curve using rectangles.

Mathematically, we define the integral as the limit of these sums as the width of the rectangles ($\Delta x$) approaches zero:

$$
\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i) \Delta x
$$

To visualize this, we can use Manim's built-in `Axes` and `get_riemann_rectangles` methods. The following code snippet demonstrates how to plot a quadratic function and visualize the area approximation:

```python
from manim import *

class RiemannVisualization(Scene):
    def construct(self):
        # 1. Create Axes
        axes = Axes(
            x_range=[0, 5], 
            y_range=[0, 10], 
            axis_config={"include_tip": False}
        )
        
        # 2. Define the function f(x) = 0.5 * x^2
        graph = axes.plot(lambda x: 0.5 * x**2, color=BLUE)
        
        # 3. Create Riemann Rectangles (dx=0.5 means width is 0.5)
        rects = axes.get_riemann_rectangles(
            graph, 
            x_range=[0, 4], 
            dx=0.5, 
            input_sample_type="left"
        )

        # 4. Animation Sequence
        self.play(Create(axes), Create(graph))
        self.play(Write(rects))
        self.wait(1)
        
        # Optional: Smoothly transform to thinner rectangles (higher precision)
        new_rects = axes.get_riemann_rectangles(graph, x_range=[0, 4], dx=0.1)
        self.play(Transform(rects, new_rects))
        self.wait(2)
```
By dynamically changing the $dx$ parameter (the width of the rectangles) using Transform, we can visually demonstrate the definition of the integral: as the rectangles get thinner, the "staircase" error vanishes, and the area of the rectangles perfectly matches the area under the smooth curve.

---

#### Citation

Riyantoko, P.A. 2025. *The Living Equation: Art of Mathematical Animation with Python*. Surabaya, Indonesia: UPNVJT Press.

```latex
@book{Manim2025,
author = {Prismahardi Aji Riyantoko},
year = {2025},
title = {The Living Equation: Art of Mathematical Animation with Python},
publisher = {UPNVJT Press},
address = {Surabaya, Indonesia},
url = {[-](-)}}
```

</div>