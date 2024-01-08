---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=SE7cM5kYZxI&list=PLvvwWYjStIQ0s2H_EdBgNSUmsZfPAZ3dq&index=4)

### Vlastnosti
> **Vstup:** NKA
> **Výstup:** NKA bez zbytečných stavů

### Definice
![](Attachments/Pasted%20image%2020231206210616.png)

### Idea
- vytvoříme množinu užitečných stavů, a inicializujeme ji množinou koncových stavů
- množinu iterativně procházíme, a pro každý stav v ní přidáme všechny stavy, do kterých se lze do daného stavu nějakým přechodem dostat
- pokud už není co přidávat, nalezená poslední množina obsahuje pouze užitečné stavy