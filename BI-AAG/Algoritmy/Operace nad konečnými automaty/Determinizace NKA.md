---
tags:
  - BI-AAG
  - Completed
  - Anki
---

[Video od Elišky Šestákové](https://www.youtube.com/watch?v=47awv0bU3Hc&list=PLvvwWYjStIQ0s2H_EdBgNSUmsZfPAZ3dq&index=2)

## Definice
![](Attachments/Pasted%20image%2020231206225618.png)

## Idea
- začneme vytvářet nový automat, jako první do tabulky přidáme počáteční stav z původního NKA (musí mít pouze jeden, pokud jich má víc, je potřeba použít [algoritmus Odstranění více počátečních stavů](BI-AAG/Algoritmy/Operace%20nad%20konečnými%20automaty/Odstranění%20více%20počátečních%20stavů.md))
- vytváříme nové stavy a přidáváme je do tabulky následujícím způsobem:
	- nový stav je definován jako množina všech stavů, do kterých se lze dostat přes jednotlivé symboly ze všech stavů, kterými je tvořena množina právě zpracovávaného stavu