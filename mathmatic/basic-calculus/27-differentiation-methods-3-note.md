---
id: 27-differentiation-methods-3-note
aliases: []
tags: []
---

예제154
모든 실수 x에 대하여 미분가능한 함수 f(x)가 $f(1-2x)=f(x),\ f'(1)=5$일때
$f'(-1)+f'(3)$의 값을 구하여라

$$
f(1-2x)=f(x) 양변 x로 미분
$$

$$
ex 1: -2f'(1-2x)=f'(x)
$$

ex1에 x=1대입하면

$$
-2f'(-1)=f'(1)=5
$$

$$
f'(-1)=-\frac{5}{2}
$$

ex1에 x=-1 대입하면

$$
-2f'(3)=f'(-1)=-\frac{5}{2}
$$

$$
f'(3)=\frac{5}{4}
$$

$$
f'(-1)+f'(3)=-\frac{5}{2}+\frac{5}{4}=-\frac{5}{4}
$$

예제155
함수

$$
f(x)=\frac{1+\sec x}{\tan x}
$$

일떄 $f'\left( \frac{\pi}{3} \right)$ 의 값을 구하여라

준식에 자연로그 취한후 미분하면

$$
\ln |f(x)|= \ln|1+\sec x| - \ln|\tan x|
$$

$$
\frac{f'(x)}{f(x)}=\frac{\sec x\tan x}{1+\sec x}-\frac{\sec ^{2}x}{\tan x}
$$

$x=\frac{\pi}{3}$ 대입

$$
\frac{f'\left( \frac{\pi}{3} \right)}{f\left( \frac{\pi}{3} \right)}
=\frac{\sec \frac{\pi}{3} \tan \frac{\pi}{3}}{1+ \sec \frac{\pi}{3}}
-\frac{\sec ^{2} \frac{\pi}{3}}{\tan \frac{\pi}{3}}
$$

$$
\frac{f'\left( \frac{\pi}{3} \right)}{f\left( \frac{\pi}{3} \right)}
=\frac{2\sqrt{ 3 }}{1+2}-\frac{4}{\sqrt{ 3 }}
=\frac{2\sqrt{ 3 }}{3}-\frac{4\sqrt{ 3 }}{3}
=-\frac{2\sqrt{ 3 }}{3}
$$

$$
f'\left( \frac{\pi}{3} \right)=-\frac{2\sqrt{ 3 }}{3}f\left( \frac{\pi}{3} \right)
=-\frac{2\sqrt{ 3 }}{3}\cdot \frac{1+2}{\sqrt{ 3 }}
=-\frac{2\sqrt{ 3 }}{3} \cdot \frac{3}{\sqrt{ 3 }}
=-2
$$


thm29  역함수의 미분법
역함수, 원함수 두 함수식 중 하나의 함수식만 명시적으로 알떄 
역함수의 미분값을 구하는 방법

미분가능한 함수 f(x)의 역함수 $y=f^{-1}(x)$가 존재하고 
미분가능할때 
$$
(f^{-1})'(x)=\frac{1}{f'(y)}
$$
이다


유도과정
우선 역함수를 원함수형태로 치환하면 dx dy가 f'(y)임을 알수있다.
$$
y=f^{-1}(x) \implies x=f(y) \implies \frac{dx}{dy}=f'(y)
$$

$$
(f^{-1})'(x)=\frac{dy}{dx}=\frac{1}{\frac{dx}{dy}}=\frac{1}{f'(y)}
$$

역함수와 원함수의 항등관계를 이용할 수도 있다.
$$
f(g(x))=x
$$

$$
f'(g(x))\cdot g'(x)=1
$$

예제156
함수 $f(x)=\tan x (-\frac{\pi}{2} < x < \frac{\pi}{2})$ 와 그 역함수 g(x)에 대하여 $g'(\sqrt{ 3 })$의 값을 구하여라


$$
\tan \frac{\pi}{3}=\sqrt{ 3 }
$$
$$
g'(\sqrt{ 3 })=\frac{1}{f'\left( \frac{\pi}{3} \right)}
$$

$$
= \frac{1}{\left( \tan \frac{\pi}{3} \right)'}
=\frac{1}{\sec ^{2} \frac{\pi}{3}}
=\frac{1}{\frac{1}{\cos ^{2} \frac{\pi}{3}}}=\frac{1}{\frac{1}{\frac{1}{4}}}
=\frac{1}{4}
$$


예제157
예제156에서 g'(x)를 x에 관한 함수로 나타내어라

$$
f(x) \implies \text{exp1: }x=\tan y \ (y=g(x))
$$

g'(x)를 구하는 두가지 방법
방법1 exp1 양변을 x로 미분(음함수 미분)
$$
1=\frac{d}{dx}\tan y
=\frac{d}{dy}\tan y \cdot \frac{dy}{dx}
=\sec ^{2}y \cdot y'
$$

$$
y'=\frac{1}{\sec ^{2}y}=\cos ^{2}y
$$
방법2 exp1 양변을 y로 미분
$$
\frac{dx}{dy}=\sec ^{2}y  \implies
\frac{dy}{dx}= \frac{1}{\sec ^{2}y}
=\cos ^{2}y
$$



$g'(x)=\cos ^{2}y$ 를 x에 관한 식으로 

$$
\because x=\tan y
$$

삼각형의 각이 y 일떄 밑변은 1, 높이는 x, 빗변$=\sqrt{ 1+x^{2} }$

$\cos ^{2}y= (\frac{1}{\sqrt{ 1+x^{2} }})^{2}$

$$
\therefore g'(x)=\frac{1}{{1+x^{2}}}
$$


예제158
함수 $f(x)=\frac{e^{x}-e^{-x}}{2}$ 일때 $(f^{-1})'(0)$ 의 값을 구하여라 

$$
(f^{-1})'(0)= \frac{1}{f'(\alpha)}\ ,\ (f(\alpha)=0) 
$$

$\alpha 가 0일때 f(0)=0$

$$
f'(x)=\frac{(e^{x}+e^{-x})}{2}
$$

$$
f'(0)=\frac{2}{2}=1
$$

$$
(f^{-1})'(0)=\frac{1}{1}=1
$$

예제159
함수 $f(x)=x^{3}+x^{2}+x+2$의 역함수 g(x)에 대하여 g'(5)의 값을 구하여라

$$
g'(5)=\frac{1}{f'(\alpha)}\ ,\ (f(\alpha)=5)
$$


$$
f(1)=5\ ,\ \alpha=1
$$

$$
f'(x)=3x^{2}+2x+1
$$

$$
f'(1)=3+2+1=6
$$

$$
g'(5)=\frac{1}{6}
$$

예제160
$$
\lim_{ x \to 1 } \frac{f(x)-1}{x-1}=3 
$$
을 만족시키는 미분가능한 함수 f(x)가 역함수 g(x)를 가질때 g'(1)의 값을 구하여라

$$
g'(1)= \frac{1}{f(\alpha)}\ ,\ (f(\alpha)=1)
$$

$given:\ f(1)=1,\ \alpha=1$ (주어진 극한식으로부터)

$$
GE=\lim_{ x \to 1 } \frac{f(x)-f(1)}{x-1}=f'(1)=3
$$

$$
g'(1)=\frac{1}{3}
$$

<다항식의 나눗셈>
예제161
다항식 $f(x)=x^{100}+ax+b$가 $(x-1)^{2}$으로 나누어 떨어질 때
$a+b$의 값을 구하여라 (단 a,b는 상수)

$$
f(x)=(x-1)^{2}\cdot g(x)+0
$$

$$
f(1)=1+a+b=0
$$

$$
b=-a-1
$$

$$
f(x)=x^{100}+ax+b
=(x-1)^{2} \cdot g(x)
$$
를 미분하면

$$
f'(x)=100x^{99}+a=2(x-1)\cdot 1 \cdot g(x)+(x-1)^{2} \cdot g'(x)
$$

$$
f'(1)=100+a=0
$$

$$
a=-100
$$

$$
b=-(-100)-1=99
$$

$$
a+b=-100+99=-1
$$

예제162
다항식 $f(x)=x^{10}+2ax+b$가 $(x-2)^{2}$으로 나누어 떨어질때 f(1)의 값을 구하여라

$$
f(x)=x^{10}+2ax+b=(x-2)^{2} \cdot g(x)
$$

$$
f(2)=2^{10}+4a+b=0
$$

$$
4a+b=-2^{10}
$$

$$
f'(x)=10x^{9}+2a=2(x-2) \cdot g(x) + (x-2)^{2} \cdot g'(x)
$$

$$
f'(2)=10\cdot 2^{9}+2a = 0
$$

$$
a=-5 \cdot 2^{9}
$$


$$
b=-2^{10}-4a=-2^{10}+20 \cdot 2^{9}=-2^{10}+10 \cdot 2^{10}=9 \cdot 2^{10}
$$

$$
f(x)=x^{10}-5\cdot 2^{10}x+9 \cdot 2^{10}
$$

$$
f(1)=1-5\cdot 2^{10} +9 \cdot 2^{10}
=1+4 \cdot 2^{10}
$$

thm30 2계도함수, n계도함수
함수 $f(x)$를 2번 미분한 것을 2계도함수라 부르고
$$f''(x),\ y''\ , \frac{d^{2}y}{dx^{2}},\ \frac{d^{2}}{dx^{2}}f(x)$$
와 같이 나타낸다


함수 $f(x)$를 n번 미분한 것을 2계도함수라 부르고
$$f^{(n)}(x),\ y^{(n)}\ , \frac{d^{n}y}{dx^{n}},\ \frac{d^{n}}{dx^{n}}f(x)$$
와 같이 나타낸다 (n은 자연수)

예제163
함수 $y=e^{x}\cdot \sin x$의 n계 도함수는 $y^{(n)}=(\sqrt{ 2 })^{n}e^{x}\sin\left( x+\frac{n\pi}{4} \right)$ 임을 
귀납적으로 보여라

n=1인 경우 성립하는가?
$$
y^{(1)}
=e^{x}\cdot \sin x + e^{x} \cdot \cos x
=e^{x}(\sin x+\cos x)
$$

$$
=e^{x}(\sqrt{ 2 }\cdot \sin (x+\alpha)), \ (\tan\alpha=1)
$$

$$
=e^{x}\left( \sqrt{ 2 }\cdot \sin \left( x+\frac{\pi}{4} \right) \right)
=\sqrt{ 2 }^{1}\cdot e^{x} \cdot \sin\left( x+\frac{1\pi}{4} \right)
$$

n=1인 경우 성립
$$
y^{(1)}
=\sqrt{ 2 }^{1}\cdot e^{x} \cdot \sin\left( x+\frac{1\pi}{4} \right)
$$



n=k인 
$$
y^{(k)}
=\sqrt{ 2 }^{k}\cdot e^{x} \cdot \sin\left( x+\frac{k\pi}{4} \right)
$$
상황에서 n=k+1인 경우에도 명제가 참인지 확인

$$
y^{(k+1)}
=\sqrt{ 2 }^{k} \left( e^{x} \cdot \sin\left( x+\frac{k\pi}{4} \right) +e^{x} \cdot \cos\left( x+ \frac{k\pi}{4} \right) \right)
$$

$$
=\sqrt{ 2 }^{k} \cdot e^{x} \left( \sin\left( x+\frac{k\pi}{4} \right)+\cos\left( x+\frac{k\pi}{4} \right) \right)
$$

$$
=\sqrt{ 2 }^{k}\cdot e^{x} \cdot \sqrt{ 2 } \cdot \sin\left( x+\frac{k\pi}{4}+\frac{\pi}{4} \right)
$$

$$
= \sqrt{ 2 }^{k+1} e^{x} \sin (x+\frac{(k+1)\pi}{4})
$$

으로 이 경우에도 예제의 명제가 성립하므로 

예제의 명제는 귀납적으로 참이라고 할 수 있다.

예제164
함수 $f(x)=e^{2x}$의 n계 도함수 $f^{(n)}(x)$에 대하여 $\Sigma^{\infty}_{n=1} \frac{e^{2}}{f^{(n)}(2)}$
의 값을 구하여라

$$
f^{(1)}=2e^{2x}
$$

$$
f^{(n)}(x)=2^{n}e^{2x}
$$

$$
f^{(n)}(x)=2^{n}e^{4}
$$

$$
GE: \Sigma^{\infty}_{n=1} \frac{e^{2}}{2^{n}e^{4}}
=\frac{1}{e^{2}} \cdot \Sigma^{\infty}_{n=1}\left( \frac{1}{2} \right)^{n}
$$

$$
=\frac{1}{e^{2}}\cdot \frac{\frac{1}{2}}{1-\frac{1}{2}}
=\frac{1}{e^{2}}
$$

예제165
함수 $f(x)=e^{2x}\cos x$의 2계 도함수 $f''(x)=0$을 만족하는 x를 $\alpha$라 할때
$\sec ^{2}\alpha$의 값을 구하여라 ($0 < \alpha < \frac{\pi}{2}$)

$$
f'(x)=2e^{2x}\cos x - e^{2x}\sin x
$$

$$
f''(x)=4e^{2x}\cos x-2e^{2x}\sin x - (2e^{2x}\sin x+e^{2x}\cos x)
$$

$$
=e^{2x}(4\cos x-2\sin x-2\sin x-\cos x)
=e^{2x}(-4\sin x+3\cos x)
$$

$$
f''(\alpha)=e^{2\alpha}(3\cos \alpha-4\sin \alpha)=0
$$

$$
4\sin\alpha=3\cos\alpha
$$

$$
4\tan\alpha=3
$$

$$
\tan\alpha=\frac{3}{4}
$$

$$
\sec ^{2}\alpha=1+\tan ^{2}\alpha
=1+\frac{9}{16}=\frac{25}{16}
$$

예제166
함수 $f(x)=\ln x$의 n계 도함수를 구하여라

$$
f^{(1)}(x)= \frac{1}{x}
$$

$$
f^{(2)}(x)=\frac{-1}{x^{2}}
$$

$$
f^{(3)}(x)
=\frac{0-(-1)2x}{x^{4}}
=\frac{1\cdot 2}{x^{3}}= \frac{2!}{x^{3}}
$$

$$
f^{(4)}(x)=\frac{0-1 \cdot 2 \cdot 3x^{2}}{x^{6}}=-\frac{3!}{x^{4}}
$$

$$
f^{(n)}(x)=\frac{(-1)^{n-1}(n-1)!}{x^{n}}
$$