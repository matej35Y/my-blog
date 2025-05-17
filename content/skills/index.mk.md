---
title: "My Skills"
date: 2025-05-16
draft: false
---

<style>
.skill-box {
  margin-bottom: 30px;
}

.skill-label {
  font-weight: 500;
  margin-bottom: 6px;
  font-size: 1rem;
  color: #f2f2f2;
}

.loader {
  width: 0;
  height: 5px;
  display: inline-block;
  position: relative;
  background: #f5f5f5;
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.3); /* slightly more glow */
  box-sizing: border-box;
  animation: animFw 2s ease-out forwards;
  border-radius: 3px;
}

.loader::after,
.loader::before {
  content: '';
  width: 8px;
  height: 1px;
  background: #f0f0f0;
  position: absolute;
  top: 8px;
  right: -2px;
  opacity: 0.5;
  transform: rotate(-45deg) translateX(0px);
  box-sizing: border-box;
  animation: coli1 0.4s linear infinite;
}

.loader::before {
  top: -4px;
  transform: rotate(45deg);
  animation: coli2 0.4s linear infinite;
}

@keyframes animFw {
  0% {
    width: 0;
  }
  100% {
    width: var(--skill-level, 100%);
  }
}

@keyframes coli1 {
  0% {
    transform: rotate(-45deg) translateX(0px);
    opacity: 0.8;
  }
  100% {
    transform: rotate(-45deg) translateX(-35px);
    opacity: 0;
  }
}

@keyframes coli2 {
  0% {
    transform: rotate(45deg) translateX(0px);
    opacity: 0.8;
  }
  100% {
    transform: rotate(45deg) translateX(-35px);
    opacity: 0;
  }
}
/* Light theme overrides */
html[data-theme='light'] .loader {
  background: #222;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.3);
}

html[data-theme='light'] .loader::after,
html[data-theme='light'] .loader::before {
  background: #444;
  opacity: 0.5;
}

html[data-theme='light'] .skill-label {
  color: #111;
}

@keyframes showScore {
  from { opacity: 0; }
  to { opacity: 1; }
}
    

</style>


<div class="skill-box">
  <div class="skill-label">C++/C</div>
  <div class="loader" style="--skill-level: 80%;"></div>
</div>

<div class="skill-box">
  <div class="skill-label">HTML / CSS </div>
  <div class="loader" style="--skill-level: 90%;"></div>
</div>
<div class="skill-box">
  <div class="skill-label">Java</div>
  <div class="loader" style="--skill-level: 72%;"></div>
</div>

<div class="skill-box">
  <div class="skill-label">JavaScript</div>
  <div class="loader" style="--skill-level: 76%;"></div>
</div>
<div class="skill-box">
  <div class="skill-label">JQuery</div>
  <div class="loader" style="--skill-level: 73%;"></div>
</div>
<div class="skill-box">
  <div class="skill-label">Python</div>
  <div class="loader" style="--skill-level: 67%;"></div>
</div>

<div class="skill-box">
  <div class="skill-label">Figma</div>
  <div class="loader" style="--skill-level: 80%;"></div>
</div>

<div class="skill-box">
  <div class="skill-label">AWS</div>
  <div class="loader" style="--skill-level: 35%;"></div>
</div>

