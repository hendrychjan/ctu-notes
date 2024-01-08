---
tags:
  - BI-AAG
  - Completed
  - Anki
---

### Vlastnosti
> **Vstup:** úplně určený NKA
> **Výstup:** KA, který generuje $L(M_1 \cup M_2)$
> - výstup bude DKA, pokud oba automaty na vstupu jsou DKA

### Definice
![](Attachments/Pasted%20image%2020231206231551.png)

### Idea
- **pro jednodušší postup automaty musí být úplně určené a deterministické!**
- automaty spustíme paralelně vedle sebe, a oběma jim postupně na vstup přidáváme stejný vstupní řetězec
- pokud po přečtení vstupu je alespoň jeden z automatů v přijímací konfiguraci, pak daný vstupní řetězec patří do jazyka vzniklého sjednocením
- pomocí tabulky - obdobně jako při determinizaci vytváříme dvojice

### Příklad
![](Attachments/Pasted%20image%2020231206231617.png)
![](Attachments/Pasted%20image%2020231206231622.png)