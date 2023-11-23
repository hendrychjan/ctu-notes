---
tags:
- BI-AG1
- Completed
---

**Breadth-First Search**

> ###### Časová složitost
> $O(|V|+|E|)$
> ###### Vstup
> - neorientovaný graf $G = (V, E)$ a vrchol $s \in V$
> ###### Výstup
> - pole vzdáleností $D$ takové, že:
>	![](Attachments/Pasted%20image%2020231031091859.png)
>- pole předchůdců $P$ takové, že:
>	![](Attachments/Pasted%20image%2020231031091917.png)

### Implementace
```
Algoritmus BFS(graf G, vrchol s):
	Pro každý vrchol v ∈ V (G):
		stav[v] := nenalezený
		D[v] := P[v] := undef
	Q := fronta obsahující jediný vrchol s
	stav[s] := otevřený
	D[s] := 0, P[s] := ⊥
	Dokud je fronta Q neprázdná:
		Odeber z Q první vrchol, nechť to je v
		Pro všechny sousedy w vrcholu v:
			Pokud stav[w] = nenalezený:
				stav[w] := otevřený
				D[w] := D[v] + 1
				P[w] := v
				Přidej w na konec fronty Q
		stav[v] := uzavřený
	Vrať (D, P)
```