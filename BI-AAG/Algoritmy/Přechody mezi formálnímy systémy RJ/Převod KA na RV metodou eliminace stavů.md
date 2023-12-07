---
tags:
  - BI-AAG
  - Completed
  - Anki
---

![Video od Elišky Šestákové](https://www.youtube.com/watch?v=kNJbcD3NcnE)

## Idea
- vytvoříme nový startovací stav, a z něj vedeme epsilon přechod na původní počáteční stav
- pokud máme více koncových stavů, vytvoříme nový koncový stav, a všem původním koncových stavům přidáme epsilon přechod do toho nového
- postupně eliminujeme jednotlivé stavy
	- identifikujeme všechny cesty délky 2 (+ případně smyčka) vedoucí přes daný stav 
	- stav odstraníme
	- cesty nahradíme: *{co vedlo do stavu}.{iterace symbolu smyčky, pokud existuje}\ *.{co vedlo ze stavu}*
	- pokud někde existují dva přechody, můžeme je nahradit *{přechod 1}+{přechod 2}*
- na konci máme pouze startovní stav a koncový stav, a mezi nimi jeden přechod, který obsahuje hledaný regulární výraz

## Příklad
![](Attachments/Pasted%20image%2020231207140641.png)