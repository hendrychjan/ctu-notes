---
tags:
  - BI-AG1
  - Completed
  - Anki
---

# Rozhraní

## Funkce
| Operace | Časová složitost | Popis |
| ------------- | --------------------------- | --------- |
| `HeapInsert(H,k)` | $O(\log{n})$ | vloží nový klíč *k* do haldy *H* |
| `HeapFindMin(H)` | $O(1)$ | Najde a vrátí minimum ze všech prvků na haldě *H* |
| `HeapExtractMin(H)` | $O(\log{n})$ | Odstraní minimum z haldy *H* a vrátí ho |
| `HeapBuild()` | $O(\log{n})$ | Vytvoří binární haldu z pole in-place |

## Struktura
### Reprezentace jako graf
**Binární halda *H***
- `H.root` je aktuální kořen
- `H.n` aktuální počet prvků
- `H.last` ukazatel na aktuální poslední list (nejpravější list v poslední hladině), pokud existuje

**Prvek *x* haldy *H***
- klíč `k(x)`
- ukazatel na otce
- ukazatel na své dva syny (pokud existují)

### Reprezentace v poli
- reprezentace pomocí dynamicky alokovaných spojových struktur je zbytečně komplikovaná
- vrcholy můžeme očíslovat po hladinách shora dolů a jejich indexy pak odpovídají indexům v poli
- ![](Attachments/Pasted%20image%2020231121082309.png)

> **Vztahy indexů v haldě**
> - má-li vrchol *v* index *i*, pak:
> 	- jeho levý syn má index $2i$
> 	- jeho pravý syn má index $2i + 1$
> 	- jeho otec má index $\lfloor \frac{i}{2} \rfloor$
> 	- výraz $i \mod 2$

# Vlastnosti
> **Věta o počtu hladin haldy**
> Binární halda s *n* prvky má $\lfloor \log{n} \rfloor$ hladin.

> **Věta o počtu vnitřních vrcholů a listů binární haldy**
> Binární halda s $n \geq 3$ prvky má $\lfloor \frac{n}{2} \rfloor$ vnitřních vrcholů a $\lceil \frac{n}{2} \rceil$ listů

# Implementace

## Heap Insert
> **Časová složitost**
> Na každé hladině strávíme $O(1)$ operací a procházených hladin je logaritmicky mnoho, celkem tedy čas $O(\log{n})$

### Idea
- vlastnost tvaru dovoluje přidat okamžitě prvek na konec nejspodnější hladiny
- pokud je poslední hladina plná, založíme novou hladinu
- pokud je haldové uspořádání mezi novým listem *l* a jeho otcem *o* v pořádku, můžeme skončit
- pokud ne, prohodíme *k(l)* a *k(o)*
- tím se ale může porušit haldové uspořádání mezi vrcholem *o* a otcem vrcholu *o*
- pokud pro ně haldové uspořádání neplatí, opět je prohodíme, jinak končíme
- toto opakujeme, nejdéle však do kořene

### Pseudokód
![](Attachments/Pasted%20image%2020231121080928.png)

## Heap Find Min
> **Časová složitost**
> $O(1)$
- vrátí klíč kořene haldy

## Heap Extract Min
> **Časová složitost**
> Na každé hladině provedeme $O(1)$ operací, a proházených hladin v probublávání je nejvíce logaritmicky mnoho, tedy celkový čas je $O(\log{n})$

### Idea
- odstranění kořene stromu by porušilo tvar haldy
- je ale triviální odstranit poslední list, čili list nejvíc napravo v poslední hladině
- postupujeme tedy následujícím způsobem:
	1. prohodíme kořen stromu a poslední list
	2. kořen, který je nyní posledním listem, triviálně odstraníme
	3. nový kořen probubláváme dolů, tak, abychom udrželi správné uspořádání

### Pseudokód
![](Attachments/Pasted%20image%2020231121082004.png)

## Heap Build
- rychlá konstrukce haldy v poli
- haldu lze z *n* prvků vytvořit opakovaným voláním funkce `HeapInsert`, což dává časovou složitost (podle Stirlingova vzorce) $O(n \log {n})$
- jde to však rychleji:

> **Časová složitost**
> $O(n)$

- `HeapBuild` lze použít pro rychlé řazení - na posloupnost zavoláme `HeapBuild`, a následně opakovaně voláme operaci `HeapExtractMin`

### Idea
- postupujeme po hladinách, a vrcholy podstromů probubláváme dolů

### Pseudokód
![](Attachments/Pasted%20image%2020231121082943.png)