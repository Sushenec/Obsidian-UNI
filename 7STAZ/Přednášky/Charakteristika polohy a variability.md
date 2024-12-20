# Základní popis dat

- deskriptivní statistika, explor. analýza dat
- graficky
    - bodový graf (XY), histogram, boxplot
    - rozptýlený diagram, leaf and stem
    - dendrogramy, ordinační diagramy (podobnosti)
- statistiky
    - tabulka četností
    - parametry populace (střední hodnota, rozptyl)
    - odhady parametrů

## Poloha, extrémy, modus

- Minimum, maximum - min {xi}
- Zejména pro diskrétní veličiny

## Modus $\hat x$

- Je to hodnota, která se vyskytuje nejčastěji v datasetu

## Aritmetický průměr $\bar x$

- Je to jakési “těžiště” hodnot (každý asi ví co je to průměr)
- Je ovlivněno extrémními hodnotami (moc malé nebo moc velké hodnoty)
- Součet všech hodnot podělených celkovým počtem hodnot

$$\displaylines{ \frac{1}{n}\sum_{i=1}^{n} x_i \\ \ \\ nebo \\ \ \\  
\sum_{i=1}^{n} \frac{x_i}{n} \\ \ \\  
n \ \to \ celkový \ počet \ prvků \\  
x_i \ \to \ hodnota \ na \ pozici \ i}$$

## Uřezaný průměr

- Uříznu p % nejmenších a největších hodnot (najdu p a 1-p kvantil) a udělám průměr
- Posouvá hodnotu k mediánu, odstraňuje extrémy
- v případě odlehlých hodnot, které nechci zařazovat do výpočtu
    - tolerance
    - obava z nepřesnosti měření
- známky: 1. student 1 4 4 4, 2.student 1 1 1 4
- měření výkonů sportovců
- testy rychlosti počítačové sítě

## Geometrický průměr

- Pro průměrné přírůstky, zisky, apod.
- Například: relativní meziroční nárůst ceny firmy
- Počítá se jako n-tá odmocnina součinu všech hodnot

$$\displaylines{\sqrt[n]{ \ \prod_{i=1}^{n} x_i} \\ \ \\  
nebo \\ \ \\  
\bigg( \prod_{i=1}^{n} x_i\bigg)^{\frac{1}{n}} \\ \ \\  
n \ \to \ celkový \ počet \ prvků \\  
x_i \ \to \ hodnota \ na \ pozici \ i}$$

## Kvantily

- Vyjadřují hodnotu na určité pozici v seřazeném seznamu hodnot
- Značí se $x_p$ p je procento (to kde se kvantil nachází relativně začátku)  
      
    $x_{0,25}$ je první kvartil
- Nejčastěji používané - Horní (první) kvartil, Medián, Dolní (Třetí) kvartil

$$\displaylines{výpočet \ indexu \ na \ kterém \ se \ nachází \ kvantil \\  
z = n \cdot p \ + (1-p) \\ \ \\  
z \ \to \ index \ kvantilu \ v \ seřazeném \ seznamu \\  
n \ \to \ celkový \ počet \ prvků \\  
p \ \to \ procento \ kvantilu$$$$Příklad \\  
Chceme \ zjistil \ na \ jaké \ pozici,\textcolor{firebrick}{ \ v \ seřazených \ datech}, se \ nachází \ x_{0,25} \ kvantil \\  
Máme \ 13 \ naměřených \ hodnot \ \to n = 13 \\ \ \\  
z = 13 \ \cdot \ 0,25 \ +(1 - 0,25) \\  
z = 4 \\ \ \\  
x_{0,25} \ kvantil \ se \ nachází \ na \ pozici \ 4}$$

- Pokud vyjde index z jako desetinné číslo, tak bereme celočíselné hodnoty okolo toho čísla a děláme průměr  
    Příklad: když index z vyjde 8,25 → bereme hodnoty na indexech 8 a 9 a uděláme průměr těch dvou hodnot  
    

### Medián $\tilde{x}$

- Medián je 50 % kvantil - hodnota větší než 50% všech hodnot
- Zjišťování mediánu - seřadíme všechny naměřené hodnoty a vybereme tu která je přesně uprostřed (50% od začátku seřazené řady)
- $1,2,3,\textcolor{darkcyan}{3},4,6,7$ Medián je 3
- Pokud je počet hodnot párný, tak bereme průměr dvou prostředních hodnot
- $1,2,2,\textcolor{darkcyan}2,\textcolor{darkcyan}3,4,5,7$ Medián je 2,5 ($\frac{2+3}{2}$)
- Alternativně jde, jako všechny kvantily, zjistit pomocí [[Charakteristika polohy a variability]]výše

### Horní kvartil $x_{0,25}$

- 25% kvantil - hodnota větší nebo rovna 25% hodnot a menší než nebo rovna 75% hodnot
- Zjišťování horního kvartilu - v seřazených hodnotách najdeme medián. Najdeme prvek hodnotu, která je uprostřed první poloviny.
- Nebo jde taky zjistil pomocí [[Charakteristika polohy a variability]]
- $1,2,\textcolor{darkcyan}2,\textcolor{darkcyan}2,3,4,5,7$ Horní kvartil je 2

### Dolní kvartil $x_{0,75}$

- 75% kvantil - hodnota větší nebo rovna 75% hodnot a menší nebo rovna 25% hodnot
- Je to stejné jako horní kvantil jenom jsou tam jiné čísla
- [[Charakteristika polohy a variability]]
- $1,2,2,2,3,\textcolor{darkcyan}4,\textcolor{darkcyan}5,7$ Dolní kvartil je 4,5 $(\frac{4+5}{2})$

## Variabilita

- variabilita dat - různorodost měření (výsledkem měření jsou různé hodnoty)
- variabilita
    - přirozená - způsobena heterogenitou prostřední
    - chybová - chyby měření

## Rozpětí (range) $R$

- Je to “vzdálenost” mezi maximem a minimem
- Vypočte se $R=x_{max}-x_{min}$
- Rozpětí jde počítat i mezi jinými hodnotami než max a min
- IQR (Inter Quartil Range) je podtyp rozpětí
- IQR je “vzdálenost” mezi horním a dolním kvartilem
- Vypočte se $R_{0,25}=x_{0,75}-x_{0,25}$
- Pro znázornění těchto hodnot se používají box-plot nebo rozmítnutý diagram rozptýlení

## Box-Plot (krabicový graf)

- Využívá se pro srovnání, charakteristiky polohy, u různých dat  
    (např. srovnání délky zobáků různých ptáků)  
    

	[![](https://miro.medium.com/v2/resize:fit:350/1*JJSEEZ6cWNHJiYkb-y7lKg.png)](https://miro.medium.com/v2/resize:fit:350/1*JJSEEZ6cWNHJiYkb-y7lKg.png)

- Horní část “krabice” je horní kvartil a dolní část “krabice” je dolní kvartil
- Medián je čára někde uvnitř “krabice” (nemusí být vždycky uprostřed, jako na obrázku)
- Whisker(hradba nebo vnější hradba) - nahoře je horní hradba a dole je spodní hradba
- Dolní hradba(lower extreme) - vypočte se $IQR \cdot 1,5 - x_{0,25}$ a umístí se k nejbližší hodnotě, která je větší než dolní hradba
- Horní hradba(upper extreme) - vypočte se $IQR \cdot 1,5 + x_{0,75}$ a umístí se k nejbližší hodnotě, která je menší než horní hradba
- Hodnoty, které jsou mimo hradby(outliers), se zakreslují jako tečky (pozor, někdy tam nejsou zakreslené, i když by tam měly být)

## Rozptyl (variace) $s^2$ nebo $\sigma^2$

- Je to průměrná “vzdálenost” hodnot od průměru
- Rozptyl není ve stejných jednotkách jako hodnoty, pokud chceme vědět průměrnou vzdálenost ve stejných jednotkách, v jakých jsou hodnoty, tak se musí použít směrodatná odchylka (standard deviation $SD$)
- Rozptyl a směrodatná odchylka mají zásadní význam ve statistice
- Pro výpočet existují 2 vzorce
- Výpočet $\sigma^2$ se používá, když máme změřené všechnu populaci (např. by jsme měli změřenou váhu všech cihel (moc často se to nestává, že by jsme mohli změřit celou populaci))
- Častěji se používá výpočet $s^2$ který se používá, když máme změřený jen nějaký výběr celku (např. změřená výška milionu lidí z 8 miliard)
- Vždy platí $\sigma^2 < s^2$

$$\displaylines{s^2=\sum_{i=1}^n \frac{(x_i - \overline x)^2}{n-1}  
\\ \ \\ nebo \\ \ \\  
s^2=\frac{1}{n-1} \cdot\sum_{i=1}^n (x_i - \overline x)^2  
\\ \ \\  
x_i \to hodnota \ na \ pozici \ i \\  
\overline x \to průměr \ hodnot \\  
n \to počet \ všech \ hodnot \\ \ \\ }$$ 

$$\displaylines{\\ \ \\ \sigma^2=\sum_{i=1}^n \frac{(x_i - \overline x)^2}{n}  
\\ \ \\ nebo \\ \ \\  
\sigma^2=\frac{1}{n} \cdot\sum_{i=1}^n (x_i - \overline x)^2  
\\ \ \\  
x_i \to hodnota \ na \ pozici \ i \\  
\overline x \to průměr \ hodnot \\  
n \to počet \ všech \ hodnot}$$

## Směrodatná odchylka (standard deviation) $s$ nebo $\sigma$

- Stejně jako rozptyl, je to průměrná “vzdálenost” hodnot od průměru, ale na rozdíl od rozptylu je ve stejných jednotkách jako hodnoty
- Stejně jako u rozptylu, $\sigma$ se používá jen, když máme naměřenou celou populaci a $s$ se používá, když máme nějaký výběr z populace

$$\displaylines{s=\sqrt{s^2} \\  
\sigma=\sqrt{\sigma^2} \\ \ \\  
s^2 \to rozptyl \ pro \ výběr \ z \ populace \\  
\sigma^2 \to rozptyl \ pro \ celou \ populaci}$$

## Přesnost měření

- variační koeficient