---
id: 20-inverse-differentiability-note
aliases: []
tags: []
---

thm22 역함수의 미분계수를 구하는 방법
 $f(g(x))=x$임을 이용

$g(x)=f^{-1}(x)$이고 $f(a)=b$일때 g'(b)를 구해보자

방법1 $f(g(x))=x$ 임을 이용
![thm22-1|400](./images/03-calculus/thm22-1.png)

$$
f(g(x))=x
$$

양변미분

$$
f'(g(x))\cdot g'(x)=1
$$

$$
f'(g(b))\cdot g'(b)=f'(a)\cdot g'(b)=1
$$

$$
g'(b)=\frac{1}{f'(a)}
$$
증명:

우선 그림 thm22-1을 통해
$$
\begin{cases}
f(a)=b \\
g(b)=a \\
f(a+\Delta x)=b+\Delta y \\
g(b+\Delta y)=a+\Delta x
\end{cases}
$$

위 식들을 구할수있다.
$$
\frac{1}{f'(a)}=\lim_{ \Delta x \to 0 } \frac{1}{\frac{f(a+\Delta x)-f(a)}{\Delta x}}
$$
분모분자에 $\Delta x$를 곱해주고 위의 그림 22-1을 통해 얻은 식을 사용하기 위해 분자에 a를 더하고 뺴준다.
$$
=\lim_{ \Delta x \to 0 } \frac{\Delta x}{f(a+\Delta x)-f(a)}=\lim_{ \Delta x \to 0 } \frac{(a+\Delta x)-a}{f(a+\Delta x)-f(a)}
$$
이제 식을 $g,\  \Delta y,\ b$에 대한 식으로 치환해주면
$$
=\lim_{ \Delta y \to 0 } \frac{g(b+\Delta y)-g(b)}{\cancel{b}+\Delta y\cancel{-b}}=g'(b)
$$
f'(a)의 역수가 g'(b)임을 알수있다.






예제 115
조건식 f(g(x))=x 를 만족하는 일대일 대응인 두 함수 f,g에 대하여,
f의 그래프 위의 점 (2,3)에서 곡선 f에 그은 접선의 기울기가 3일때,
점(3,2)에서 $y=g(x)$에 그은 접선의 기울기를 구하라.

위 문제에서 아래 사항을 도출해낼수있다.

$$
g(x)=f^{-1}(x) \;,\; f(2)=3 \;,\; f'(2)=3
$$

조건식을 미분하고 x=3을 대입하면

$$
f'(g(x))\cdot g'(x)=1
$$

$$
f'(g(3))\cdot g'(3)=1
$$

$$
f'(2)\cdot g'(3)=1
$$

$$
3\cdot g'(3)=1
$$

$$
g'(3)=\frac{1}{3}
$$

예제 116
함수 $f(x)=\tan x (-\frac{\pi}{2}<x< \frac{\pi}{2})$ 이고 함수 g(x)는 임의의 실수 x에 대하여
조건식 $g(f(x))=x$를 만족한다고 할때 $g'\left( \frac{1}{\sqrt{ 3 }} \right)$의 값을 구하라
note: 초월함수 미분 증명은 이후 초월함수 미분강의에서 배웁니다.
sinx를 미분하면 cos x
tanx를 미분하면 $\sec ^{2}x=\frac{1}{\cos ^{2}x}$

조건식을 $f(g(x))=x$ 로 치환후 미분

$$
f'(g(x))\cdot g'(x)=1
$$

$x=\frac{1}{\sqrt{ 3 }}$을 대입하면

$$
f'\left( g\left( \frac{1}{\sqrt{ 3 }} \right) \right)\cdot g'\left( \frac{1}{\sqrt{ 3 }} \right)=1
$$

$$
g'\left( \frac{1}{\sqrt{ 3 }} \right)=\frac{1}{f'\left( \frac{\pi}{6} \right)}
$$

$$
g'\left( \frac{1}{\sqrt{ 3 }} \right)=\frac{1}{\sec ^{2} \frac{\pi}{6}}=\cos ^{2} \frac{\pi}{6}=\frac{3}{4}
$$

$$
g'\left( \frac{1}{\sqrt{ 3 }} \right)=\frac{4}{3}
$$

thm23 연속성과 미분가능성
f가 x=a에서 미분계수 즉 f'(a)가 존재할때 f는 x=a에서 미분가능이라고 한다
함수가 미분가능하다는 말은
함수가 전체구간에서 연속적이며,
좌미분 우미분의 값이 같다는 말이다.

예제 117
다음 보기 중 x=0에서 미분가능한 함수를 모두 골라라
ㄱ)

$$
f(x)=\begin{cases}
x & (x\geq0) \\
-x & (x<0)
\end{cases}
$$

ㄴ)

$$
f(x)=\begin{cases}
(x+1)^{2} & (x\geq 0) \\
2x+1 & (x<0)
\end{cases}
$$

ㄷ)

$$
f(x)=\begin{cases}
x^{2}+x+1 & (x\geq 0) \\
-x^{2}+x-1 & (x<0)
\end{cases}
$$

ㄹ)

$$
f(x)=\begin{cases}
x^{2} & (x\geq 0) \\
-2x & (x<0)
\end{cases}
$$

ㄱ)

$$
\lim_{ x \to 0^{+} } f(x)=0 \;,\; \lim_{ x \to 0^{-} } f(x)=0 \;,\; f(0)=0
$$

이므로 f(x)는 x=0에서 연속이다.

$$
f'_{-}(0)=-1 \;,\;
f'_{+}(0)=1
$$

로 좌미분 우미분 값이 다르므로 ㄱ)은 x=0에서 미분불능이다.

ㄴ)

$$
\lim_{ x \to 0^{+} } f(x)=1 \;,\; \lim_{ x \to 0^{-} } f(x)=1 \;,\; f(0)=1
$$

ㄴ)은 x=0에서 연속이다.

$$
f'_{-}(0)=2 \ ,\  f'_{+}(0)=2(x+1)=2
$$

$$
f'_{-}(0)=f'_{+}(0)
$$

이므로 ㄴ)은 x=0에서 미분가능하다

ㄷ)

$$
\lim_{ x \to 0^{-} } f(x)=-1 \ ,\ \lim_{ x \to 0^{+} } f(x)=1\ ,\ f(0)=1
$$

ㄷ)은 x=0에서 불연속이므로 미분불능이다.

ㄹ)

$$
\lim_{ x \to 0^{-}} f(x)=0 \ ,\ \lim_{ x \to 0^{+} } f(x)=0 \ ,\ f(0)=0
$$

으로 ㄹ)은 x=0에서 연속이다.

$$
f'_{-}(0)=-2 \ ,\ f'_{+}(0)=2x=0
$$

로 좌미분 우미분 값이 다르므로 ㄹ)은 x=0에서 미분불능이다.

