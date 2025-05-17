---
title: "Three.js Projects"
date: 2024-05-13
tags: ["three.js", "webgl", "creative coding"]
showToc: false
---


Во слободно време почнав да експериментирам со Three.js и WebGL. Еден од виновниците беше  https://bruno-simon.com/ - ова портофлио. Следејќи го неговиот курс и играјќи си со алатките на Three.js успеав да научам доста работи и да направам неколку мини проекти.

---

### * Galaxy Generator

Првиот проект е Galaxy Generator – сцена со илјадници честички `(particles)` што се вртат и создаваат динамична структура, слично на спирална галаксија. Од таму, ми дојде идеја да напрвам  варијанта каде што со истите particles ќе направам структура во форма на буква или пак име. 
<!-- 
<img src="/images/galaxy-gen.png" alt="Galaxy Generator" style="max-width: 650px; width: 100%; height: auto; display: block; margin: 1.5rem auto;" /> -->

Направив варијанта каде што буквата се нацртува „невидливо“ на еден `canvas`, а потоа тие точки се пренесуваат во 3D. Едноставен ефект, ама изгледа интересно, различно – и секојпат кога ќе ја сменам буквата, добивам нова форма на галаксија.
<div style="display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;">
  <div style="flex: 1; min-width: 250px; max-width: 48%;">
    {{< figure src="/images/galaxy-gen.png" alt="Galaxy Spiral" caption="Galaxy Spiral" >}}
  </div>
  <div style="flex: 1; min-width: 250px; max-width: 48%;">
    {{< figure src="/images/galaxy-latter.png" alt="Galaxy Letter" caption="Galaxy Letter" >}}
  </div>
</div>





📂 [Кодот и демо](https://github.com/matej35Y/ThreeJs-Galaxy-)

---

### * Haunted House

Вториот проект е една малку поразлична сцена – мрачна, со стара куќа, гробишта и "духови" поточно сенки што се движат низ просторот. Работев со текстури, сенки и `point lights`, со цел да направам сцена што изгледа живо, но и со малку атмосфера и ефект на `fog`.

Во сцената додадов и мал билборд што светка, текстови на гробовите, и неколку ефекти што ми беа предизвик да ги имплементирам. На двата проекти додадов `gui` - алатка со која може директно од сајтот да приспособуваш некои од опциите како(светлина, позиција на светло, јачина на светло итн...)

<img src="/images/hunted house.png" alt="Galaxy Generator" style="max-width: 650px; width: 100%; height: auto; display: block; margin: 1.5rem auto;" />

📂 [Погледни на GitHub](https://github.com/matej35Y/ThreeJS-Haunted-House)

---

Овие проекти се мали, но ми беа одличен начин да учам преку игра. Ако сакаш да ги истражиш подетално, имаш линкови до GitHub каде што е поставен целиот код.
