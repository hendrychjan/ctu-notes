---
tags:
  - BI-AAG
  - Completed
  - Anki
---

### Definice
![](Attachments/Pasted%20image%2020231206233439.png)

### Idea
#### První jazyk neobsahuje prázdný řetězec
- jako první proběhne první automat
- jeho koncové stavy už nejsou koncové, ale vstupy do těchto původně koncových stavů nakopírujeme do počátečního stavu druhého automatu

#### První jazyk obsahuje prázdný řetězec
- vytvoříme nový počáteční stav
- nakopírujeme do něj odchozí přechody z počátečních stavů obou automatů
- původním počátečním stavům, pokud byly zároveň koncové, odebereme status koncových stavů

### Příklad
![](Attachments/Pasted%20image%2020231206233503.png)