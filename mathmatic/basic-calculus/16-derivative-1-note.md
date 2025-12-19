---
id: 16-derivative-1-note
aliases: []
tags: []
---

$$
\lim_{ b \to a } \frac{f(b)-f(a)}{b-a} = \lim_{ \Delta x \to 0 } \frac{f(a+\Delta x)-f(a)}{\Delta x} = f'(a)
$$

$$
\lim_{ \Delta x \to 0 } \frac{f(x+\Delta x)-f(x)}{\Delta x} = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} = f'(x)
$$

유도과정 예시

$f(x)=x^{2}, f'(x)=2x \; 의 유도과정$

$$
f(x)=x^2 \to f'(x)=2x
$$

$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}=\lim_{ h \to 0 } \frac{(x+h)^2-x^2}{h}
$$

$$
=\lim_{ h \to 0 } \frac{x^{2}+2xh+h^{2}-x^{2}}{h}=\lim_{ h \to 0 } \frac{2xh}{h}+\frac{h^{2}}{h}=2x
$$

$f(x)=\sin x \to f'(x)=\cos x 의 유도과정$

$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}=\lim_{ h \to 0 } \frac{\sin (x+h)-\sin x}{h}
$$

$$
\lim_{ h \to 0 } \frac{2{\cos\left( \frac{x+h+x}{2} \right)}\sin\left( \frac{h}{2} \right)}{h}=\lim_{ h \to 0 } \frac{2}{h} \cdot \cos\left( \frac{2x}{2}+\frac{h}{2} \right)\cdot \sin\left( \frac{h}{2} \right)
$$

$$
= \lim_{ h \to 0 } \cos x \cdot \frac{\sin\left( \frac{h}{2} \right)}{\frac{h}{2}}=\cos x \cdot 1 = \cos x
$$

$$
\therefore f(x)=\sin x \;,\; f'(x)=\cos x
$$

미분법 공식

1. $y=c \to y'=0$
2. $y=x^n  \to y'=nx^{n-1}$
3. $y=f(x)g(x) \to y'=f'(x)g(x)+f(x)g'(x)$
4. $y={f(x)}^n \to y'=n{f(x)}n-1$

1)의 유도과정 $y=c\to y'=0$

$$
f(x)=c 일떄,
$$

$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)}{h}=\frac{c- c}{h}=\frac{0}{h}=0
$$

**c-c는 0이고 h는 극한값이 0이라 결과는 0이다.**

2)의 유도과정 $y=x^{n} \to y'=nx^{n-1}$
일반화된 합차공식
$a^{n}-b^{n}=(a-b)(a^{n-1}+a^{n-2}\cdot b+a^{n-3}\cdot b^{2}\dots b^{n-1})$
$a^{2}-b^{2}=(a-b)(a+b)$
$a^{3}-b^{3}=(a-b)(a^{2}+ab+b^{2})$

$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}=\lim_{ h \to 0 } \frac{(x+h)^{n}-x^{n}}{h}
$$

$$
=\lim_{ h \to 0 } \frac{h((x+h)^{n-1}+(x+h)^{n-2}\cdot x+(x+h)^{n-3}\cdot x^{2})\dots x^{n-1})}{h}
$$

$$
=\lim_{ h \to 0 } (x+h)^{n-1}+(x+h)^{n-2}\cdot x+(x+h)^{n-3}\cdot x^{2}\dots +x^{n-1}
$$

$$
=\lim_{ h \to 0 } (x+h)^{n-1}+(x+h)^{n-2}\cdot x+(x+h)^{n-3}\cdot x^{2}\dots +x^{n-1}
$$

$$
=(x+0)^{n-1}+(x+0)^{n-2}\cdot x+(x+0)^{n-3}\cdot x^{2}\dots +x^{n-1}
$$

$$
=(x)^{n-1}+(x)^{n-2}\cdot x+x^{n-3}\cdot x^{2}\dots +x^{n-1}=nx^{n-1}
$$

$$
\therefore f(x)=x^{n} \;,\; f'(x)=nx(n-1)
$$

3)의 유도과정 $y=f(x)g(x) \to y'=f'(x)g(x)+f(x)g'(x)$

$$
\text{put}\;F(x)=f(x)g(x)
$$

$$
\lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h}=\lim_{ h \to 0 } \frac{f(x+h)\cdot g(x+h)-f(x)\cdot g(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{f(x+h)\cdot g(x+h)}{h}-\lim_{ h \to 0 } \frac{f(x)g(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{f(x+h)\cdot g(x+h)-g(x+h)f(x)}{h}-\lim_{ h \to 0 } \frac{f(x)g(x)-g(x+h)f(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}\cdot g(x+h) - \lim_{ h \to 0 } \frac{g(x)-g(x+h)}{h}\cdot f(x)
$$

$$
=f'(x)\cdot g(x)+g'(x)\cdot f(x)
$$

4)의 유도과정 $y=\\{f(x)}^{n} \to y'=n\\{f(x)}^{n-1} \cdot f'(x)$

$$
\text{put}\;F(x)=f(x)^{n}
$$

$$
F'(x)=\lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h}=\lim_{ h \to 0 } \frac{f(x+h)^{n}-f(x)^{n}}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\{ f(x+h)-f(x) \}\{f(x+h)^{n-1}+f(x+h)^{n-2}\cdot f(x)+f(x+h)^{n-3}\cdot f(x)^{2}\dots f(x)^{n-1}\}}{h}
$$

$$
= f'(x) \cdot \{f(x+0)^{n-1}+f(x+0)^{n-2}\cdot f(x)+f(x+0)^{n-3}\cdot f(x)^{2}\dots f(x)^{n-1}\}
$$

$$
=nf(x)^{n-1} \cdot f'(x)
$$
