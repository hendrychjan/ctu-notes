---
tags:
  - BI-AAG
  - Completed
  - Anki
---

[Video od Elišky Šestákové](https://www.youtube.com/watch?v=_VSWCA3c4q8&list=PLvvwWYjStIQ0s2H_EdBgNSUmsZfPAZ3dq&index=3)

## Definice
![](Attachments/Pasted%20image%2020231206205729.png)

## Idea
- vytvoříme si množinu dosažitelných stavů, do které jako první vložíme počáteční stav
- iterativně množinu procházíme, a pro každý stav v ní přidáme všechny stavy, do kterých se z daného stavu lze dostat
- až už nebude možné nic dalšího přidat, stavy v množině jsou dosažitelné, a zbylé jsou nedosažitelné - můžeme je z automatu odstranit
