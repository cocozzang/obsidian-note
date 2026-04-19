---
id: c7e4d2f1-8b3a-4e59-b1c0-2f9d5e7a3b84
aliases:
  - 초월함수의 넓이(2)
  - 삼각함수 넓이 이등분
  - 매개변수 곡선 넓이
  - 역함수 넓이
tags:
  - 초월함수
  - 넓이와적분
  - 삼각함수
  - 매개변수
  - 역함수적분
  - 이등분
  - 사이클로이드
pages: 183-187
subject: 대학기초수학
title: 초월함수의 넓이(2)
topics:
  - 두 곡선이 접하는 조건과 넓이
  - 넓이 이등분 조건 설정
  - 역함수와 넓이의 관계
  - 매개변수 곡선의 넓이 (사이클로이드)
---

# 초월함수의 넓이(2)

이번 강의에서는 초월함수 넓이의 심화 주제를 다룬다. 두 함수가 **접하는 조건**으로 교점을 구하고 넓이를 계산하거나, 곡선이 넓이를 **이등분**하는 방정식을 세우는 문제, **역함수**와 넓이의 관계, 그리고 **매개변수로 나타낸 곡선**(사이클로이드)의 넓이가 핵심 주제이다.

---

## 1. 두 함수가 접하는 조건

두 함수 $f(x)$, $g(x)$가 점 $t$에서 접한다 = **한 점에서 만나고 그 점에서 기울기도 같다**:

$$f(t) = g(t) \qquad \text{(함수값 일치)}$$
$$f'(t) = g'(t) \qquad \text{(도함수 일치)}$$

두 조건을 연립해 접점 $t$와 미지 계수를 구한다.

---

## 2. 넓이 이등분 조건

곡선 $y = h(x)$가 도형의 넓이를 이등분할 때:

$$\text{(이등분선 한쪽 넓이)} = \frac{1}{2} \times \text{(전체 넓이)}$$

교점 $\alpha$를 기준으로 적분 구간을 분할하고, 한쪽 넓이 = 전체의 절반이라는 방정식을 세운다. 이때 교점 $\alpha$와 미지 계수 $k$를 **연립**하여 푸는 것이 핵심이다.

---

## 3. 역함수와 넓이

$f(x)$와 역함수 $g(x) = f^{-1}(x)$의 넓이 관계:

$$\int_{f(a)}^{f(b)} g(x)\, dx = b \cdot f(b) - a \cdot f(a) - \int_{a}^{b} f(x)\, dx$$

이는 직사각형 넓이에서 $f$의 정적분을 뺀 값이다 (그래프의 대칭성 활용).

---

## 4. 매개변수 곡선의 넓이

$x = x(\theta)$, $y = y(\theta)$로 주어진 곡선의 $x$축과의 넓이:

$$S = \int y\, dx = \int_{\theta_1}^{\theta_2} y(\theta) \cdot \frac{dx}{d\theta}\, d\theta$$

$dx = \frac{dx}{d\theta} d\theta$로 치환하여 $\theta$에 대한 적분으로 변환한다.

---

## 5. 예제

### 예제 398

양의 실수로 이루어진 수열 $\{a_n\}$에 대하여 두 곡선 $y = a_n x^n$과 $y = \ln x$는 한 점에서 만난다. 다음 보기에서 옳은 것을 모두 고른 것은?

![[images/04-integral/exer398.png|400]]

> ㄱ. $a_n = \dfrac{1}{ne}$ 이다.
>
> ㄴ. 두 곡선 $y = a_n x^n$, $y = \ln x$와 $x$축으로 둘러싸인 부분의 넓이 $S_n$은
> $$S_n = \frac{n}{n+1}e^{\frac{1}{n}} - 1 \text{ 이다.}$$
>
> ㄷ. $\displaystyle\lim_{n \to \infty}(1 + S_n)^n = 1$ 이다.

① ㄱ　② ㄴ　③ ㄱ, ㄴ　④ ㄴ, ㄷ　**⑤ ㄱ, ㄴ, ㄷ**

> [!summary]- 풀이
>
> #### ㄱ. $a_n = \dfrac{1}{ne}$ 확인
>
> 두 곡선이 한 점 $t$에서 **접하는** 조건 (함수값 일치 + 도함수 일치):
>
> $$a_n t^n = \ln t \qquad \cdots (1)$$
>
> $$n \cdot a_n t^{n-1} = \frac{1}{t} \implies n \cdot a_n t^n = 1 \implies a_n t^n = \frac{1}{n} \qquad \cdots (2)$$
>
> (1), (2)에서: $\ln t = \frac{1}{n}$이므로 $t = e^{\frac{1}{n}}$
>
> (2)에 대입: $a_n \cdot e = \frac{1}{n}$ $\implies$ $a_n = \frac{1}{ne}$ $\quad\checkmark$
>
> #### ㄴ. $S_n = \dfrac{n}{n+1}e^{\frac{1}{n}} - 1$ 확인
>
> 접점이 $t = e^{\frac{1}{n}}$이고, $x \in [0, t]$ 구간에서 $a_n x^n \geq \ln x$ (단, $x \geq 1$에서는 $\ln x \geq 0$이므로 구간 분리 필요):
>
> $$S_n = \int_{0}^{t} a_n x^n\, dx - \int_{1}^{t} \ln x\, dx$$
>
> ※ $\int_{0}^{1}\ln x\, dx$는 $[x\ln x - x]_{0}^{1} = -1$이므로 실제로 $\int_{0}^{t}\ln x\, dx$의 올바른 하한은 1이 아닌 0에서 시작함에 주의. 노트 풀이는 $[x\ln x - x]_{1}^{t}$ 로 쓰되 적분 하한을 $x=1$ 기준으로 쪼개어 계산한 것이다.
>
> $$= a_n \left[\frac{x^{n+1}}{n+1}\right]_0^t - \left[x\ln x - x\right]_1^t$$
>
> $$= \frac{1}{ne} \cdot \frac{t^{n+1}}{n+1} - (t\ln t - t + 1)$$
>
> $t = e^{\frac{1}{n}}$ 대입:
>
> $$= \frac{1}{ne} \cdot \frac{e^{1+\frac{1}{n}}}{n+1} - \left(e^{\frac{1}{n}} \cdot \frac{1}{n} - e^{\frac{1}{n}} + 1\right)$$
>
> $$= \frac{e^{\frac{1}{n}}}{n(n+1)} - e^{\frac{1}{n}}\left(\frac{1}{n} - 1\right) - 1$$
>
> $$= e^{\frac{1}{n}}\left(\frac{1}{n^2+n} - \frac{n+1}{n^2+n} + \frac{n^2+n}{n^2+n}\right) - 1$$
>
> $$= e^{\frac{1}{n}} \cdot \frac{n^2}{n^2+n} - 1 = \frac{n}{n+1}e^{\frac{1}{n}} - 1 \quad\checkmark$$
>
> #### ㄷ. $\displaystyle\lim_{n \to \infty}(1+S_n)^n = 1$ 확인
>
> $1 + S_n = \dfrac{n}{n+1}e^{\frac{1}{n}}$이므로:
>
> $$\lim_{n \to \infty}\left(\frac{n}{n+1}e^{\frac{1}{n}}\right)^n = \lim_{n \to \infty}\left(\frac{n}{n+1}\right)^n \cdot e = \lim_{n \to \infty}\frac{e}{\left(1+\frac{1}{n}\right)^n} = \frac{e}{e} = 1 \quad\checkmark$$
>
> **ㄱ, ㄴ, ㄷ 모두 참 → 정답: ⑤**

---

### 예제 399

![[images/04-integral/exer399.png]]

그림과 같이 곡선 $y = \dfrac{1}{x}$과 $x$축 및 두 직선 $x=1$, $x=8$로 둘러싸인 도형의 넓이를 직선 $x=a$가 이등분할 때, 상수 $a$의 값은?

① $\sqrt{2}$ ② $\sqrt{3}$ ③ $2$ ④ $2\sqrt{2}$ ⑤ $3$

> [!summary]- 풀이
>
> 이등분 조건: $\displaystyle\int_{1}^{a}\frac{1}{x}\,dx = \int_{a}^{8}\frac{1}{x}\,dx$
>
> $$[\ln x]_{1}^{a} = [\ln x]_{a}^{8}$$
>
> $$\ln a - \ln 1 = \ln 8 - \ln a$$
>
> $$2\ln a = \ln 8 = \frac{1}{2}\ln 8^2 \implies \ln a = \ln\sqrt{8}$$
>
> $$a = \sqrt{8} = 2\sqrt{2}$$
>
> **정답: ④ $2\sqrt{2}$**

---

### 예제 400

![[images/04-integral/exer400.png]]

연속함수 $f(x)$의 그래프는 다음과 같다. 이 곡선과 $x$축으로 둘러싸인 두 부분 A, B의 넓이가 각각 $\alpha$, $\beta$일 때, 정적분 $\displaystyle\int_{0}^{p} xf(2x^2)\,dx$의 값은? $\left(\text{단},\ p > \frac{1}{2}\right)$

① $\dfrac{1}{2}(\alpha+\beta)$ ② $\dfrac{1}{2}(\alpha-\beta)$ ③ $\alpha+\beta$
④ $\dfrac{1}{4}(\alpha+\beta)$ **⑤ $\dfrac{1}{4}(\alpha-\beta)$**

> [!summary]- 풀이
>
> $2x^2 = t$로 치환하면 $4x\,dx = dt$, 즉 $x\,dx = \dfrac{1}{4}dt$
>
> $x: 0 \to p$일 때 $t: 0 \to 2p^2$
>
> $$\int_{0}^{p}xf(2x^2)\,dx = \frac{1}{4}\int_{0}^{2p^2}f(t)\,dt = \frac{1}{4}\int_{0}^{2p^2}f(x)\,dx$$
>
> 그래프에서 A 구간은 $f(x) > 0$, B 구간은 $f(x) < 0$이므로:
>
> $$\int_{0}^{2p^2}f(x)\,dx = \alpha - \beta$$
>
> $$\therefore \int_{0}^{p}xf(2x^2)\,dx = \frac{1}{4}(\alpha - \beta)$$
>
> **정답: ⑤ $\dfrac{1}{4}(\alpha-\beta)$**

---

### 예제 401

![[images/04-integral/exer401.png]]

오른쪽 그림과 같이 구간 $\left[0,\,\dfrac{\pi}{2}\right]$에서 곡선 $y = \cos x$와 직선 $y = a$로 둘러싸인 색칠한 두 부분의 넓이가 서로 같을 때, $a$의 값은?

① $\dfrac{1}{\pi}$ ② $\dfrac{2}{\pi}$ ③ $\dfrac{\pi}{3}$ ④ $\dfrac{\pi}{4}$ ⑤ $\dfrac{\pi}{5}$

> [!summary]- 풀이
>
> 두 색칠 부분의 넓이가 같다 = 직선 $y=a$가 곡선과 $x$축 사이의 직사각형을 분할할 때, **곡선 위쪽 넓이 = 직선 아래 직사각형 나머지 넓이**
>
> 이를 정적분 조건으로 표현하면:
>
> $$\int_{0}^{\frac{\pi}{2}}\cos x\,dx - \frac{a\pi}{2} = 0$$
>
> $$[\sin x]_{0}^{\frac{\pi}{2}} = \frac{a\pi}{2}$$
>
> $$1 = \frac{a\pi}{2} \implies a = \frac{2}{\pi}$$
>
> **정답: ② $\dfrac{2}{\pi}$**

---

### 예제 402

곡선 $y = \sin 2x$ $\left(0 \leq x \leq \dfrac{\pi}{2}\right)$와 $x$축으로 둘러싸인 도형의 넓이를 곡선 $y = k\cos x$가 이등분할 때, 상수 $k$의 값은?

① $1$ ② $2-\sqrt{2}$ ③ $\sqrt{2}$ ④ $2$ ⑤ $2+\sqrt{2}$

> [!summary]- 풀이
>
> ![[images/04-integral/exer402.png]]
>
> **교점 구하기:**
>
> $$\sin 2x = k\cos x \implies 2\sin x\cos x = k\cos x$$
>
> $x = \dfrac{\pi}{2}$ 제외한 구간에서 $\cos x \neq 0$이므로 약분 가능:
>
> $$\sin x = \frac{k}{2} \implies \sin\alpha = \frac{k}{2}$$
>
> 즉 교점의 $x$좌표를 $\alpha$라 하면 $\sin\alpha = \dfrac{k}{2}$, 범위 $-2 \leq k \leq 2$.
>
> **전체 넓이의 절반:**
>
> $$\frac{1}{2}\int_{0}^{\frac{\pi}{2}}\sin 2x\,dx = \frac{1}{2}\left[-\frac{1}{2}\cos 2x\right]_{0}^{\frac{\pi}{2}} = \frac{1}{2}\left(\frac{1}{2}+\frac{1}{2}\right) = \frac{1}{2}$$
>
> **이등분 조건** ($\alpha$부터 $\dfrac{\pi}{2}$까지 두 곡선 사이 넓이 = 전체의 절반):
>
> $$\int_{\alpha}^{\frac{\pi}{2}}(\sin 2x - k\cos x)\,dx = \frac{1}{2}$$
>
> $$\left[-\frac{1}{2}\cos 2x - k\sin x\right]_{\alpha}^{\frac{\pi}{2}} = \frac{1}{2}$$
>
> $$\left(\frac{1}{2} - k\right) - \left(-\frac{1}{2}\cos 2\alpha - k\sin\alpha\right) = \frac{1}{2}$$
>
> $$(\sin\alpha - 1)k + \frac{1}{2}\cos 2\alpha = 0$$
>
> $$k = \frac{-\frac{1}{2}\cos 2\alpha}{\sin\alpha - 1} = \frac{-\frac{1}{2}(1 - 2\sin^2\alpha)}{\sin\alpha - 1}$$
>
> **$\sin\alpha = \dfrac{k}{2}$ 대입:**
>
> $$k = \frac{-\frac{1}{2} + \frac{k^2}{4}}{\frac{k}{2} - 1} = \frac{k^2 - 2}{2k - 4}$$
>
> $$k(2k-4) = k^2 - 2 \implies k^2 - 4k + 2 = 0$$
>
> $$k = \frac{4 \pm \sqrt{8}}{2} = 2 \pm \sqrt{2}$$
>
> $-2 \leq k \leq 2$ 조건에서: $k = 2 - \sqrt{2}$
>
> **정답: ② $2 - \sqrt{2}$**

---

### 예제 403

곡선 $y = \sin x$ $(0 \leq x \leq \pi)$ 위의 한 점 $\mathrm{P}(\alpha,\, \sin\alpha)$가 있다. 원점 $\mathrm{O}$와 점 $\mathrm{P}$를 잇는 선분 $\mathrm{OP}$가 이 곡선과 $x$축으로 둘러싸인 부분의 넓이를 이등분할 때, $\alpha\tan\alpha$의 값은?

① $-1$ ② $-2$ ③ $-3$ ④ $-4$ ⑤ $-5$

> [!summary]- 풀이
>
> ![[images/04-integral/exer304.png]]
>
> 선분 $\mathrm{OP}$의 기울기: $\dfrac{\sin\alpha}{\alpha}$, 삼각형 $\mathrm{OPA}$의 넓이 $= \dfrac{1}{2}\alpha\sin\alpha$
>
> 이등분 조건 (선분 $\mathrm{OP}$ 아래 넓이 = 전체의 절반):
>
> $$\int_{0}^{\alpha}\sin x\,dx - \frac{1}{2}\alpha\sin\alpha = \frac{1}{2}\int_{0}^{\pi}\sin x\,dx$$
>
> $$[-\cos x]_{0}^{\alpha} - \frac{1}{2}\alpha\sin\alpha = \frac{1}{2} \cdot 2$$
>
> $$(1 - \cos\alpha) - \frac{1}{2}\alpha\sin\alpha = 1$$
>
> $$-\cos\alpha - \frac{1}{2}\alpha\sin\alpha = 0$$
>
> 양변을 $\cos\alpha$로 나누면:
>
> $$-1 - \frac{1}{2}\alpha\tan\alpha = 0$$
>
> $$\alpha\tan\alpha = -2$$
>
> **정답: ② $-2$**

---

### 예제 404

역함수를 갖는 연속함수 $f(x)$가 다음 두 조건을 만족한다.

> i ) $f(1) = 1$, $f(2) = 2$
>
> ii ) $\displaystyle\int_{1}^{2}f(x)\,dx = A$

$f(x)$의 역함수를 $g(x)$라 할 때, $\displaystyle\int_{1}^{2}g(x)\,dx$의 값을 $A$로 나타내면?

① $A$ ② $A-1$ ③ $A+1$ ④ $3-A$ ⑤ $4-A$

> [!summary]- 풀이
>
> 역함수의 정적분 공식을 이용한다. $f(1)=1$, $f(2)=2$이므로 $g(1)=1$, $g(2)=2$이고:
>
> $$\int_{1}^{2}g(x)\,dx = \int_{f(1)}^{f(2)}g(x)\,dx$$
>
> 역함수 적분 공식:
>
> $$= b \cdot f(b) - a \cdot f(a) - \int_{a}^{b}f(x)\,dx$$
>
> 여기서 $a=1$, $b=2$:
>
> $$= 2 \cdot f(2) - 1 \cdot f(1) - \int_{1}^{2}f(x)\,dx$$
>
> $$= 2 \cdot 2 - 1 \cdot 1 - A = 4 - 1 - A = 3 - A$$
>
> **정답: ④ $3-A$**

---

### 예제 405

좌표평면 위를 움직이고 있는 점 $\mathrm{P}(\theta - \sin\theta,\; 1 - \cos\theta)$가 있다. $\theta$가 $0$부터 $2\pi$까지 변할 때, 점 $\mathrm{P}$가 그리는 곡선과 $x$축으로 둘러싸인 부분의 넓이 $S$를 구하면?

① $\pi$ ② $2\pi$ ③ $3\pi$ ④ $4\pi$ ⑤ $5\pi$

> [!summary]- 풀이
>
> ![[images/04-integral/exer405.png]]
>
> 매개변수: $x = \theta - \sin\theta$, $y = 1 - \cos\theta$ ($0 \leq \theta \leq 2\pi$)
>
> **$dx$를 $d\theta$로 변환:**
>
> $x = \theta - \sin\theta$를 $x$에 대해 미분하면:
>
> $$1 = \frac{d}{d\theta}(\theta - \sin\theta) \cdot \frac{d\theta}{dx} \implies \frac{dx}{d\theta} = 1 - \cos\theta \implies dx = (1-\cos\theta)\,d\theta$$
>
> **넓이 계산:**
>
> $$S = \int_{0}^{2\pi}y\,dx = \int_{0}^{2\pi}(1-\cos\theta)(1-\cos\theta)\,d\theta$$
>
> $$= \int_{0}^{2\pi}(1 - 2\cos\theta + \cos^2\theta)\,d\theta$$
>
> $\cos^2\theta = \dfrac{1 + \cos 2\theta}{2}$ 적용:
>
> $$= \int_{0}^{2\pi}\left(\frac{3}{2} - 2\cos\theta + \frac{\cos 2\theta}{2}\right)d\theta$$
>
> $$= \left[\frac{3}{2}\theta - 2\sin\theta + \frac{\sin 2\theta}{4}\right]_{0}^{2\pi}$$
>
> $$= \frac{3}{2} \cdot 2\pi - 0 + 0 = 3\pi$$
>
> **정답: ③ $3\pi$**

---

## 관련 주제

- [[58-transcendental-area-1|초월함수의 넓이(1)]]
- [[60-volume-integral-1|부피와 적분(1)]]
- [[52-integral-inverse-function|정적분의 계산기법(3), 역함수와 정적분]]
- [[45-integration-by-parts|부분적분]]

---

**학습 포인트:**
1. 두 함수가 **접하는 조건** (함수값 + 도함수값 일치)으로 접점 $t$와 계수를 동시에 구한다.
2. 넓이 이등분 문제는 교점 $\alpha$와 미지수 $k$를 **연립**하여 $k$에 대한 방정식을 만드는 것이 핵심이다.
3. 역함수 적분: $\int_{f(a)}^{f(b)}g(x)\,dx = bf(b) - af(a) - \int_a^b f(x)\,dx$
4. 매개변수 곡선 넓이: $dx = \frac{dx}{d\theta}d\theta$로 치환하여 $\theta$에 대해 적분한다.
