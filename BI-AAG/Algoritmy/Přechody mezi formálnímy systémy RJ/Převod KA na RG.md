---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=QgAkc1tD6ik)

## Idea
- na vstupu je NKA (bez epsilon přechodů, a jediným počátečním stavem)
- neterminály gramatiky se rovnají stavům
- díváme se na přechody, a stavům přidáváme pravidla: *stav -> {symbol}{stav}*
- pokud vede přechod *stav->koncový stav*, přidáme danému stavu jako pravidlo jen ten samotný symbol z přechodu (tím reprezentujeme fakt, že po přijetí stavu řetězec skončí a je automatem přijat)
- pokud jazyk obsahuje prázdný řetězec, přidáme k počátečnímu stavu pravidlo pro epsilon
- pokud ale je porušena podmínka, že stav obsahující pravidlo pro epsilon se vyskytuje v některé z pravých stran pravidel, to porušuje vlastnost regulární gramatiky, a proto provedeme úpravu:
	- vytvoříme nový počáteční stav
	- nakopírujeme do něj všechna pravidla původního počátečního stavu
	- z původního počátečního stavu odebereme pravidlo s epsilon

## Příklad
![](Attachments/Pasted%20image%2020231207140535.png)