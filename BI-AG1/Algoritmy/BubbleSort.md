---
tags:
- BI-AG1
- Completed
---

> **časová složitost:** $O(n^2)$
> **paměťová náročnost**: in-place
> **stabilita**: stabilní
> **datová citlivost**: datově citlivý

- vhodný algoritmus, pokud je např. vstupní posloupnost z velké části seřazená

### Vstup
- neseřazená posloupnost

### Výstup
- seřazená vstupní posloupnost

### Idea
- řazení "probubláváním" větších prvků doprava
- postupně zleva doprava se porovnávají dvojice sousedních prvků a pokud jsou prvky dvojice v nesprávném pořadí, prohodí se
- po prvním průchodu se největší prvek dostane na poslední místo
- celý postup se opakuje nejvýše $(n-1)$-krát: pokaždé se seřazená podposloupnost vpravo prodlouží o jednu pozici doleva
- pokud se během jednoho průchodu neprohodila žádná dvojice sousedů, už se nikdy žádná neprohodí a řazení skončilo

### Implementace
![](Attachments/Pasted%20image%2020231107182034.png)

### Důkaz korektnosti
![](Attachments/Pasted%20image%2020231107182116.png)

### Důkaz charakteristik
![](Attachments/Pasted%20image%2020231107182201.png)