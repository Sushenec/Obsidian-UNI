> Kolcun bude chtít vědět jenom jestli konverguje nebo n

# Správný zápis číselné řady

- Číselná řada je součet všech hodnot z posloupnosti
- Z číselné řady se pak dá udělat limita a zjistit kam se to blíží

$$\lim_{n\rarr \infin} \sum_{i=1}^{n}{a_i}  
\\ \ \\  
a_i \rarr posloupnost \\ \ \\  
\sum_{i=1}^{n}{a_i} \rarr součet \ hodnot \ posloupnosti \ od \ 1 \ do \ n. \\ n \ je \ jakékoliv \ číslo \ které \ si \ zvolím \\ \ \\  
\lim_{n\rarr \infin} \rarr n \ se \ zvětšuje \ do \ nekonečna$$

# Jak zjistit jestli číselná řada konverguje

## Základní pravidlo

- Posloupnot musí konvergovat k nule aby mohla i číselná řada konvergovat  
    takže když posloupnost nekonverguje k nule tak i číselná řada nekonverguje  
    
- např. kdyby posloupnost konvergovala k 0,1 tak číselná řada nekonverguje
- ==POZOR== - to že posloupnost konverguje k nule neznamená že číselná řada konverguje
- Pokud posloupnost konverguje k nule, tak se používají kritéria pro zjištění jestli konverguje řada

## Kritéria

- Kritéria jsou nějaké operace jenom s posloupností, které nám řeknou něco o číselné řadě
- Existuje víc kriterií než ty napsané níže, ale na test stačí jen ty napsané tady

### Podílové kritérium (d´alambert kritérium)

- Bere v potaz limitu zlomku posloupnosti a členu o 1 větší

$$\lim_{n\rarr\infin}\frac{a_{n+1}}{a_n} \rarr q$$$$q \rarr limita \ toho \ zlomku \\ \ \\  
q<1 \rarr číselná \ řada \ konverguje \\  
q>1 \rarr číselná \ řada \ nekonverguje \\  
q=1 \rarr nemůžeme \ nic \ určit$$

  

$$\Large \mathrm{Příklad} \\ \normalsize \lim_{n\rarr \infin} \sum_{i=1}^{n}{a_n} \\ \ \\  
a_n = \frac{n}{2^n}$$$$\mathrm{použití \ kritéria }\\ \ \\  
\lim_{n\rarr\infin}\frac{\frac{n+1}{2^{n+1}}}{\frac{n}{2^n}} \rarr q\\ \ \\  
\lim_{n\rarr\infin}\frac{\frac{n+1}{2^{n+1}}}{\frac{n}{2^n}}=\lim_{n\rarr\infin}\frac{(n+1)\cdot2^n}{n\cdot2^{n+1}}= \lim_{n\rarr\infin}\frac{n+1}{n}\cdot\frac{2^n}{2^{n+1}}= \\ \ \\  
=\lim_{n\rarr\infin}\frac{n+1}{n}\cdot\frac{1}{2}= \lim_{n\rarr\infin}\frac{n\cdot(1+\frac{1}{n})}{n}\cdot\frac{1}{2}=\\ \ \\  
=\lim_{n\rarr\infin}\frac{\textcolor{red}{\cancel{n}}\cdot(1+\frac{1}{n})}{\textcolor{red}{\cancel{n}}}\cdot\frac{1}{2}=\lim_{n\rarr\infin}(1+\frac{1}{n})\cdot\frac{1}{2}  
\\ \ \\  
\frac{1}{n} \ \ se \ v \ limitě \ blíží \ nule, \ takže\ zlomek \ je \ "\textcolor{green}{nula}" \\  
(1+\textcolor{green}{0})\cdot\frac{1}{2} \\ \ \\  
\lim_{n\rarr\infin}\frac{1}{2}\rarr \frac{1}{2} \\  
limita \ konstanty \ je \ konstanta$$$$q=\frac{1}{2} \\  
q<1 \rarr číselná \ řada \ konverguje$$

### Odmocninové kritérium (**Cauchyovo limitní odmocninové kritérium**)

- Hodnotí limitu n-té odmocniny z posloupnosti

$$\lim_{n\rarr\infin}\sqrt[n]{a_n} \rarr q$$$$q \rarr limita \ odmocniny \\ \ \\  
q<1 \rarr číselná \ řada \ konverguje \\  
q>1 \rarr číselná \ řada \ nekonverguje \\  
q=1 \rarr nemůžeme \ nic \ určit$$

  

$$\Large \mathrm{Příklad} \\ \normalsize \lim_{n\rarr \infin} \sum_{i=1}^{n}{a_n} \\ \ \\  
a_n = e^{\frac{1}{n}-n} \\  
e\rarr eulerovo \ číslo \approx 2.71828$$$$\mathrm{použití \ kritéria}\\ \ \\  
\lim_{n\rarr \infin} \sqrt[n]{e^{\frac{1}{n}-n}} \rarr q \\ \ \\  
\lim_{n\rarr \infin} \sqrt[n]{e^{\frac{1}{n}-n}} = \lim_{n\rarr \infin} e^{\frac{\frac{1}{n}-n}{n}}= \\ \ \\  
\lim_{n\rarr \infin}e^{\frac{\frac{1}{n}}{n}-\frac{n}{n}}=\lim_{n\rarr \infin}e^{\frac{\frac{1}{n}}{n}-1}= \lim_{n\rarr \infin}e^{\frac{1}{n^2}-1} =\\ \ \\  
\lim_{n\rarr \infin}\frac{e^{\frac{1}{n^2}}}{e} \\ \ \\  
\frac{1}{n^2} \ \ se \ bliží \ nule, \ takže \ můžeme \ nahradit \ "\textcolor{green}{nulou}" \\  
\frac{e^{\textcolor{green}{0}}}{e} \\ \ \\  
\lim_{n\rarr \infin}\frac{1}{e} \rarr \frac{1}{e} \\  
limita \ konstanty \ je \ konstanta$$$$q=\frac{1}{e} \\  
q<1 \rarr číselná \ řada \ konverguje$$