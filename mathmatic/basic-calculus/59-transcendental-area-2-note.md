---
id: 59-transcendental-area-2-note
aliases: []
tags: []
---

## 예제 398


양의 실수로 이루어진 수열 $\{a_{n}\}$에 대하여 두 곡선 $y=a_{n}x^{n}$과 $y=\ln x$는 한 점에서
만난다. 다음 보기 에서 옳은 것을 모두 고른 것은?
![[exer398.png|300]]

> ㄱ. $a_{n}=\dfrac{1}{ne}$ 이다.
>
> ㄴ. 두 곡선 $y=a_{n}x^{n}$, $y=\ln x$와 $x$축으로 둘러싸인 부분의 넓이 $S_{n}$은
>
> $$S_{n}=\dfrac{n}{n+1}e^{\frac{1}{n}}-1 \text{ 이다.}$$
>
> ㄷ. $\displaystyle\lim_{n \to \infty}(1+S_{n})^{n}=1$ 이다.

① ㄱ $\quad$ ② ㄴ $\quad$ ③ ㄱ, ㄴ $\quad$ ④ ㄴ, ㄷ $\quad$ ⑤ ㄱ, ㄴ, ㄷ

---

(ㄱ)
$$
given: f(t)=g(t),\ f'(t)=g'(t)
$$
$$
a_{n}t^{n}= \ln t
$$
$$
n \cdot a_{n}t^{n-1}=\frac{1}{t}
$$
$$
n\cdot a_{n}t^{n}=1
$$
$$
a_{n}t^{n} = \frac{1}{n}
$$
$$
\ln t=\frac{1}{n}
$$
$$
e^{\frac{1}{n}}=t
$$
$$
a_{n} \left( e^{\frac{1}{n}} \right)^{n}
=a_{n}e
= \frac{1}{n}
$$
$$
a_{n}= \frac{1}{ne}
$$
ㄱ은 참이다 

(ㄴ)
$$
S_{n}=\int_{0}^{t} a_{n}x^{n}\ dx- \int_{0}^{t} \ln x \ dx
$$
$$
=a_{n}\left[ \frac{1}{n+1}x^{n+1} \right]_{0}^{t}-[x\ln x-x]_{1}^{t}
$$
$$
=a_{n}\left( \frac{1}{n+1}\cdot t^{n+1} \right)- (t\ln t-t+1)
$$
$$
\because t= e^{\frac{1}{n}},\ a_{n}= \frac{1}{ne}
$$
$$
=\frac{1}{ne}\left( \frac{1}{n+1} \cdot \left( e^{\frac{1}{n}} \right)^{n+1} \right)-\left( e^{\frac{1}{n}} \ln e^{\frac{1}{n}}-e^{\frac{1}{n}}+1 \right)
$$
$$
=\frac{1}{ne} \cdot \frac{1}{n+1} \cdot e^{1+\frac{1}{n}}-e^{\frac{1}{n}}\left( \frac{1}{n}-1 \right)-1
$$
$$
=\frac{1}{n} \cdot \frac{1}{n+1} \cdot e^{\frac{1}{n}}- e^{\frac{1}{n}}\left( \frac{1}{n}-1 \right)-1
$$
 $$
=e^{\frac{1}{n}}\left( \frac{1}{n^{2}+n}-\frac{n+1}{n^{2}+n} +\frac{n^{2}+n}{n^{2}+n} \right)-1
$$
$$
=e^{\frac{1}{n}} \cdot \frac{n^{2}}{n^{2}+n}-1
$$
$$
=\frac{n}{n+1}e^{\frac{1}{n}}-1
$$
ㄴ은 참이다

(ㄷ)
$$
\lim_{ n \to \infty } (1+S_{n})^{n}
=\lim_{ n \to \infty } \left(\frac{n}{n+1}e^{\frac{1}{n}}\right)^{n}
$$
$$
=\lim_{ n \to \infty } \left( \frac{n}{n+1} \right)^{n} \cdot e
$$
$$
=\lim_{ n \to \infty } \frac{e}{\left( \frac{n+1}{n} \right)^{n}}
$$
$$
=\lim_{ n \to \infty } \frac{e}{\left( 1+\frac{1}{n} \right)^{n}}
$$
$$
=\frac{e}{e}=1
$$
ㄷ은 참이다 


### 예제399
![[exer399.png]]

---

$$
given : \int_{1}^{a} \frac{1}{x}\ dx = \int_{a}^{8} \frac{1}{x}\ dx
$$
$$
[\ln x]_{1}^{a}=[\ln x]_{a}^{8}
$$
$$
\ln a - \ln 1 = \ln 8 - \ln a
$$
$$
2 \ln a= \ln 8 
$$
$$
\ln a= \frac{1}{2} \ln 8
$$
$$
\ln a = \ln 8 ^{\frac{1}{2}}
$$
$$
a=\sqrt{ 8 }=2\sqrt{ 2 }
$$

### 예제400
![[exer400.png]]

---

$$
\text{put}\ 2x^{2}=t \implies 4x \cdot dx = dt
$$
$$
GE= \int_{0}^{2p^{2}}f(t) \left( \frac{1}{4} dt \right)
=\frac{1}{4}\int_{0}^{2p^{2}}f(t)\ dt
$$
$$
=\frac{1}{4} \int_{0}^{2p^{2}} f(x)\ dx 
= \frac{1}{4}(\alpha-\beta)
$$

### 예제401
![[exer401.png]]

---

$$
given: \int_{0}^{\frac{\pi}{2}} \cos x\ dx - \frac{a\pi}{2} = 0
$$
$$
=[\sin x]_{0}^{\frac{\pi}{2}}-\frac{a\pi}{2}
$$
$$
=1-\frac{a\pi}{2}=0
$$
$$
a\pi=2
$$
$$
a=\frac{2}{\pi}
$$

## 예제 402 (어렵당..)

곡선 $y=\sin 2x$ $\left(0 \leq x \leq \dfrac{\pi}{2}\right)$와 $x$축으로 둘러싸인 도형의 넓이를 곡선 $y=k\cos x$가
이등분할 때, 상수 $k$의 값은?


① $1$ $\quad$ ② $2-\sqrt{2}$ $\quad$ ③ $\sqrt{2}$ $\quad$ ④ $2$ $\quad$ ⑤ $2+\sqrt{2}$

---

풀이에 앞서
해당구간내에서 두 곡선 그래프는 아래 이미지와 같다
![[exer402.png|300]]

우선 k에 대한 방정식을 만들어야하는데 
$y=k\cos x$와 $y=\sin 2x$ , y축으로 둘러쌓인 넓이를 사용하여 
두 함수의 관계식을 설정하기 굉장히 힘들기 떄문에 
적분구간을 옮겨서 두 함수의 관계식을 만들어 k에 대한 방정식으로 만들어야한다.

---

$0\leq x \leq \frac{\pi}{2}$ 구간에서의 두 함수의 교점의 x좌표를 $\alpha$ 라고 하면
$$
\frac{1}{2} \int_{0}^{\frac{\pi}{2}} \sin 2x
=\int_{\alpha}^{\frac{\pi}{2}} \sin 2x-\int_{\alpha}^{\frac{\pi}{2}}k \cos x
$$

되고 $\left[ 0, \frac{\pi}{2} \right]$ 구간내의 아래 넓이를 뺸 sin2x의 적분값이 되는것을 알수있다.

위 식은 $\alpha$와 k에 관한 식이므로 

두 함수를 연립하여 $\alpha$ 와 k에 관한 관계식을 찾아보자 

$$
\sin 2x = k \cos x
$$
$$
2\sin x \cancel{\cos x} = k \cancel{\cos x}
$$
$$
\sin x = \frac{k}{2}
$$
$$
\sin\alpha = \frac{k}{2}
$$
$$
-2\leq k \leq 2
$$
로  $\alpha$를 임의의 한 근으로 설정한다 나머지 한근은 이미지를 보면 알 수 있듯이 
$(\frac{\pi}{2},0)$ 에 해당하는 교점이다 

여기서 cosx를 약분해야하는데 
찾고자하는 해는 $\frac{\pi}{2}$가 아니며 
문제 범위의 모든 넓이에 대해 $\frac{\pi}{2}$에  해당하는 점을 뺴더라고 
도형의 넓이 자체를 정의하는데는 문제가 없고 
해당 넓이에 대응하는 적분값을 구하는데 문제가 없기 떄문에 (해석학에서 배움)
cosx를 약분할수가 있다.


$$
\frac{1}{2}\int_{0}^{\frac{\pi}{2}} \sin 2x
=\frac{1}{2} \left[ -\frac{1}{2}\cos 2x \right]_{0}^{\frac{\pi}{2}}
$$
$$
=\frac{1}{2}\left( \frac{1}{2} -\left( -\frac{1}{2} \right)\right)
=\frac{1}{2} \cdot 1
=\frac{1}{2}
$$
$$
\therefore \int_{\alpha}^{\frac{\pi}{2}} \sin 2x - k \cos x \ dx = \frac{1}{2}
$$
$$
=\left[ -\frac{1}{2} \cos 2x - k\sin x \right]_{\alpha}^{\frac{\pi}{2}}
$$
$$
= \left( \frac{1}{2}-k \right)-\left( -\frac{1}{2}\cos 2\alpha-k\sin\alpha \right)
$$
$$
=\frac{1}{2}-k+\frac{1}{2} \cos 2\alpha + k\sin\alpha
$$
$$
=(\sin\alpha-1)k+\frac{1}{2}+\frac{1}{2} \cos 2\alpha 
= \frac{1}{2}
$$
$$
(\sin\alpha-1)k = -\frac{1}{2}\cos 2\alpha
$$
$$
k= \frac{-\frac{1}{2} \cos 2\alpha}{\sin\alpha -1}
$$
$$
=\frac{-\frac{1}{2}(1-2\sin ^{2}\alpha)}{\sin\alpha -1}
$$
$$
\because \sin\alpha= \frac{k}{2}
$$
$$
k= \frac{-\frac{1}{2}+\frac{k^{2}}{4}}{\frac{k}{2}-1}
$$
$$
=\frac{-2+k^{2}}{2k-4}
$$

$$
k(2k-4)=k^{2}-2
$$
$$
2k^{2}-4k=k^{2}-2
$$
$$
k^{2}-4k+2=0
$$
$$
k=\frac{4\pm \sqrt{ 16-4\cdot 1 \cdot 2 }}{2}
$$
$$
=\frac{4\pm \sqrt{ 8 }}{2}
=2\pm \sqrt{ 2 }
$$
$$
\because -2 \leq k \leq 2
$$
$$
k= 2-\sqrt{ 2 }
$$


## 예제 403

곡선 $y=\sin x$ $(0 \leq x \leq \pi)$위의 한 점 $\text{P}(\alpha,\ \sin\alpha)$가 있다. 원점 $\text{O}$와 점 $\text{P}$를 잇는
선분 $\text{OP}$가 이 곡선과 $x$축으로 둘러싸인 부분의 넓이를 이등분할 때, $\alpha\tan\alpha$의 값은?

① $-1$ $\quad$ ② $-2$ $\quad$ ③ $-3$ $\quad$ ④ $-4$ $\quad$ ⑤ $-5$

---

![[exer304.png|300]]

$$
\int_{0}^{\pi} \sin x \ dx 
= 2\left\{  \int_{0}^{\alpha} \sin x\ dx - \frac{1}{2}\alpha \sin\alpha  \right\}
$$
$$
[-\cos x]_{0}^{\pi}= 2\left( [-\cos x]_{0}^{\alpha}-\frac{1}{2} \alpha \sin \alpha \right)
$$
$$
1-(-1)= 2 \left( -\cos\alpha - (-1)-\frac{1}{2}\alpha \sin\alpha \right)
$$
$$
2=-2\cos \alpha +2 - \alpha \sin \alpha
$$
$$
-2\cos \alpha - \alpha \sin \alpha = 0
$$
$$
-2-\alpha \tan\alpha =0
$$
$$
\alpha \tan\alpha = -2
$$


## 예제 404

역함수를 갖는 연속함수 $f(x)$가 다음 두 조건을 만족한다.

> i ) $f(1)=1$, $f(2)=2$
>
> ii ) $\displaystyle\int_{1}^{2}f(x)\,dx = A$

$f(x)$의 역함수를 $g(x)$라 할 때, $\displaystyle\int_{1}^{2}g(x)\,dx$의 값을 $A$로 나타내면?

① $A$ $\quad$ ② $A-1$ $\quad$ ③ $A+1$ $\quad$ ④ $3-A$ $\quad$ ⑤ $4-A$

---

$$
\int_{1}^{2} g(x)\ dx = \int_{f(1)}^{f(2)}g(x)\ dx = 2f(2)- 1\cdot f(1) - \int_{1}^{2}f(x)\ dx
$$
$$
=4-1-A
$$
$$
=3-A
$$

## 예제 405

좌표평면 위를 움직이고 있는 점 $\text{P}(\theta-\sin\theta,\ 1-\cos\theta)$가 있다. $\theta$가 $0$부터 $2\pi$까지
변할 때, 점 $\text{P}$가 그리는 곡선과 $x$축으로 둘러싸인 부분의 넓이 $S$를 구하면?

① $\pi$ $\quad$ ② $2\pi$ $\quad$ ③ $3\pi$ $\quad$ ④ $4\pi$ $\quad$ ⑤ $5\pi$

---

매겨변수로 나타내여진 함수
$$
x=\theta-\sin\theta,\ 
y=1-\cos\theta
$$
$$
\because 0\leq \theta \leq 2\pi
$$
정의역 치역 범위는 아래와 같다 
$$
0\leq x \leq 2\pi
$$
$$
0 \leq y \leq 2
$$

함수의 개형을 그리기위해 우선 미분계수가 0인 지점을 찾아야한다.
$$
\frac{dx}{d\theta}=1-\cos\theta
$$
$$
\frac{dy}{d\theta}=\sin\theta
$$
$$
\frac{dy}{dx}=\frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}}
=\frac{\sin\theta}{1-\cos\theta}
=0
$$
경계값을 제외하면 $1-\cos\theta$를 약분할수있다
$$
\sin\theta=0
$$
$$
\theta= \pi
$$
구간내에서 극점은 $\theta=\pi$ 인 경우 하나 이다.

$$
P(\pi-\sin \pi, 1-\cos \pi)= (\pi,2)
$$

극점의 극대 극소 조사
$$
\frac{d^{2}y}{dx^{2}}=\frac{d}{dx}\left( \frac{dy}{dx} \right)
$$
$$
=\frac{d}{dx}\left( \frac{\sin\theta}{1-\cos\theta} \right)
$$
$$
=\frac{d}{d\theta}\left( \frac{\sin\theta}{1-\cos\theta} \right) \frac{d\theta}{dx}
$$
$$
=\frac{\cos\theta(1-\cos\theta)-\sin\theta \sin\theta}{(1-\cos\theta)^{2}} \cdot \frac{1}{1-\cos\theta}
$$
$$
=\frac{\cos\theta-\cos ^{2}\theta-\sin ^{2}\theta}{(1-\cos\theta)^{3}}
$$
$$
=\frac{\cos\theta-1}{(1-\cos\theta)^{3}}
$$
$$
= \frac{-1}{(1-\cos\theta)^{2}} < 0
$$
$\theta$ 값에 상관없이 함수는 극대권만을 가지는 것을 알수있다.
$(\pi,2)$ 는 극대점임을 알수있다.

이제 $\theta$ 구간과 함수의 정의역,치역 범위와 극대점으로 함수의 개형을 그려보면 
![[exer405.png|300]]

$$
S=\int_{0}^{2\pi}y\ dx 
=\int_{0}^{2\pi}(1-\cos\theta)\ dx
$$
$$
\because \frac{dx}{d\theta}=1-\cos\theta
$$
$$
dx=(1-\cos\theta)d\theta
$$

$$
S= \int_{0}^{2\pi}(1-\cos\theta)(1-\cos\theta)d\theta
$$
$$
=\int_{0}^{2\pi}(1-2\cos\theta+\cos ^{2}\theta)\ d\theta
$$
$$
=\int_{0}^{2\pi}\left( 1-2\cos\theta+\frac{1+\cos 2\theta}{2} \right)\ d\theta
$$
$$
=\left[ \theta-2\sin\theta+\frac{1}{2}\theta + \frac{1}{4}\sin 2\theta \right]_{0}^{2\pi}
$$
$$
=(2\pi+\pi)-0=3\pi
$$
$$
\therefore S=3\pi
$$
