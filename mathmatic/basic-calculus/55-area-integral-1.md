---
id: 7f3a2c81-9d4e-4b7f-a1c5-3e8f6d0b2a94
aliases:
  - 정적분과 함수의 결정
  - 넓이와 적분(1)
  - 적분방정식
tags:
  - 정적분
  - 함수의결정
  - 적분방정식
  - 치환적분
  - 부분적분
  - 넓이와적분
pages: 168-171
subject: 대학기초수학
title: 정적분과 함수의 결정, 넓이와 적분(1)
topics:
  - 정적분으로 정의된 함수 결정
  - 상수 치환법 (k 치환)
  - 연립 적분방정식
  - 부분적분을 이용한 함수 결정
---

# 55강. 정적분과 함수의 결정, 넓이와 적분(1)

## 1. 정적분과 함수의 결정

### Thm (53): 정적분과 함수의 결정

$$f(x) = g(x) + p\int_{a}^{b} f(t)\,dt \text{ 에서 } f(x) \text{를 결정하려면}$$

**풀이 전략:**

① $\displaystyle\int_{a}^{b} f(t)\,dt = k$ 로 치환

② $f(x) = g(x) + pk$ 임을 이용하여 $k = \displaystyle\int_{a}^{b}(g(t) + pk)\,dt$ 를 푼다.

> [!note] 핵심 아이디어
> 정적분 $\displaystyle\int_a^b f(t)\,dt$ 는 **상수**이므로 $k$로 놓을 수 있다.
> $f(x)$를 $k$로 표현한 뒤, 다시 $k$에 대한 방정식을 세워 $k$를 구한다.

---

## 2. 예제

### 예제 370

$$f(x) = e^{x} + \int_{0}^{2} f(t)\,dt \text{ 일 때 } f(1)\text{의 값을 구하여라.}$$

> [!summary]- 풀이
> $\displaystyle\int_{0}^{2} f(t)\,dt = k$ 로 놓으면
>
> $$f(x) = e^{x} + k$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{0}^{2}(e^{t} + k)\,dt = \left[e^{t} + kt\right]_{0}^{2}$$
>
> $$= e^{2} + 2k - e^{0} - 0 = e^{2} + 2k - 1$$
>
> $$k = e^{2} + 2k - 1$$
>
> $$-k = e^{2} - 1$$
>
> $$k = 1 - e^{2}$$
>
> 따라서
>
> $$f(1) = e^{1} + k = e + 1 - e^{2}$$

---

### 예제 371

$$\text{함수 } f(x)\text{가 } f(x) = \cos 2x + 4x + \int_{0}^{\pi} f(t)\,dt \text{ 일 때 } f(\pi)\text{의 값을 구하여라.}$$

> [!summary]- 풀이
> $\displaystyle\int_{0}^{\pi} f(t)\,dt = k$ 로 놓으면
>
> $$f(x) = \cos 2x + 4x + k$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{0}^{\pi}(\cos 2t + 4t + k)\,dt = \left[\frac{1}{2}\sin 2t + 2t^{2} + kt\right]_{0}^{\pi}$$
>
> $$= 0 + 2\pi^{2} + k\pi - 0 = 2\pi^{2} + k\pi$$
>
> $$k = 2\pi^{2} + k\pi$$
>
> $$k(1 - \pi) = 2\pi^{2}$$
>
> $$k = \frac{2\pi^{2}}{1 - \pi}$$
>
> 따라서
>
> $$f(\pi) = \cos 2\pi + 4\pi + \frac{2\pi^{2}}{1-\pi} = 1 + 4\pi + \frac{2\pi^{2}}{1-\pi}$$

---

### 예제 372

이차함수 $f(x)$가

$$f(x) = \frac{12}{7}x^{2} - 2x\int_{1}^{2}f(t)\,dt + \left(\int_{1}^{2}f(t)\,dt\right)^{2}$$

일 때, $10\displaystyle\int_{1}^{2}f(x)\,dx$ 의 값을 구하시오.

> [!summary]- 풀이
> $\displaystyle\int_{1}^{2}f(t)\,dt = k$ 로 놓으면
>
> $$f(x) = \frac{12}{7}x^{2} - 2xk + k^{2}$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{1}^{2}\left(\frac{12}{7}t^{2} - 2tk + k^{2}\right)dt = \left[\frac{4}{7}t^{3} - kt^{2} + k^{2}t\right]_{1}^{2}$$
>
> $$= \frac{4}{7}\cdot 8 - 4k + 2k^{2} - \frac{4}{7} + k - k^{2}$$
>
> $$= 4 - 3k + k^{2}$$
>
> 따라서
>
> $$k = 4 - 3k + k^{2}$$
>
> $$k^{2} - 4k + 4 = 0$$
>
> $$(k-2)^{2} = 0 \implies k = 2$$
>
> $$10\int_{1}^{2}f(x)\,dx = 10k = \boxed{20}$$

---

### 예제 373

함수 $f(x)$가 $f(x) = x^{5}+x^{4}+x^{3}+x^{2}+x+\displaystyle\int_{-1}^{1}f(t)\,dt$ 를 만족할 때, $f(0)$의 값은?

① $-\dfrac{4}{5}$ ② $-\dfrac{5}{7}$ ③ $-\dfrac{16}{15}$ ④ $\dfrac{7}{9}$ ⑤ $\dfrac{15}{23}$

> [!summary]- 풀이
> $\displaystyle\int_{-1}^{1}f(t)\,dt = k$ 로 놓으면
>
> $$f(x) = x^{5}+x^{4}+x^{3}+x^{2}+x+k$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{-1}^{1}(t^{5}+t^{4}+t^{3}+t^{2}+t+k)\,dt$$
>
> $t^5, t^3, t$는 **기함수**, $t^4, t^2, k$는 **우함수**이므로 우함수 부분만 남는다:
>
> $$k = 2\int_{0}^{1}(t^{4}+t^{2}+k)\,dt = 2\left[\frac{1}{5}t^{5}+\frac{1}{3}t^{3}+kt\right]_{0}^{1}$$
>
> $$= 2\left(\frac{1}{5}+\frac{1}{3}+k\right) = \frac{2}{5}+\frac{2}{3}+2k$$
>
> $$k - 2k = \frac{2}{5}+\frac{2}{3} = \frac{6}{15}+\frac{10}{15} = \frac{16}{15}$$
>
> $$-k = \frac{16}{15} \implies k = -\frac{16}{15}$$
>
> $$f(0) = k = \boxed{-\frac{16}{15}} \quad \text{③}$$

---

### 예제 374

함수 $f(x)$, $g(x)$가

$$f(x) = 3x^{2}\int_{0}^{1}g(x)\,dx, \quad g(x) = 1 + 2\int_{0}^{x}f(t)\,dt$$

를 만족할 때, $f(1)+g(1)$의 값은?

① $11$ ② $13$ ③ $15$ ④ $17$ ⑤ $19$

> [!summary]- 풀이
> $\displaystyle\int_{0}^{1}g(x)\,dx = k$ 로 놓으면
>
> $$f(x) = 3kx^{2}$$
>
> $g(x) = 1 + 2\displaystyle\int_{0}^{x}f(t)\,dt$ 의 양변을 $x$로 미분하면
>
> $$g'(x) = 2f(x) = 6kx^{2}$$
>
> 적분하면
>
> $$g(x) = 2kx^{3} + C$$
>
> 초기조건: $g(0) = 1 + 0 = 1$ 이므로 $C = 1$
>
> $$g(x) = 2kx^{3} + 1$$
>
> $k$의 정의에 대입하면
>
> $$k = \int_{0}^{1}(2kx^{3}+1)\,dx = \left[\frac{k}{2}x^{4}+x\right]_{0}^{1} = \frac{k}{2}+1$$
>
> $$k - \frac{k}{2} = 1 \implies \frac{k}{2} = 1 \implies k = 2$$
>
> 따라서
>
> $$f(x) = 6x^{2}, \quad g(x) = 4x^{3}+1$$
>
> $$f(1)+g(1) = 6 + 4 + 1 = \boxed{11} \quad \text{①}$$

---

### 예제 375

다음 식을 만족시키는 함수 $f(x)$를 구하여라.

$$f(x) = x + \int_{0}^{\pi}f(t)\sin t\,dt$$

> [!summary]- 풀이
> $\displaystyle\int_{0}^{\pi}f(t)\sin t\,dt = k$ 로 놓으면
>
> $$f(x) = x + k$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{0}^{\pi}(t+k)\sin t\,dt$$
>
> **부분적분** 적용: $u = t+k$, $dv = \sin t\,dt$ 로 놓으면 $du = dt$, $v = -\cos t$
>
> $$k = \left[-(t+k)\cos t\right]_{0}^{\pi} + \int_{0}^{\pi}\cos t\,dt$$
>
> $$= \left[-(t+k)\cos t + \sin t\right]_{0}^{\pi}$$
>
> $$= \left(-(\pi+k)\cos\pi + \sin\pi\right) - \left(-(0+k)\cos 0 + \sin 0\right)$$
>
> $$= (\pi+k) + 0 - (-k \cdot 1 + 0)$$
>
> $$= \pi + k + k = \pi + 2k$$
>
> $$k = \pi + 2k \implies k = -\pi$$
>
> $$\therefore f(x) = x - \pi$$

---

### 예제 376

함수 $f(x)$에 대하여 $f(x) = x - \displaystyle\int_{1}^{e}\frac{f(t)}{t}\,dt$ 가 성립할 때, $f(e)$의 값은?  
(단, $e$는 자연로그의 밑이다.)

① $-\dfrac{e+1}{2}$ ② $\dfrac{e-1}{2}$ ③ $\dfrac{e+1}{2}$ ④ $e-1$ ⑤ $e-2$

> [!summary]- 풀이
> $\displaystyle\int_{1}^{e}\frac{f(t)}{t}\,dt = k$ 로 놓으면
>
> $$f(x) = x - k$$
>
> 이를 $k$의 정의에 대입하면
>
> $$k = \int_{1}^{e}\frac{t-k}{t}\,dt = \int_{1}^{e}\left(1 - \frac{k}{t}\right)dt$$
>
> $$= \left[t - k\ln|t|\right]_{1}^{e}$$
>
> $$= (e - k\ln e) - (1 - k\ln 1) = e - k - 1 + 0$$
>
> $$k = e - k - 1$$
>
> $$2k = e - 1 \implies k = \frac{e-1}{2}$$
>
> $$f(x) = x - \frac{e-1}{2}$$
>
> $$f(e) = e - \frac{e-1}{2} = \frac{2e - e + 1}{2} = \boxed{\frac{e+1}{2}} \quad \text{③}$$

---

## 관련 주제

- [[54-derivative-integral-2|54강. 미분과 정적분(2), 극한과 정적분]]
- [[56-area-integral-2|56강. 넓이와 적분(2)]]

---

**학습 포인트:**

1. 정적분 $\displaystyle\int_a^b f(t)\,dt$ 는 **상수**임을 인식하고 $k$로 치환한다.
2. $f(x)$를 $k$로 표현한 뒤, 원래 정적분에 대입하여 $k$에 대한 방정식을 세운다.
3. 연립 적분방정식(예제 374)은 미분을 활용해 $g'(x) = 2f(x)$ 관계를 이용한다.
4. 피적분함수에 $f(t)\sin t$ 형태가 있으면 **부분적분**을 적용한다.
5. 기함수와 우함수의 대칭성을 이용하면 계산을 크게 단순화할 수 있다(예제 373).
