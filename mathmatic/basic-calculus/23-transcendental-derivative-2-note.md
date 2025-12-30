---
id: 23-transcendental-derivative-2-note
aliases: []
tags: []
---
[[22-transcendental-derivative-1-note|삼각함수, 지수로그함수의 도함수]]

예제123
다음 함수를 미분하여라

1. $y=\sin 5x$
2. $y=e^{\sin x}$
3. $y=e^{x}\cdot \cos 2x$

123-1

$$
f'(x)=5\cdot \cos 5x
$$

123-2

$$
\cos x \cdot e^{\sin x}
$$

123-3

$$
f'(x)=e^{x}\cdot(\cos 2x) + e^{x}\cdot(-2\sin 2x)
$$

예제124
함수 $f(x)=\frac{1}{2}\cdot \sin 2x$일때,
준식 $\lim_{ x \to 0 } \frac{f(\pi-\sin x)-f(\pi)}{x}$의 값을 구하라

$$
\text{준식}=\frac{f(\pi-\sin x)-f(\pi)}{-\sin x} \cdot \frac{-\sin x}{x}
=f'(\pi) \cdot -1 = -f'(\pi)
$$

$$
f'(x)=\frac{1}{2} \cdot 2\cos 2x= \cos 2x
$$

$$
-f'(\pi)=-\cos 2\pi = -1
$$

예제125
함수 $f(x)=\ln x$일때,
GE: $\lim_{ h \to 0 } \frac{f(e+h)-f(e-h)}{h}$ 를 구하라

$$
given: f(x)=\ln x \to f'(x)=\frac{1}{x}
$$

$$
GE= \lim_{ h \to 0 } \frac{f(e+h)-f(e)}{h}-\lim_{ h \to 0 } \frac{f(e-h)-f(e)}{h \cdot-1} \cdot -1
$$

$$
=\lim_{ h \to 0 } \frac{f(e+h)-f(e)}{h}+\lim_{ h \to 0 } \frac{f(e+h)-f(e)}{-h}
$$

$$
=f'(e)+f'(e)=2f'(e)
$$

$$
2f'(e)=\frac{2}{e}
$$

예제126
$f(x)=x\cos x$일떄,
GE: $\lim_{ h \to 0 } \frac{f(\pi+2h)-f(\pi-3h)}{h}$ 의 값을 구하라

$$
GE=\lim_{ h \to 0 } \frac{f(\pi+2h)-f(\pi-3h)}{5h} \cdot 5 = 5f'(\pi)
$$

$$
f'(x)=1\cdot \cos x + -x\sin x=\cos x-x\sin x
$$

$$
f'(\pi)=\cos \pi-\pi \sin \pi=-1
$$

$$
5f'(\pi)=5\cdot-1=-5
$$

$$

$$

예제127
모든 실수 x에 대하여 미분가능한 함수 f(x)가 f'(1)=2 일떄,

$$
GE = \lim_{ x \to 0 } \frac{f(\cos 3x)-f(\cos x)}{x^{2}}
$$

GE를 구하여라

$$
GE=\lim_{ x \to 0 } \frac{f(\cos 3x)-f(\cos x)}{\cos 3x-\cos x} \cdot \frac{\cos 3x-\cos x}{x^{2}}
$$

$$
=\lim_{ x \to 0 } f'(1)\cdot \frac{\cos 3x-\cos x}{x^{2}}
$$

$$
=\lim_{ x \to 0 } 2\cdot \frac{-2 \cdot \sin 2x\cdot \sin x}{x^{2}}
$$

$$
\lim_{ x \to 0 } 2 \cdot -2 \cdot \frac{2 \cdot \sin 2x}{2x} \cdot \frac{\sin x}{x}=2\cdot(-2)\cdot 2
$$

$$
GE= -8
$$

예제128
함수 f(x)는 실수 전체에서 미분가능하고 $f(0)=2$ , $f'(0)=1$ 일때,

$$
GE=\lim_{ h \to 0 } \frac{f(h+\sin h)-a}{h}=b
$$

를 만족하는 두 상수 a,b의 합 a+b를 구하라

GE극한값이 상수b임으로 분모분자는 0/0꼴
그러므로 $a=f(0)$

$$
\lim_{ h \to 0 } \frac{f(\sin h+h)-f(0)}{h}=\lim_{ h \to 0 } \frac{f(\sin h+h)-f(0)}{\sinh+h}\cdot \frac{\sin h+h}{h}
$$

$$
f'(0)\cdot 2=1\cdot 2 = 2
$$

a=2, b=2
a+b=4

예제129

$$
GE= \lim_{ x \to e } \frac{\ln x -1}{x-e}
$$

GE=?

$$
\text{put}\ f(x)=\ln x \ , f(e)=\ln e=1\ ,f'(x)=\frac{1}{x}
$$

$$
=\lim_{ x \to e } \frac{f(x)-f(e)}{x-e}=f'(e)=\frac{1}{e}
$$

예제 130
함수 $f(x)=\ln(\tan x)$와 미분가능한 함수 g(x)의 합성함수 $h(x)=(g \circ f)(x)$ 에 대하여,
$h'\left( \frac{\pi}{4} \right)=8$ 일때, g'(0)의 값은? (단 $0 < x < \frac{\pi}{2}$)

$$
h(x)=g(f(x)), h'(x)=f'(x)\cdot g'(f(x))
$$

$$
given: h'\left( \frac{\pi}{4} \right)=8\to
h'\left( \frac{\pi}{4} \right)=f'\left( \frac{\pi}{4} \right) \cdot g'\left( f\left( \frac{\pi}{4} \right) \right)=8
$$

$$
f\left( \frac{\pi}{4} \right)=\ln\left( \tan \left( \frac{\pi}{4} \right) \right)=0
$$



$$
f'\left( \frac{\pi}{4} \right) \cdot g'(0)=8
$$

$$
f'(x)= \frac{\sec ^{2} x}{\tan x}
$$

$$
f'\left( \frac{\pi}{4} \right)= \frac{\sec ^{2} \frac{\pi}{4}}{\tan \frac{\pi}{4}}
=\frac{\frac{1}{\cos ^{2} \frac{\pi}{4}}}{1}=\frac{\frac{1}{\frac{1}{2}}}{1}=2
$$

$$
g'(0)=\frac{8}{2}=4
$$

예제 131
함수 $f(x)=\sin x-\sqrt{ 3 }\cos x -x$ 일때 $f'(\theta)=0$을 만족하는 $\theta$를 구하라 (단 $0<\theta\leq \pi$)

$$
f'(x)=\cos x+\sqrt{ 3 }\sin x-1
$$

$$
f'(\theta)=\cos\theta+\sqrt{ 3 }\sin\theta-1=0
$$

$$
\cos\theta+\sqrt{ 3 }\sin\theta=1
$$

$$
=2\sin(\theta+\alpha)=1 \ , \  \left( \tan \alpha=\frac{1}{\sqrt{ 3 }} \right)
$$

$$
=2\sin\left( \theta+\frac{\pi}{6} \right)=1
$$

$$
\sin\left( \theta+ \frac{\pi}{6} \right)=\frac{1}{2}
$$

$$
\theta+ \frac{\pi}{6}=\frac{\pi}{6}\ or\ \frac{5}{6}\pi
$$

$$
\theta=0\ or\ \frac{2}{3} \pi
$$

$$
\because 0<\theta\leq \pi
$$

$$
\therefore \theta=\frac{2}{3}\pi
$$

예제132
함수 $f(x)=e^{x}\cos x$일때 $f'(\theta)=0$을 만족하는 $\theta$를 구하라 ($0<\theta<\pi$)

$$
f'(x)=e^{x}\cdot \cos x + e^{x}\cdot -\sin x
$$

$$
f'(\theta)=e^{\theta}(\cos \theta -\sin \theta)=0
$$

$e^{\theta}$는 0보다 큰범위니까 약분하고 양변에 $\cos\theta$로 나누면

$$
=1-\tan\theta=0
$$

$$
\theta=\frac{\pi}{4}
$$

예제133
함수 $f(x)=\sin x \ (-\frac{\pi}{2}<x< \frac{\pi}{2})$ 이고 함수 g(x)는 임의의 실수 x에 대해서
g(f(x))=x 를 만족할때, $g'\left( \frac{1}{2} \right)$ 의 값을 구하라

$$
g'(x)=f'(x)\cdot g'(f(x))=1
$$

$$
g'\left( \frac{\pi}{6} \right)=f'\left( \frac{\pi}{6} \right)\cdot g'\left( \frac{1}{2} \right)=1
$$

$$
g'\left( \frac{1}{2} \right)=\frac{1}{f'\left( \frac{\pi}{6} \right)}
=\frac{1}{\frac{\sqrt{ 3 }}{2}}=\frac{2}{\sqrt{ 3 }}
$$

$$
g'\left( \frac{1}{2} \right)=\frac{2\sqrt{ 3 }}{3}
$$

예제134
미분가능한 함수 $f(x)$의 역함수 g(x)가 $\lim_{ x \to 1 } \frac{g(x)-2}{x-1}=3$을 만족할떄,
f'(2)의 값을 구하여라

$$
\lim_{ x \to 1 } \frac{g(x)-2}{x-1}=\lim_{ x \to 1 } \frac{g(x)-g(1)}{x-1}=3
$$

$$
g'(1)=3\ ,\ g(1)=2
$$

$$
f(g(x))=x
$$

$$
f'(x)=g'(x)\cdot f'(g(x))=1
$$

$$
f'(1)=g'(1)\cdot f'(2)=1
$$

$$
3\cdot f'(2)=1
$$

$$
f'(2)=\frac{1}{3}
$$
