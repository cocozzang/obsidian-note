---
id: 36-extrema-4-note
aliases: []
tags: []
---

예제224
함수 $f(x)=\frac{x^{2}}{\ln x}$ 의 그래프에 대한 다음 보기의 설명 중 옳은 것을 모두 골라라
(1) f(x)는 오직 하나의 극값을 가진다
(2) $\lim_{ x \to 1 }f(x)$ 의 값은 존재하지 않는다
(3) 방정식 $\frac{x^{2}}{\ln x}=3e$ 는 서로 다른 두 실근을 가진다

(1)

$$
f'(x)=\frac{2x\ln x-x^{2} \cdot \frac{1}{x}}{(\ln x)^{2}}=0
$$

$$
x(2\ln x-1)=0
$$

$$
2\ln x-1=0
$$

$$
x=e^{\frac{1}{2}}=\sqrt{ e }
$$

$$
f(\sqrt{ e })=2e
$$

가 극점이 된다
(1)은 참이다

(2)
x의 범위는 $\frac{x^{2}}{\ln x}$ 에서 lnx는 0이 되선 안되고 진수x는 0보다 커야함으로
$0<x<1,\ 1<x<\infty$

경계값조사

$$
\lim_{ x \to 0+ } \frac{x^{2}}{\ln x}
=\frac{0}{1}
=0
$$

$$
\lim_{ x \to 1+ } \frac{x^{2}}{\ln x}
=\frac{1}{0}
=\infty
$$

$$
\lim_{ x \to -1 } \frac{x^{2}}{\ln x}
=\frac{1}{-0}
=-\infty
$$

$$
\lim_{ x \to \infty } \frac{x^{2}}{\ln x}
=\lim_{ x \to \infty } \frac{2x}{\frac{1}{x}}=
\lim_{ x \to \infty } 2x^{2}
=\infty
$$

극점과 각 경계값을 그래프에 적용하면
![exer224|300](./images/03-calculus/exercise224.png)

(2)는 참이다

(3) 그래프를 확인했을떄 (3) 또한 참이다.

예제225
구간 $[0,2\pi]$ 에서 곡선 $f(x)=e^{x}\cos x$ 가 아래로 볼록인 구간은?
(1) $\left( 0, \frac{\pi}{2} \right)$
(2) $(0,\pi)$
(3) $\left( \frac{\pi}{2}, \pi \right)$
(4) $(\pi, 2\pi)$
(5) $\left( \frac{\pi}{2}, \frac{3}{2}\pi \right)$

조건중에 f''>0인 구간은

$$
f'(x)=e^{x}\cos x+e^{x}(-\sin x)
=e^{x}(\cos x-\sin x)
$$

$$
f''(x)=e^{x}(\cos x-\sin x)+e^{x}(-\sin x-\cos x)
$$

$$
=-2e^{x}\cdot \sin x
$$

$-2e^{x}$ 는 무조건 음수임으로 $\sin x$가 음수가되는구간은
4번이다
5번은 f''>0구간과 f''<0인 구간이 모두존재함으로 제외

예제226
$x=t-\sin t,\ y=1-\cos t\ (0<t<2\pi$) 의 개형을 그려보아라

극점조사

$$
\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}= \frac{\sin t}{1-\cos t}=0
$$

$$
\sin t=0,\ t=\pi
$$

경계값조사

$$
t=\pi,\ x=\pi,\ y=2
$$

$$
t=0,\ x=0,\ y=0
$$

$$
t=2\pi,\ x=2\pi,\ y=0
$$

임으로 그래프는
![exer226|300](./images/03-calculus/exercise226.png)

Thm37 곡선의 요철판단
간단하게 요약하자면 $f''(x)$ 가 0보다 작을떄의
곡선의 성질을 이야기 하는거 같다

예제227 스킵

예제228
임의의 세 실수 a,b,c (0<a<b<c<$\pi$) 에 대하여 부등식

$$
\frac{f(b)-f(a)}{b-a}> \frac{f(c)-f(b)}{c-b}
$$

가 성립하는 함수를 보기에서 모두 골라라
(1) $f(x)=\sin x$
(2) $f(x)=\cos x-x$
(3) $f(x)=x-\ln x$

문제조건의 부등식이 성립한다는 것은 구간$x \in (0,\pi)$ 에서 함수가 극대권인지 확인하라는 의미
(위로 볼록한 함수(f''<0)를 찾는것)
(1)
sinx의 그래프를 그려보면 해당구간에서 위로 볼록하므로 (1)은 참이다

(2)

$$
f'(x)=-\sin x-1,\ f''(x)=-\cos x
$$

$$
0<x< \frac{\pi}{2} \implies \ f''<0
$$

$$
\frac{\pi}{2}<x< \pi \implies \ f''>0
$$

임으로 해당구간에서 (2)는 극대 극소권이 모두 있다 (2)는 거짓

(3)

$$
f'(x)=1+\frac{1}{x},\ f''(x)=-\frac{1}{x^{2}}
$$

모든 구간에서 $f''(x)<0$ 이므로 (3) 은 참이다

예제229
구간 $[0,2\pi]$에서 정의된 함수 $f(x)=x+2\sin x$ 의 그래프에 대한 보기의
설명 중 옳은 것을 모두 골라라
(1) $x=\frac{4}{3}\pi$에서 극솟값을 갖는다
(2) 점 ($\pi,\pi$) 은 곡선 f(x)의 변곡점이다
(3) $\frac{5}{3}\pi < x_{1}<x_{2}<2\pi$ 인 $x_{1},x_{2}$ 에 대하여
$f\left( \frac{x_{1}+x_{2}}{2} \right) > \frac{f(x_{1}+f(x_{2}))}{2}$ 이다

(1)

$$
f'(x)=1+2\cos x=0
$$

$$
\cos x=-\frac{1}{2},\ x=\frac{2}{3}\pi,\ \frac{4}{3}\pi
$$

$$
f''(x)=-2\sin x
$$

$$
f''\left( \frac{2}{3}\pi \right)<0 , (극대권)
$$

$$
f''\left( \frac{4}{3}\pi \right)>0,\ (극소권)
$$

$f'\left( \frac{4}{3}\pi \right)$=0이고 $f''\left( \frac{4}{3}\pi \right)>0$ 이므로 (1) 은 참이다

(2)
$f''(\pi)=-2\sin \pi=0$ 이므로 $x=\pi$에서 변곡점이고
변곡점의 함수값은 $f(\pi)=\pi+2\sin \pi=\pi$ 임으로 (2)는 참이다

(3)
조건은 해당구간에서 함수가 극대권에 있는지 물어보고 있다
$x \in \left( \frac{5}{3}\pi, 2\pi \right), f''(x)=-2\sin x >0$
이므로 (3) 은 거짓이다
