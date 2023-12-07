---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=GIZqiyGvAIY)

## Idea
- do gramatiky přidáme nové neterminály a pravidla:
	- $S' \rightarrow S$
	- $F' \rightarrow \epsilon$
- ke každému pravidlu, které na pravé straně obsahuje pouze terminál, daný terminál zřetězíme s $F'$
- pro každý symbol, kde se na pravých stranách jeho pravidel vyskytuje pouze tento symbol, upravíme:
	- ![](Attachments/Pasted%20image%2020231207123236.png)
- postupně eliminujeme jednotlivé symboly
	- všude, kde se daný neterminál vyskytuje na pravé straně pravidla, nahradíme tím, co daný neterminál generuje
- když se dostaneme do situace, že gramatika obsahuje pouze S' a F', pravidlo S' (bez F') je výsledný regulární výraz

## Příklad
![](Attachments/Pasted%20image%2020231207123818.png)