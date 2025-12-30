---
id: a7b2e4f1-3c8d-4a5e-9f6b-8d1c2e3a4b5c
aliases:
  - 초월함수의 도함수(2)
  - 초월함수 미분 응용
  - 미분계수와 극한
tags:
  - 초월함수
  - 도함수
  - 미분계수
  - 극한
  - 합성함수미분
  - 역함수미분
pages: 64-66
subject: 대학기초수학
title: 초월함수의 도함수(2) - 초월함수 미분의 응용
topics:
  - 초월함수의 미분 계산
  - 미분계수의 정의를 활용한 극한
  - 합성함수의 미분
  - 역함수의 미분계수
---

# 초월함수의 도함수(2)

## 1. 초월함수의 미분 계산

### 예제 123

다음 함수를 미분하여라.

(1) $y = \sin 5x$

(2) $y = e^{\sin x}$

(3) $y = e^x \cos 2x$

> [!summary]- 풀이
> **(1)** 합성함수의 미분법 적용
>
> $$y' = 5 \cos 5x$$
>
> **(2)** 합성함수의 미분법 적용
>
> $$y' = e^{\sin x} \cdot (\sin x)' = \cos x \cdot e^{\sin x}$$
>
> **(3)** 곱의 미분법 적용
>
> $$y' = (e^x)' \cos 2x + e^x (\cos 2x)'$$
>
> $$= e^x \cos 2x + e^x \cdot (-2\sin 2x)$$
>
> $$= e^x(\cos 2x - 2\sin 2x)$$

---

## 2. 미분계수의 정의를 활용한 극한

### 핵심 공식

미분계수의 정의:

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

### 예제 124

함수 $f(x) = \frac{1}{2} \sin 2x$일 때, $\displaystyle\lim_{x \to 0} \frac{f(\pi - \sin x) - f(\pi)}{x}$의 값을 구하여라.

> [!summary]- 풀이
> 주어진 극한을 미분계수 형태로 변형한다.
>
> $$\lim_{x \to 0} \frac{f(\pi - \sin x) - f(\pi)}{x}$$
>
> $-\sin x$를 매개로 분리하면
>
> $$= \lim_{x \to 0} \frac{f(\pi - \sin x) - f(\pi)}{-\sin x} \cdot \frac{-\sin x}{x}$$
>
> $x \to 0$일 때 $-\sin x \to 0$이므로
>
> $$= f'(\pi) \cdot (-1) = -f'(\pi)$$
>
> $f'(x)$를 구하면
>
> $$f'(x) = \frac{1}{2} \cdot 2\cos 2x = \cos 2x$$
>
> 따라서
>
> $$-f'(\pi) = -\cos 2\pi = -1$$

### 예제 125

함수 $f(x) = \ln x$일 때, $\displaystyle\lim_{h \to 0} \frac{f(e+h) - f(e-h)}{h}$의 값을 구하여라.

> [!summary]- 풀이
> 주어진 극한을 두 부분으로 분리한다.
>
> $$\lim_{h \to 0} \frac{f(e+h) - f(e-h)}{h}$$
>
> $f(e)$를 더하고 빼면
>
> $$= \lim_{h \to 0} \frac{f(e+h) - f(e)}{h} + \lim_{h \to 0} \frac{f(e) - f(e-h)}{h}$$
>
> 두 번째 항에서 $-h = t$로 치환하면
>
> $$= \lim_{h \to 0} \frac{f(e+h) - f(e)}{h} + \lim_{t \to 0} \frac{f(e+t) - f(e)}{t}$$
>
> $$= f'(e) + f'(e) = 2f'(e)$$
>
> $f'(x) = \frac{1}{x}$이므로
>
> $$2f'(e) = \frac{2}{e}$$

### 예제 126

$f(x) = x\cos x$일 때, $\displaystyle\lim_{h \to 0} \frac{f(\pi + 2h) - f(\pi - 3h)}{h}$의 값을 구하여라.

> [!summary]- 풀이
> 분자에서 $(\pi + 2h) - (\pi - 3h) = 5h$임을 이용한다.
>
> $$\lim_{h \to 0} \frac{f(\pi + 2h) - f(\pi - 3h)}{h}$$
>
> $$= \lim_{h \to 0} \frac{f(\pi + 2h) - f(\pi - 3h)}{5h} \cdot 5 = 5f'(\pi)$$
>
> $f'(x)$를 구하면
>
> $$f'(x) = 1 \cdot \cos x + x \cdot (-\sin x) = \cos x - x\sin x$$
>
> $$f'(\pi) = \cos \pi - \pi \sin \pi = -1 - 0 = -1$$
>
> 따라서
>
> $$5f'(\pi) = 5 \cdot (-1) = -5$$

### 예제 127

모든 실수 $x$에 대하여 미분가능한 함수 $f(x)$가 $f'(1) = 2$일 때, $\displaystyle\lim_{x \to 0} \frac{f(\cos 3x) - f(\cos x)}{x^2}$의 값을 구하여라.

> [!summary]- 풀이
> $x \to 0$일 때 $\cos 3x \to 1$, $\cos x \to 1$이므로 분자, 분모 모두 0으로 수렴한다.
>
> $$\lim_{x \to 0} \frac{f(\cos 3x) - f(\cos x)}{x^2}$$
>
> $\cos 3x - \cos x$를 매개로 분리하면
>
> $$= \lim_{x \to 0} \frac{f(\cos 3x) - f(\cos x)}{\cos 3x - \cos x} \cdot \frac{\cos 3x - \cos x}{x^2}$$
>
> 첫 번째 인수는 $f'(1)$이고, 두 번째 인수는 합차를 곱으로 변환한다.
>
> $$\cos 3x - \cos x = -2\sin 2x \sin x$$
>
> 따라서
>
> $$= f'(1) \cdot \lim_{x \to 0} \frac{-2\sin 2x \sin x}{x^2}$$
>
> $$= 2 \cdot (-2) \cdot \lim_{x \to 0} \frac{\sin 2x}{x} \cdot \frac{\sin x}{x}$$
>
> $$= 2 \cdot (-2) \cdot 2 \cdot 1 = -8$$

### 예제 128

함수 $f(x)$는 실수 전체에서 미분가능하고 $f(0) = 2$, $f'(0) = 1$일 때, $\displaystyle\lim_{h \to 0} \frac{f(h + \sin h) - a}{h} = b$를 만족하는 두 상수 $a$, $b$의 합 $a + b$를 구하여라.

> [!summary]- 풀이
> 극한값이 상수 $b$이고 분모가 0으로 수렴하므로, 분자도 0으로 수렴해야 한다.
>
> $h \to 0$일 때 $h + \sin h \to 0$이므로
>
> $$f(h + \sin h) - a \to f(0) - a = 2 - a = 0$$
>
> 따라서 $a = 2$
>
> 이제 극한을 계산한다.
>
> $$\lim_{h \to 0} \frac{f(h + \sin h) - f(0)}{h}$$
>
> $h + \sin h$를 매개로 분리하면
>
> $$= \lim_{h \to 0} \frac{f(h + \sin h) - f(0)}{h + \sin h} \cdot \frac{h + \sin h}{h}$$
>
> $$= f'(0) \cdot \lim_{h \to 0} \left(1 + \frac{\sin h}{h}\right)$$
>
> $$= 1 \cdot (1 + 1) = 2$$
>
> 따라서 $b = 2$
>
> $$a + b = 2 + 2 = 4$$

### 예제 129

$\displaystyle\lim_{x \to e} \frac{\ln x - 1}{x - e}$의 값을 구하여라.

> [!summary]- 풀이
> $f(x) = \ln x$로 놓으면 $f(e) = \ln e = 1$
>
> 주어진 극한은 미분계수의 정의와 같다.
>
> $$\lim_{x \to e} \frac{\ln x - 1}{x - e} = \lim_{x \to e} \frac{f(x) - f(e)}{x - e} = f'(e)$$
>
> $f'(x) = \frac{1}{x}$이므로
>
> $$f'(e) = \frac{1}{e}$$

---

## 3. 합성함수의 미분

### 예제 130

함수 $f(x) = \ln(\tan x)$와 미분가능한 함수 $g(x)$의 합성함수 $h(x) = (g \circ f)(x)$에 대하여, $h'\left(\frac{\pi}{4}\right) = 8$일 때, $g'(0)$의 값은? (단, $0 < x < \frac{\pi}{2}$)

> [!summary]- 풀이
> $h(x) = g(f(x))$이므로 합성함수의 미분법에 의해
>
> $$h'(x) = f'(x) \cdot g'(f(x))$$
>
> $x = \frac{\pi}{4}$를 대입하면
>
> $$h'\left(\frac{\pi}{4}\right) = f'\left(\frac{\pi}{4}\right) \cdot g'\left(f\left(\frac{\pi}{4}\right)\right) = 8$$
>
> $f\left(\frac{\pi}{4}\right)$를 구하면
>
> $$f\left(\frac{\pi}{4}\right) = \ln\left(\tan\frac{\pi}{4}\right) = \ln 1 = 0$$
>
> 따라서
>
> $$f'\left(\frac{\pi}{4}\right) \cdot g'(0) = 8$$
>
> $f'(x)$를 구하면
>
> $$f'(x) = \frac{(\tan x)'}{\tan x} = \frac{\sec^2 x}{\tan x}$$
>
> $$f'\left(\frac{\pi}{4}\right) = \frac{\sec^2\frac{\pi}{4}}{\tan\frac{\pi}{4}} = \frac{\frac{1}{\cos^2\frac{\pi}{4}}}{1} = \frac{1}{\frac{1}{2}} = 2$$
>
> 따라서
>
> $$2 \cdot g'(0) = 8$$
>
> $$g'(0) = 4$$

---

## 4. 도함수가 0이 되는 점 찾기

### 예제 131

함수 $f(x) = \sin x - \sqrt{3}\cos x - x$일 때, $f'(\theta) = 0$을 만족하는 $\theta$를 구하여라. (단, $0 < \theta \leq \pi$)

> [!summary]- 풀이
> $f'(x)$를 구하면
>
> $$f'(x) = \cos x + \sqrt{3}\sin x - 1$$
>
> $f'(\theta) = 0$에서
>
> $$\cos\theta + \sqrt{3}\sin\theta - 1 = 0$$
>
> $$\cos\theta + \sqrt{3}\sin\theta = 1$$
>
> [[12-advanced-trigonometry-5|삼각함수의 합성]]을 적용하면
>
> $$2\sin\left(\theta + \frac{\pi}{6}\right) = 1$$
>
> (여기서 $\tan\alpha = \frac{1}{\sqrt{3}}$이므로 $\alpha = \frac{\pi}{6}$)
>
> $$\sin\left(\theta + \frac{\pi}{6}\right) = \frac{1}{2}$$
>
> $0 < \theta \leq \pi$에서 $\frac{\pi}{6} < \theta + \frac{\pi}{6} \leq \frac{7\pi}{6}$
>
> $$\theta + \frac{\pi}{6} = \frac{\pi}{6} \text{ 또는 } \frac{5\pi}{6}$$
>
> $$\theta = 0 \text{ 또는 } \frac{2\pi}{3}$$
>
> $0 < \theta \leq \pi$이므로
>
> $$\theta = \frac{2\pi}{3}$$

### 예제 132

함수 $f(x) = e^x \cos x$일 때, $f'(\theta) = 0$을 만족하는 $\theta$를 구하여라. (단, $0 < \theta < \pi$)

> [!summary]- 풀이
> $f'(x)$를 구하면
>
> $$f'(x) = e^x \cos x + e^x(-\sin x) = e^x(\cos x - \sin x)$$
>
> $f'(\theta) = 0$에서
>
> $$e^\theta(\cos\theta - \sin\theta) = 0$$
>
> $e^\theta > 0$이므로
>
> $$\cos\theta - \sin\theta = 0$$
>
> $$\cos\theta = \sin\theta$$
>
> 양변을 $\cos\theta$로 나누면 ($\cos\theta \neq 0$인 범위에서)
>
> $$\tan\theta = 1$$
>
> $0 < \theta < \pi$에서
>
> $$\theta = \frac{\pi}{4}$$

---

## 5. 역함수의 미분

### 핵심 공식

$g(x)$가 $f(x)$의 역함수일 때:

$$g'(x) = \frac{1}{f'(g(x))}$$

또는 $f(g(x)) = x$의 양변을 미분하면:

$$f'(g(x)) \cdot g'(x) = 1$$

### 예제 133

함수 $f(x) = \sin x$ $\left(-\frac{\pi}{2} < x < \frac{\pi}{2}\right)$이고, 함수 $g(x)$는 임의의 실수 $x$에 대해서 $g(f(x)) = x$를 만족할 때, $g'\left(\frac{1}{2}\right)$의 값을 구하여라.

> [!summary]- 풀이
> $g(f(x)) = x$이므로 $g$는 $f$의 역함수이다.
>
> 양변을 $x$에 대해 미분하면
>
> $$f'(x) \cdot g'(f(x)) = 1$$
>
> $g'\left(\frac{1}{2}\right)$를 구하기 위해 $f(x) = \frac{1}{2}$인 $x$를 찾는다.
>
> $$\sin x = \frac{1}{2} \Rightarrow x = \frac{\pi}{6}$$ (주어진 범위에서)
>
> $x = \frac{\pi}{6}$을 대입하면
>
> $$f'\left(\frac{\pi}{6}\right) \cdot g'\left(\frac{1}{2}\right) = 1$$
>
> $f'(x) = \cos x$이므로
>
> $$f'\left(\frac{\pi}{6}\right) = \cos\frac{\pi}{6} = \frac{\sqrt{3}}{2}$$
>
> 따라서
>
> $$g'\left(\frac{1}{2}\right) = \frac{1}{f'\left(\frac{\pi}{6}\right)} = \frac{1}{\frac{\sqrt{3}}{2}} = \frac{2}{\sqrt{3}} = \frac{2\sqrt{3}}{3}$$

### 예제 134

미분가능한 함수 $f(x)$의 역함수 $g(x)$가 $\displaystyle\lim_{x \to 1} \frac{g(x) - 2}{x - 1} = 3$을 만족할 때, $f'(2)$의 값을 구하여라.

> [!summary]- 풀이
> 주어진 극한에서
>
> $$\lim_{x \to 1} \frac{g(x) - 2}{x - 1} = 3$$
>
> 이 극한이 존재하므로 $x \to 1$일 때 분자도 0으로 수렴해야 한다.
>
> $$g(1) = 2$$
>
> 따라서 주어진 극한은 미분계수의 정의이다.
>
> $$\lim_{x \to 1} \frac{g(x) - g(1)}{x - 1} = g'(1) = 3$$
>
> $g$가 $f$의 역함수이므로 $f(g(x)) = x$
>
> $g(1) = 2$이므로 $f(2) = 1$
>
> $f(g(x)) = x$의 양변을 미분하면
>
> $$f'(g(x)) \cdot g'(x) = 1$$
>
> $x = 1$을 대입하면
>
> $$f'(g(1)) \cdot g'(1) = 1$$
>
> $$f'(2) \cdot 3 = 1$$
>
> $$f'(2) = \frac{1}{3}$$

---

## 연습문제

다음 극한값을 구하시오.

(1) $f(x) = e^{2x}$일 때, $\displaystyle\lim_{h \to 0} \frac{f(1+h) - f(1-h)}{h}$

(2) $f(x) = \cos x$일 때, $\displaystyle\lim_{x \to 0} \frac{f\left(\frac{\pi}{2} + x\right) - f\left(\frac{\pi}{2}\right)}{x}$

---

## 관련 주제

- [[22-transcendental-derivative-1|22강: 초월함수의 도함수(1)]]
- [[24-transcendental-continuity|24강: 초월함수의 연속과 미분가능성]]
- [[12-advanced-trigonometry-5|12강: 심화삼각함수(5) - 삼각함수의 합성]]

---

**학습 포인트:**

1. 극한을 미분계수의 정의 형태로 변형하는 기술을 익힐 것
2. $\displaystyle\lim_{h \to 0} \frac{f(a+h) - f(a-h)}{h} = 2f'(a)$ 패턴을 기억할 것
3. 합성함수의 미분에서 연쇄법칙을 정확히 적용할 것
4. 역함수의 미분계수 관계식 $f'(g(x)) \cdot g'(x) = 1$을 활용할 것
5. $f'(\theta) = 0$을 풀 때 삼각함수의 합성을 활용할 수 있음을 기억할 것
