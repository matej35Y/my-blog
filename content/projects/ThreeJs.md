---
title: "Three.js Projects"
date: 2024-05-13
tags: ["three.js", "webgl", "creative coding"]
showToc: false
---


In my free time, I started experimenting with Three.js and WebGL. One of the biggest inspirations was [Bruno Simon’s portfolio](https://bruno-simon.com/). After following his course and playing around with the Three.js tools, I managed to learn quite a lot and build a few small projects.

---

### * Galaxy Generator

The first project is Galaxy Generator — a scene with thousands of particles rotating to form a dynamic spiral galaxy-like structure. From there, I got the idea to create a variation where the same particles form the shape of a letter or even a full name.

I made a version where the letter is "invisibly" drawn on a canvas, and then those points are transferred into 3D space. It's a simple effect but looks visually unique and interesting — and every time I change the letter, a new galaxy shape is formed.

<div style="display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;">
  <div style="flex: 1; min-width: 250px; max-width: 48%;">
    {{< figure src="/images/galaxy-gen.png" alt="Galaxy Spiral" caption="Galaxy Spiral" >}}
  </div>
  <div style="flex: 1; min-width: 250px; max-width: 48%;">
    {{< figure src="/images/galaxy-latter.png" alt="Galaxy Letter" caption="Galaxy Letter" >}}
  </div>
</div>

📂 [Code & Demo](https://github.com/matej35Y/ThreeJs-Galaxy-)

---

### * Haunted House

The second project is a slightly darker scene — an old haunted house, a graveyard, and ghost-like shadows moving through the space. I worked with textures, shadows, and point lights to build something that feels atmospheric and immersive, with effects like fog and glowing objects.

I also added a small flickering billboard, text on gravestones, and a few tricky effects that were fun to implement. Both projects include a GUI panel (dat.GUI), allowing users to interact with the scene and tweak parameters like light position, brightness, and more — directly from the browser.

<img src="/images/hunted house.png" alt="Haunted House Scene" style="max-width: 650px; width: 100%; height: auto; display: block; margin: 1.5rem auto;" />

📂 [View on GitHub](https://github.com/matej35Y/ThreeJS-Haunted-House)

---

These projects are small but served as a great way to learn through play. If you'd like to explore them further, feel free to check out the GitHub links where the full source code is available.
