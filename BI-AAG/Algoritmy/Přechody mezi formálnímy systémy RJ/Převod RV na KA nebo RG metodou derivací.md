---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=dHq2BNAwIWI)

## Idea
- vytváříme výrazy, a derivujeme podle každého symbolu abecedy - pokud derivací vznikne nový výraz, který není podobný žádnému z dosud objevených, derivujeme ho také
- skončíme, až se dostaneme do stavu, kdy jsme zderivovali všechny nalezené výrazy, a už jsme nezískali žádné nové
- konečný automat tvoříme:
	- stavy budou odpovídat výrazům
	- počáteční stav bude odpovídat $V_0$
	- koncové stavy budou výrazy, jejichž hodnota obsahuje epsilon
	- přechody doplníme:
		- *{výraz} --- {podle čeho jsme ho derivovali} ---> {výraz výsledkem derivace}*
	- výsledný automat je deterministický, a úplně určený
- regulární gramatiku tvoříme:
	- počáteční odpovídá $V_0$
	- u všech výrazů, které obsahují epsilon, přidáme pravidlo v gramatice tak, aby byly koncové

## Příklad
![](Attachments/Pasted%20image%2020231207131234.png)