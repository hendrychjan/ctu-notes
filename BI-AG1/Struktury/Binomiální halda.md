---
tags:
  - BI-AG1
  - Completed
  - Anki
---
# Rozhraní

## Funkce
| Operace | Časová složitost | Popis |
| ------- | ---------------- | ----- | 
| `BHInsert` | $O(\log{n})$, $O*(1) | Vloží do BH nový prvek |
| `BHFindMin` | $O(1)$ | Vrátí minimum množiny prvků BH |
| `BHExtractMin` | $O(\log{n})$ | Odstraní z BH minimum množiny jejích prvků |
| `BHMerge` | $O(\log{n})$ | Sloučí dvě BH do jedné |
| `BHDecreaseKey` | $O(\log{n})$ | Sníží hodnotu klíče prvku BH |
| `BHIncreaseKey` | $O(\log{n})$ | Zvýší hodnotu klíče prvku BH |
| `BHDelete` | $O(\log{n})$ | Smaže prvek BH |

# Vlastnosti
> **Věta o počtu hladin, počtu vrcholů a stupni kořene**
> - Počet hladin stromu $B_k$ je roven $k + 1$, stupeň kořene je $k$, a počet vrcholů $B_k$ je roven $2^k$.

> **Věta o počtu synů kořene**
> Binomiální strom s $n$ vrcholy (pokud existuje), má $1 + \log{n}$ hladin a počet synů kořene $\log{n}$

> **Věta o počtu vrcholů na hladině** 
> Počet vrcholů stromu $B_k$ na hladině $i$ ($i\in\{0,...,k\}$) je $n_{k}(i) = {{k}\choose{i}}$

> **Věta o podobě binomiální haldy**
> Binomiální strom $B_i$ se vyskytuje v seznamu $T$ *n*-prvkové BH právě tehdy, když ve dvojkovém zápisu $b_{k}b_{k-1}...b_0$ čísla *n* je $b_{i}=1$

> **Věta o podobě binomiální haldy**
> Binomiální strom $B_i$ se vyskytuje v seznamu $T$ *n*-prvkové BH právě tehdy, když ve dvojkovém zápisu $b_{k}b_{k-1}...b_0$ čísla *n* je $b_{i}=1$

> **Věta o poštu binomiálních stromů v binomiální haldě**
> *n*-prvková binomiální halda má až $O(\log{n})$ binomiálních stromů
> ![](Attachments/Pasted%20image%2020231125194438.png)

# Paměťová reprezentace
- prvek BH bude v paměti reprezentován podle následující struktury:
- ![](Attachments/Pasted%20image%2020231125195727.png)
- ![](Attachments/Pasted%20image%2020231125195754.png)

# Implementace

## `BHFindMin(H)`
- minimum celé BH se musí nacházet v jednom z kořenů stromů $T_i$
- stačí tedy projít seznam $T$, což bude trvat čas $O(\log{n})$
- pokud budeme tuto funkci používat často, vyplatí se udržovat ukazatel na tento globálně nejmenší kořen, operaci pak lze provést v konstantním čase

## `BHMergeTree`
![](Attachments/Pasted%20image%2020231125194827.png)

> BH lze implementovat tak, že `BHMergeTree(T1, T2)` má časovou složitost $O(1)$

![](Attachments/Pasted%20image%2020231125194951.png)

## `BHMerge`

### Idea
![](Attachments/Pasted%20image%2020231125195031.png)
![](Attachments/Pasted%20image%2020231125195055.png)

### Pseudokód
![](Attachments/Pasted%20image%2020231125195152.png)
![](Attachments/Pasted%20image%2020231125195210.png)
![](Attachments/Pasted%20image%2020231125195229.png)

### Příklad
![](Attachments/Pasted%20image%2020231125195122.png)

## `BHInsert`
> **Časová složitost**
> ![](Attachments/Pasted%20image%2020231125195405.png)

### Pseudokód
![](Attachments/Pasted%20image%2020231125195313.png)

### Příklad
![](Attachments/Pasted%20image%2020231125195323.png)

## `BHBuild`
- voláním `BHInsert` *n*-krát po sobě vytvoříme BH o velikosti *n*
- podle analýzy časové složitosti `BHInsert` bude trvat vytvoření *n*-prvkové BH čas $O(n)$

## `BHExtractMin`
### Pseudokód
![](Attachments/Pasted%20image%2020231125195548.png)