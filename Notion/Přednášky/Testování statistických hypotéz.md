## Hypotéza

- Na základě nějakého výběru z populace děláme předpoklad o celé populaci (např. změřím 1000 lidí a budu mít hypotézu, že muži jsou vyšší než ženy)
- Hypotézy testujeme ať zjistíme jestli je značný rozdíl mezi hodnotami (např. jestli je Nvidia značně rychlejší než AMD)
- Testování hypotéz je nezbytnou součástí výzkumu a publikování

### Obecná hypotéza

- Předpoklad o nějakém fenoménu
- např. různé databázové systémy ovlivňují práci z databází

### Výzkumná hypotéza

- Předpoklad o náhodné [veličině](obsidian://open?vault=Obsidian-UNI&file=7STAZ%2FP%C5%99edn%C3%A1%C5%A1ky%2FVztah%20dvou%20veli%C4%8Din%2C%20pravd%C4%9Bpodobnost%2C%20n%C3%A1hodn%C3%A1%20veli%C4%8Dina)
- např. hypotéza: databázový systém Oracle má menší střední hodnotu odezvy než databázový systém SQL (lidsky řečeno - v průměru je Oracle rychlejší než SQL)

### Nulová hypotéza $H_0$

- Anglicky null hypothesis
- Zpravidla obsahuje rovnost (např. $\mathrm{H_0}$: průměrná rychlost Oracle _**=**_ průměrná rychlost SQL)
- Často se využívá ve statistických testech
- Pokud pomocí testu zamítnu nulovou hypotézu, tak platí alternativní hypotéza, která je opak nulové hypotézy (logicky: když zjistím že tam není rovnost, tak tam musí být nerovnost)

## Typy chyb

- Při testování hypotéz můžou nastat chyby, protože měříme jen nějaký výběr z populace

### Chyba prvního druhu $\alpha$

- Zamítnu nulovou hypotézu, když měla být přijata
- např. $\mathrm{H_0: člověk \ je \ nevinen}$, pak chyba prvního druhu = odsouzen nevinný člověk
- Pravděpodobnost této chyby se standardně nastavuje na 0,05

### Chyba druhého druhu $\beta$

- Příjmu nulovou hypotézu, když měla být zamítnuta
- např. $\mathrm{H_0: člověk \ je \ nevinen}$, pak chyba druhého druhu = propuštěn zločinec

## Test

- Test se vybírá podle rozdělení veličiny, kterou testujeme (normální rozdělení, exponenciální rozdělení atd.)

## Testové kritérium

- Je to hodnota vypočtená distribuční funkcí, na základě distribuce veličiny kterou testujeme
- ==Pokud je hodnota testového kritéria větší než hodnota z tabulky, pro dané rozdělení dat a počtu měření, tak zamítáme nulovou hypotézu==
- P-hodnota je pravděpodobnost že uděláme chybu když zamítneme $H_0$
- ==Když je P-hodnota menší než== ==$\alpha$== ==(0,05) tak zamítáme nulovou hypotézu==

## T-test

- Test založený na normálním (Gaussovském) rozdělení veličin
- Porovnává střední hodnoty
- Veličiny spojené s člověkem mají většinou normální rozdělení (např. výška, váha, IQ atd.)

### Jednovýběrový t-test

- Používá se pro testování že střední hodnota se rovná nějakému $\mu_0$ (např. průměrná výška se rovná 170 cm)

$$\displaylines{\mathrm{Výpočet \ testového \ kritéria} \\  
T=\frac{|\overline {x} - \mu_0|}{S}\cdot \sqrt{n} \\  
\overline {x}\to průměr \\  
\mu_0 \to hodnota \ se \ kterou \ porovnáváme \\  
S \to směrodatná \ odchylka \\  
n \to počet \ záznamů \ /\ měření}$$

- Testové kritérium porovnáme s hodnotami v tabulce (kritická hodnota t) pro t-test  
    Pokud je testové kritérium větší než kritická hodnota → zamítá se nulová hypotéza  
    

### Párový t-test

- Používá se pro měření dvou stejných naměřených hodnot stejného výběru po nějakém procesu s výběrem (např. lidi a jejich váha před a po dietě)

$$\displaylines{\mathrm{Výpočet \ testového \ kritéria} \\  
x_i=y_i-z_i \\  
y_i\to např. \ hodnota\ před \ dietou \\  
z_i\to např. \ hodnota \ po \ dietě  
\\ \ \\  
T=\frac{|\overline {x}|}{S}\cdot \sqrt{n} \\  
\overline {x}\to průměr \ z\ x_i \\  
S \to směrodatná \ odchylka \ x_i\\  
n \to počet \ záznamů \ /\ měření}$$

### Dvouvýběrový t-test

- Používá se pro porovnání stejné hodnoty u dvou různých výběrech (např. průměrná výška žen vs průměrná výška mužů)
- Postup výpočtu testovacího kritéria
    - pomocí f-testu se zjistí jestli se rovnají rozptyly dvou výběrů
    - podle toho jestli se rozptyly rovnají nebo ne, se vybere vzorec pro výpočet testovacího kritéria