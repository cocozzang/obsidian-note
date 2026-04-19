---
id: a9e1c374-2d58-4f07-b5c0-3e8f1a6d4b27
aliases:
  - 이상적분, 간단한 이중적분
  - 이상적분
  - 이중적분
  - 중적분
tags:
  - 이상적분
  - 이중적분
  - 중적분
  - 무한구간적분
  - 누적적분
  - 반복적분
pages: 210-213
subject: 대학기초수학
title: 이상적분, 간단한 이중적분
topics:
  - 이상적분 정의와 계산
  - 무한구간 이상적분
  - 이중적분 - 직사각형 영역
  - 이중적분 - 일반 영역
  - 반복적분 계산 기법
---

# 이상적분, 간단한 이중적분

이번 강의는 대학 미적분 과정의 마지막 주제로, **이상적분**과 **이중적분**을 다룬다. 이상적분은 적분 구간이 무한대로 확장된 경우로, 극한을 이용해 정의한다. 이중적분은 2변수 함수를 2차원 영역에서 적분하는 것으로, 반복적분(누적 적분)으로 계산한다. 이 강의에서는 개념과 계산법의 핵심만 파악하며, 자세한 내용은 대학미적분학에서 다룬다.

---

## 1. Def (6): 이상적분

함수 $f : [a,\ \infty) \to \mathbb{R}$가 임의의 $b \in (a,\ \infty)$에 대하여 구간 $[a,\ b]$에서 리만적분가능할 때,

$$\int_a^\infty f(x)\,dx = \lim_{b \to \infty}\int_a^b f(x)\,dx$$

이 극한이 존재하면 이 값을 $[a,\ \infty)$에서 $f$의 **이상적분**이라 한다.

마찬가지로 아래쪽 끝이 $-\infty$인 경우:

$$\int_{-\infty}^b f(x)\,dx = \lim_{a \to -\infty}\int_a^b f(x)\,dx$$

양쪽 모두 무한대인 경우는 임의의 $c$를 기준으로 분리:

$$\int_{-\infty}^\infty f(x)\,dx = \int_{-\infty}^c f(x)\,dx + \int_c^\infty f(x)\,dx$$

> [!note] 이상적분의 수렴과 발산
> 극한값이 존재하면 **수렴(convergent)**, 존재하지 않으면 **발산(divergent)**이라 한다.
> $\int_{-\infty}^\infty f(x)\,dx$를 계산할 때, 반드시 두 구간으로 **분리하여** 각각 극한을 취해야 한다.
> "대칭성"으로 $\lim_{b\to\infty}\int_{-b}^{b}f(x)\,dx$를 쓰는 것은 주값(Cauchy principal value)으로, 이상적분과 다른 개념이다.

---

## 2. Thm (59): 일반 영역에서의 중적분 유형별 정리 ①

공간좌표에서 정의되는 곡면 $z = f(x,\ y)$에 대하여 $z = f(x,\ y)$가 **직사각형 영역** $D = [a,b] \times [c,d]$상에서 연속이면

$$\iint_D f(x,\ y)\,dA = \int_a^b\int_c^d f(x,\ y)\,dy\,dx = \int_c^d\int_a^b f(x,\ y)\,dx\,dy$$

이 성립한다 (적분 순서 교환 가능).

> [!tip] 중적분 계산 요령
> **편미분처럼** — 안쪽 적분 시, 적분 대상이 아닌 변수는 **상수**로 취급한다.
> 예: $\int_c^d f(x,y)\,dy$ 계산 시, $x$는 상수로 취급하고 $y$에 대해서만 적분.

---

## 3. Thm (60): 일반 영역에서의 중적분 유형별 정리 ②

**유형 1** — $y$가 $x$의 함수로 경계가 정해진 경우 ($g_1(x) \leq y \leq g_2(x)$):

$$\iint_D f(x,\ y)\,dA = \int_a^b\int_{g_1(x)}^{g_2(x)} f(x,\ y)\,dy\,dx$$

**유형 2** — $x$가 $y$의 함수로 경계가 정해진 경우 ($h_1(y) \leq x \leq h_2(y)$):

$$\iint_D f(x,\ y)\,dA = \int_c^d\int_{h_1(y)}^{h_2(y)} f(x,\ y)\,dx\,dy$$

> [!note] 적분 순서 선택
> 영역 $D$가 두 곡선 사이의 영역일 때, 어느 변수를 먼저 적분할지는 경계가 어느 변수의 함수로 표현되느냐에 따라 결정한다. 계산이 더 단순해지는 순서를 선택하는 것이 효율적이다.

---

## 4. 예제

### 예제 445

$$\int_{-\infty}^{-2}\frac{2}{x^2-1}\,dx$$

> [!summary]- 풀이
>
> **부분분수 분해**:
>
> $$\frac{2}{x^2-1} = \frac{2}{(x-1)(x+1)} = \frac{1}{x-1} - \frac{1}{x+1}$$
>
> **이상적분 정의 적용**:
>
> $$= \lim_{b \to -\infty}\int_b^{-2}\left(\frac{1}{x-1} - \frac{1}{x+1}\right)dx$$
>
> $$= \lim_{b \to -\infty}\left[\ln|x-1| - \ln|x+1|\right]_b^{-2}$$
>
> $$= \lim_{b \to -\infty}\left[\ln\left|\frac{x-1}{x+1}\right|\right]_b^{-2}$$
>
> $x = -2$ 대입: $\ln\left|\dfrac{-3}{-1}\right| = \ln 3$
>
> $x = b \to -\infty$ 대입: $\ln\left|\dfrac{b-1}{b+1}\right| \to \ln 1 = 0$
>
> $$= \ln 3 - 0 = \boxed{\ln 3}$$

---

### 예제 446

$$\int_{-\infty}^{\infty}\frac{2x}{(x^2+1)^2}\,dx$$

> [!summary]- 풀이
>
> **두 구간으로 분리**:
>
> $$= \int_{-\infty}^{0}\frac{2x}{(x^2+1)^2}\,dx + \int_{0}^{\infty}\frac{2x}{(x^2+1)^2}\,dx$$
>
> **치환**: $t = x^2 + 1$, $dt = 2x\,dx$
>
> - $x: 0 \to \infty$일 때 $t: 1 \to \infty$
> - $x: -\infty \to 0$일 때 $t: \infty \to 1$
>
> $$= \int_{\infty}^{1}\frac{1}{t^2}\,dt + \int_{1}^{\infty}\frac{1}{t^2}\,dt$$
>
> $$= -\int_{1}^{\infty}\frac{1}{t^2}\,dt + \int_{1}^{\infty}\frac{1}{t^2}\,dt = \boxed{0}$$
>
> **직관적 이해**: 피적분함수 $\dfrac{2x}{(x^2+1)^2}$는 **기함수** (홀함수) → $\int_{-\infty}^\infty (\text{기함수})\,dx = 0$

---

### 예제 447

$$\int_{-\infty}^{0} xe^x\,dx$$

> [!summary]- 풀이
>
> **부분적분 결과 활용**: $\int xe^x\,dx = xe^x - e^x + C$
>
> $$= \lim_{b \to -\infty}\left[xe^x - e^x\right]_b^{0}$$
>
> $x = 0$ 대입: $0 \cdot 1 - 1 = -1$
>
> $x = b \to -\infty$ 대입: $be^b - e^b = e^b(b-1)$
>
> $\lim_{b \to -\infty} e^b(b-1) = 0$ ($e^b$가 $|b|$보다 훨씬 빠르게 $0$으로 감)
>
> $$= -1 - 0 = \boxed{-1}$$

---

### 예제 448

$$\int_{-\infty}^{\ln 2}\frac{\pi}{4}e^{2x}\,dx$$

> [!summary]- 풀이
>
> $$= \frac{\pi}{4}\lim_{b \to -\infty}\left[\frac{1}{2}e^{2x}\right]_b^{\ln 2} = \frac{\pi}{8}\left(e^{2\ln 2} - \lim_{b \to -\infty}e^{2b}\right)$$
>
> $e^{2\ln 2} = (e^{\ln 2})^2 = 2^2 = 4$, $\lim_{b \to -\infty}e^{2b} = 0$
>
> $$= \frac{\pi}{8}(4 - 0) = \boxed{\frac{\pi}{2}}$$

---

### 예제 449

$$\int_0^\infty x^2 e^{-\frac{x}{2}}\,dx \text{ 를 계산하시오.}$$

① $2$ $\quad$ ② $4$ $\quad$ ③ $16$ $\quad$ ④ $25$

> [!summary]- 풀이
>
> **부분적분을 반복** 적용 ($\int x^n e^{ax}dx$ 패턴):
>
> $e^{-x/2}$의 반복 적분: $\int e^{-x/2}dx = -2e^{-x/2}$, $\int(-2e^{-x/2})dx = 4e^{-x/2}$, $\int 4e^{-x/2}dx = -8e^{-x/2}$
>
> 표 형식 부분적분:
>
> $$\int x^2 e^{-x/2}dx = x^2\cdot(-2e^{-x/2}) - 2x\cdot(4e^{-x/2}) + 2\cdot(-8e^{-x/2}) + C$$
>
> $$= e^{-x/2}\left(-2x^2 - 8x - 16\right) + C$$
>
> 이상적분 계산:
>
> $$= \left[e^{-x/2}(-2x^2 - 8x - 16)\right]_0^\infty$$
>
> $x \to \infty$: $\lim_{x \to \infty}\dfrac{-2x^2 - 8x - 16}{e^{x/2}} = 0$ (지수함수가 다항식보다 빠르게 발산)
>
> $x = 0$: $e^0 \cdot (-0 - 0 - 16) = -16$
>
> $$= 0 - (-16) = \boxed{16}$$
>
> **정답: ③**

---

### 예제 450

$$\int_{-\infty}^{\ln 2}\frac{1}{4}e^{2x}\,dx \text{ 를 계산하시오.}$$

① $\dfrac{1}{2}$ $\quad$ ② $1$ $\quad$ ③ $\dfrac{3}{2}$ $\quad$ ④ $2$

> [!summary]- 풀이
>
> $$= \frac{1}{4}\lim_{b \to -\infty}\left[\frac{1}{2}e^{2x}\right]_b^{\ln 2} = \frac{1}{8}\left(e^{2\ln 2} - 0\right)$$
>
> $e^{2\ln 2} = 4$
>
> $$= \frac{1}{8} \cdot 4 = \boxed{\frac{1}{2}}$$
>
> **정답: ①**

---

### 예제 451

$\displaystyle\int_0^3\int_0^1\sqrt{x+y}\,dx\,dy$의 값은?

① $\dfrac{4}{15}(32+9\sqrt{3})$ $\quad$ ② $\dfrac{4}{15}(32-9\sqrt{3})$ $\quad$ ③ $\dfrac{4}{15}(31+9\sqrt{3})$ $\quad$ ④ $\dfrac{4}{15}(31-9\sqrt{3})$

> [!summary]- 풀이
>
> **안쪽 적분** (x에 대해, y는 상수 취급):
>
> $$\int_0^1(x+y)^{1/2}\,dx = \left[\frac{2}{3}(x+y)^{3/2}\right]_0^1 = \frac{2}{3}(1+y)^{3/2} - \frac{2}{3}y^{3/2}$$
>
> **바깥 적분** (y에 대해):
>
> $$\int_0^3\left[\frac{2}{3}(1+y)^{3/2} - \frac{2}{3}y^{3/2}\right]dy = \left[\frac{2}{3}\cdot\frac{2}{5}(1+y)^{5/2} - \frac{2}{3}\cdot\frac{2}{5}y^{5/2}\right]_0^3$$
>
> $$= \frac{4}{15}\left[(1+y)^{5/2} - y^{5/2}\right]_0^3$$
>
> $y=3$: $(4)^{5/2} - (3)^{5/2} = 2^5 - 9\sqrt{3} = 32 - 9\sqrt{3}$
>
> $y=0$: $(1)^{5/2} - 0 = 1$
>
> $$= \frac{4}{15}\left[(32 - 9\sqrt{3}) - 1\right] = \boxed{\frac{4}{15}(31 - 9\sqrt{3})}$$
>
> **정답: ④**

---

### 예제 452

$D$가 포물선들 $y = 2x^2$, $y = 1 + x^2$에 의해 유계된 영역이라 할 때, $\displaystyle\iint_D(x + 2y)\,dA$를 구하여라.

![[images/04-integral/exer452.png|400]]

> [!summary]- 풀이
>
> **교점 계산**: $2x^2 = 1 + x^2$ → $x^2 = 1$ → $x = \pm 1$
>
> 영역 $D$에서 $2x^2 \leq y \leq 1+x^2$, $-1 \leq x \leq 1$
>
> **안쪽 적분** (y에 대해):
>
> $$\int_{2x^2}^{1+x^2}(x+2y)\,dy = \left[xy + y^2\right]_{2x^2}^{1+x^2}$$
>
> $$= \left[x(1+x^2) + (1+x^2)^2\right] - \left[x\cdot 2x^2 + (2x^2)^2\right]$$
>
> $$= x + x^3 + 1 + 2x^2 + x^4 - 2x^3 - 4x^4$$
>
> $$= -3x^4 - x^3 + 2x^2 + x + 1$$
>
> **바깥 적분** (대칭 활용 — 홀함수 항 $-x^3, x$는 소거):
>
> $$\int_{-1}^{1}(-3x^4 - x^3 + 2x^2 + x + 1)\,dx = 2\int_0^1(-3x^4 + 2x^2 + 1)\,dx$$
>
> $$= 2\left[-\frac{3}{5}x^5 + \frac{2}{3}x^3 + x\right]_0^1 = 2\left(-\frac{3}{5} + \frac{2}{3} + 1\right)$$
>
> $$= 2\left(-\frac{9}{15} + \frac{10}{15} + \frac{15}{15}\right) = 2 \cdot \frac{16}{15} = \boxed{\frac{32}{15}}$$

---

### 예제 453

$$\int_1^{\ln 2}\int_0^{3y} e^{x+y}\,dx\,dy \text{ 의 값은?}$$

> [!summary]- 풀이
>
> **안쪽 적분** (x에 대해, y는 상수 취급):
>
> $$\int_0^{3y}e^{x+y}\,dx = \left[e^{x+y}\right]_0^{3y} = e^{3y+y} - e^{0+y} = e^{4y} - e^y$$
>
> **바깥 적분** (y에 대해):
>
> $$\int_1^{\ln 2}(e^{4y} - e^y)\,dy = \left[\frac{1}{4}e^{4y} - e^y\right]_1^{\ln 2}$$
>
> $y = \ln 2$: $\dfrac{1}{4}e^{4\ln 2} - e^{\ln 2} = \dfrac{1}{4}\cdot 16 - 2 = 4 - 2 = 2$
>
> $y = 1$: $\dfrac{1}{4}e^4 - e$
>
> $$= 2 - \left(\frac{e^4}{4} - e\right) = \boxed{2 + e - \frac{e^4}{4}}$$

---

## 관련 주제

- [[64-arc-length-2|속도와 거리 및 곡선의 길이(2)]]
- [[45-integration-by-parts|부분적분]]
- [[44-integration-substitution-1|치환적분(1)]]
- [[47-fundamental-theorem|정적분과 부정적분의 관계]]

---

**학습 포인트:**
1. **이상적분 정의**: $\int_a^\infty f\,dx = \lim_{b\to\infty}\int_a^b f\,dx$ — 극한이 존재해야 수렴
2. **$\int_{-\infty}^\infty$는 반드시 분리**: $c$를 기준으로 두 구간으로 나눠 각각 극한 취하기
3. **기함수의 이상적분**: 피적분함수가 기함수(홀함수)면 $\int_{-\infty}^\infty = 0$ (단, 각 부분이 수렴할 때)
4. **$\lim_{x\to\infty}\frac{x^n}{e^x} = 0$**: 지수함수가 다항함수보다 빠르게 발산 — 이상적분에서 자주 활용
5. **중적분 = 반복적분**: 안쪽부터 순서대로 계산, 적분 대상이 아닌 변수는 상수 취급
6. **홀짝성 활용**: $\int_{-a}^{a}(\text{기함수})\,dx = 0$, $\int_{-a}^{a}(\text{우함수})\,dx = 2\int_0^a$ — 계산 단축
