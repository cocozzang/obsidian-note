---
id: 26-differentiation-methods-2-note
aliases: []
tags: []
---

예제147

$$
\begin{cases}
x=e^{t}+e^{-t} \\
y=e^{t}-e^{-t}
\end{cases}
$$

일때 $\frac{d^{2}y}{dx^{2}}$ 를 구하여라

$$
\frac{dy}{dx}=\frac{\frac{dy}{dt}}{\frac{dx}{dt}}
=\frac{e^{t}+e^{-t}}{e^{t}-e^{-t}}
=\frac{x}{y}
$$

$\frac{dy}{dx}$를 한번 더 미분해주면 몫의 미분인듯

$$
\frac{d^{2}y}{dx^{2}}
=\frac{d}{dx}\left( \frac{dy}{dx} \right)
=\frac{d}{dx}\left( \frac{x}{y} \right)
=\frac{1\cdot y-x\cdot y'}{y^{2}}
$$

$$
=\frac{y-\frac{x^{2}}{y}}{y^{2}}
=\frac{y^{2}-x^{2}}{y^{3}}
$$

예제148
함수 $f(x)=x^{\sin x}\ , (x>0)$ 에 대하여

$$
\lim_{ h \to 0 } \frac{f\left( \frac{\pi}{2}+2h \right)-f\left( \frac{\pi}{2} \right)}{h}
$$

의 값을 구하여라

$$
GE=\lim_{ h \to 0 } \frac{f\left( \frac{\pi}{2}+2h \right)-f\left( \frac{\pi}{2} \right)}{2h} \cdot 2
=2f'\left( \frac{\pi}{2} \right)
$$

함수식 f(x)를 양변 로그 ㅊㅊ

$$
\ln f(x)=\sin x \ln x
$$

양변 미분

$$
\frac{f'(x)}{f(x)}=\cos x \cdot \ln x + \sin x \cdot \frac{1}{x}
$$

$$
f'(x)=f(x)\cdot\left( \cos x\cdot \ln x + \frac{\sin x}{x} \right)
$$

$$
2f'\left( \frac{\pi}{2} \right)
=2\left(\frac{\pi}{2}\right)^{\sin \frac{\pi}{2}}\left( \cos \frac{\pi}{2}\cdot \ln \frac{\pi}{2} + \frac{\sin \frac{\pi}{2}}{\frac{\pi}{2}} \right)
$$

$$
=2 \cdot \frac{\pi}{2} \cdot \frac{2}{\pi}=2
$$

$$
2f'\left( \frac{\pi}{2} \right)=2
$$

예제149
함수 $f(x)=e^{3x}+\cos x$와 실수 전체에서 미분가능한 두 함수 g(x), h(x)가 있다
합성함수 $P(x)=(h \circ g \circ f)(x)$에 대해 P'(0)=12 일때 $(h \circ g)'(2)$의 값을 구하여라

$$
P'(x)=h'(g(f(x))) \cdot g'(f(x)) \cdot f'(x)
$$

f(x)는 2겠지? 2여야 답이 풀릴듯?

$$
f'(x)=3e^{3x}-\sin x
$$

$$
f'(0)=3-0=3
$$

$$
f(0)=2
$$

$$
P'(0)=h'(g(f(0))) \cdot g'(f(0)) \cdot f'(0)
$$

$$
=h'(g(2)) \cdot g'(2)\cdot 3 = 12
$$

$$
h'(g(2)) \cdot g'(2)=4
$$

$$
\because (h \circ g)'(2)=h'(g(2)) \cdot g'(2)
$$

$$
\therefore (h \circ g)'(2)=4
$$

예제150
곡선 $x=\theta-\sin\theta, y=1-\cos\theta$에 대하여
기울기가 1인 접선의 y절편을 구하여라 (단 $0< \theta < \pi$)

$$
\frac{dy}{dx}=\frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}}
=\frac{\sin\theta}{1-\cos\theta}
$$

$\theta$가 $\frac{\pi}{2}$ 일떄 곡선의 접선기울기는 1이 된다 (식이 간단해서 직관적으로 알수있다.)

접점은

$$
x=\frac{\pi}{2}-\sin \frac{\pi}{2}, y=1-\cos \frac{\pi}{2}
$$

$$
x=\frac{\pi}{2}-1\ ,\ y=1
$$

기울기가 1이며 점 $( \frac{\pi}{2} -1,1)$ 을 지나는 직선의 y절편은 양점에 $\frac{\pi}{2}-1$ 만큼 뺴주면 될듯

$$
점 \left( \frac{\pi}{2}-1-\left( \frac{\pi}{2}-1 \right),1-\left( \frac{\pi}{2} -1\right) \right)=\left( 0,-\frac{\pi}{2}+2 \right)
$$

강의상의 문제풀이

$$
\frac{dy}{dx}=\frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}}
=\frac{\sin\theta}{1-\cos\theta}=1
$$

$$
\sin \theta=1-\cos\theta
$$

$$
\sin\theta+\cos\theta=1
$$

$$
\tan \alpha=\frac{1}{1},\ \alpha=\frac{\pi}{4}
$$

$$
\sqrt{ 2 }\sin \left( \theta+\frac{\pi}{4} \right)=1
$$

$$
\sin\left( \theta+\frac{\pi}{4} \right)=\frac{1}{\sqrt{ 2 }}
$$

$$
\theta+\frac{\pi}{4}=\frac{\pi}{4} or \frac{3}{4}\pi
$$

$$
\theta=0\ or\ \frac{\pi}{2}
$$

$$
given: (0 < \theta < \pi)
$$

$$
\therefore \theta=\frac{\pi}{2}
$$

식 x,y에 $\theta=\frac{\pi}{2}$를 대입하면

$$
x=\frac{\pi}{2}-1,\ y=1
$$

접선y의 식은

$$
y-1=1\cdot\left( x-\frac{\pi}{2}+1 \right)
$$

$$
y=x-\frac{\pi}{2}+2
$$

$$
y절편=2-\frac{\pi}{2}
$$

예제151

$$
x=\cos ^{3}\theta,\ y=\sin ^{3}\theta 일때 \left[ \frac{d^{2}y}{dx^{2}} \right]_{\theta=\frac{\pi}{4}}
$$

의 값을 구하여라

$$
\frac{dy}{dx}
=\frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}}
=\frac{3\sin ^{2}\theta \cdot \cos\theta}{3\cos ^{2}\theta \cdot -\sin\theta}
=-\frac{3\sin ^{2}\theta \cos\theta}{3\cos ^{2}\theta \sin\theta}
=-\frac{\sin\theta}{\cos\theta}
=-\tan\theta
$$

$$
\frac{d^{2}y}{dx^{2}}
=\frac{d}{dx}(-\tan\theta)
=\frac{d}{d\theta}(-\tan\theta) \cdot \frac{d\theta}{dx}
$$

$\frac{d\theta}{dx}$는 $\frac{dx}{d\theta}$ 의 역수임으로

$$
=-\sec ^{2}\theta \cdot -\frac{1}{3\cos ^{2}\theta \sin\theta}
$$

$$
\frac{d^{2}y}{dx^{2}}
=\sec ^{2}\theta \cdot \frac{1}{3\cos ^{2}\theta \sin\theta}
$$

$$
\left[ \frac{d^{2}y}{dx^{2}} \right]_{\theta=\frac{\pi}{4}}
=\sec^{2} \frac{\pi}{4} \cdot \frac{1}{3\cos ^{2} \frac{\pi}{4} \sin \frac{\pi}{4}}
$$

$$
=2 \cdot \frac{1}{3\cdot \frac{1}{2} \cdot \frac{1}{\sqrt{ 2 }}}
=2 \cdot \frac{2\sqrt{ 2 }}{3}
=\frac{4\sqrt{ 2 }}{3}
$$

예제152
함수

$$
f(x)= \frac{(x-1)^{3}}{x^{3}+x^{2}}
$$

일때 f'(2) 의 값을 구하여라

$$
f'(x)
=\frac{3(x-1)^{2} \cdot 1 \cdot (x^{3}+x^{2})-((x-1)^{3} \cdot 3x^{2}+2x)} {(x^{3}+x^{2})^{2}}
$$

$$
f'(2)=\frac{3\cdot 12 - (12+4)}{12^{2}}
=\frac{36-16}{12^{2}}
=\frac{20}{12\times 12}
=\frac{5}{12\times 3}
=\frac{5}{36}
$$

예제153
함수

$$
f(x)=\frac{x^{6}(x-1)^{5}(x-2)^{4}}{(x-3)^{3}(x-4)^{2}}
$$

일떄, $\lim_{ x \to 6 } \frac{f'(x)}{f(x)}$의 값을 구하여라

f'(x)부터 구해보자

분수식이 복잡하니 양변에 자연로그를 취하고 미분해준다

$$
\ln |f(x)|=6\ln |x|+5\ln|(x-1)|+4\ln|(x-2)|-3\ln|(x-3)|-2\ln|(x-4)|
$$

$$
\frac{f'(x)}{f(x)}
=\frac{6}{x}+\frac{5}{x-1}+\frac{4}{x-2}-\frac{3}{x-3}-\frac{2}{x-4}
$$

극한값이 부정형으로 나오진 않을것 같으니 x=6대입후 계산

$$
\frac{f'(x)}{f(x)}=1+1+1-1-1=1
$$

