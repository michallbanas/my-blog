---
title: Responzívny navigation bar
description: This is a post on My Blog about leveraging agile frameworks.
date: 2021-02-18
tags:
  - flexbox
layout: layouts/post.njk
---

Existuje veľa spôsobov a možností ako vytvoriť na webovej stránke responzívnu navigáciu, ale zo všetkých najradšej mám vytvorenie navigácie pomocou flexboxu. Je to veľmi rýchly spôsob a stačí nám pri tom naštýlovať iba pár elementov. Budem sa snažiť používať hlavne sémantický kód, aby sme sa vyhli samému používaniu div kontajneru, ako to vidím vo veľa iných tutoriálov. Náš kód je potom oveľa prehladnejší, lepšie čitateľný a prístupný.

Najprv si vytvoríme navigáciu v HTML. Bude nám na to stačiť týchto 5 elementov: body, nav, a, ul a li. Čo sa týka HTML, tak je to všetko, jednoduché že? Teraz už iba tieto elementy naštýlovať pomocou CSS vlastností.

<img src="../../img/01html.png">

Dlhú dobu sa na vytváranie layoutu stránky používali CSS vlastnosti ako float alebo position. Ich používanie však bolo do istej miery frustrujúce a malo svoje limity. Vďaka flexboxu nám však stačí v prípade responzívnej navigácie použiť iba tri hodnoty: display:flex, justify-content: space between a align-items: center.

Prvá hodnota urobí to, že sa položky v nav usporiadajú vertikálne. Justify-content definuje ako sa rozdelí priestor medzi a okolo obsahu vo flex kontajneri. A nakoniec align-items v našom prípade vycentruje a dá na jednu líniu element a a element ul, teda naše logo a položky v menu. Prvú a tretiu hodnotu musíme nastaviť aj pre ul, inak by sa nám zoznam zobrazoval horizontálne, čo nechceme.

<img src="../../img/02css.png">

Všetky ostatné CSS vlastnosti v tomto príklade slúžili na skrášlenie či zrušenie nechcených hodnôt ako napríklad nastavenie list-style či text-decoration na “none”. V prípade zobrazenie na mobilnom zariadení som nastavil, aby sa smer flexboxu zmenil z vertikálneho na horizontálny, pomocou flex-direction: column, takto sa v prípade zariadenií so šírkou obrazovky menšou ako 688px, zobrazí navigácia usporiadaná pekne pod sebou.

<hr>

<p class="codepen" data-height="273" data-theme-id="dark" data-default-tab="html,result" data-user="michallbanas" data-slug-hash="oNYjQjQ" data-preview="true" style="height: 273px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Responsive Nav Bar">
  <span>See the Pen <a href="https://codepen.io/michallbanas/pen/oNYjQjQ">
  Responsive Nav Bar</a> by michallbanas (<a href="https://codepen.io/michallbanas">@michallbanas</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
