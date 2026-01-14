---
id: 25-differentiation-methods-1-note
aliases: []
tags: []
---

thm26 몫의 미분법, 합성함수 미분법

thm26-1 몫의 미분법 
$$
\left\{ \frac{f(x)}{g(x)} \right\}'=\frac{f'(x)g(x)-f(x)g'(x)}{g(x)^{2}}
$$

유도과정
$$
\text{put}\ F(x)=\frac{f(x)}{g(x)}
$$
$$
\left\{ \frac{f(x)}{g(x)} \right\}'=F'(x)=\lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\frac{f(x+h)}{g(x+h)}-\frac{f(x)}{g(x)}}{h}
$$

분모분자에 $g(x)\cdot g(x+h)$를 곱해주면

$$
=\lim_{ h \to 0 } \frac{f(x+h)\cdot g(x)-f(x)\cdot g(x+h)}{h} \cdot \frac{1}{g(x)\cdot g(x+h)}
$$

왼쪽분자의 각 항에 $f(x)g(x)$를 더하고 뺴주면
$$
=\lim_{ h \to 0 } \frac{f(x+h)g(x)-f(x)g(x)}{h}-\frac{f(x)g(x+h)-f(x)g(x)}{h} \cdot \frac{1}{g(x) \cdot g(x+h)}
$$

$$
=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}g(x)-\frac{g(x+h)-g(x)}{h}f(x) \cdot \frac{1}{g(x)\cdot g(x+h)}
$$

$$
=f'(x)\cdot g(x)-g'(x)\cdot f(x)\cdot \frac{1}{g(x)^{2}}
=\frac{f'(x)\cdot g(x)-g'(x)\cdot f(x)}{g(x)^{2}}
$$

$$
\left\{ \frac{f(x)}{g(x)}' \right\}=\frac{f'(x)g(x)-f(x)g'(x)}{g(x)^{2}}
$$


thm26-2 함성함수의 미분법
$$
\{f(g(x))\}'=f'(g(x))\cdot g'(x)
$$

우선 $'$프라임의 정의에 대해 다시 짚어보자
프라임은 함수의 독립변수(가장안쪽변수)에 대해 미분하라는 의미이다.
위 식에서 함수 f의 독립변수는 g(x)이지만 함수$f \circ g$ 의 독립변수는 x임으로

$\{f(g(x))\}'=\frac{df(g(x))}{dg(x)}$이 아니라 

$\{f(g(x))\}'=\frac{df(g(x))}{dx}$ 가 되게 된다

유도과정
$$
\{f(g(x))\}'=\frac{d}{dx}f(g(x))
$$

현재 d f(g(x))부분을 도함수로 표현하기 위해서
함수 f 의 독립변수인 g(x)의 차가 존재해야하기 떄문에
분모분자에 d g(x)를 곱해주면

$$
=\frac{df(g(x))}{dg(x)} \cdot \frac{dg(x)}{dx}
$$

$$
= f'(g(x)) \cdot g'(x)
$$

$$
{f(g(x))}'=f'(g(x)) \cdot g'(x)
$$


연습문제
$\{\sin ^{2}x\}'$ 
$$
\{\sin ^{2}x\}'=\{(\sin x)^{2}\}'=2\sin x \cdot \cos x = \sin 2x
$$

$\{\sec ^{3}x\}'$ 
$$
\{\sec^{3}x\}'=\{(\sec x)^{3}\}'=3\sec ^{2} x \cdot \sec x \cdot \tan x
=3\sec ^{3}x \cdot \tan x
$$

thm27 매개변수 미분법, 음함수 미분법

thm27-1 매개변수로 나타내어진 함수의 미분법
미분가능한 두함수 $x=f(t), y=g(t)$에 대하여 
$$
\frac{dy}{dx}=\frac{g'(t)}{f'(t)}
$$

유도과정
dy dx 분모분자에 dt를 나눠주면 
$$
\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}=\frac{g'(t)}{f'(t)}
$$

ex) $x=\sin\theta, y=\cos\theta 일떄, x^{2}+y^{2}=1의 \frac{dy}{dx}$ 를 구하여라
$$
\frac{dy}{dx}=\frac{(\cos\theta)'}{(\sin\theta)'} =\frac{-\sin\theta}{\cos\theta}
$$


thm27-2 음함수의 미분법
양함수 음함수 다가함수의 간단한 설명

양함수(explicit function)란, 종속변수와 독립변수들이 분리된 함수를 말한다.
독립변수가 하나일 경우, 양함수는 다음과 같은 형태가 된다.
$y=f(x)$

음함수(implicit function)는 종속변수가 독립변수와 분리되지 않은 하나의 관계식으로 주어진
함수를 말한다. 독립변수가 하나일 경우, 음함수는 다음과 같은 형태가 된다.
$F(x,y)=0$

$x^{2}+y^{2}=1$ (원의방정식) 과 같은 식도 음함수라고 부르고 아래처럼 표현가능
$F(x, y) = x^2 + y^2 - 1, \quad F(x, y) = 0$

하지만 이 음함수를 양함수로 표현하게 되면 
$y=\pm \sqrt{ 1-x^{2} }$  가 되면서
하나의 독립변수에 두개의 종속변수가 할당되게 되므로 함수에 정의에 어긋난다.

이 식은 두개의 양함수로 이루어진 것으로 볼 수 있고,
양함수로 표현하고자 할떄 아래처럼 두개의 양함수로 표현할수 있다.
$y=\sqrt{ 1-x^{2} }$   (상반원)
$y=-\sqrt{ 1-x^{2} }$   (하반원)

이런 성질을 가진 음함수를 다가함수(multivalued function)라고 부르고 함수 취급해주기도 한다.

---

음함수의 미분법
$$
\frac{d}{dx}(y^{n})=ny^{n-1} \frac{dy}{dx}=ny^{n-1}y'
$$

유도과정
$$
\frac{d}{dx}(y^{n})=\frac{d}{dy}(y^{n}) \frac{dy}{dx}=ny^{n-1}y'
$$

ex) 음함수 $2x^{2}+y^{2}=4$ 의 도함수를 구하여라

양변을 x에 관해 미분
$$
\frac{d(2x^{2})}{dx}+\frac{d(y^{2})}{dx}=\frac{d(4)}{dx}
$$

$$
4x+\frac{d(y^{2})}{dy} \frac{dy}{dx}=0
$$

$$
4x+2y\cdot y'=0
$$

$$
y'=-\frac{2x}{y}
$$

음함수 $F(1,\sqrt{ 2 })$  에서의 미분계수, 점($1,\sqrt{ 2 }$)에서의 접선의 기울기는 

$$
\frac{dy}{dx}=y'=-\frac{2x}{y} \ ,\ 
F'(1,\sqrt{ 2 })=-\frac{2\cdot 1} {\sqrt{ 2 }}=-\sqrt{ 2 }
$$

ex) $x\cdot \tan x+y^{2}=4$ 의 $\frac{dy}{dx}=?$

$$
\frac{dx}{dx} \cdot \tan x + x \cdot \frac{d(\tan x)}{dx}+ \frac{d(y^{2})}{dx}=0
$$

$$
\tan x+x \cdot \sec ^{2}x+\frac{d(y^{2})}{dy}\cdot \frac{dy}{dx}=0
$$

$$
\tan x + x\sec ^{2}x+2y\cdot \frac{dy}{dx}=0
$$

$$
\frac{dy}{dx}=-\frac{\tan x+x\sec ^{2}x}{2y}
$$

thm28 로그를 취하는 미분법 
밑과 지수 둘 모두에 독립변수가 있거나 몫에미분으로 미분하기 복잡한 분수식을 미분할떄
양변에 자연로그를 취하고 미분해준다.

$y=x^{x} \implies y'=x^{x}(\ln x +1)$  
$y=x^{\ln x} \implies y'=x^{\ln x} \cdot \frac{2\ln x}{x}$
$\{\ln |f(x)|\}'=\{\ln f(x)\}'$ 

$y=x^{x} \implies y'=x^{x}(\ln x +1)$ 유도과정

$$
y=x^{x}
$$
양변에 자연로그 취해줌
$$
\ln y=\ln x^{x}=x \ln x
$$

양변을 x에 관해 미분
$$
\frac{1}{y} \cdot y'=\ln x + x \cdot \frac{1}{x}
$$

$$
y'=y(\ln x +1)=x^{x}(\ln x+1)
$$


$y=x^{\ln x} \implies y'=x^{\ln x} \cdot \frac{2\ln x}{x}$  유도과정

$$
y=x^{\ln x}
$$

양변에 자연로그 취해줌
$$
\ln y=\ln x^{\ln x}=\ln x \cdot \ln x = (\ln x)^{2}
$$

양변 x에 관해 미분하면
$$
\frac{1}{y}\cdot y'=2\ln x \cdot \frac{1}{x}
$$

$$
y'=y\cdot \frac{2\ln x}{x}
$$

$$
y'=x^{\ln x} \frac{2\ln x}{x}
$$

$\{\ln |f(x)|\}'=\{\ln f(x)\}'$ 의 유도과정
$$
\begin{align}
f(x)>0일떄  \\
\{\ln |f(x)|\}'=\frac{f'(x)}{f(x)} \\
f(x)<0 일떄  \\
\{\ln |f(x)|\}'=\frac{-f'(x)}{-f(x)}=\frac{f'(x)}{f(x)} \\
\end{align}
$$


예제144
곡선 $\sec ^{2}(xy)=2x$ 위의 점 $(1, \frac{\pi}{4})$ 에서의 접선의 기울기를 구하여라

$$
(\sec xy)^{2}=2x
$$

양변 x로 미분하면
$$
2\sec xy \cdot (\sec xy)'=2
$$

$$
2\sec xy \cdot \sec xy \cdot \tan xy \cdot (xy)'=2
$$

(xy)'은 곱의 미분
$$
2\sec xy \cdot \sec xy \cdot \tan xy \cdot (1\cdot y+xy')=2
$$


$x=1, y= \frac{\pi}{4}$ 대입

$$
2\sec \frac{\pi}{4} \cdot \sec \frac{\pi}{4} \cdot \tan \frac{\pi}{4} \cdot \left( \frac{\pi}{4} + y' \right)=2
$$

$$
2\cdot \sqrt{ 2 } \cdot \sqrt{ 2 } \cdot 1 \cdot \left( \frac{\pi}{4} + y' \right)=2
$$

$$
\pi+4y'=2
$$

$$
y'=\frac{2-\pi}{4}= \frac{1}{2}-\frac{\pi}{4}
$$


예제145
음함수 $x+y\cos x=1$에 대하여 $x=\pi$에서의 접선의 기울기를 구하여라

양변 x로 미분
$$
1+(y'\cos x+y\cdot-\sin x)=0
$$

$x=\pi$ 대입
$$
1-y'=0
$$

$$
y'=1
$$

예제146
$f(x)=\left( \frac{1}{x} \right)^{\ln x}$ 일때 f'(e) 의 값을 구하여라

양변에 자연로그 ㅊㅊ
$$
\ln f(x)= \ln x \cdot \ln \left(\frac{1}{x} \right) =\ln x \cdot \ln x^{-1}=-(\ln x)^{2}
$$

양변 미분
$$
\frac{f'(x)}{f(x)}=-2\ln x \cdot \frac{1}{x}
$$

$$
f'(x)=-\frac{2}{x}\ln x \cdot f(x)= -\frac{2}{x}\ln x \cdot \left( \frac{1}{x} \right)^{\ln x}
$$

$$
f'(e)=-\frac{2}{e}\ln e \cdot \left( \frac{1}{e} \right)^{\ln e}
=-\frac{2}{e}\cdot 1 \cdot \frac{1}{e}
=-\frac{2}{e^{2}}
$$