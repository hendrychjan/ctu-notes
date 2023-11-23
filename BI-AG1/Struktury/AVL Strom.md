# Vyvažování
- při automatickém vyvažování postupujeme podle toho, z jakého syna při rekurzi přišla informace o změně hladin

## Z levého syna

#### Vrchol měl znaménko +1
- Hloubka levého podstromu se vyrovnala s hloubkou pravého, znaménko se změní na 0
- Hloubka podstromu T(x) se nezměnila, takže propagování zastavíme
	
#### Vrchol měl znaménko 0
- Znaménko x se změní na -1
- Hloubka podstromu T(x) se změnila, takže musíme pokračovat v propagování

#### Vrchol x měl znaménko -1
- ...tedy teď se změní na -2, a je potřeba vyvažovat
- Označme y vrchol, z nějž přišla informace o prohloubení, čili levého syna vrcholu x

###### Vrchol y má znaménko -1
- Provedeme jednoduchou rotaci R hrany {x, y}
![](Attachments/Pasted%20image%2020231120154245.png)
- Z pohledu vyšších pater se nic nezměnilo, propagování tedy zastavíme
		
###### Vrchol y má znaménko +1
- Označíme z jako pravého syna vrcholu y (musí existovat)
- Provedeme dvojitou rotaci LR, která celou konfiguraci překoření za vrchol z
![](Attachments/Pasted%20image%2020231120155156.png)
- Propagování zastavíme

## Z pravého syna
#### Vrchol měl znaménko -1
- Hloubka pravého podstromu se vyrovnala s hloubkou levého, znaménko se změní na 0
- Hloubka podstromu T(x) se nezměnila, takže propagování zastavíme

#### Vrchol měl znaménko 0
- Znaménko x se změní na +1
- Hloubka podstromu T(x) se změnila, takže musíme pokračovat v propagování

#### Vrchol x měl znaménko +1
- ...tedy teď se změní na +2, a je potřeba vyvažovat
- Označme y vrchol, z nějž přišla informace o prohloubení, čili pravého syna vrcholu x

###### Vrchol y má znaménko +1
- Provedeme jednoduchou rotaci L hrany {x, y}
![](Attachments/Pasted%20image%2020231120154231.png)
- Z pohledu vyšších pater se nic nezměnilo, propagování tedy zastavíme

###### Vrchol y má znaménko -1
- Označíme z jako levého syna vrcholu y (musí existovat)
- Provedeme dvojitou rotaci RL, která celou konfiguraci překoření za vrchol z
![](Attachments/Pasted%20image%2020231120155230.png)
- Propagování zastavíme