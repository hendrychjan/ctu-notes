---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=JW1_KbkGfic&list=PLvvwWYjStIQ0s2H_EdBgNSUmsZfPAZ3dq&index=1)

### Vlastnosti
> **Vstup:** NKA s epsilon přechody
> **Výstup:** NKA bez epsilon přechodů

### Definice
![](Attachments/Pasted%20image%2020231206211102.png)

### Idea
- pro každý stav v automatu nalezneme *epsilon-closure*, což je stav samotný, a všechny stavy, do kterých se lze z daného stavu dostat pomocí epsilon přechodu
- pro každý symbol všem stavům nakopírujeme přechody ze stavů v jeho epsilon-closure
- stav je koncový, pokud jeho epsilon-closure obsahuje alespoň jeden původně koncový stav

- algoritmus odstranění epsilon přechodů nezvýší počet stavů automatu, nemění počáteční stav, množina koncových stavů se však může zvětšit
- konečný automat s epsilon přechody může přijímat i epsilon přechodem do koncového stavu