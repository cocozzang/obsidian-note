---
id: a7c2e548-1f3d-4b9e-8c01-5d2a6f7e3b14
aliases:
  - 53강 미분과 정적분(1)
  - 정적분의 미분
  - 미분과 정적분
  - 정적분으로 정의된 함수의 미분
tags:
  - 정적분
  - 미분과정적분
  - 정적분의미분
  - 연속함수
  - 적분법
pages: 160-163
subject: 대학기초수학
title: 미분과 정적분(1)
topics:
  - 정적분의 정리(미분과 정적분) Thm51
  - 정적분으로 정의된 함수의 미분
  - 정적분 등식에서 미지수 결정
  - 적분과 미분이 결합된 응용 문제
---

# 미분과 정적분(1)

## 1. Thm 51: 정적분의 정리 (미분과 정적분)

미적분학의 핵심 결과. 정적분의 상한 또는 하한이 변수 $x$를 포함할 때 $x$에 대해 미분한다.

---

### (1) 기본형

$$\frac{d}{dx}\int_{a}^{x} f(t)\, dt = f(x)$$

**유도:**
$$\int_{a}^{x} f(t)\, dt = F(x) - F(a)$$
$$\frac{d}{dx}(F(x) - F(a)) = F'(x) = f(x)$$

---

### (2) 이동형 (양쪽 한계 모두 $x$ 포함)

$$\frac{d}{dx}\int_{x}^{x+a} f(t)\, dt = f(x+a) - f(x)$$

**유도:**
$$\int_{x}^{x+a} f(t)\, dt = F(x+a) - F(x)$$
$$\frac{d}{dx}(F(x+a) - F(x)) = f(x+a) - f(x)$$

---

### (3) 합성형 (한계가 $x$의 함수)

$$\frac{d}{dx}\int_{h(x)}^{g(x)} f(t)\, dt = f(g(x))\cdot g'(x) - f(h(x))\cdot h'(x)$$

**유도:**
$$\int_{h(x)}^{g(x)} f(t)\, dt = F(g(x)) - F(h(x))$$
$$\frac{d}{dx}(F(g(x)) - F(h(x))) = F'(g(x))\cdot g'(x) - F'(h(x))\cdot h'(x)$$
$$= f(g(x))\cdot g'(x) - f(h(x))\cdot h'(x)$$

---

### 예제 347

다음을 각각 증명하여라.

**(1)** $\dfrac{d}{dx}\displaystyle\int_{a}^{x} xf(t)\, dt = \displaystyle\int_{a}^{x} f(t)\, dt + xf(x)$

**(2)** $\dfrac{d}{dx}\displaystyle\int_{a}^{x} (x-t)f(t)\, dt = \displaystyle\int_{a}^{x} f(t)\, dt$

**(3)** $\dfrac{d}{dx}\displaystyle\int_{ax+b}^{cx+d} f(t)\, dt = cf(cx+d) - af(ax+b)$

> [!summary]- 풀이
> **(1)** $x$를 적분 밖으로 꺼내어 곱의 미분을 적용한다.
>
> $$\frac{d}{dx}\int_{a}^{x} xf(t)\, dt = \frac{d}{dx}\left(x \cdot \int_{a}^{x} f(t)\, dt\right)$$
>
> 곱의 미분: $(uv)' = u'v + uv'$
>
> $$= 1 \cdot \int_{a}^{x} f(t)\, dt + x \cdot f(x) = \int_{a}^{x} f(t)\, dt + xf(x) \quad \blacksquare$$
>
> ---
>
> **(2)** $(x-t)$를 분리하여 두 적분으로 나눈다.
>
> $$\frac{d}{dx}\int_{a}^{x}(x-t)f(t)\, dt = \frac{d}{dx}\left\{x\int_{a}^{x}f(t)\, dt - \int_{a}^{x} tf(t)\, dt\right\}$$
>
> $$= \left(\int_{a}^{x} f(t)\, dt + xf(x)\right) - xf(x) = \int_{a}^{x} f(t)\, dt \quad \blacksquare$$
>
> ---
>
> **(3)** Thm 51 (3)의 합성형을 직접 적용한다. $g(x) = cx+d$, $h(x) = ax+b$이므로:
>
> $$\frac{d}{dx}\int_{ax+b}^{cx+d} f(t)\, dt = f(cx+d)\cdot c - f(ax+b)\cdot a = cf(cx+d) - af(ax+b) \quad \blacksquare$$

---

## 2. 정적분으로 정의된 함수에서 미지수 결정

### 핵심 전략

$$\int_{a}^{x} f(t)\, dt = \phi(x) \text{ 꼴}$$

① **양변 미분** → $f(x) = \phi'(x)$

② **$x = a$ 대입** → $\displaystyle\int_{a}^{a} f(t)\, dt = 0$ 이므로 $\phi(a) = 0$ → 미지수 결정

---

### 예제 348

다항함수 $f(x)$가 $\displaystyle\int_{2}^{x} f(t)\, dt = x^2 + ax + 2$를 만족시킬 때, $f(10)$의 값을 구하여라.

> [!summary]- 풀이
> **양변 미분:**
> $$f(x) = 2x + a$$
>
> **$x = 2$ 대입** ($\int_2^2 = 0$):
> $$0 = 4 + 2a + 2 \implies a = -3$$
>
> $$f(x) = 2x - 3$$
> $$f(10) = 20 - 3 = 17$$

---

### 예제 349

다항함수 $f(x)$가 모든 실수 $x$에 대하여 $\displaystyle\int_{1}^{x} f(t)\, dt = x^3 - 2ax^2 + ax$를 만족시킬 때, $f(3)$의 값을 구하여라.

> [!summary]- 풀이
> **양변 미분:**
> $$f(x) = 3x^2 - 4ax + a$$
>
> **$x = 1$ 대입**:
> $$0 = 1 - 2a + a \implies a = 1$$
>
> $$f(x) = 3x^2 - 4x + 1$$
> $$f(3) = 27 - 12 + 1 = 16$$

---

## 3. $f(x)$가 적분 내에 포함된 등식

### 핵심 전략

$$f(x) = g(x) + \int_{a}^{x} f(t)\, dt \text{ 꼴}$$

양변 미분하여 $f'(x)$를 $f(x)$로 표현한 뒤, 초기값($x = a$ 대입)으로 $f(a)$를 결정한다.

---

### 예제 350

모든 실수 $x$에 대하여 미분가능한 함수 $f(x)$가 등식 $f(x) = x^2\cos x + \displaystyle\int_{\pi}^{x} tf(t)\, dt$가 성립할 때, $f'(\pi)$의 값을 구하여라.

> [!summary]- 풀이
> **양변 미분:**
> $$f'(x) = -x^2\sin x + 2x\cos x + xf(x)$$
>
> **$f(\pi)$ 구하기** — $x = \pi$ 대입 ($\int_\pi^\pi = 0$):
> $$f(\pi) = \pi^2\cos\pi + 0 = -\pi^2$$
>
> **$f'(\pi)$ 계산:**
> $$f'(\pi) = -\pi^2 \cdot 0 + 2\pi \cdot (-1) + \pi \cdot f(\pi)$$
> $$= -2\pi + \pi(-\pi^2) = -\pi^3 - 2\pi$$

---

### 예제 351

두 함수 $f(x) = ax + b$와 $g(x) = e^x$가
$$f(g(x)) = \int_{0}^{x} f(t)g(t)\, dt - xe^x + 3$$
을 만족할 때, $f(2)$의 값은?

① 4 ② 2 ③ 0 ④ $-2$ ⑤ $-4$

> [!summary]- 풀이
> **양변 미분** (좌변에 합성함수 미분 적용):
> $$g'(x) \cdot f'(g(x)) = f(x)g(x) - (xe^x + e^x)$$
>
> $f'(x) = a$, $g'(x) = e^x$이므로:
> $$ae^x = e^x(ax + b) - e^x(x + 1)$$
>
> $e^x$으로 나누면:
> $$a = ax + b - x - 1 = (a-1)x + (b-1)$$
>
> 양변의 계수를 비교하면:
> $$a - 1 = 0 \implies a = 1, \quad b - 1 = a = 1 \implies b = 2$$
>
> $$f(x) = x + 2 \implies f(2) = 4$$
>
> **정답: ①**

---

### 예제 352

함수 $f(x)$는 연속함수이고 모든 실수 $x$에 대하여
$$f(x) - 2\int_{0}^{x} e^t f(t)\, dt = 1$$
이 성립한다. $f''(0)$의 값은?

① 2 ② 4 ③ 6 ④ 8 ⑤ 10

> [!summary]- 풀이
> **$x = 0$ 대입** → $f(0)$ 결정:
> $$f(0) - 0 = 1 \implies f(0) = 1$$
>
> **양변 1차 미분:**
> $$f'(x) - 2e^x f(x) = 0 \tag{★}$$
>
> $x = 0$ 대입:
> $$f'(0) = 2f(0) = 2$$
>
> **★을 한 번 더 미분:**
> $$f''(x) - 2\{e^x f(x) + e^x f'(x)\} = 0$$
> $$f''(x) = 2e^x(f(x) + f'(x))$$
>
> $x = 0$ 대입:
> $$f''(0) = 2(f(0) + f'(0)) = 2(1 + 2) = 6$$
>
> **정답: ③**

---

### 예제 353

실수 전체의 집합에서 미분가능한 함수 $f(x)$가 $f(x) = e^x - 1 + \displaystyle\int_{0}^{x} f(t)\, dt$를 만족할 때, 보기 중 옳은 것을 모두 고르시오.

> ㄱ. $f(0) = 0$이다.
> ㄴ. $f'(0) = 0$이다.
> ㄷ. 모든 실수 $x$에 대하여 $f'(x) > f(x)$이다.

① ㄱ ② ㄴ ③ ㄱ, ㄴ ④ ㄱ, ㄷ ⑤ ㄴ, ㄷ

> [!summary]- 풀이
> **ㄱ.** $x = 0$ 대입:
> $$f(0) = e^0 - 1 + 0 = 0 \quad \to \text{참}$$
>
> **ㄴ.** 양변 미분:
> $$f'(x) = e^x + f(x)$$
> $x = 0$: $f'(0) = 1 + f(0) = 1 \neq 0 \quad \to \text{거짓}$
>
> **ㄷ.** $f'(x) = e^x + f(x)$이고 $e^x > 0$이므로 $f'(x) > f(x)$ $\quad \to \text{참}$
>
> **정답: ④ (ㄱ, ㄷ)**

---

## 4. $(x-t)$ 꼴의 적분 함수

### 핵심 전략

$$F(x) = \int_{a}^{x}(x-t)f(t)\, dt$$

$x$를 적분 밖으로 분리한 뒤 예제 347 (2)의 결과를 이용한다.

$$F(x) = x\int_{a}^{x} f(t)\, dt - \int_{a}^{x} tf(t)\, dt$$

$$F'(x) = \int_{a}^{x} f(t)\, dt$$

---

### 예제 354

함수 $F(x) = \displaystyle\int_{0}^{x}(x-t)\cos t\, dt$의 도함수를 구하여라.

> [!summary]- 풀이
> $$F(x) = x\int_{0}^{x}\cos t\, dt - \int_{0}^{x} t\cos t\, dt$$
>
> $$F'(x) = 1 \cdot \int_{0}^{x}\cos t\, dt + x\cos x - x\cos x = \int_{0}^{x}\cos t\, dt$$
>
> $$= [\sin t]_{0}^{x} = \sin x$$
>
> $$\therefore F'(x) = \sin x$$

---

## 5. 미분과 적분의 교환 조건

### 핵심 아이디어

$$\frac{d}{dx}\int_{a}^{x} f(t)\, dt = \int_{a}^{x} \frac{d}{dt}f(t)\, dt$$

좌변 = $f(x)$, 우변 = $[f(t)]_a^x = f(x) - f(a)$

따라서 이 등식이 성립하려면 $f(a) = 0$이어야 한다.

---

### 예제 355

함수 $f(x) = x^3 - x$가
$$\frac{d}{dx}\int_{a}^{x} f(t)\, dt = \int_{a}^{x}\frac{d}{dt}f(t)\, dt$$
를 만족할 때, 실수 $a$의 개수를 구하여라.

> [!summary]- 풀이
> 좌변 $= f(x)$, 우변 $= f(x) - f(a)$이므로:
>
> $$f(a) = 0$$
>
> $$a^3 - a = a(a^2 - 1) = a(a+1)(a-1) = 0$$
>
> $$a = 0,\ a = 1,\ a = -1$$
>
> 실수 $a$의 개수 $= \mathbf{3}$

---

## 6. 극한과 정적분의 결합 — 로피탈 응용

### 핵심 아이디어

$$\lim_{x \to 0} \frac{\displaystyle\int_{0}^{x} f(t)\, dt}{x} \quad \left(\frac{0}{0} \text{ 형태}\right)$$

로피탈의 정리를 적용하면:

$$= \lim_{x \to 0} \frac{f(x)}{1} = f(0)$$

---

### 예제 356

$$\lim_{x \to 0}\int_{0}^{x}\frac{e^t\cos t}{x}\, dt$$의 값은?

> [!summary]- 풀이
> $$= \lim_{x \to 0} \frac{\displaystyle\int_{0}^{x} e^t\cos t\, dt}{x}$$
>
> $x \to 0$일 때 분자·분모 모두 0이므로 로피탈 적용:
>
> $$= \lim_{x \to 0} \frac{e^x\cos x}{1} = e^0 \cdot \cos 0 = 1$$

---

### 예제 357

실수 전체에서 정의된 함수 $F(x) = \displaystyle\int_{0}^{x}(1-t)e^t\, dt$의 최댓값은?

① $1 + e$ ② $1 - e$ ③ $e - 1$ ④ $e + 2$ ⑤ $e - 2$

> [!summary]- 풀이
> **임계점 탐색:**
> $$F'(x) = (1-x)e^x = 0 \implies x = 1$$
>
> **이계도함수 판정:**
> $$F''(x) = -e^x + (1-x)e^x = e^x(1-x-1) = -xe^x$$
> $$F''(1) = -e < 0 \implies x = 1\text{에서 극대}$$
>
> **최댓값 계산** (부분적분 이용):
> $$F(1) = \int_{0}^{1}(1-t)e^t\, dt = \left[(1-t)e^t + e^t\right]_{0}^{1}$$
>
> $u = 1-t$, $dv = e^t\, dt$로 부분적분하면:
> $$= \left[(1-t)e^t\right]_{0}^{1} + \int_{0}^{1}e^t\, dt = (0 - 1) + [e^t]_{0}^{1} = -1 + (e - 1) = e - 2$$
>
> **정답: ⑤**

---

## 관련 주제

- [[52-integral-inverse-function|52강: 정적분의 계산기법(3), 역함수와 정적분]]
- [[47-fundamental-theorem|47강: 정적분과 부정적분의 관계]]
- [[54-derivative-integral-2|54강: 미분과 정적분(2), 극한과 정적분]]

---

**학습 포인트:**

1. Thm 51의 세 가지 패턴을 구별하여 적용한다: 기본형 / 이동형 / 합성형
2. $\int_a^x f(t)\, dt = \phi(x)$ 꼴에서는 **양변 미분 + $x=a$ 대입**으로 미지수를 결정한다
3. $(x-t)$ 꼴 적분 함수는 **$x$를 분리**하여 두 항으로 나눈 뒤 미분한다
4. $\lim_{x\to 0}\frac{\int_0^x f(t)\,dt}{x}$ 형태는 **로피탈**을 적용하면 $f(0)$이 된다
