analýza rozptylu, korelace, regrese, test shody

## Intervalový odhad

- odhad parametru populace na základě dat z výběru
- výsledkem je interval
- např. střední hodnota IQ je s 95% šancí <65;95>
- používá se na: populační rozptyl, střední hodnota

### Vzorec pro odhad střední hodnoty

- ==Vzorec není nutné si pamatovat==
- Výpočet určuje interval ve kterém se nachází střední hodnota
- Pravděpodobnost, se kterou se střední hodnota nachází v intervalu, se vypočítá: $1-\alpha$  
    Většinou bude 0,95, protože  
    $\alpha$ je většinou 0,05

$$\displaylines{\bigg[\overline{X}-t_{n-1}\Big(1-\frac{\alpha}{2}\Big) \cdot \frac{s}{\sqrt{n}} \ \ , \ \overline{X}+t_{n-1}\Big(1-\frac{\alpha}{2}\Big) \cdot \frac{s}{\sqrt{n}} \bigg]\\ \ }$$
$$\displaylines{\overline X \to průměrná \ hodnota \ měření \\  
n \to počet \ měření \\  
\alpha \to pravděpodobnost \ pro \ chybu \ prvního \ typu \ (většinou \ 0,05) \\  
s \to směrodatná \ odchylka \\ \ \\  
t_{n-1}\Big(1-\frac{\alpha}{2}\Big) \to hodnota \ z \ tabulky \ t-rozdělení. \\ dolní \ index \ určuje \ řádek \ v \ tabulce\\  
číslo \ v \ závorce \ určuje \ sloupce \ v \ tabulce}$$

### Vzorec pro odhad rozptylu populace

- ==Vzorec není nutné si pamatovat==
- Určuje interval ve kterém se nachází rozptyl
- Pravděpodobnost, se kterou se rozptyl nachází v intervalu, se vypočítá: $1-\alpha$  
    Většinou bude 0,95, protože  
    $\alpha$ je většinou 0,05

$$\bigg[\frac{(n-1)\cdot s^2}{X^2_{n-1}(1-\frac{\alpha}{2})} \ \ , \ \frac{(n-1)\cdot s^2}{X^2_{n-1}(\frac{\alpha}{2})}\bigg]$$
$$\displaylines{\\ \\ n \to počet \ měření \\  
s^2 \to rozptyl \ výběru\\  
\alpha \to pravděpodobnost \ pro \ chybu \ prvního \ typu \ (většinou \ 0,05) \\ \ \\  
X^2_{n-1}\Big(1-\frac{\alpha}{2}\Big) \ \ a \ \ X^2_{n-1}\Big(\frac{\alpha}{2}\Big) \to hodnota \ z \ rozdělení \ Chí-kvadrát \\  
dolní \ index \ určuje \ řádek \ v \ tabulce\\  
číslo \ v \ závorce \ určuje \ sloupce \ v \ tabulce}$$

## Test nezávislosti

- Porovnává 2 kategorické veličiny (např. vzdělání a pohlaví)
- Testuje hypotézu, že naměřené četnosti jsou stejné jako očekávané četnosti  
    (jinak řečeno: testuje hypotézu, že mezi testovanými kategorickými veličinami není žádný vztah)  
    

### Postup výpočtu

- pomocí marginálních četností se spočítají očekávané četnosti, potom se otestují s naměřenými četnostmi jestli jsou veličiny různé
- Jde to těžce popsat tady, takže je lepší se podívat na [komentář Duška](https://365osu-my.sharepoint.com/:x:/r/personal/dusema22_osu_cz/Documents/7STAZ%20-%20Du%C5%A1ek%20cvi%C4%8Den%C3%AD/Cv8_komentar.xlsx?d=w6995ba4c10b84cf387b66b4cb26d80c9&csf=1&web=1&e=DYeYAs) (list Nezávislost 2)

## Korelace (souvislost)

- toto bylo i v [[Vztah dvou veličin, pravděpodobnost, náhodná veličina]]
- oboustranná lineární závislost
- hodnotí lineární vztah dvou spojitých proměnných (bez kauzality)
- jak se pozná kauzalita (jedna veličina způsobuje druhou. např. hlasitější hudba → ztráta sluchu)
    - pomocí jedné proměnné vysvětluji druhou
    - jednu nastavuji a druhou měřím
    - jedna je fixní, druhá je zatížena náhodou variabilitou

$$\displaylines{\mathbf{\textcolor{salmon}{Toto \ není \ povinné \ se \ učit}} \\ \ \\  
covariance(X, Y) = \frac{1}{n-1} \cdot \sum^{n}_{i=1}(x_i - \bar x) \cdot (y_i - \bar y) \\  
n \to počet \ hodnot \\  
\bar x,\bar y \to průměr \ hodnot \ x \ a \ y \\  
x_i \ , y_i \to hodnoty \ na \ pozici \ i \\  
\ \\ \ \\  
correlation(X,Y) = \frac{covariance(X,Y)}{s_x \cdot s_y} \\  
s_x \ ,s_y \to směrodatná \ odchylka \ pro \ x \ a \ y}$$

### Testování pravdivosti korelačního koeficientu

- testuje hypotézu že výběrový korelační koeficient r se blíží nule

## Analýza rozptylu (ANOVA)

- Porovnává jestli střední hodnoty jsou si rovny
- je to něco jako dvouvýběrový t-test
- srovnává 2 nebo více skupin
- závislost spojité proměnné na diskrétní
    - výška obyvatel v různých oblastech (Afrika, Amerika, Austálie)
    - průměrná mzda různých povolání (kuchař, učitel, prodavačka)
- jednocestná (jednofaktorová) - jedna diskrétní veličina (dělíme lidi podle jedné veličiny)
- Nulová hypotéza je: všechny skupiny jsou si rovny
- Když zamítáme nulovou hyporétu, tak říkáme: minimálně jedna skupina je jinak

### Výstupní tabulka ANOVA

- Na testu může být otázka na zjištění informací z výstupní tabulky ANOVA

Tabulka ze skript

![[Vystup-ANOVA.png]]

$$\displaylines{\mathrm{I \to počet \ měřených \ skupin}\\  
\mathrm{n \to počet \ všech \ měření}\\  
\mathrm{F \to testovací \ kritérium}}$$

  

Tabulka z excelu

![[Vystup-ANOVA-excel.png]]

- V excelu je tabulka stejná jako ve skriptech, jen tam jsou jinak názvy
    - Mezi výběry → mezi skupinami
    - Všechny výběry → uvnitř skupin
    - SS → suma čtverců
    - Rozdíl → stupně volnosti
    - MS → střední čtverec

## Lineární regrese

- Připomíná korelaci ale není to úplně korelace
- Zjišťuje jednostannou závislost
- nastavuje se x a měří se y (např. nastavuji topení a měřím jak se bude měnit teplota)
- měří závislost y na x
- může být více vstupních veličin x a měříme jednu výslednou veličinu y
- x vysvětluje y
- např. rozloha oproti počtu obyvatel města (z rozlohy města budeme chtít predikovat počet obyvatel)
- $R^2$ je hodnota od 0 do 1, která ukazuje jak dobře model regrese predikuje skutečnost
- Lineární regrese vrací vzorec přímky, se kterou dokážeme vypočítat výstupní hodnotu y
- přímka se vkládá mezi naměřené body tak ať má ke každému bodu nejblíž