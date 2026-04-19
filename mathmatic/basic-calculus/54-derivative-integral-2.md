---
id: d4f1a892-3e7b-4c56-b0d2-8e9f1c2a5d37
aliases:
  - 54강 미분과 정적분(2)
  - 극한과 정적분
  - Thm52
  - 정적분 합성형 미분 심화
tags:
  - 정적분
  - 미분과정적분
  - 극한과정적분
  - 합성형미분
  - 로피탈
  - 역함수미분
  - 적분법
pages: 164-167
subject: 대학기초수학
title: 미분과 정적분(2), 극한과 정적분
topics:
  - 합성형 정적분 미분 (상한이 x의 함수)
  - 정적분 등식에서 f(x) 결정 심화
  - Thm52 극한과 정적분
  - 로피탈 정리와 정적분 극한
---

# 미분과 정적분(2), 극한과 정적분

## 1. 합성형 정적분 미분 심화

[[53-derivative-integral-1|53강]] Thm 51 (3)의 합성형 공식을 복잡한 함수에 적용한다.

$$\frac{d}{dx}\int_{h(x)}^{g(x)} f(t)\, dt = f(g(x))\cdot g'(x) - f(h(x))\cdot h'(x)$$

---

### 예제 358

연속함수 $f(x)$가 $\displaystyle\int_{0}^{x^2} f(t)\, dt = \sin^2\frac{\pi}{2}x$를 만족시킬 때, $f\!\left(\dfrac{1}{4}\right)$의 값은?

① $\dfrac{\pi}{4}$ ② $\dfrac{\pi}{2}$ ③ $\pi$ ④ $2\pi$ ⑤ $4\pi$

> [!summary]- 풀이
> 상한이 $g(x) = x^2$이므로 합성형 공식을 적용하여 양변 미분한다.
>
> $$2x \cdot f(x^2) = 2\sin\frac{\pi}{2}x \cdot \frac{\pi}{2}\cos\frac{\pi}{2}x$$
>
> $f\!\left(\dfrac{1}{4}\right)$을 구하려면 $x^2 = \dfrac{1}{4}$, 즉 $x = \dfrac{1}{2}$을 대입한다.
>
> $$2 \cdot \frac{1}{2} \cdot f\!\left(\frac{1}{4}\right) = 2\sin\frac{\pi}{4} \cdot \frac{\pi}{2}\cos\frac{\pi}{4}$$
>
> $$f\!\left(\frac{1}{4}\right) = 2 \cdot \frac{1}{\sqrt{2}} \cdot \frac{\pi}{2} \cdot \frac{1}{\sqrt{2}} = \frac{\pi}{2}$$
>
> **정답: ②**

---

### 예제 359

$\displaystyle\int_{-1}^{x} f(t)\, dt = xf(x) - x^3 e^x$일 때, $f(1)$의 값을 구하여라. (단, $x \neq 0$)

> [!summary]- 풀이
> **양변 미분** (우변에 곱의 미분 적용):
>
> $$f(x) = f(x) + xf'(x) - (x^3 e^x + 3x^2 e^x)$$
>
> 정리하면:
>
> $$xf'(x) = e^x(x^3 + 3x^2)$$
>
> $$f'(x) = e^x(x^2 + 3x)$$
>
> **$f(x)$ 구하기** — 부분적분:
>
> $$f(x) = \int e^x(x^2 + 3x)\, dx = e^x(x^2 + 3x) - e^x(2x + 3) + 2e^x + C$$
>
> **초기값 결정** — 원식에 $x = -1$ 대입 ($\int_{-1}^{-1} = 0$):
>
> $$0 = (-1)f(-1) - (-1)^3 e^{-1} = -f(-1) + e^{-1}$$
>
> $$f(-1) = e^{-1}$$
>
> $f(-1)$에 대입:
>
> $$e^{-1}(1 - 3) - e^{-1}(-2 + 3) + 2e^{-1} + C = e^{-1}$$
>
> $$-2e^{-1} - e^{-1} + 2e^{-1} + C = e^{-1} \implies C = 2e^{-1}$$
>
> $$f(x) = e^x(x^2 + 3x) - e^x(2x + 3) + 2e^x + 2e^{-1}$$
>
> **$f(1)$ 계산:**
>
> $$f(1) = e(1 + 3) - e(2 + 3) + 2e + 2e^{-1} = 4e - 5e + 2e + 2e^{-1} = e + 2e^{-1}$$

---

### 예제 360

모든 실수 $x$에 대하여 함수 $f(x)$가 $f(x) = \displaystyle\int_{0}^{x}(x-t)\cos 2t\, dt$로 정의될 때, $f(x)$의 최댓값을 구하면?

① $\dfrac{1}{2}$ ② $\dfrac{1}{3}$ ③ $\dfrac{1}{4}$ ④ $\dfrac{1}{5}$ ⑤ $1$

> [!summary]- 풀이
> $f(0) = 0$을 확인한다.
>
> $(x-t)$를 분리한다:
> $$f(x) = x\int_{0}^{x}\cos 2t\, dt - \int_{0}^{x} t\cos 2t\, dt$$
>
> **미분** (예제 347 (2) 결과 활용):
> $$f'(x) = \int_{0}^{x}\cos 2t\, dt = \left[\frac{1}{2}\sin 2t\right]_{0}^{x} = \frac{1}{2}\sin 2x$$
>
> **$f(x)$ 역적분:**
> $$f(x) = \int \frac{1}{2}\sin 2x\, dx = -\frac{1}{4}\cos 2x + C$$
>
> $f(0) = 0$에서: $-\dfrac{1}{4} + C = 0 \implies C = \dfrac{1}{4}$
>
> $$f(x) = -\frac{1}{4}\cos 2x + \frac{1}{4}$$
>
> $\cos 2x$의 최솟값은 $-1$이므로 최댓값:
>
> $$f_{\max} = -\frac{1}{4}\cdot(-1) + \frac{1}{4} = \frac{1}{2}$$
>
> **정답: ①**

---

### 예제 361

두 함수 $f(x) = \tan x\ \left(-\dfrac{\pi}{2} \leq x \leq \dfrac{\pi}{2}\right)$, $g(x) = f^{-1}(x)$에 대하여
$F(x) = \displaystyle\int_{0}^{g(x)} f(t)\, dt$일 때, $F'(1)$의 값은?

① $\dfrac{1}{2}$ ② $\dfrac{1}{\sqrt{2}}$ ③ $1$ ④ $\dfrac{\pi}{4}$ ⑤ $\dfrac{\pi}{2}$

> [!summary]- 풀이
> **합성형 미분** ($g(x)$가 상한):
>
> $$F'(x) = f(g(x)) \cdot g'(x)$$
>
> $g(x) = f^{-1}(x)$이므로 $f(g(x)) = x$:
>
> $$F'(x) = x \cdot g'(x)$$
>
> $$F'(1) = 1 \cdot g'(1)$$
>
> **역함수 미분 공식** — $f(a) = b \iff g(b) = a$일 때 $g'(b) = \dfrac{1}{f'(a)}$
>
> $g(1) = f^{-1}(1) = \dfrac{\pi}{4}$ ($\tan\dfrac{\pi}{4} = 1$)이므로 $g'(1) = \dfrac{1}{f'(\pi/4)}$
>
> $f'(x) = \sec^2 x$이므로:
>
> $$g'(1) = \frac{1}{\sec^2\!\frac{\pi}{4}} = \cos^2\!\frac{\pi}{4} = \left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{2}$$
>
> $$F'(1) = \frac{1}{2}$$
>
> **정답: ①**

> [!tip]- 역함수 미분 관계 정리
> $g(x) = f^{-1}(x)$일 때 $f(g(x)) = x$를 미분하면:
>
> $$g'(x) \cdot f'(g(x)) = 1 \implies g'(x) = \frac{1}{f'(g(x))}$$
>
> 특히 $f(a) = b$ (즉 $g(b) = a$)이면:
>
> $$g'(b) = \frac{1}{f'(a)}$$

---

## 2. 정적분 등식에서 f(x) 결정 심화

### 예제 362

함수 $f(x) = (ax+b)e^x$이 모든 실수 $x$에 대하여 $f(x) = 4e^x + 2 + \displaystyle\int_{0}^{x} f(t)\, dt$를 만족시킨다.
두 상수 $a$, $b$에 대하여 $a^2 + b^2$의 값을 구하시오.

> [!summary]- 풀이
> **$x = 0$ 대입** → $b$ 결정:
>
> $$f(0) = 4e^0 + 2 + 0 = 6$$
> $$f(0) = (a \cdot 0 + b)e^0 = b$$
>
> $$b = 6$$
>
> **양변 미분:**
>
> $$f'(x) = 4e^x + f(x)$$
>
> 좌변: $f'(x) = ae^x + (ax + 6)e^x = (ax + a + 6)e^x$
>
> 우변: $4e^x + (ax + 6)e^x = (ax + 10)e^x$
>
> 계수 비교:
>
> $$ax + a + 6 = ax + 10 \implies a = 4$$
>
> $$a^2 + b^2 = 16 + 36 = 52$$

---

### 예제 363

상수 $a$, $b$에 대하여 이차함수 $f(x) = x^2 + ax + b$가
$$f(x) - 2\int_{0}^{x} e^{t+x} f(t)\, dt = 4$$
를 만족한다. $f(1)$의 값을 구하시오.

> [!summary]- 풀이
> **$x = 0$ 대입** → $b$ 결정:
>
> $$f(0) - 0 = 4 \implies b = 4$$
>
> 적분 안의 $e^{t+x} = e^x \cdot e^t$이므로 $e^x$을 밖으로 꺼낼 수 있다:
>
> $$f(x) = 2e^x\int_{0}^{x} e^t f(t)\, dt + 4$$
>
> **양변 미분** (우변에 곱의 미분):
>
> $$f'(x) = 2e^x \cdot e^x f(x) + 2e^x\int_{0}^{x} e^t f(t)\, dt$$
>
> **$x = 0$ 대입** → $a$ 결정:
>
> $f'(0) = 2a + 0 \cdot a = a$ (좌변 $f'(x) = 2x + a$에서)
>
> $f'(0) = 2e^0 \cdot e^0 \cdot f(0) + 0 = 2f(0) = 2 \cdot 4 = 8$ (우변에서)
>
> $$a = 8$$
>
> $$f(x) = x^2 + 8x + 4$$
> $$f(1) = 1 + 8 + 4 = 13$$

---

## 3. Thm 52: 극한과 정적분

두 경우 모두 $\dfrac{0}{0}$ 꼴이므로 **로피탈의 정리**를 적용한다.

$$\textbf{(1)}\quad \lim_{x \to a} \frac{1}{x-a}\int_{a}^{x} f(t)\, dt = f(a)$$

$$\textbf{(2)}\quad \lim_{x \to 0} \frac{1}{x}\int_{a}^{a+x} f(t)\, dt = f(a)$$

**유도 (로피탈):**

$$\lim_{x \to a}\frac{\displaystyle\int_{a}^{x} f(t)\, dt}{x - a} \xrightarrow{\text{로피탈}} \lim_{x \to a}\frac{f(x)}{1} = f(a)$$

---

### 예제 364

연속함수 $f(x)$에 대하여 $a$가 $0$이 아닌 실수일 때,
$\displaystyle\lim_{x \to a} \dfrac{1}{x^2 - a^2}\int_{a}^{x} f(t)\, dt$의 값을 구하여라.

> [!summary]- 풀이
> $x^2 - a^2 = (x-a)(x+a)$로 분해한다.
>
> $$\lim_{x \to a}\frac{\displaystyle\int_{a}^{x} f(t)\, dt}{x^2 - a^2} \xrightarrow{\text{로피탈}} \lim_{x \to a}\frac{f(x)}{2x} = \frac{f(a)}{2a}$$

---

### 예제 365

미분가능한 함수 $f(x)$에 대하여 $f(2) = 4$, $f'(2) = 2$일 때,
$\displaystyle\lim_{x \to 2} \dfrac{1}{x-2}\int_{2}^{x}\{f(t)\}^2 f'(t)\, dt$의 값은?

① $1$ ② $8$ ③ $16$ ④ $32$ ⑤ $64$

> [!summary]- 풀이
> Thm 52 (1) 공식에서 피적분함수 $h(t) = \{f(t)\}^2 f'(t)$로 놓으면:
>
> $$\lim_{x \to 2}\frac{\displaystyle\int_{2}^{x}\{f(t)\}^2 f'(t)\, dt}{x-2} \xrightarrow{\text{로피탈}} \{f(2)\}^2 f'(2) = 4^2 \cdot 2 = 32$$
>
> **정답: ④**

---

### 예제 366

$f'(1) = 1$, $f(1) = 2$일 때,
$\displaystyle\lim_{x \to 1}\dfrac{1}{x-1}\int_{f(1)}^{f(x)}(t-1)\, dt$의 값은?

① $1$ ② $2$ ③ $3$ ④ $4$ ⑤ $5$

> [!summary]- 풀이
> 상한이 $f(x)$인 합성형이므로 로피탈 적용 시 합성함수 미분이 필요하다.
>
> $$\lim_{x \to 1}\frac{\displaystyle\int_{f(1)}^{f(x)}(t-1)\, dt}{x-1} \xrightarrow{\text{로피탈}} \lim_{x \to 1}\frac{(f(x)-1)\cdot f'(x)}{1}$$
>
> $x = 1$ 대입:
>
> $$(f(1) - 1)\cdot f'(1) = (2-1)\cdot 1 = 1$$
>
> **정답: ①**

---

### 예제 367

함수 $f(x) = \displaystyle\int_{0}^{x}(\sin^2 t - \cos t)\, dt$에 대하여 $\displaystyle\lim_{x \to 0}\dfrac{f(x)}{x}$의 값을 구하여라.

> [!summary]- 풀이
> $$\lim_{x \to 0}\frac{f(x)}{x} = \lim_{x \to 0}\frac{\displaystyle\int_{0}^{x}(\sin^2 t - \cos t)\, dt}{x}$$
>
> Thm 52 (1) 공식 적용 ($a = 0$):
>
> $$= \sin^2 0 - \cos 0 = 0 - 1 = -1$$

---

### 예제 368

극한값 $\displaystyle\lim_{x \to 1}\int_{1}^{x^2}\dfrac{(1+2\cos\pi t)^3}{x^3-1}\, dt$를 구하여라.

① $-\dfrac{3}{2}$ ② $-1$ ③ $-\dfrac{2}{3}$ ④ $-\dfrac{1}{2}$ ⑤ $-\dfrac{1}{3}$

> [!summary]- 풀이
> $$= \lim_{x \to 1}\frac{\displaystyle\int_{1}^{x^2}(1+2\cos\pi t)^3\, dt}{x^3 - 1}$$
>
> 로피탈 적용 (분자는 합성형 미분: 상한 $x^2$의 미분 $2x$ 곱함):
>
> $$= \lim_{x \to 1}\frac{2x\cdot(1+2\cos\pi x^2)^3}{3x^2}$$
>
> $x = 1$ 대입:
>
> $$= \frac{2(1+2\cos\pi)^3}{3} = \frac{2(1-2)^3}{3} = \frac{2\cdot(-1)}{3} = -\frac{2}{3}$$
>
> **정답: ③**

---

### 예제 369

$\displaystyle\lim_{x \to \pi}\dfrac{1}{x-\pi}\int_{-1}^{\cos x}\sin^2\theta\cos^3\theta\, d\theta$의 값은?

① $-1$ ② $0$ ③ $1$ ④ $\pi$ ⑤ $2\pi$

> [!summary]- 풀이
> 상한이 $\cos x$인 합성형. 로피탈 적용:
>
> $$= \lim_{x \to \pi}\frac{(-\sin x)\cdot\sin^2(\cos x)\cos^3(\cos x)}{1}$$
>
> $x = \pi$ 대입: $\sin\pi = 0$이므로
>
> $$= 0 \cdot \sin^2(\cos\pi)\cos^3(\cos\pi) = 0$$
>
> **정답: ②**

---

## 관련 주제

- [[53-derivative-integral-1|53강: 미분과 정적분(1)]]
- [[45-integration-by-parts|45강: 부분적분]]
- [[55-area-integral-1|55강: 정적분과 함수의 결정, 넓이와 적분(1)]]

---

**학습 포인트:**

1. 상한이 $g(x)$인 경우 미분하면 **$f(g(x))\cdot g'(x)$** — 합성함수 미분을 반드시 곱한다
2. 역함수 $g = f^{-1}$가 포함된 경우 $f(g(x)) = x$를 이용해 단순화한다
3. Thm 52: $\dfrac{\int_a^x f(t)dt}{x-a}$ 꼴은 **로피탈** 적용 → $f(a)$
4. 피적분함수가 복합 함수이거나 상한이 합성함수일 때도 로피탈 + 합성형 미분을 결합한다
