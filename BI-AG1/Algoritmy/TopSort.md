---
tags:
- BI-AG1
- Completed
---

**Topologial sort**

> ###### Časová složitost
> $O(|V|+|E|)$
> ###### Paměťová složitost
> $O(|V|+|E|)$
> ###### Vstup
> - orientovaný graf $G$
> ###### Výstup
> - nějaké topologické uspořádání $G$, pokud byl acyklický, a detekce cykličnosti v opačném případě


### Idea
- průběžně:
	- počítej vstupní stupně vrcholů
	- zdroje zařazuj do fronty
	- odebírej vrcholy z fronty, zařazuj je do výstupního pořadí a odebírej je z grafu a to znamená, že jejich následníkům snižuj vstupní stupně
- pokud po vyprázdnění fronty zbyly v grafu nějaké vrcholy, byl v něm orientovaný cyklus

### Implementace
![](Attachments/Pasted%20image%2020231107173632.png)