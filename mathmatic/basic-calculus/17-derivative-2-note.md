---
id: 17-derivative-2-note
aliases: []
tags: []
---

예제89)
함수 $f(x)=x^{3}-2x+1$ 에 대하여 구간 $[1,a]  단 (a>1)$ 에서의 평균변화율이 5일때 상수 a의 값을 구하여라

$$
\frac{f(a)-f(1)}{a-1}=5
$$

$$
=\frac{a^{3}-2a+1-(1^{3}-2\cdot1+1)}{a-1}=5
$$

$$
=\frac{a^{3}-2a+1-0}{a-1}=\frac{(a-1)(a^{2}+a-1)}{a-1}=a^{2}+a-1=5
$$

$$
a^{2}+a-6=0
$$

$$
(a+3)(a-2)=0
$$

$$
\because a > 1 \; \therefore a = 2
$$

예제90)
자연수 n에 대하여 구간 $[n,n+1]$에서 함수 y=f(x)의 평균변화율은 n+1 이다. 이때 함수 y=f(x)의 구간 1,100 에서의 평균변화율을 구하시오

$$
\frac{f(n+1)-f(n)}{n+1-n}=n+1
$$

$$
f(n+1)-f(n)=n+1
$$

$$
\text{equation1} \to f(100)-f(99)=99+1
$$

$$
f(99)-f(98)= 98 +1
$$

$$
\dots
$$

$$
\text{equation99} \to f(2)-f(1)=1+1
$$

equation1부터 99까지 모두 더하면 망원급수로 f(100)-f(1) 에 대한 식을 얻을수있다.

$$
f(100)-f(1)=\frac{102\times99}{2}
$$

함수 f(x)의 구간 1~100에 대한 평균 변화율은 아래와 같다.

$$
\frac{f(100)-f(1)}{100-1}= \frac{102\times 99}{99 \times 2}=\frac{102}{2} = 51
$$

예제91)

$$
\lim_{ h \to 0 } \frac{f(1+2h)-f(1)}{h}=\lim_{ h \to 0 } 2\frac{f(1+2h)-f(1)}{2h}=2f'(1)=2 \cdot (4\cdot 1^{3}+8\cdot 1)=12 \times 2 = 24
$$

예제92)

$$
\lim_{ h \to 0 } \frac{g(h)}{h} = ?
$$

$$
f'(a)=2
$$

$$
\lim_{ h \to 0 } \frac{f(a+2h)-f(a)-g(h)}{h}=0
$$

$$
\lim_{ h \to 0 }  \frac{g(h)}{h}=\lim_{ h \to 0 } \frac{f(a+2h)-f(a)}{h}
$$

$$
=2f'(a)=4
$$

예제93)

$$
\lim_{ x \to 3 } \frac{f(x)-2}{x-3}=1
$$

$$
\lim_{ x \to 3 } \frac{g(x)-1}{x-3}=2
$$

위 두 식의 값이 유한확정한 값이므로 f(3)=2, g(3)=1 임을 알수있다.

$$
y=f(x)g(x) \;,\; y'=f'(x)g(x)+f(x)g'(x)
$$

$$
y'_{x=3}=f'(3)g(3)+f(3)g'(3)
$$

$$
\lim_{ x \to 3 } \frac{f(x)-2}{x-3}=\lim_{ x \to 3 } \frac{f(x)-f(3)}{x-3}=f'(3)=1
$$

$$
\lim_{ x \to 3 } \frac{g(x)-g(3)}{x-3}=g'(3)=2
$$

$$
y'_{x=3} = 1 \cdot 1 + 2 \cdot 2 = 5
$$

예제94)
아래조건 을 만족할떄
g'(0) = ?
$f(0)=1 \;,\; f'(0)=-6 \;,\; g(0)=4$
$\lim_{ x \to 0 } \frac{f(x)g(x)-4}{x}=0$

$$
\text{put} \; F(x)=f(x)g(x) \; , F'(x)=f'(x)g(x)+f(x)g'(x)
$$

$$
\lim_{ x \to 0 } \frac{F(x)-F(0)}{x}=0=F'(0)
$$

$$
F'(0)=f'(0)g(0)+f(0)g'(0)= -6 \cdot 4 + 1 \cdot g'(0)=0
$$

$$
\therefore g'(0)=24
$$

예제95)
note: 지수함수의 미분 (지수미분 x 원형 x ln 밑)
$(a^{x})'=a^{x}\cdot \ln a$
$(a^{f(x)})'= f'(x)\cdot a^{f(x)}\cdot \ln a$
$(2^{10x})'=10\cdot 2^{10x}\cdot \ln a$

$$
\lim_{ x \to 0 } \frac{2^{x}+2^{2x}+2^{3x}+\dots+2^{10x}-10}{x}
$$

$$
\text{put} \; F(x)=2^{x}+2^{2x}\dots +2^{10x}
$$

$$
\lim_{ x \to 0 } \frac{F(x)-F(0)}{x}= F'(0)
$$

$$
F'(0)=2^{x}\cdot \ln 2 + 2 \cdot 2^{2x} \cdot \ln 2+ 3\cdot 2^{3x} \cdot \ln 2 \dots + 10 \cdot 2^{10x} \cdot \ln 2
$$

$$
= \ln 2(1+2+3+\dots+10) = 55 \cdot \ln 2
$$

예제 96)
다항함수 f(x)에 대하여 $lim_{x\to2}\frac{f(x)-8}{x^2-4}=10$ 일때, $f(2)+f'(2)$의 값은?

$$\lim_{x\to2}\frac{f(x)-8}{x^2-4}=10$$

$$put \; f(2)=8$$

$$\lim_{x\to2}\frac{f(x)-f(2)}{(x+2)(x-2)}=\lim_{x\to2}\frac{f(x)-f(2)}{(x-2)}\cdot\frac{1}{(x+2)}$$

$$\frac{1}{4}\cdot f'(2)=10$$
$$f'(2)=40 \;,\; f(2)=8$$
$$\therefore f(2)+f'(2)=48$$

예제97)
다항함수 f(x)에 대하여 $\lim_{x\to a}\frac{f(x^3)-f(a^3)}{x-a}$ 을 구하여라

준식 분모분자에 (x^2+ax+a^2)을 곱하면
$$\lim_{x \to a}\frac{f(x^3)-f(a^3)}{(x-a)\cdot(x^2+ax+a^2)}\cdot(x^2+ax+a^2)$$

$$=3a^2\cdot f'(a^3)$$
