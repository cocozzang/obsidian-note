---
id: 18-derivative-3-note
aliases: []
tags: []
---


예제 98 
다항함수 f(x)에 대하여 f'(2)=3일때 $\lim_{ x \to 2 } \frac{x^{3}-8}{f(x)-f(2)}$ 를 구하여라 
$$
\lim_{ x \to 2 } \frac{x^{3}-8}{f(x)-f(2)}=\lim_{ x \to 2 } \frac{(x-2)(x^{2}+2x+2^{2})}{f(x)-f(2)}\cdot \frac{\frac{1}{x-2}}{\frac{1}{x-2}}
$$
$$
=\lim_{ x \to 2 } \frac{x^{2}+2x+2^{2}}{\frac{f(x)-f(2)}{x-2}}=\lim_{ x \to 2 } \frac{x^{2}+2x+2^{2}}{f'(2)}
$$
$$
=\lim_{ x \to 2 } \frac{x^{2}+2x+2^{2}}{3}=\frac{4+2\cdot 2+4}{3}=\frac{12}{3}=4
$$


예제 99 
다항함수 f(x)에 대하여 f(-x)=f(x) , f'(3)=6 , f'(9)=-8 일떄,
$$
\lim_{ x \to -3 } \frac{f(x^{2})-f(9)}{f(x)-f(3)} 을 구하여라 
$$
note : 
f(x)가 우함수 이면, f(-x)=f(x) 
f'(x)는 기함수가 된다. f'(-x)=-f'(x)

$$
=\lim_{ x \to -3 } \frac{\frac{f(x^{2})-f(9)}{x^{2}-9}\cdot (x^{2}-9)}{\frac{f(x)-f(-3)}{x-(-3)}\cdot x+3}
$$
$$
=\lim_{ x \to -3 } \frac{f'(9)\cdot(x^{2}-9)}{f'(-3)\cdot (x+3)}
$$
$$
=\lim_{ x \to -3 } \frac{-8 \cdot (x-3)(x+3)}{-6 \cdot (x+3)}
$$
$$
= \frac{-8 \cdot -6}{-6} = -8
$$

예제 100 
다항함수 f(x)에 대하여 f(2)=9, f'(2)=2 일때,
$$
\lim_{ x \to 2 } \frac{\sqrt{ f(x) }-\sqrt{ f(2) }}{\sqrt{ x }-\sqrt{ 2 }} 를 구하라 
$$
$$
=lim_{ x \to 2 } \frac{f(x)-f(2)}{x-2}\cdot \frac{\sqrt{ x }+\sqrt{ 2 }}{\sqrt{ f(x)}+\sqrt{ f(2) } }
$$
$$
=\lim_{ x \to 2 } f'(2) \cdot \frac{2\sqrt{ 2 }}{3+3}
$$
$$
=2\cdot \frac{\sqrt{ 2 }}{3}
$$


예제101
$$
\lim_{ x \to a } \frac{x^{n}f(a)-a^{n}f(x)}{x-a}=na^{n-1}f(a)-a^{n}f'(a)
$$
임 을 보여라.


$$
=\lim_{ x \to a } \frac{x^{n}f(a)}{x-a}-\lim_{ x \to a } \frac{a^{n}f(x)}{x-a}
$$
$$
=\lim_{ x \to a } \frac{x^{n}f(a) - a^{n}f(a)}{x-a}-\lim_{ x \to a } \frac{a^{n}f(x)- a^{n}f(a)}{x-a}
$$
$$
=\lim_{ x \to a } \frac{x^{n}-a^{n}}{x-a}\cdot f(a)-\lim_{ x \to a } \frac{f(x)-f(a)}{x-a}\cdot a^{n}
$$
$$
=\lim_{ x \to a } \frac{\cancel{(x-a)}(x^{n-1}+ax^{n-2}+a^{2}x^{n-3}+\dots+a^{n-1})}{\cancel{x-a}} \cdot f(a) - \lim_{ x \to a } f'(a) \cdot a^{n}
$$
$$
=\lim_{ x \to a } (x^{n-1}+ax^{n-2}+a^{2}x^{n-3}+\dots+a^{n-1}) \cdot f(a)-\lim_{ x \to a } f'(a)\cdot a^{n}
$$
$$
= na^{n-1} \cdot f(a)- f'(a)\cdot a^{n}
$$

thm20 미분계수를 이용한 극한 계산
1)
$$
\lim_{ h \to 0 } \frac{f(a+mh)-f(a+nh)}{h}=(m-n)f'(a)
$$
2)
$$
\lim_{ n \to \infty } n\left\{ f\left( a+\frac{k}{n} \right)-f(a) \right\}=k\cdot f'(a)
$$

1)의 유도과정
$$
\lim_{ h \to 0 } \frac{f(a+mh)-f(a+nh)}{a+mh-(a+nh)}\times (m-n)= (m-n)\cdot f'(a)
$$

2)의 유도과정 
$$
=\lim_{ n \to \infty } n \cdot \frac{k}{n} \cdot \frac{f\left( a+\frac{k}{n} \right)-f(a)}{\frac{k}{n}}=k\cdot f'(a)
$$

예제 102
다항함수 f(x)에 대하여 f'(1)=4일때, $\lim_{ h \to 0 } \frac{f(1-3h)-f(1+4h)}{h}$를 구하여라 
$$
=\lim_{ h \to 0 } \frac{f(1-3h)-f(1+4h)}{(1-3h)-(1+4h)} \cdot \frac{(1-3h)-(1+4h)}{h}
$$
$$
\lim_{ h \to 0 } f'(1)\cdot -\frac{7h}{h}=-7f'(1)= -7 \cdot 4 = 28
$$

예제 103
다항함수 f(x)에 대하여 f'(3)=6이고 $\lim_{ h \to 0 } \frac{f(3+ph)-f(3-gh)}{h}=12$ 일때, p+g의 값을 구하라
$$
=\lim_{ h \to 0 } \frac{f(3+ph)-f(3-gh)}{(3+ph)-(3-gh)}\cdot \frac{(3-ph)-(3-gh))}{h}
$$
$$
= \lim_{ h \to 0 } f'(3) \cdot \frac{(p+g) \cancel{h}}{\cancel{h}}=12
$$
$$
=(p+g)\cdot 6=12 \;,\; p+g=2
$$

예제 104
다항함수 f(x)에 대하여 f'(a)=4일떄 $\lim_{ h \to 0 } \frac{f(a+2h)-f(a+h^{2})}{h}$ 의 값을 구하여라
$$
=\lim_{ h \to 0 } \frac{f(a+2h)-f(a+h^{2})}{(2-h)h} \cdot(2-h)
$$
$$
=2f'(a)=8
$$

예제 105
다항함수 f(x)에 대하여 
$$
\lim_{ n \to \infty } n\left\{ f\left( a+\frac{b}{n} \right)-f\left( a-\frac{b}{n} \right) \right\}
$$
의 값을 구하여라 (단 $b\neq 0$)

$$
=\lim_{ n \to \infty } n \cdot \frac{f\left( a+\frac{b}{n} \right)-f\left( a-\frac{b}{n} \right)}{\frac{2b}{n}} \cdot \frac{2b}{n}
$$
$$
=2b\cdot f'(a)
$$

예제 106
미분가능한 함수 y=f(x)의 그래프 위의 한점 P(2,1)에서의 접선의 방정식이 y=3x-5일때 
$$
\lim_{ n \to \infty } \frac{n}{2}\left\{ f\left( 2+\frac{1}{3n}\right)-f(2)  \right\}
$$
의 값을 구하여라 

위 문제의 조건에 따라 $f'(2)=3$ 임을 알수있다. (x=2에서의 접선 기울기가 3이므로)

$$
\lim_{ n \to \infty } \frac{n}{2} \cdot \frac{f\left( 2+\frac{1}{3n} \right)-f(2)}{\frac{1}{3n}}\cdot \frac{1}{3n}
$$
$$
\frac{1}{6}\cdot f'(2)= \frac{1}{6} \cdot 3 = \frac{1}{2}
$$

예제 107
함수 $f(x)=(1+x)^{100}$일떄 $\lim_{ n \to \infty }n\{ f\left( 1+\frac{1}{n} \right)-f(1) \}$ 의 값을 구하여라.
$$
=\lim_{ n \to \infty } n \cdot \frac{f\left( 1+\frac{1}{n} \right)-f(1)}{\frac{1}{n}} \cdot \frac{1}{n}
$$
$$
=\frac{n}{n} \cdot f'(1)= f'(1)
$$

$$
\because f(1)=2^{100} \;(상수) \;,\; \therefore f('1)=0
$$

위의 답은  오답임
위의 풀이의 논리적 오류는 f(1)의 결과가 상수임으로 그것을 미분한 f'(1)이 0이라는 것
f(x)=2일떄 함수 전체 그래프의 기울기가 0이므로 f'(x)=0이 되지만
$f(x)=(1+x)^{100}$ 일떈 x의 변화에 따라 각 구간의 기울기가 달라지니, f'(x)로 부터 f'(1)을 구해야함


함수 $f(x)=(1+x)^{100}$을 미분하고 준식이 f'(1)을 알아낸후 f'(x)식에 1을 대입하여 f'(1)을 구해야함
$$
f'(x)=100(1+x)^{99} \;,\; f'(1)=100\cdot 2^{99}
$$


예제 108 
함수 $f(x)=|x-2|$ 일떄, 준식  $\lim_{ h \to 0 } \frac{f(2+h)-f(2-h)}{2h}$를 구하여라 

준식은 $f'(2)$ 임을 알수있다.
$f(x)=|x-2|$ 임으로 (2,0) 지점에서 v자 그래프가 나옴
$f'(x)=\pm 1$ 
하지만 정확이 x=2지점에서의 기울기를 머라고 정의할수 있을까? 기울기가 없는 0일까?

---
정답: 위의 f(x)처럼 좌미분계수와 우미분계수가 다른 지점 또는 불연속함수의 끊어진부분을 미분불능지점이라 정의하고 해당 지점에 대한 순간기울기를 정의할수없기떄문에 미분하지 않는다.

위의문제를 단순 극한문제로 풀이하면 아래와 같다.
$$
\text{준식}=\lim_{ h \to 0 } \frac{|2+h-2|-|2-h-2|}{2h} = \frac{h-h}{2h}=0
$$
