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
| `BVSShow(v)` | $O(\lvert T(v) \rvert)$ | Vypíše vzestupně uspořádanou posloupnost všech klíčů | 
| `BVSMin(v)`, `BVSMax(v)` | $O(h(T(v)))$ | Vrátí vrchol obsahující minimální/maximální klíč |
| `BVSPred(v, w), BVSSucc(v, w)` | $O(h(T(v)))$ | Vrátí předchůdce/následníka vrcholu |
| `BVSFind(v, x)` | $O(h(T(v)))$ | Vrátí vrchol ve stromě s hledaným klíčem, pokud existuje |
| `BVSInsert(v, x)` | $O(h(T(v)))$ | Vloží do stromu nový vrchol s daným klíčem, pokud tam ještě neexistuje |
| `BVSDelete(v, x)` | $O(h(T(v)))$ | Pokud existuje, odstraní ze stromu vrchol s daným klíčem |

## Struktura
- strom reprezentujeme pomocí spojových struktur
- v algoritmech popisujících pseudokód operace nad binárními stromy budeme pracovat s ukazateli na jejich vrcholy

# Implementace

## `BVSShow(v)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)*
> **Výstup:** vzestupně uspořádaná posloupnost klíčů všech vrcholů v *T(v)*

![](Attachments/Pasted%20image%2020231126120213.png)

## `BVSMin(v)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)*
> **Výstup:** ukazatel na vrchol obsahující nejmenší klíč v *T(v)*

- nejmenší klíč je první v posloupnosti vzestupně uspořádaných klíčů, tedy ve stromě leží úplně nejvíc vlevo

![](Attachments/Pasted%20image%2020231126120444.png)

## `BVSPred(v)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)* a na nějaký jeho vrchol *w*
> **Výstup:** ukazatel na předchůdce *w* v *T(v)*

![](Attachments/Pasted%20image%2020231126120551.png)

## `BVSFind(v, x)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)* a klíč *x*
> **Výstup:** ukazatel na vrchol s klíčem *x*, pokud takový v *T(v)* existuje, jinak `nullptr`

![](Attachments/Pasted%20image%2020231126120811.png)

## `BVSInsert(v, x)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)* a klíč *x*
> **Výstup:** ukazatel na kořen *v* v BVS s prvkem s klíčem *x*

![](Attachments/Pasted%20image%2020231126120934.png)

## `BVSDelete(v, x)`
> **Vstup:** ukazatel na kořen *v* nějakého BVS *T(v)* a klíč *x*
> **Výstup:** ukazatel na kořen BVS, ze kterého byl odstraněn vrchol s klíčem *x*, pokud takový vrchol existoval

### Idea
- nejdříve nalezneme vrchol, který obsahuje klíč, který chceme smazat
- při mazání vrcholu rozlišujeme několik situací:

##### 1. Vrchol ve stromě neexistuje
- strom necháme beze změny

##### 2. Vrchol je listem
- jednoduše ho odtrhneme od stromu
- ![](Attachments/Pasted%20image%2020231126121444.png)

##### 3. Vrchol má jednoho syna
- jednoduše ho nahradíme tímto synem
- ![](Attachments/Pasted%20image%2020231126121536.png)

##### 4. Vrchol má dva syny
- nemůžeme ho odstranit přímo, protože by nebylo kam připojit jeho syny
- využijeme faktu, že má ve stromě následníka, který má nutně pouze jednoho syna (pravého)
- ![](Attachments/Pasted%20image%2020231126121743.png)

### Pseudokód
![](Attachments/Pasted%20image%2020231126121806.png)