1

$$\lim_{n\rarr\infin}\Bigg(1+\frac{4}{n^2+4n+4}\Bigg)^{n^2} =\ ?$$$$\lim_{n\rarr\infin}\bigg(1+\frac{4}{n^2+4n+4}\bigg) \approx \lim_{n\rarr\infin}\bigg(1+\frac{4}{n^2}\bigg)$$$$Podle \ vzorce :\\  
\lim_{n\rarr\infin}\bigg(1+\frac{x}{a_n}\bigg)^{a_n}= e^x \\ \ \\  
\lim_{n\rarr\infin}\bigg(1+\frac{4}{n^2}\bigg)^{n^2} = e^4$$

---

2

$$\lim_{n\rarr\infin}\bigg(1+\frac{2n}{400n+9}\bigg)^{\frac{400n+9}{2n}}= \ ?$$$$\lim_{n\rarr\infin}\bigg(1+\frac{2n}{400n+9}\bigg)^{\frac{400n+9}{2n}}=\lim_{n\rarr\infin} \bigg(1+\frac{1}{(400n+9)\cdot(2n)^{-1}}\bigg)^{(400n+9)\cdot(2n)^{-1}}$$$$Podle \ vzorce \ : \\  
\lim_{n\rarr\infin}\bigg(1+\frac{1}{a_n}\bigg)^{a_n}=e \\  
\lim_{n\rarr\infin} \bigg(1+\frac{1}{(400n+9)\cdot(2n)^{-1}}\bigg)^{(400n+9)\cdot(2n)^{-1}} = e$$

---

3

$$\lim_{n\rarr\infin}\bigg(\frac{2n^2+5n+1}{3n^3+4n+2}+1\bigg)=\ ?$$$$\lim_{n\rarr\infin}\bigg(\frac{2n^2+5n+1}{3n^3+4n+2}+1\bigg)=\lim_{n\rarr\infin}  
\bigg(\frac{n^2\cdot(2+\frac{5}{n}+\frac{1}{n^2})}{n^3\cdot(3+\frac{4}{n^2}+\frac{2}{n^3})}+1\bigg)= \\ \ \\=  
\lim_{n\rarr\infin}\bigg(\frac{\textcolor{red}{\cancel{n^2}}\cdot(2+\frac{5}{n}+\frac{1}{n^2})}{n^{\textcolor{red}{\cancel{3}}}\cdot(3+\frac{4}{n^2}+\frac{2}{n^3})}+1\bigg)=  
\lim_{n\rarr\infin}\bigg(\frac{2+\frac{5}{n}+\frac{1}{n^2}}{n^3\cdot(3+\frac{4}{n^2}+\frac{2}{n})}+1\bigg)$$$$\frac{5}{n} \ ;\frac{1}{n} \ ; \frac{4}{n^2} \ ; \frac{2}{n} \ \ tyhle\ 4 \ se \ limitně \ blíží \ nule$$$$\bigg(\frac{\lim_{n\rarr\infin}\big(2+\frac{5}{n}+\frac{1}{n^2}\big)}{\lim_{n\rarr\infin}(n^3)\cdot\lim_{n\rarr\infin}(3+\frac{4}{n^2}+\frac{2}{n})}+\lim_{n\rarr\infin}(1)\bigg)=  
\bigg(\frac{2}{\lim_{n\rarr\infin}(n^3)\cdot3}+1\bigg) = \\ \ \\  
\lim_{n\rarr\infin}\bigg(\frac{2}{3n^3}+1\bigg) = 1$$

ty poslední kroky používají toto

vynásobení posloupnosti v limitě, je to stejné co vynásobení limity

![[image 10.png]]

---

4 (ten důkaz ohraničení a monotónosti tam asi nebude chtít)

$$a_n=\sqrt{4+a_{n-1}} \\  
\lim_{n\rarr\infin}a_n = \ ?$$

Když má posloupnost ohraničení a je monotóní, tak má limitu

Trochu lidsky: Když posloupnost roste a má ohraničení shora, nebo když posloupnost klesá a má ohraničení zdola, tak potom má posloupnost určitě limitu

$$\large ohraničení \ shora \\ \ \\  
\normalsize ohraniření \ jde \ dokázat \ indukcí: \\  
Nechť \ a_n < 4\cdot\sqrt{4} \\  
potom \\  
a_{n+1}=\sqrt{4+a_n}\\  
\sqrt{4+a_n}<\sqrt{4+4\cdot\sqrt{4}} \\  
\sqrt{4+4\cdot\sqrt{4}} = \sqrt{4\cdot\big(1+\sqrt{4} \ \big)} = \sqrt{4}\cdot\sqrt{1+\sqrt{4}} \\  
\sqrt{4}\cdot\sqrt{1+\sqrt{4}} < 4\cdot\sqrt{4} \\  
z \ toho \ vyplývá \ že \ každé \ a_n \ je \ menší \ než \ 4\cdot\sqrt{4} \\  
takže \ a_n \ je \ ohraničené \ shora$$$$\large růst \\  
\normalsize  
když \ si \ vypíšeme \ první \ členy: \\  
a_1 = \sqrt{2}, \ \ a_2=\sqrt{2+\sqrt{2}}, \ \ a_3=\sqrt{2+\sqrt{2+\sqrt{2}}} \\  
je \ jasné \ že \ posloupnost\ je \ rostoucí$$

teď víme že posloupnost má limitu

$$když \ víme \ že \ posloupnost \ a_n=\sqrt{4+a_{n-1}} \ má \ limitu, \\ tak \ musí \ platit\ \alpha=\sqrt{4+\alpha} \ \ (\alpha \ je\ limita )\\ \ \\  
\alpha=\sqrt{4+\alpha}\\  
\alpha^2=4+\alpha\\  
\alpha^2-\alpha-4=0 \\ \ \\  
x_{1,2}= \frac{-b\pm\sqrt{b^2-4ac}}{2a} \\ \ \\  
x_1=\frac{1-\sqrt{(-1)^2+16}}{2}=\frac{1-\sqrt{17}}{2}\\ \ \\  
x_2=\frac{1+\sqrt{(-1)^2+16}}{2}=\frac{1+\sqrt{17}}{2}$$$$protože \ \frac{1-\sqrt{17}}{2} < 0 \\ \ \\  
a_n=\sqrt{4+a_{n-1}} \\  
\lim_{n\rarr\infin}a_n = \frac{1+\sqrt{17}}{2}$$