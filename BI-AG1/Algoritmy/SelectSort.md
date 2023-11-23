---
tags:
- BI-AG1
- Completed
---

> **časová složitost:** $\theta(n^2)$
> **paměťová náročnost**: in-place
> **stabilita**: nestabilní
> **datová citlivost**: datově necitlivý

### Vstup
- neseřazená posloupnost

### Výstup
- seřazená vstupní posloupnost

### Idea
- vstupní posloupnost se rozdělí na levou seřazenou a pravou neseřazenou část
- na počátku je levá část prázdná a pravá část je celá vstupní posloupnost
- po vložení prvku se hranice mezi seřazenou a neseřazenou částí posune o jednu pozici doprava
- z neseřazené pravé části se vybere **minimum** a prohodí se s jejím prvním prvkem, tj. přímo za seřazenou část