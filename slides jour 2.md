---
theme: seriph
background: https://images.unsplash.com/photo-1682687220067-dced9a881b56?q=80&w=1975&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Cours d'introduction aux réseaux et à docker CODA School.

drawings:
  persist: false
transition: slide-left
title: Introduction aux réseaux et à docker
mdc: true
monaco: true
monacoTypesSource: local # or cdn or none
---

# Introduction aux réseaux et à docker

Marius Ambayrac, 2-3 Mai 2024

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    <carbon:arrow-right class="inline"/>
  </span>
</div>

---
transition: fade-out
hideInToc: true
---
<div class="flex">
  <img
    class="w-50 border-3 rounded-80"
    src="assets/Profil.png"
    alt="marius_ambayrac"
  />
  <div class="mx-20 mt-20">
    <div class="text-3xl">
    Marius Ambayrac
    </div>
    Head of Engineering @Gojob
  </div>
</div>

<br> </br>
<br> </br>

- Introduction à Linux (2 jours)
- Gestion de projets Informatiques (5 jours)
- Introduction à Docker et à la conteneurisation (2 jours)

<!--
Vous me reverrez également pour vos projets en autonomie en fin d'année ou je viendrai 1 jours pour vous accompagner.
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
hideInToc: true
---
# Plan du Cours



<Toc maxDepth="1"></Toc>



---
src: ./pages/jour2/practical_docker.md
transition: fade-out
---

