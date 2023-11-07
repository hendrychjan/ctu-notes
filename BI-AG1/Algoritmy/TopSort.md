---
tags:
- BI-AAG
---

**Topologial sort**

### Vstup
- orientovaný graf $G$

### Výstup
- nějaké topologické uspořádání $G$, pokud byl acyklický, a detekce cykličnosti v opačném případě

### Idea
- průběžně:
	- počítej vstupní stupně vrcholů
	- zdroje zařazuj do fronty
	- odebírej vrcholy z fronty, zařazuj je do výstupního pořadí a odebírej je z grafu a to znamená, že jejich následníkům snižuj vstupní stupně
- pokud po vyprázdnění fronty zbyly v grafu nějaké vrcholy, byl v něm orientovaný cyklus

### Implementace
![](Attachments/Pasted%20image%2020231107173632.png)

### Důkaz správnosti
![](Attachments/Pasted%20image%2020231107175815.png)
![](Attachments/Pasted%20image%2020231107175822.png)
![](Attachments/Pasted%20image%2020231107175831.png)

### Časová složitost
> Algoritmus `TopSort(G)`, kde $G=(V,E)$ je orientovaný graf reprezentovaný pomocí pole následníků, má časovou i paměťovou složitost $O(|V|+|E|)$

![](Attachments/Pasted%20image%2020231107180012.png)