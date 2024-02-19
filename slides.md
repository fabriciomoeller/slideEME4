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
title: Datainfo - EME4 - Manufatura 
mdc: true
---

# Manufatura

Uma visão para Industria <br>
de Laticínios

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Precione barra de espaço <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
O último bloco de comentários de cada slide será tratado como notas do slide. Ele ficará visível e editável no Modo Apresentador junto com o slide. [Leia mais na documentação](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Módulos do manufatura 

O manufatura EME4 é composto por 4 módulos:

 ---
 <br>

- **<carbon-settings/> Parâmetros Globais** - Configurações globais que serão utilizadas por todos os módulos
- **<ic-baseline-engineering/> Engenharia de produtos** - Configuração de produtos e suas variantes 
- **<fluent-production-24-regular/> Controle de produção** - Criação, controle e apontamento de ordens de produção
- **<fluent-production-checkmark-24-regular/> Controle de Formulários** - Desenvolvimento específico para  o Controle da Manufatura e Qualidade



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


# <carbon-settings/> Parâmetros Globais

Configurações globais que serão utilizadas por todos os módulos

 ---
 <br>


 - Parâmetros Filiais Manufatura
 - Calendário de produção
 - Turnos de produção
---
transition: slide-up
level: 2
---

# <ic-baseline-engineering/> Engenharia de produtos

Configuração de produtos e suas variantes

 
  ---
<br>

- Linha de produção
- Recursos
- Ferramentas
- Lista de materiais (BOM) Versionadas (Preferencia, Alternativa, opcional, Co-produto, Sub-Produto)
- Roteiro de operações (Routing) Versionadas


---


# <fluent-production-24-regular/> Controle de produção

Criação, controle e apontamento de ordens de produção

 ---
 <br>

- Criação de ordem de produção ( Empurrada, Puxada ou Mista) 
- Consumo da engenharia de produtos e suas proporções
- Uma ordem para multiplos produtos saída (Co-produtos)
- Ordens de produção Planejadas, Firmes, Em Andamento, Baixa Parcial e Finalizada
- Apontamento de ordem de produção (Parcial e Total) - Opcionalmente com formulários Web
- Rastreabilidade de ordem de produção

<!--
Fazendo as anotações do apresentador
-->

---

# <fluent-production-checkmark-24-regular/> Controle de Formulários

Controle de formulários para ordem de produção e controle de qualidade

 ---
 <br>

- Criação de multiplos formulários a partir de uma ordem de produção
- Criação de formulários manualmente 
- Rastreabilidade de formulários pelas ordens de produção
- Fila de inspeção para os formulários
- Controle supervisionado de formulários
- Apontamento de produção com formulários


<!--
Presenter note with **bold**, *italic*, and ~~striked~~ text.

Also, HTML elements are valid:
<div class="flex w-full">
  <span style="flex-grow: 1;">Left content</span>
  <span>Right content</span>
</div>
-->



---
clicks: 6
mdc: true
---

# Diagramas
Situações da Ordem de produção por etapas

<div >
  <div class="absolute w-12 h-63 border-r-1 border-sky-500 ">
    <div class="rotate-270 absolute top-50% left-0" > Etapas </div>
  </div>
<div class="flex flex-col mt-5 ml-15 ">
<div class="flex gap-4 font-mono justify-center">
  Ordem de Produção
  <DialogBox v-click class="flex-auto">
    Planejada
  </DialogBox>

  <DialogBox v-click class="flex-auto">
    Firme
  </DialogBox>

  <DialogBox v-click class="flex-auto">
    Em Andamento
  </DialogBox>

  <DialogBox v-click class="flex-auto">
    Baixa parcial
  </DialogBox>

  <DialogBox v-click class="flex-auto">
    Finalizada
  </DialogBox>

  <DialogBox v-click class="flex-auto">
    Concluída
  </DialogBox>

</div>
  
  
<div class="pb-5 border-b-1 border-gray-530"/>
  

<div class="flex gap-4 mt-5 font-mono">
 Apontamento de Produção

  <div class="flex-auto w-5"/>

  <DialogBox v-click="[2,7]" class="flex-auto bg-gray-500">
    Firme
  </DialogBox>
 
  <DialogBox v-click="[3,7]" class="flex-auto bg-gray-500">
    Em Andamento
  </DialogBox>

  <DialogBox v-click="[4,7]" class="flex-auto bg-gray-500">
    Baixa Parcial
  </DialogBox>

  <DialogBox v-click="[5,7]" class="flex-auto bg-gray-500">
    Finalizada
  </DialogBox>

  <DialogBox v-click="[6,7]" class="flex-auto bg-gray-500">
    Concluída
  </DialogBox>
</div>

<div class="pb-5 border-b-1 border-gray-530"/>
  

<div class="flex gap-4 mt-5 font-mono">
 Estoque

<div class="flex-auto"/>
  
  <DialogBox v-click="[4,7]" class="w-28" bg="gray-600 dark:gray-300" text="gray-300 dark:gray-600">
    Baixa Parcial
  </DialogBox>

  <DialogBox v-click="[5,7]" class=" w-23" bg="gray-600 dark:gray-300" text="gray-300 dark:gray-600">
    Finalizada
  </DialogBox>

  <DialogBox v-click="[6,7]" class=" w-21" bg="gray-600 dark:gray-300" text="gray-300 dark:gray-600">
    Concluída
  </DialogBox>

</div>

<div class="pb-5 border-b-1 border-gray-530"/>

<div class="flex gap-4 mt-5 font-mono">
 Custos

<div class="flex-auto"/>

  <DialogBox v-click="[6,7]" class=" w-21" bg="gray-800 dark:gray-300" text="gray-300 dark:gray-800">
    Concluído
  </DialogBox>

</div>
</div>
</div>

  <table mt-2>
  <tr border-t-1>
    <th border-r-1 >Situação</th>
    <th>Descrição</th>
  </tr>
  <tr border-t-1>
    <td class="border-r-1"> <div class="border rounded pl-1 pr-1 w-17" v-click="1"> Planejada </div> </td>
    <td v-click="1" > A Ordem de Produção foi criada e esta na situação de Planejamento.</td>
  </tr>
  <tr class="">
    <td border-r-1> <div class="rounded pl-1 pr-1 w-10 bg-gray-500" v-click="2"> Firme </div> </td>
    <td v-click="2" >O produto e a quantidade da Ordem é Firmada e esta pronta para receber os apontamentos.</td>
  </tr>
  <tr>
    <td border-r-1> <div class="rounded pl-1 pr-1 w-25 bg-gray-500" v-click="3"> Em Andamento </div> </td>
    <td v-click="3" > A Ordem já tem apontamento.</td>
  </tr>
  <tr>
    <td border-r-1> <div class="rounded pl-1 pr-1 w-22 bg-gray-600 text-gray-300 dark:text-gray-800 dark:bg-gray-400" v-click="4"> Baixa Parcial </div> </td>
    <td v-click="4" > A Ordem já tem apontamento integrado no Estoque.</td>
  </tr>
  <tr>
    <td border-r-1 > <div class="rounded pl-1 pr-1 w-17 bg-gray-600 text-gray-300 dark:text-gray-800 dark:bg-gray-400" v-click="5"> Finalizada </div> </td>
    <td v-click="5" > A Ordem foi 100% apontada e integrada Estoque.</td>
  </tr>
  <tr>
    <td border-r-1> <div class="rounded pl-1 pr-1 w-17 bg-gray-800 text-gray-300 dark:text-gray-800 dark:bg-gray-300" v-click="6"> Concluído </div> </td>
    <td v-click="6" > A Ordem foi Custeada o o produto fabricado valorizado.</td>
  </tr>
  </table>


<style>
  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0);
  }

  .slidev-layout table {
    font-size: 10px;
  }

  .slidev-layout tr {
    border-bottom-width: 0px;
    --un-border-opacity: 1;
    border-color: rgb(156 163 175 / var(--un-border-opacity));
    --un-border-opacity: 0.2;
  }
  .slidev-layout td, .slidev-layout th {
    padding: 0.1rem;
    /*border-right-width: 1px;*/
    /* padding-top: 0.75rem; */
    /* padding-bottom: 0.75rem; */
  }

</style>

---


# A Manufatura do Queijo Minas Frescal
Resolvendo a Lista de Material e Roteiro de Produção

<div class="absolute top-5 right-25 ">

![](/vitalatte_matinal_minas_frescal_tradicional.png){width=150px lazy}

</div>


<div class="grid grid-cols-3 gap-4 mt-10">
  <div class="col-span-2">

 | ITEM | QUANTIDADE PAI (EM LITROS) | QUANTIDADE FILHO |
 | --- | --- | --- |
 | Leite vaca in natura padrão | 10 | 100 litros |
 | Sal ref extra cisne 25kg ind(vermelho) | 10 | 1.000 g |
 | Cloreto de calcio | 10 | 300 ml |
 | Fermento dvs tcc 20 500u congelado | 10 | 1.000 ml |
 | Chy max extra bb 5 litros (coagulante) | 10 | 60 ml |
 | Pote ( prt 530 ) - leve | 10 | 20 un |
 | Pote vita 500g - minas frescal tradicional ( PRT 530 ) | 10 | 20 un |
 | Tampa vita 500g - minas frescal trad (imp) (st 125) (st 130) | 10 | 20 un |
 | Saco vita/eur 20 x 35 - minas frescal pote (bobina) (liso) | 10 | 20 un |
 | Saco vita/eur 20 x 35 - minas frescal pote (bobina) (liso) | 10 | 20 un |
 | Cx vita - nº 15 - 06 pt - 500g | 10 | 3 un |
 | Fita adesiva 12mmx120m branca (embalar queijo) - 50 microns | 10 | 3 metros |

</div> 

<div class="col-span-1">

|ROTEIRO DE PRODUÇÃO|TEMPO|
|--|--|
|Mistura Fermento Lácteo (DVS) | 30 minutos |
|Mistura Cloreto de Calcio e Coagulação| 45 minutos |
|Corte da Coalhada com a Lira| 10 minutos |
|Mexedura| 20 minutos |
|Salga| 10 minutos |
|Formas de Minas Frescal | 60 minutos |
|Embalagem| 15 minutos |
</div>

</div>

Observação: Na lista de material podem ser adicionados itens Alternativos, geralmente substitutos para os itens da lista caso faltem.

<style>
  .slidev-layout table {
    width: 100%;
    font-size: small;
  }

  tr:nth-child(even) {background-color: #f2f2f2;}

  .slidev-layout td, .slidev-layout th {
      padding: 0.1rem;
      font-size: 10px;
      /*padding-top: 0.75rem;*/
      /*padding-bottom: 0.75rem;*/
  }

</style>


---


# A Manufatura do Queijo Minas Frescal
Resolvendo a venda em caixa ou unidade

<div class="absolute top-5 right-25 ">

![](/vitalatte_matinal_minas_frescal_tradicional.png){width=150px lazy}

</div>


Usando a Unidades de Conversão entre almoxarifados

- As unidades de converção servem para converter a unidade de um produto em outra, por exemplo, a unidade de venda de um produto pode ser em caixa ou em unidade.

- Pode ter o queijo no almoxarifado de produção em kg e ao movimentar para o almoxarifado de venda é convertido em unidade ou em caixa.
---
preload: false
layout: image
image: ./EME4_FUNDO_FIM2.png
---

# Contato 




