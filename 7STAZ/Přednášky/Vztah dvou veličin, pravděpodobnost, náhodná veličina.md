# Vztah dvou veličin

- Veličiny - **diskrétní** a **spojité**
- Diskrétní - data mají určené kategorie (např. známky nebo pohlaví)
- Spojité - data jsou čísla, které můžou být i desetinné (např. věk nebo cena)
- V popisné statistice se vztah dvou veličin měří třemi způsoby

1. dvě diskrétní veličin - kontingenční tabulka + sloupcový graf
2. spojitá vs. diskrétní veličina - popisné charakteristiky odděleně dle kategorií + krabicový graf
3. dvě spojité veličiny - kovariance, korelace + bodový graf

  

## Vztah dvou diskrétních veličin

- Pro znázornění se používá kontingenční tabulka a sloupcový graf
- Četnosti “sdružených typu” - počty, které nastávají současně (buňka v tabulce ukazuje např. kolik lidí jsou muži a zároveň mají ZŠ )

	![[Vztah-diskertni-diskretni.png]]

- Skupinové popisné charakteristiky

## Vztah diskrétní a spojité veličiny

- Pro znázornění se používá krabicový graf (box-plot)

	![[Vztah-diskretni-spojite.png]]

## Vztah dvou spojitých proměnných

- Pro vyjádření se používá bodový graf

	![[Vztah-spojite-spojite.png]]

### Lineární závislost

- Můžeme měřit 2 veličiny
    
    - Kovariance (Covariance) - může nabývat různých hodnot, podstatné je znaménko (není zase tak užitečná)
        - pokud je znaménko plus - pozitivní závislost (když roste veličina x roste veličina y. např. s výškou člověka roste i jeho hmotnost)
        - pokud je znaménko mínus - negativní závislost (když roste veličina x klesá veličina y. např. s růstem času stráveným v Lolku klesá chuť k životu)
        - pokud je kolem nuly tak tam není závislost (je těžké určit kdy je kovariance blízko nule, protože nabývá libovolných hodnot)
    - Korelace (Correlation) - nabývá hodnot $\mathrm{\langle -1,1 \rangle}$ (je více užitečná než kovariance)
        - pokud se korelace blíží -1, je to negativní závislost (když roste veličina x klesá veličina y. např. s růstem času stráveným v Lolku klesá chuť k životu)
        - pokud se korelace blíží 1, je to pozitivní závislost (když roste veličina x roste veličina y. např. s výškou člověka roste i jeho hmotnost)
        - pokud se korelace blíží nule, není žádná závislost
        - oproti kovarianci můžeme z hodnoty určit sílu závislosti
    
    $$\displaylines{\mathbf{\textcolor{salmon}{Toto \ není \ povinné \ se \ učit}} \\ \ \\  
    covariance(X, Y) = \frac{1}{n-1} \cdot \sum^{n}_{i=1}(x_i - \bar x) \cdot (y_i - \bar y) \\  
    n \to počet \ hodnot \\  
    \bar x,\bar y \to průměr \ hodnot \ x \ a \ y \\  
    x_i \ , y_i \to hodnoty \ na \ pozici \ i \\  
    \ \\ \ \\  
    correlation(X,Y) = \frac{covariance(X,Y)}{s_x \cdot s_y} \\  
    s_x \ ,s_y \to směrodatná \ odchylka \ pro \ x \ a \ y}$$
    

# Náhodný jev a pokus

- výskyt některých jevů uvažujeme za náhodný
- jestliže označíme jev za náhodný, pak to neznamená, že je zcela chaotický (pomoci může pravděpodobnost)
- Jeho hodnoty závisí na výsledku náhodného pokusu
- náhodný pokus - nelze předem určit výsledek, bývají nezávislé
- náhodný jev je jeden z možných (alespoň dvou) výsledků náhodného pokusu
- náhodné jevy nastávají s určitou pravděpodobností $P(X=x)$

# Pravděpodobnost $P$

- Pravděpodobnost jde zjistit 2 způsoby
    - Uděláme náhodný pokus hodně krát a zjistíme jak často je vyskytuje jev.  
        Např. hodíme kostkou hodně moc krát a zjistíme kolik krát se objeví třeba šestka  
        
    - Vypočítáme pomocí matematického výpočtu
- Je v hodnotách $\langle 0,1\rangle$
- proporce výskytů daného jevu k celkové množině náhodných jevů

$$\displaylines{P(X=x) = \frac{m}{n} \\  
P \to pravděpodobnost \\  
X=x \to další \ jev \ se \ bude \ rovnat \ x \\  
m \to počet \ výskytu \ hodnoty \ x \\  
n \to počet \ všech \ možných \ výsledků \\ \ \\ \ }$$
$$\displaylines{\mathrm{pravděpodobnost \ že \ na \ kostce \ padne \ číslo \ 5} \\  
P(X=5) = \frac{1}{6} \\  
X = 5 \to \mathrm{\ znamená \ že \ na \ kostce\ padne \ 5} \\  
m = 1 \to \mathrm{ \ číslo \ pět\ je \ na \ kostce \ jen \ 1} \\  
n = 6 \to \mathrm{\ celkový \ počet \ čísel \ na \ kostce \ je \ 6}}$$

## Jevy pravděpodobnosti

- Jev se značí velkým písmenem např. $A$
- Jev elementární (je nedělitelný, u hodu kostkou např. jev že hodím jedničku)
- Jev jistý (pravděpodobnost 1, v hodu kostkou: hodím nějaké číslo)
- Jev nemožný (pravděpodobnost 0, v hodu kostkou: hodím záporné čísla)
- Jev opačný (doplněk) $A´$ (v hodu kostkou - jev: hodím jedničku, opačný jev: nehodím jedničku)
    - výpočet $P(A)=1-P(A´)$
- Průnik jevů - nastává jev A a zároveň jev B
    - $P(A \cap B) = P(A) \cdot P(B)$
- Sjednocení jevů - nastává jev A nebo jev B (nebo oba)
    - pokud můžou nastat oba jevy zároveň (u kostek, A = padne dvojka, B = padne sudé číslo) $P(A \cup B) = P(A) +P(B) - P(A \cap B)$
    - pokud jsou neslučitelné (nemají nic společného)  
          
        $P(A \cup B) = P(A) + P(B)$

## Náhodná veličina X

- Funkce, která ohodnocuje elementární jevy reálnými čísly
- Abstraktní představa vymezuje pravidla induktivní statistiky
- Modelování rozdělení pravděpodobnosti náhodných veličin
- Na základě metod o Náhodné Veličině pak můžeme zobecňovat z výsledku výběrových na populaci

## Diskrétní náhodné veličiny

- $X \in \mathbb Z$ jevy bývají přirozená čísla (nemusí to tak být vždy)
- Rozdělení pravděpodobnosti $P_x \ \ \ P(x) = P(X=x)$
    - výčet všech hodnot a jejich pravděpodobností (např. tabulka s rozdělení pravděpodobnosti pro přežití mláďat. na řádku bude počet mláďat a pravděpodobnost přežití)
- Distribuční funkce $F_x \ \ \ F(x)$
    - pravděpodobnost že hodnota bude menší než x (např. přežije 2 a méně mláďat)
    - $F(x)$ je součet pravděpodobností všech menších hodnot než je $x$
    - $F(x) = P(X < x) = \sum_{x_i < x} P(X=x_i)$
- Střední hodnota $E(X)$
    - střední hodnota je jakoby vážený průměr pro jevy a jejich pravděpodobnosti

$$\displaylines{Střední \ hodnota \ E(X) \\  
E(X) = \sum_{i=1}^{n} x_i \cdot P(X=x_i) \\  
n \to počet \ všech \ jevů \\  
x_i \to jev \ na \ pozici \ i \\  
P(X=x_i) \to pravděpodobnost \ že \ nastane \ jev \ x_i}$$

- Rozptyl
    - idk
    - $rozptyl(X) = E(X^2)-(E(X))^2$
- Binomické rozdělení $X \  \big({{n}\atop{p}}\big)$
    - používá se když jev, který má nějakou pravděpodobnost $p$, se opakuje $n$-krát (opakování jeden na druhém nezávisí) a chceme zjistit pravděpodobnost, že nastane $k$-krát
    - $({n\atop k})\cdot p^k\cdot(1-p)^{n-k}$
    - např. kolikrát mi na ruletě padne červená, když si 10 krát vsadím

### Příklad

- Rozdělení pravděpodobnosti přežívání mláďat

|xᵢ (kolik jich přežije)|P(xᵢ)=P(X=xᵢ)|F(xᵢ)=P(X<xᵢ)|
|---|---|---|
|0|0,2|0,2|
|1|0,4|0,6|
|2|0,3|0,9|
|3|0,1|1,0|

$$\displaylines{\mathrm{Výpočet \ střední \ hodnoty} \\  
E(X) = 0\cdot0,2 + 1\cdot 0,4 + 2\cdot0,3 + 3\cdot0,1 = 1,3 \\  
\ \\  
\mathrm{Takže \ "průměrně" \ přežije \ 1,3 \ mláďat}\\ \ \\ \ }$$
$$\displaylines{\mathrm{Výpočet \ rozptylu} \\  
rozptyl(X)=E(X^2)-(E(X))^2 \\  
E(X^2) = 0^2\cdot0,2 + 1^2\cdot0,4 + 2^2\cdot0,3 + 3^2\cdot0,1 = 2,5 \\  
(E(X))^2 = (0\cdot0,2 + 1\cdot 0,4 + 2\cdot0,3 + 3\cdot0,1)^2 = 1,3^2 = 1,69 \\  
rozptyl(X) = 2,5-1,69 = 0,81 \\ \ \\  
\mathrm{rozptyl \ je \ 0,81}}$$

### Příklad

- Chci zjistit jaká je pravděpodobnost, že když budu na ruletě vsázet, tak mi z 10 zatočení padne červená

$$\displaylines{\mathrm{Výpočet \ binomického \ rozvoje} \\ \ \\  
pravděpodobnost \ že \ po \ 1 \ zatočení \ padne \ červená \to p = 0,486 \\  
celkový \ počet \ zatočení \to n = 10 \\  
kolikrát \ chceme \ ať \ to \ padne \to k=5 \\ \ \\  
\Big( {10 \atop 5}\Big)\cdot 0,486^5 \cdot (1-0,486)^{10-5} = \\ = 252 \cdot 0,027113235502176 \cdot 0,035876956577824 \\ = 0,245130573944562880660466946048 \\ \ \\  
\mathrm{pravděpodobnost, \ že \ při \ 10 \ zatočení \ padne \ 5 \ krát \ červená, \ je \ 0,245130574}}$$

## Spojitá náhodná veličina