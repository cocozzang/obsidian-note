---
id: b3f2a1e4-7c9d-4f58-a2b0-1d8e3c6f9a21
aliases:
  - 초월함수의 넓이(1)
  - 로그함수 넓이
  - 지수함수 넓이
  - 삼각함수 넓이
tags:
  - 초월함수
  - 넓이와적분
  - 로그함수
  - 지수함수
  - 삼각함수
  - 무한급수
  - 망원급수
pages: 180-182
subject: 대학기초수학
title: 초월함수의 넓이(1)
topics:
  - 로그함수로 둘러싸인 넓이
  - 지수함수와 관련된 넓이의 급수
  - 삼각함수로 둘러싸인 넓이의 극한
  - 역함수를 이용한 넓이 계산
---

# 초월함수의 넓이(1)

이전 강의에서 다항함수로 둘러싸인 넓이를 다루었다면, 이번 강의부터는 **로그함수, 지수함수, 삼각함수** 등 초월함수가 포함된 넓이 문제를 다룬다. 핵심 전략은 동일하다: 위 함수 - 아래 함수를 적분한다. 다만, 초월함수의 역함수 관계와 급수의 합을 함께 활용하는 복합 문제가 자주 출제된다.

---

## 1. 로그함수로 둘러싸인 넓이

### 핵심 공식

$y = \log_a x$는 $\frac{1}{\ln a} \ln x$와 같으므로, 두 로그함수의 차이는 다음과 같이 상수 비율로 분리된다.

$$\log_a x - \log_b x = \frac{\ln x}{\ln a} - \frac{\ln x}{\ln b} = \left(\frac{1}{\ln a} - \frac{1}{\ln b}\right)\ln x$$

따라서 두 로그함수 사이의 넓이는 $\int \ln x \, dx$의 상수 배로 표현된다.

### 역함수 이용 전략

$y = \log_a x$의 역함수는 $y = a^x$이다. x축 방향으로 적분하기 어려운 경우, 역함수를 이용해 y축 방향으로 적분하면 계산이 단순해지는 경우가 있다.

---

## 2. 예제

### 예제 391

![[images/04-integral/exer391.png]]

그림과 같이 두 직선 $x=p$, $x=q$와 $x$축 및 곡선 $y=\log_a x$로 둘러싸인 부분을 곡선 $y=\log_b x$가 두 부분 A와 B로 나눈다. A와 B의 넓이를 각각 $\alpha$, $\beta$라 할 때, $\dfrac{\alpha}{\beta}$의 값은? (단, $1 < a < b$, $1 < p < q$)

① $\left(\dfrac{b}{a}-1\right)(q-p)$ ② $\dfrac{a}{b}-1$ ③ $\log_a b - 1$
④ $\log_b a - 1$ ⑤ $(q-p)\log_b a$

> [!summary]- 풀이
>
> **A의 넓이 $\alpha$** (두 로그함수 사이):
>
> $$\alpha = \int_{p}^{q} \left(\frac{\ln x}{\ln a} - \frac{\ln x}{\ln b}\right) dx = \frac{1}{\ln a}\int_{p}^{q}\ln x\, dx - \frac{1}{\ln b}\int_{p}^{q}\ln x\, dx$$
>
> **B의 넓이 $\beta$** ($y = \log_b x$와 $x$축 사이):
>
> $$\beta = \int_{p}^{q} \frac{\ln x}{\ln b}\, dx = \frac{1}{\ln b}\int_{p}^{q}\ln x\, dx$$
>
> **비율 계산**: $\int_{p}^{q}\ln x\, dx = K$로 놓으면
>
> $$\alpha = \frac{K}{\ln a} - \frac{K}{\ln b}, \quad \beta = \frac{K}{\ln b}$$
>
> $$\frac{\alpha}{\beta} = \frac{\dfrac{K}{\ln a} - \dfrac{K}{\ln b}}{\dfrac{K}{\ln b}} = \frac{\ln b}{\ln a} - 1 = \log_a b - 1$$
>
> **정답: ③ $\log_a b - 1$**

---

### 예제 392

곡선 $y = 3\sqrt{x-9}$와 이 곡선 위의 점 $(18,\ 9)$에서의 접선 및 $x$축으로 둘러싸인 영역의 넓이를 구하시오.

> [!summary]- 풀이
>
> **접선 방정식 구하기:**
>
> $$y = 3(x-9)^{\frac{1}{2}} \implies y' = 3 \cdot \frac{1}{2\sqrt{x-9}} = \frac{3}{2\sqrt{x-9}}$$
>
> $x = 18$에서의 기울기:
>
> $$y'_{x=18} = \frac{3}{2\sqrt{18-9}} = \frac{3}{2 \cdot 3} = \frac{1}{2}$$
>
> 점 $(18, 9)$를 지나고 기울기 $\dfrac{1}{2}$인 접선:
>
> $$y - 9 = \frac{1}{2}(x-18) \implies y_{\tan} = \frac{1}{2}x$$
>
> **넓이 계산** (삼각형 넓이 - 곡선 아래 넓이):
>
> 접선 $y = \dfrac{1}{2}x$는 원점을 지나고, 곡선은 $x=9$에서 $y=0$이다.
>
> $$S = \frac{1}{2} \cdot 18 \cdot 9 - \int_{9}^{18} 3\sqrt{x-9}\, dx$$
>
> $$= 81 - 3\left[\frac{2}{3}(x-9)^{\frac{3}{2}}\right]_{9}^{18}$$
>
> $$= 81 - 2\left[(x-9)^{\frac{3}{2}}\right]_{9}^{18}$$
>
> $$= 81 - 2\left[27 - 0\right] = 81 - 54 = \boxed{27}$$

---

### 예제 393

![[images/04-integral/exer393.png]]

함수 $f(x) = e^{-x}$과 자연수 $n$에 대하여 점 $P_n$, $Q_n$을 각각 $P_n(n,\ f(n))$, $Q_n(n+1,\ f(n))$이라 하자. 삼각형 $P_n P_{n+1} Q_n$의 넓이를 $A_n$, 선분 $P_n P_{n+1}$과 함수 $y=f(x)$의 그래프로 둘러싸인 도형의 넓이를 $B_n$이라 할 때, 보기에서 옳은 것을 모두 고른 것은?

$$\text{ㄱ.}\ \int_{n}^{n+1}f(x)\,dx = f(n) - (A_n + B_n)$$

$$\text{ㄴ.}\ \sum_{n=1}^{\infty} A_n = \frac{1}{2e}$$

$$\text{ㄷ.}\ \sum_{n=1}^{\infty} B_n = \frac{3-e}{2e(e-1)}$$

① ㄱ　　② ㄱ, ㄴ　　③ ㄱ, ㄷ　　④ ㄴ, ㄷ　　**⑤ ㄱ, ㄴ, ㄷ**

> [!summary]- 풀이
>
> **ㄱ 검증:**
>
> 그림에서 높이 $f(n)$인 직사각형의 넓이 = (정적분) + (삼각형 $A_n$) + (곡선 사이 $B_n$)이므로:
>
> $$f(n) = \int_{n}^{n+1}f(x)\,dx + A_n + B_n$$
>
> $$\therefore \int_{n}^{n+1}f(x)\,dx = f(n) - (A_n + B_n) \quad \checkmark$$
>
> **ㄴ 검증:**
>
> $A_n$은 삼각형 $P_n P_{n+1} Q_n$의 넓이로, 밑변 $= 1$, 높이 $= f(n) - f(n+1)$:
>
> $$A_n = \frac{1}{2}(e^{-n} - e^{-(n+1)})$$
>
> 이는 망원급수(Telescoping series)이므로:
>
> $$\sum_{n=1}^{\infty} A_n = \frac{1}{2}(e^{-1} - e^{-2}) + \frac{1}{2}(e^{-2} - e^{-3}) + \cdots = \frac{1}{2}e^{-1} = \frac{1}{2e} \quad \checkmark$$
>
> **ㄷ 검증:**
>
> ㄱ에서 $B_n = f(n) - A_n - \int_{n}^{n+1}f(x)\,dx$이므로:
>
> $$\sum_{n=1}^{\infty} B_n = \sum_{n=1}^{\infty} f(n) - \sum_{n=1}^{\infty} A_n - \int_{1}^{\infty} f(x)\,dx$$
>
> - $\displaystyle\sum_{n=1}^{\infty} e^{-n} = \frac{e^{-1}}{1-e^{-1}} = \frac{1}{e-1}$
>
> - $\displaystyle\sum_{n=1}^{\infty} A_n = \frac{1}{2e}$ (ㄴ에서)
>
> - $\displaystyle\int_{1}^{\infty} e^{-x}\,dx = \left[-e^{-x}\right]_{1}^{\infty} = \frac{1}{e}$
>
> $$\sum_{n=1}^{\infty} B_n = \frac{1}{e-1} - \frac{1}{2e} - \frac{1}{e} = \frac{1}{e-1} - \frac{3}{2e}$$
>
> 통분: $\displaystyle\frac{2e - 3(e-1)}{2e(e-1)} = \frac{3-e}{2e(e-1)} \quad \checkmark$
>
> **ㄱ, ㄴ, ㄷ 모두 참 → 정답: ⑤**

---

### 예제 394

자연수 $n$에 대하여 구간 $[0,\ \pi]$에서 두 곡선 $y = \dfrac{1}{n}\sin x$, $y = \dfrac{1}{n+1}\sin x$로 둘러싸인 부분의 넓이를 $S_n$이라 할 때, $\displaystyle\lim_{n \to \infty}\sum_{k=1}^{n} S_k$의 값은?

① $1$ ② $\sqrt{2}$ ③ $2$ ④ $\dfrac{\pi}{2}$ ⑤ $\pi$

> [!summary]- 풀이
>
> 구간 $[0, \pi]$에서 $\sin x \geq 0$이므로 $\dfrac{1}{n}\sin x \geq \dfrac{1}{n+1}\sin x$이다.
>
> $$S_n = \int_{0}^{\pi}\left(\frac{1}{n} - \frac{1}{n+1}\right)\sin x\, dx = \left(\frac{1}{n} - \frac{1}{n+1}\right)\int_{0}^{\pi}\sin x\, dx$$
>
> $$= \left(\frac{1}{n} - \frac{1}{n+1}\right)\left[-\cos x\right]_{0}^{\pi} = \left(\frac{1}{n} - \frac{1}{n+1}\right) \cdot 2$$
>
> 망원급수:
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n} S_k = \lim_{n \to \infty} 2\sum_{k=1}^{n}\left(\frac{1}{k} - \frac{1}{k+1}\right) = \lim_{n \to \infty} 2\left(1 - \frac{1}{n+1}\right) = 2$$
>
> **정답: ③ 2**

---

### 예제 395

자연수 $n$에 대하여 구간 $[(n-1)\pi,\ n\pi]$에서 곡선 $y = \left(\dfrac{1}{2}\right)^n \sin x$와 $x$축으로 둘러싸인 부분의 넓이를 $S_n$이라 하자. $\displaystyle\sum_{n=1}^{\infty} S_n = \alpha$일 때, $50\alpha$의 값을 구하시오.

> [!summary]- 풀이
>
> 구간 $[(n-1)\pi, n\pi]$에서 $|\sin x|$의 적분은 구간 $[0, \pi]$에서 $\sin x$의 적분과 같다.
>
> $$S_n = \left(\frac{1}{2}\right)^n \int_{(n-1)\pi}^{n\pi}|\sin x|\, dx = \left(\frac{1}{2}\right)^n \cdot 2 = \left(\frac{1}{2}\right)^{n-1}$$
>
> ※ $\displaystyle\int_{0}^{\pi}\sin x\, dx = \left[-\cos x\right]_{0}^{\pi} = 1-(-1) = 2$
>
> 등비급수 (첫째항 1, 공비 $\dfrac{1}{2}$):
>
> $$\alpha = \sum_{n=1}^{\infty}\left(\frac{1}{2}\right)^{n-1} = \frac{1}{1 - \dfrac{1}{2}} = 2$$
>
> $$50\alpha = 50 \times 2 = \boxed{100}$$

---

### 예제 396

각 항이 양수인 수열 $\{a_n\}$은 모든 자연수 $n$에 대하여 다음 두 조건을 만족한다.

> (가) $a_n > a_{n+1}$
>
> (나) 곡선 $y = \dfrac{1}{x}$과 두 직선 $x = a_{n+1}$, $x = a_n$ 및 $x$축으로 둘러싸인 부분의 넓이는 $1$이다.

$a_1 = 2$일 때, $\displaystyle\sum_{n=1}^{\infty} a_n$의 값은? (단, $e$는 자연로그의 밑이다.)

① $\dfrac{e}{e-1}$ ② $\dfrac{2e}{e-1}$ ③ $\dfrac{2e+1}{e}$ ④ $\dfrac{2e+3}{e}$ ⑤ $\dfrac{3e+1}{2e+1}$

> [!summary]- 풀이
>
> ![[images/04-integral/exer396.png]]
>
> 조건 (나)에서 ($a_n > a_{n+1} > 0$이므로):
>
> $$\int_{a_{n+1}}^{a_n} \frac{1}{x}\, dx = \left[\ln x\right]_{a_{n+1}}^{a_n} = \ln\frac{a_n}{a_{n+1}} = 1$$
>
> $$\therefore \frac{a_n}{a_{n+1}} = e \implies a_{n+1} = \frac{1}{e} a_n$$
>
> 즉, 수열 $\{a_n\}$은 첫째항 $a_1 = 2$, 공비 $\dfrac{1}{e}$인 등비수열이다.
>
> $$\sum_{n=1}^{\infty} a_n = \frac{2}{1 - \dfrac{1}{e}} = \frac{2e}{e-1}$$
>
> **정답: ② $\dfrac{2e}{e-1}$**

---

### 예제 397

![[images/04-integral/exer397.png]]

그림과 같이 곡선 $y = \ln x$ 위의 두 점 $P_n(e^n,\ n)$, $P_{n+1}(e^{n+1},\ n+1)$을 지나는 직선과 곡선으로 둘러싸인 도형의 넓이를 $S_n$이라 하자. 이 때, $\displaystyle\sum_{n=1}^{\infty}\dfrac{1}{S_n}$의 값은? (단, $n$은 자연수이다.)

① $\dfrac{1}{2e(e-1)}$ ② $\dfrac{1}{2e(e-2)}$ ③ $\dfrac{2}{(4-e)(e-2)}$
④ $\dfrac{2}{(3-e)(e-1)}$ ⑤ $\dfrac{2}{(e-1)(e-2)}$

> [!summary]- 풀이
>
> **방법 1: 직접 적분**
>
> 두 점 $P_n(e^n, n)$, $P_{n+1}(e^{n+1}, n+1)$을 잇는 직선의 기울기:
>
> $$m = \frac{(n+1) - n}{e^{n+1} - e^n} = \frac{1}{e^n(e-1)}$$
>
> $S_n$ = (직선 아래 사다리꼴 넓이) - (곡선 아래 넓이)
>
> $$S_n = \frac{1}{2}(n + n+1)(e^{n+1} - e^n) - \int_{e^n}^{e^{n+1}}\ln x\, dx$$
>
> $\int \ln x\, dx = x\ln x - x + C$를 이용하면:
>
> $$\int_{e^n}^{e^{n+1}}\ln x\, dx = \left[x\ln x - x\right]_{e^n}^{e^{n+1}}$$
> $$= e^{n+1}(n+1) - e^{n+1} - (n \cdot e^n - e^n)$$
> $$= n e^{n+1} + e^n - \frac{1}{2}e^{n+1} \cdot \text{(전개 후 정리)}$$
>
> 정리하면:
>
> $$S_n = \frac{3-e}{2} \cdot e^n$$
>
> **방법 2: 역함수 이용** ($y = \ln x$의 역함수는 $y = e^x$)
>
> $$S_n = \frac{1}{2}(2e^n + e^{n+1}) \cdot 1 - \int_{n}^{n+1}e^x\, dx$$
>
> $$= \frac{e^n + e^{n+1}}{2} - \left[e^x\right]_{n}^{n+1}$$
>
> $$= \frac{e^n}{2} + \frac{e^{n+1}}{2} - e^{n+1} + e^n = \frac{3}{2}e^n - \frac{1}{2}e^{n+1}$$
>
> $$= \frac{1}{2}e^n(3-e)$$
>
> **급수 계산:**
>
> $$\sum_{n=1}^{\infty}\frac{1}{S_n} = \frac{2}{3-e}\sum_{n=1}^{\infty}\left(\frac{1}{e}\right)^n = \frac{2}{3-e} \cdot \frac{\dfrac{1}{e}}{1 - \dfrac{1}{e}} = \frac{2}{3-e} \cdot \frac{1}{e-1} = \frac{2}{(3-e)(e-1)}$$
>
> **정답: ④ $\dfrac{2}{(3-e)(e-1)}$**

---

## 관련 주제

- [[57-area-integral-3|넓이와 적분(3)]]
- [[59-transcendental-area-2|초월함수의 넓이(2)]]
- [[45-integration-by-parts|부분적분]]
- [[44-integration-substitution-1|치환적분]]

---

**학습 포인트:**
1. 두 로그함수 사이의 넓이는 $\int \ln x\, dx$의 비율로 분리하여 계산한다.
2. 초월함수 넓이 + 급수가 결합된 문제는 망원급수(Telescoping), 등비급수를 적극 활용한다.
3. 역함수 이용: $y = \ln x$의 역함수 $y = e^x$로 y축 방향 적분으로 전환하면 계산이 단순해진다.
4. $\int_0^\pi \sin x\, dx = 2$는 자주 쓰이는 값이므로 암기한다.
