---
title: "Being Comfortable with What I am Not"
date: 2026-07-24
permalink: /posts/2026/07/being-comfortable-with-what-i-am-not/
tags:
  - Semester 2 S2 - UNIPD M1
cover_image: "https://refrainfr.github.io/assets/images/20260724-mob-fight-on.jpg"
description: "Sharing my growth from the past one year since I have completed my first year in Italy. TL;DR: during this time, I have been working with objects that I was uncomfortable with. Actually, I gain rapid progress by making peace with my discomfort."
---

<p align="center">
  <img src="/assets/images/20260724-mob-fight-on.jpg" alt="Mob sweating and working out with the Body Improvement Club from Mob Psycho 100" width="100%">
</p>

<p align="justify">  
One of the things that has always bugged me—ever since my math olympiad days—is the mentality of outright refusing to touch a specific topic.
</p>
<p align="justify">  
Take me as an example. I hated combinatorics so much that during my undergraduate olympiad, I won the national level by solving 8 out of 10 problems—the remaining two were, predictably, combinatorics. I even remember the head jury telling me to "git gud" at it, lol.
</p>
<p align="justify">  
But this hatred for combinatorics wasn't the main thing blocking my progress. A much bigger roadblock was my sheer stubbornness to get my hands dirty with computations and concrete examples.
</p>
<p align="justify">  
During my undergrad years, my approach was all about the concepts: learn the definitions, memorize the lemmas, prove the theorems, and repeat. I was perfectly happy just living in pure theory, completely avoiding the actual work of testing those ideas on examples. This is exactly why I stayed so far away from analysis in my early days. Looking back, it's pretty funny, considering I am heavily leaning into analysis nowadays!
</p>
<p align="justify">  
Back then, I wouldn't even dare to read a real analysis problem. I would look at things like differentiability, integrability, and continuity and wonder what they were actually used for in practice. Just looking at how heavy the calculations were made me deeply uncomfortable.
</p>

<p align="center">
  <img src="/assets/images/20260724-rizu-and-fumino-struggling.jpg" alt="Fumino or Rizu struggling from Bokuben" width="100%">
</p>

<p align="justify">  
To be fair, I still can't tell you the exact reason I pivoted to analysis for my Master's. For the past year, it felt like my body was actively rejecting the subject, yet I kept pushing forward—all because of a single problem that started this whole change.
</p>
<p align="justify">  
The turning point was during the 2023 IMC in Blagoevgrad, Bulgaria. I ran into a problem that kept me completely stuck for three hours. (Pardon the "skill issue" of spending that much time on a single problem). But in those three hours, I finally made peace with my discomfort. It was actually the only problem I managed to solve that day, but the thought process required to crack it made me realize that I needed to stop running from the math that scared me.
</p>

> **IMC 2023, Problem 7**<br>
> Let $$V$$ be the set of all continuous functions $$f:[0,1]\to\mathbb{R}$$, differentiable on $$(0,1)$$, with the property that $$f(0)=0$$ and $$f(1)=1$$. Determine all $$\alpha\in\mathbb{R}$$ such that for every $$f\in V$$, there exists some $$\xi\in(0,1)$$ such that $$f(\xi)+\alpha=f'(\xi).$$

<p align="justify">  
I was completely stuck on this problem until I forced myself to take a radical approach. Instead of just playing with the given conditions abstractly, I tried to directly solve the differential equation \(f(x)+\alpha=f'(x)\). Getting my hands dirty like that gave me a simple half-page proof. When I finally dropped the "abstract nonsense" that I was so comfortable with, the insight just clicked.
</p>
<p align="justify">  
It still surprises me how much I've improved after just a year of rigorous (and occasionally traumatic) training. I openly admit that I was terrible at handling analytic inequalities, but after spending a lot of time figuring out why they actually work, I can now genuinely appreciate basic inequalities like:
</p>

<p align="justify">  
<b>1. The Cauchy-Schwarz Inequality</b><br>
$$ \left| \int fg \right| \leq \left( \int f^2 \right)^{\frac{1}{2}} \left( \int g^2 \right)^{\frac{1}{2}} $$
</p>

<p align="justify">  
<b>2. Young's Inequality</b><br>
$$ ab \leq \frac{a^p}{p} + \frac{b^q}{q} $$
</p>

<p align="justify">  
<b>3. Hölder's Inequality</b><br>
$$ \int |fg| \leq \left( \int |f|^p \right)^{\frac{1}{p}} \left( \int |g|^q \right)^{\frac{1}{q}} $$
</p>

<p align="justify">  
Back in my early days, I couldn't understand why anyone would put an arbitrary \(\varepsilon>0\) into Young's inequality. But now? I literally cannot unsee Young's inequality with \(\varepsilon\) whenever I look at a bounding problem involving products:
</p>

$$ \int |fg| \leq \frac{\varepsilon}{2} \int f^2 + \frac{1}{2\varepsilon} \int g^2 $$

<p align="justify">  
That \(\varepsilon\) isn't meant to be scary at all! It acts as a placeholder so you can easily absorb terms into one another. One of the best times to use Young's inequality is when finding bounds for the solution to an elliptic PDE, like:
</p>

$$ -\operatorname{div}(A\nabla u) = 0 $$

<p align="justify">  
By multiplying by a test function that includes a smooth cutoff \(\eta\) and applying Young's inequality with \(\varepsilon\), we can absorb the gradient terms to get the <b>Caccioppoli inequality</b>:
</p>

$$ \int_{\Omega} \eta^2 |\nabla u|^2 \, dx \leq C \int_{\Omega} |\nabla \eta|^2 |u|^2 \, dx $$

<p align="justify">  
This inequality is our way of controlling the gradient (the derivative) using just the integral of the solution itself. From there, we can prove even more, to the point of showing that the weak solution \(u\) is actually a smooth, nice function!
</p>
<p align="justify">  
The beauty of the very things that once made me so uncomfortable suddenly made perfect sense.
</p>

<p align="justify">  
Perhaps the only thing that ever truly held me back was my own rigid mindset. If I had kept hating inequalities, I never would have survived, let alone enjoyed, my first year in Italy. If I had just stuck to abstract algebraic reasoning, I would never have understood why the Poincaré inequality is so useful. If I only stayed in my comfort zone, I would never let myself appreciate anything new.
</p>
<p align="justify">  
To the readers: I really urge you to try to work on things that make you uncomfortable. Staying stuck in a familiar bubble doesn't do you any good in the long run.
</p>
<p align="justify">  
I have no idea if, in ten years, I'll still be working on the exact same math I like today. But I can say for sure that I am willing to adapt—not just in math, but in life overall. 
</p>
<p align="justify">  
Adapt and overcome.
</p>

<script src="https://giscus.app/client.js"
        data-repo="orlandoferrari/orlandoferrari.github.io"
        data-repo-id="R_kgDOOY8AQA"
        data-category="Announcements"
        data-category-id="DIC_kwDOOY8AQM4CpDpE"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="dark_dimmed"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>