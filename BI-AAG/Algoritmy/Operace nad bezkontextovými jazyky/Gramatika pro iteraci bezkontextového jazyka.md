---
tags:
  - BI-AAG
  - Completed
  - Anki
---

## Definice
![](Attachments/Pasted%20image%2020231206124643.png)

## Idea
- vytvoříme nový počáteční stav, který bude řetězit libovolně krát za sebe původní počáteční stav (tím dostaneme iteraci), a nebo prázdný řetězec (pro ukončení iterace, a nebo prázdný řetězec)
- sjednotíme množiny neterminálů obou gramatik, a přidáme do nich nový počáteční stav
- sjednotíme množiny pravidel obou gramatik, a přidáme do nich přechod z nového počátečního stavu
- nový počáteční stav nastavíme výchozím