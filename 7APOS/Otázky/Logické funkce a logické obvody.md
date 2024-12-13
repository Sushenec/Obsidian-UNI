Logické funkce a logické obvody pracují s binárními/logickými hodnotami (0, 1)

# Logické funkce

- Obecně, logická funkce přijímá binární hodnotu/hodnoty a vrací binární hodnotu

Tabulka ukazuje všechny možné funkce pro 2 vstupní hodnoty (A, B)

| A   | B   |  $\mathrm{f_0}$   | $\mathrm{f_1}$   |$\mathrm{f_2}$   |$\mathrm{f_3}$   |$\mathrm{f_4}$   |$\mathrm{f_5}$   |$\mathrm{f_5}$   |$\mathrm{f_6}$|$\mathrm{f_7}$   |$\mathrm{f_8}$   |$\mathrm{f_9}$   |$\mathrm{f_{10}}$   |$\mathrm{f_{12}}$   |$\mathrm{f_{13}}$   |$\mathrm{f_{14}}$   |$\mathrm{f_{15}}$   |
| --- | --- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |
|  0  |  0  |   0  |   0  |0 |0 |0 |0 |0 |0|1 |1|1 |1|1 |1|1 |1 |
|  0  |  1  |   0  |   0  |0 |0 |1 |1 |1 |1|0 |0|0 |0|1 |1|1 |1 |
|  1  |  0  |   0  |   0  |1 |1 |0 |0 |1 |1|0 |0|1 |1|0 |0|1 |1 |
|  1  |  1  |   0  |   1  |0 |1 |0 |1 |0 |1|0 |1|0 |1|0 |1|0 |1 |

## Funkce jedné proměnné

- **Konstanty**
    - $\mathrm {f_0 = 0}$ a $\mathrm {f_{15} = 1}$
    - Pro jakýkoliv vstup vrací stejnou hodnotu
- **Funkce YES (Buffer)**
    - $\mathrm {f_{3} = A}$ a $\mathrm {f_{5} = B}$
    - Vrací hodnotu vstupní proměnné
- **Funkce NOT**
    - $\mathrm {f_{12} = not(A)}$ a $\mathrm {f_{10} = not(B)}$
    - Vrací opak vstupní hodnoty

## Funkce dvou proměnných

### Funkce odpovídající základním operátorům

- Stejně jako v matematice, součin má přednost před součtem, při vyhodnocování výpočtu
- **Funkce OR (Logický součet)**
    - $\mathrm {f_{7} = A+B}$
    - Vrací hodnotu 1 pokud jakákoliv vstupní proměnná má hodnotu 1
- **Funkce AND (Logický součin)**
    - $\mathrm {f_{1} = A\cdot B}$
    - Vrací hodnotu 1 pokud jsou obě vstupní hodnoty rovné 1

### Další funkce dvou proměnných

- **Funkce XOR (Nonekvivalce)**
    - $\mathrm {f_{6} = A\cdot not(B) +not(A)\cdot B}$
    - Vrací hodnotu 1 když je jen jedna vstupní hodnota rovna 1
- **Funkce NOR**
    - $\mathrm {f_{8} = not(A+B) = not(A)\cdot not(B)}$
    - Vrací hodnotu jedna jen když jsou obě vstupní hodnoty rovny 0
- **Funkce NAND**
    - $\mathrm {f_{14} = not(A\cdot B)=not(A)+not(B)}$
    - Vrací hodnotu 0 pokud jsou obě vstupní hodnoty rovné 1, jinak vrací hodntu 1
- **Funkce ekvivalence**
    - $\mathrm {f_{9} = A\cdot B +not(A)\cdot not(B)}$
    - Vrací hodnotu 1 pokud se vstupní hodnoty rovnají

## Zákony Booleovy algebry

- Booleova algebra je matika s hodnotami 1 a 0

### Zákon komutativity

- $\mathrm A\cdot B=B\cdot A \\ \mathrm A+ B=B+ A$

### Zákon asociativity

- $\mathrm{A\cdot(B\cdot C)=(A\cdot B)\cdot C}\\ \mathrm{A+(B+ C)=(A+ B)+ C}$

### Zákon distribuce

- $\mathrm{A\cdot(B+C)=A\cdot B+A\cdot C}\\ \mathrm{A+(B\cdot C)=(A+ B)\cdot (A+ C)}$

### Zákon vyloučení třetí možnosti

- $\mathrm{A\cdot not(A)=0}\\ \mathrm{A+not(A)=1}$

### Zákon negace negace

- $\mathrm{not(not(A))=A}$

### Zákon agresivity hodnot

- $\mathrm{A\cdot0=0}\\ \mathrm{A+1=1}$

### Zákon neutrálnosti hodnot

- $\mathrm{A\cdot1=A}\\ \mathrm{A+0=A}$

### Zákon absorpce

- $\mathrm{A\cdot A=A}\\ \mathrm{A+A=A}\\ \mathrm{A\cdot(A+B)=A}\\ \mathrm{A+A\cdot B=A}$

### Zákon absorpce negace

- $\mathrm{A+not(A)\cdot B=A+B}\\ \mathrm{not(A)+A\cdot B=not(A)+B}$

### Zákony de Morganovy

- $\mathrm{not(A\cdot B)=not(A)+not(B)}\\ \mathrm{not(A+B)=not(A)\cdot not(B)}$

## Využití logických funkcí

- Na základě logických funkcí fungují číslicové počítač

### Příklad

- Pokud chceme ať počítač umí sčítat 2 jednobitové čísla ve dvojkové soustavě, můžeme použít logické funkce
- Pro součet dvou čísel platí  
      
    $\mathrm {0 + 0 = 0 \ (přenos \ do dalšího\ řádu\ 0)}\\ \mathrm {0 + 1 = 1 \ (přenos \ do dalšího\ řádu\ 0)}\\ \mathrm {1 + 0 = 1 \ (přenos \ do dalšího\ řádu\ 0)}\\ \mathrm {1 + 1 = 0 \ (přenos \ do dalšího\ řádu\ 1)}$
- Toto chování můžeme vytvořit pomocí funkcí AND a XOR

|A|B|AND|XOR|
|---|---|---|---|
|0|0|0|0|
|0|1|0|1|
|1|0|0|1|
|1|1|1|0|

- Funkce AND se chová jako přenos do dalšího řádu
- Funkce XOR se chová jako součet v daném řádu

## Grafické značení

- Logické funkce si lze znázornit pomoci grafického značení, kde vstupy jsou na levé straně a výstupy na pravé straně
- Tyto grafické značky se nazývají jako hradla (logic gates)
- Pomocí hradel se zakreslují logické obvody

![[Hradla-ANSI.png]]

Grafické značení logických funkcí podle normy ANSI

  

![[Hradla-IEC.png]]

Grafické znčení logických funkcí podle normy IEC

  

  

# Logické obvody

- Logické obvody se skládají z elektronických součástek (kapacitory, tranzistory atd.) a provádějí logické funkce

## Typy logických obvodů

### Kombinační

- Výstup je určen pouze okamžitými vstupními hodnotami

### Sekvenční

- Výstup je určen hodnotami na vstupech, ale i vnitřním stavem (pamětí) obvodu
-  Sekvenční obvody se mohou dělit podle řízení
    - ##### Asynchronní (neřízené)
        - Změna vstupní hodnoty se hned promítne do výstupu nebo paměti sekvenčního obvodu
    - #####  Synchronní (řízené)
        - Obvod je řízený synchronizačním signálem
        - Změna vstupní hodnoty, výstupu nebo paměti, se promítne až po příchodu synchronizačního signálu
- Dále můžeme dělit podle stability
    - #####  Astabilní
        - Obvod nemá žádný stabilní stav
        - Neustále oscilují mezi stavy 1 a 0
        - Využívají se např. jako generátor impulsů
    - #####  Monostabilní
        - Má jeden stabilní stav
        - Pokud se obvod dostane do nestabilního stavu, po chvíli vrátí se do stabilního stavu
        - Využívají se k proudložení signálu
    - #####  Bistabilní
        - Má dva stabilní stavy
        - Obvod se nachází ve stabilním stavu dokud není přepnutý vnějším impulsem
        - Využívají se jako paměťové obvody

## Parametry logických obvodů

- Zpoždění
    - Doba od změny vstupu do změny výstupní hodnoty nebo změny v paměti
- Spínací rychlost (frekvence)
- Větvení
- Úrovně signálních napětí
    - Při jaké hodnotě napětí se elektrický signál považuje jako hodnota 1 nebo 0
- Náběh a doběh impulsů
    - Ilustrace náběhu (červená) a doběhu (modrá)

		![[Nabeh-Dobeh-impulsu.png]]
		Osa x je čas, osa y je hodnota signálu

- Odolnost proti rušení
- Přípustný rozptyl napájecího napětí
    - Maximální kmitání napětí při kterém obvod správně funguje

## Příklady kombinačních logických obvodů

### Logický komparátor

- Porovnáva 2 vstupní hodnoty
- Vždy jen jeden ze tří výstupů má hodnotu 1

	![[Logicky-komparator.png]]
 Logický komparátor

### Binární sčítačka

- Sčítá 2 jednobitová čísla
- Pokud chceme sčítat vícebitová čísla, můžeme zapojit více sčítaček do sebe

	![[Binarni-scitacka.png]]

- A1 B1 jsou vstupy v řádu ve kterém sčítám
- R0 je hodnota přenášena z minulého řádu
- V1 je výstup v danném řádu
- R1 je hodnota která se přenáší do dalšího řádu

## Příkaldy sekvenčních obvodů

### Logický obvod RS

- Je to bistabilní asynchronní klopný obvod
- Uchovává informaci ikdyž na vstupu už není

	![[Logicky-obvod-RS.png]]

- S (Set) je vstup který nastavuje hodnotu, kterou si má obvod pamatovat
- R (Reset) je vstup který resetuje vnitřní paměť obvodu
- Q je výstup který ukazuje hodnotu kterou si obvod pamatuje
- $\mathrm {\overline Q}$ je negace výstupu Q
- Pravdivostní tabulka obvodu

|S|R|Qn|
|---|---|---|
|0|0|Qn-1|
|1|0|1|
|0|1|0|
|1|1|nelze|

- Qn je nynější hodnota výstupu Q
- Qn-1 je předchozí hodnota výstupu Q

### Paměťový člen D

- Je to bistabilní synchronní obvod
- Používá se jako paměťová jednotka

	![[Pametovy-clen-D.png]]

- D (Data) je vstup který určuje jaká informace se má uchovat
- C (Clock) je vstup řídícího signálu, který ukazuje zda se má informace uchovat
- Pravdivostní tabulka

|D|C|Qn|
|---|---|---|
|0|0|Qn-1|
|0|1|0|
|1|0|Qn-1|
|1|1|1|

- Qn je nynější hodnota výstupu Q
- Qn-1 je předchozí hodnota výstupu Q

# Zdroje

> [!Zdroje]  
> https://moodle.osu.cz/mod/resource/view.php?id=501118https://cs.wikipedia.org/wiki/Logická_funkcehttps://community.robotshop.com/tutorials/show/electronics-done-quick-7-logic-gateshttps://en.wikipedia.org/wiki/Logic_gatehttps://moodle.osu.cz/mod/resource/view.php?id=501123https://cs.wikipedia.org/wiki/Logický_obvodhttps://cs.wikipedia.org/wiki/Sekvenční_obvodhttps://www.desmos.com/calculator/sld6mb3ew6