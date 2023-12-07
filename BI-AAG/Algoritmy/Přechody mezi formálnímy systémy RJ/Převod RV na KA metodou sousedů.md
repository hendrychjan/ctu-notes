---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=58n3P6tz9T8)

## Idea
- vytvoříme množinu Z, která bude obsahovat všechny symboly, kterými může přijímaný řetězec začínat
- vytvoříme množinu F, která bude obsahovat všechny symboly, kterými může přijímaný řetězec končit
- vytvoříme množinu P, kam přidáme dvojice takové, že první prvek je symbol, a druhý prvek je symbol, který může s prvním symbolem sousedit
- konečný automat obsahuje:
	- startovní stav - nový stav, ze kterého vedeme přechody podle množiny Z
	- stavy - všechny stavy podle symbolů
	- množina P představuje přechody
	- množina F představuje koncové stavy
	- pokud hodnota regulárního výrazu obsahuje epsilon, pak q0 je zároveň koncový

## Příklad
![](Attachments/Pasted%20image%2020231207125507.png)