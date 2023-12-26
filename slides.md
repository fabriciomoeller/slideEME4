---
theme: ./theme
background: ./EME4background.png
class: text-center
highlighter: shikiji
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: Welcome to Slidev
mdc: true
---

# Bem vindo ao <br>Manufatura 4.0

Apresentação slides para desenvolvedores

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Precione barra de espaço <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
O último bloco de comentários de cada slide será tratado como notas do slide. Ele ficará visível e editável no Modo Apresentador junto com o slide. [Leia mais na documentação](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Módulos do manufatura 4.0

O manufatura 4.0 é composto por 4 módulos:


- **<carbon-settings/> Parâmetros Globais** - Configurações globais que serão utilizadas por todos os módulos
- **<ic-baseline-engineering/> Engenharia de produtos** - Configuração de produtos e suas variantes 
- **<fluent-production-24-regular/> Controle de produção** - Criação, controle e apontamento de ordens de produção
- **<fluent-production-checkmark-24-regular/> Controle de Formulários** - Controle de formulários para ordem de produção e controle de qualidade



<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
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

<!--
Here is another comment.
-->

---
layout: default
---

# <carbon-settings/> Parâmetros Globais

Configurações globais que serão utilizadas por todos os módulos


---
transition: slide-up
level: 2
---

# <ic-baseline-engineering/> Engenharia de produtos

Configuração de produtos e suas variantes


### Linha de produção
### Recursos
### Ferramentas
### Lista de materiais
### Roteiro de operações


---


# <fluent-production-24-regular/> Controle de produção

Criação, controle e apontamento de ordens de produção

<!--
Fazendo as anotações do apresentador
-->

---

# <fluent-production-checkmark-24-regular/> Controle de Formulários

Controle de formulários para ordem de produção e controle de qualidade

<!--
Presenter note with **bold**, *italic*, and ~~striked~~ text.

Also, HTML elements are valid:
<div class="flex w-full">
  <span style="flex-grow: 1;">Left content</span>
  <span>Right content</span>
</div>
-->



---

# Diagramas


```mermaid {scale: 0.7}
journey
    title Fluxo de uma ordem de produção
    section OP - Ordem de produção
      Planejada: 10.5: 1 - OP
      Firme: 10.5: 1 - OP
    section AP - Apontamento
      Em Andamento: 10.5: 1 - OP, 2 - AP
      Baixada: 10.5: 1 - OP, 2 - AP
      Finalizada: 10.5: 1 - OP, 2 - AP
```
---

# Diagramas

<img src="fluxoOP.png" />

<v-clicks>

1. Criação de ordem de produção como Planejada
2. Firma a ordem de produção para que seja possível apontar
3. Inicia apontamento da ordem de produção muda status para Em Andamento
4. Apontamento parcial da ordem de produção muda status para Baixada
5. 100% apontamento da ordem de produção muda status para Finalizada

</v-clicks>
<br>

> A ordem de produção só pode ser apontada se estiver no status Firme

<style>
  ol {
    @apply text-sm;
  }
  blockquote {
    @apply text-sm italic;
  }
</style> 

---

<div v-click>1</div>
<div v-click>2</div>
<div v-click>3</div>



---
preload: false
---

# Agradecimentos 

- Mauricio Costa
- Osnir Alves
- Rafael Correa
- Gustavo Silva
- Diogo Bento

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-square.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
      alt=""
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

</div>
