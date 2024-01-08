---
tags:
  - BI-AAG
  - Completed
  - Anki
---

### Vlastnosti
> **Vstup:** úplně určený NKA
> **Výstup:** KA, který generuje $L(M_1 \cap M_2)$
> - výstup bude DKA, pokud oba automaty na vstupu jsou DKA

### Definice
![](Attachments/Pasted%20image%2020231206232318.png)

### Idea
- pokud chceme mít výsledný automat deterministický, oba automaty na vstupu musí být deterministické
- pro jednodušší postup je lepší mít na vstupu deterministické automaty
- automaty spustíme paralelně vedle sebe, a oběma jim postupně na vstup přidáváme stejný vstupní řetězec
- pokud po přečtení vstupu jsou oba automaty v přijímací konfiguraci, pak daný vstupní řetězec patří do jazyka vzniklého sjednocením
- do tabulky:
	- postupně vkládáme dvojice obdobně jako při determinizaci
