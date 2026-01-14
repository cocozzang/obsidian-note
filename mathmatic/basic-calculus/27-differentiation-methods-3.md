---
id: b3c5d7e9-f1a2-4b6c-8d0e-2f4a6b8c0d2e
aliases:
  - 여러가지 함수의 미분법(3)
  - 역함수의 미분법
  - 다항식의 나눗셈
  - n계도함수
tags:
  - 역함수미분법
  - 다항식나눗셈
  - 이계도함수
  - n계도함수
  - 수학적귀납법
pages: 74-78
subject: 대학기초수학
title: 여러가지 함수의 미분법(3) - 역함수 미분법, 다항식 나눗셈, n계도함수
topics:
  - 함수 방정식과 미분
  - 역함수의 미분법
  - 다항식의 나눗셈과 미분
  - 2계도함수와 n계도함수
---

# 여러가지 함수의 미분법(3)

## 1. 함수 방정식과 미분

함수 관계식이 주어졌을 때, 양변을 미분하여 도함수 값을 구할 수 있다.

### 예제 154

모든 실수 $x$에 대하여 미분가능한 함수 $f(x)$가 $f(1-2x) = f(x)$, $f'(1) = 5$일 때 $f'(-1) + f'(3)$의 값을 구하여라.

> [!summary]- 풀이
> **$f(1-2x) = f(x)$의 양변을 $x$로 미분**
> 
> $$-2f'(1-2x) = f'(x) \quad \cdots (*)$$
> 
> **$(*)$에 $x = 1$ 대입**
> 
> $$-2f'(-1) = f'(1) = 5$$
> 
> $$f'(-1) = -\frac{5}{2}$$
> 
> **$(*)$에 $x = -1$ 대입**
> 
> $$-2f'(3) = f'(-1) = -\frac{5}{2}$$
> 
> $$f'(3) = \frac{5}{4}$$
> 
> $$\therefore f'(-1) + f'(3) = -\frac{5}{2} + \frac{5}{4} = -\frac{5}{4}$$

---

### 예제 155

함수 $f(x) = \frac{1 + \sec x}{\tan x}$일 때 $f'\left(\frac{\pi}{3}\right)$의 값을 구하여라.

> [!summary]- 풀이
> **로그 미분법 적용**
> 
> $$\ln|f(x)| = \ln|1 + \sec x| - \ln|\tan x|$$
> 
> 양변을 $x$로 미분하면
> 
> $$\frac{f'(x)}{f(x)} = \frac{\sec x \tan x}{1 + \sec x} - \frac{\sec^2 x}{\tan x}$$
> 
> **$x = \frac{\pi}{3}$ 대입**
> 
> $\sec\frac{\pi}{3} = 2$, $\tan\frac{\pi}{3} = \sqrt{3}$이므로
> 
> $$\frac{f'\left(\frac{\pi}{3}\right)}{f\left(\frac{\pi}{3}\right)} = \frac{2 \cdot \sqrt{3}}{1 + 2} - \frac{4}{\sqrt{3}} = \frac{2\sqrt{3}}{3} - \frac{4\sqrt{3}}{3} = -\frac{2\sqrt{3}}{3}$$
> 
> $$f\left(\frac{\pi}{3}\right) = \frac{1 + 2}{\sqrt{3}} = \frac{3}{\sqrt{3}} = \sqrt{3}$$
> 
> $$f'\left(\frac{\pi}{3}\right) = -\frac{2\sqrt{3}}{3} \cdot \sqrt{3} = -\frac{2 \cdot 3}{3} = -2$$

---

## 2. 역함수의 미분법

### Thm (29): 역함수의 미분법

미분가능한 함수 $f(x)$의 역함수 $y = f^{-1}(x)$가 존재하고 미분가능할 때

$$(f^{-1})'(x) = \frac{1}{f'(y)}$$

> [!summary]- 유도 과정
> **방법 1: 역함수 관계 이용**
> 
> $y = f^{-1}(x)$이면 $x = f(y)$이므로
> 
> $$\frac{dx}{dy} = f'(y)$$
> 
> $$(f^{-1})'(x) = \frac{dy}{dx} = \frac{1}{\frac{dx}{dy}} = \frac{1}{f'(y)}$$
> 
> **방법 2: 항등관계 이용**
> 
> $f(f^{-1}(x)) = x$의 양변을 $x$로 미분하면
> 
> $$f'(f^{-1}(x)) \cdot (f^{-1})'(x) = 1$$
> 
> $$(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))} = \frac{1}{f'(y)}$$

---

### 예제 156

함수 $f(x) = \tan x$ $\left(-\frac{\pi}{2} < x < \frac{\pi}{2}\right)$와 그 역함수 $g(x)$에 대하여 $g'(\sqrt{3})$의 값을 구하여라.

> [!summary]- 풀이
> $g(x) = f^{-1}(x)$이고, $\tan\frac{\pi}{3} = \sqrt{3}$이므로 $g(\sqrt{3}) = \frac{\pi}{3}$
> 
> 역함수 미분법에 의해
> 
> $$g'(\sqrt{3}) = \frac{1}{f'\left(\frac{\pi}{3}\right)}$$
> 
> $f'(x) = \sec^2 x$이므로
> 
> $$f'\left(\frac{\pi}{3}\right) = \sec^2\frac{\pi}{3} = \frac{1}{\cos^2\frac{\pi}{3}} = \frac{1}{\left(\frac{1}{2}\right)^2} = 4$$
> 
> $$\therefore g'(\sqrt{3}) = \frac{1}{4}$$

---

### 예제 157

예제 156에서 $g'(x)$를 $x$에 관한 함수로 나타내어라.

> [!summary]- 풀이
> $y = g(x)$이면 $x = \tan y$
> 
> **방법 1: 음함수 미분**
> 
> $x = \tan y$의 양변을 $x$로 미분하면
> 
> $$1 = \sec^2 y \cdot \frac{dy}{dx}$$
> 
> $$\frac{dy}{dx} = \frac{1}{\sec^2 y} = \cos^2 y$$
> 
> **$x$에 관한 식으로 변환**
> 
> $x = \tan y$이므로 직각삼각형에서 밑변 $= 1$, 높이 $= x$, 빗변 $= \sqrt{1+x^2}$
> 
> $$\cos y = \frac{1}{\sqrt{1+x^2}}$$
> 
> $$\therefore g'(x) = \cos^2 y = \frac{1}{1+x^2}$$
> 
> > [!note] 참고
> > 이것이 $(\arctan x)' = \frac{1}{1+x^2}$의 유도 과정이다.

---

### 예제 158

함수 $f(x) = \frac{e^x - e^{-x}}{2}$일 때 $(f^{-1})'(0)$의 값을 구하여라.

> [!summary]- 풀이
> $(f^{-1})'(0) = \frac{1}{f'(\alpha)}$ (단, $f(\alpha) = 0$)
> 
> $f(0) = \frac{e^0 - e^0}{2} = 0$이므로 $\alpha = 0$
> 
> $$f'(x) = \frac{e^x + e^{-x}}{2}$$
> 
> $$f'(0) = \frac{1 + 1}{2} = 1$$
> 
> $$\therefore (f^{-1})'(0) = \frac{1}{1} = 1$$

---

### 예제 159

함수 $f(x) = x^3 + x^2 + x + 2$의 역함수 $g(x)$에 대하여 $g'(5)$의 값을 구하여라.

> [!summary]- 풀이
> $g'(5) = \frac{1}{f'(\alpha)}$ (단, $f(\alpha) = 5$)
> 
> $f(1) = 1 + 1 + 1 + 2 = 5$이므로 $\alpha = 1$
> 
> $$f'(x) = 3x^2 + 2x + 1$$
> 
> $$f'(1) = 3 + 2 + 1 = 6$$
> 
> $$\therefore g'(5) = \frac{1}{6}$$

---

### 예제 160

$$\lim_{x \to 1} \frac{f(x) - 1}{x - 1} = 3$$

을 만족시키는 미분가능한 함수 $f(x)$가 역함수 $g(x)$를 가질 때 $g'(1)$의 값을 구하여라.

> [!summary]- 풀이
> $g'(1) = \frac{1}{f'(\alpha)}$ (단, $f(\alpha) = 1$)
> 
> 주어진 극한식에서 $x \to 1$일 때 분모 $\to 0$이고 극한값이 존재하므로 분자 $\to 0$
> 
> 따라서 $f(1) = 1$이므로 $\alpha = 1$
> 
> $$\lim_{x \to 1} \frac{f(x) - 1}{x - 1} = \lim_{x \to 1} \frac{f(x) - f(1)}{x - 1} = f'(1) = 3$$
> 
> $$\therefore g'(1) = \frac{1}{f'(1)} = \frac{1}{3}$$

---

## 3. 다항식의 나눗셈과 미분

다항식 $f(x)$가 $(x-a)^2$으로 나누어 떨어지면:
- $f(a) = 0$ (나머지가 0)
- $f'(a) = 0$ (중근 조건)

### 예제 161

다항식 $f(x) = x^{100} + ax + b$가 $(x-1)^2$으로 나누어 떨어질 때 $a + b$의 값을 구하여라. (단, $a$, $b$는 상수)

> [!summary]- 풀이
> $f(x) = (x-1)^2 \cdot g(x)$로 나타낼 수 있으므로
> 
> **조건 1: $f(1) = 0$**
> 
> $$f(1) = 1 + a + b = 0 \quad \cdots (1)$$
> 
> **조건 2: $f'(1) = 0$**
> 
> $$f'(x) = 100x^{99} + a$$
> 
> $$f'(1) = 100 + a = 0$$
> 
> $$a = -100$$
> 
> $(1)$에 대입하면
> 
> $$1 - 100 + b = 0$$
> 
> $$b = 99$$
> 
> $$\therefore a + b = -100 + 99 = -1$$

---

### 예제 162

다항식 $f(x) = x^{10} + 2ax + b$가 $(x-2)^2$으로 나누어 떨어질 때 $f(1)$의 값을 구하여라.

> [!summary]- 풀이
> **조건 1: $f(2) = 0$**
> 
> $$f(2) = 2^{10} + 4a + b = 0$$
> 
> $$4a + b = -2^{10} \quad \cdots (1)$$
> 
> **조건 2: $f'(2) = 0$**
> 
> $$f'(x) = 10x^9 + 2a$$
> 
> $$f'(2) = 10 \cdot 2^9 + 2a = 0$$
> 
> $$a = -5 \cdot 2^9$$
> 
> $(1)$에 대입하면
> 
> $$b = -2^{10} - 4a = -2^{10} - 4(-5 \cdot 2^9) = -2^{10} + 20 \cdot 2^9 = -2^{10} + 10 \cdot 2^{10} = 9 \cdot 2^{10}$$
> 
> **$f(1)$ 계산**
> 
> $$f(x) = x^{10} + 2(-5 \cdot 2^9)x + 9 \cdot 2^{10} = x^{10} - 5 \cdot 2^{10}x + 9 \cdot 2^{10}$$
> 
> $$f(1) = 1 - 5 \cdot 2^{10} + 9 \cdot 2^{10} = 1 + 4 \cdot 2^{10}$$

---

## 4. 2계도함수, n계도함수

### Thm (30): 2계도함수, n계도함수

**(1) 2계도함수**

함수 $f(x)$의 도함수 $f'(x)$가 모든 실수 $x$에 대하여 미분가능할 때, $f'(x)$의 도함수를 함수 $f(x)$의 **2계도함수**라고 하고 다음과 같이 나타낸다:

$$f''(x), \quad y'', \quad \frac{d^2y}{dx^2}, \quad \frac{d^2}{dx^2}f(x)$$

**(2) n계도함수**

양의 정수 $n$에 대하여 함수 $f(x)$를 $n$번 미분하여 얻은 함수를 함수 $f(x)$의 **n계도함수**라 하고 다음과 같이 나타낸다:

$$f^{(n)}(x), \quad y^{(n)}, \quad \frac{d^ny}{dx^n}, \quad \frac{d^n}{dx^n}f(x)$$

---

### 예제 163

함수 $y = e^x \sin x$의 $n$계 도함수는 $y^{(n)} = (\sqrt{2})^n e^x \sin\left(x + \frac{n\pi}{4}\right)$임을 증명하여라.

> [!summary]- 풀이 (수학적 귀납법)
> **[1] $n = 1$인 경우**
> 
> $$y' = e^x \sin x + e^x \cos x = e^x(\sin x + \cos x)$$
> 
> 삼각함수의 합성: $\sin x + \cos x = \sqrt{2}\sin\left(x + \frac{\pi}{4}\right)$
> 
> $$y' = \sqrt{2} \cdot e^x \sin\left(x + \frac{\pi}{4}\right)$$
> 
> $n = 1$일 때 성립 ✓
> 
> **[2] $n = k$일 때 성립한다고 가정**
> 
> $$y^{(k)} = (\sqrt{2})^k e^x \sin\left(x + \frac{k\pi}{4}\right)$$
> 
> **[3] $n = k + 1$일 때 성립함을 보임**
> 
> $$y^{(k+1)} = \frac{d}{dx}\left[(\sqrt{2})^k e^x \sin\left(x + \frac{k\pi}{4}\right)\right]$$
> 
> $$= (\sqrt{2})^k \left[e^x \sin\left(x + \frac{k\pi}{4}\right) + e^x \cos\left(x + \frac{k\pi}{4}\right)\right]$$
> 
> $$= (\sqrt{2})^k e^x \left[\sin\left(x + \frac{k\pi}{4}\right) + \cos\left(x + \frac{k\pi}{4}\right)\right]$$
> 
> 삼각함수의 합성 적용:
> 
> $$= (\sqrt{2})^k e^x \cdot \sqrt{2} \sin\left(x + \frac{k\pi}{4} + \frac{\pi}{4}\right)$$
> 
> $$= (\sqrt{2})^{k+1} e^x \sin\left(x + \frac{(k+1)\pi}{4}\right)$$
> 
> $n = k + 1$일 때도 성립 ✓
> 
> 따라서 수학적 귀납법에 의해 모든 자연수 $n$에 대해 성립한다.

---

### 예제 164

함수 $f(x) = e^{2x}$의 $n$계 도함수 $f^{(n)}(x)$에 대하여 $\sum_{n=1}^{\infty} \frac{e^2}{f^{(n)}(2)}$의 값을 구하여라.

> [!summary]- 풀이
> **$n$계 도함수 구하기**
> 
> $$f'(x) = 2e^{2x}$$
> 
> $$f''(x) = 4e^{2x} = 2^2 e^{2x}$$
> 
> $$f^{(n)}(x) = 2^n e^{2x}$$
> 
> **$f^{(n)}(2)$ 계산**
> 
> $$f^{(n)}(2) = 2^n e^4$$
> 
> **급수 계산**
> 
> $$\sum_{n=1}^{\infty} \frac{e^2}{f^{(n)}(2)} = \sum_{n=1}^{\infty} \frac{e^2}{2^n e^4} = \frac{1}{e^2} \sum_{n=1}^{\infty} \left(\frac{1}{2}\right)^n$$
> 
> 등비급수의 합: $\sum_{n=1}^{\infty} \left(\frac{1}{2}\right)^n = \frac{\frac{1}{2}}{1 - \frac{1}{2}} = 1$
> 
> $$\therefore \sum_{n=1}^{\infty} \frac{e^2}{f^{(n)}(2)} = \frac{1}{e^2}$$

---

### 예제 165

함수 $f(x) = e^{2x} \cos x$의 2계 도함수 $f''(x) = 0$을 만족하는 $x$를 $\alpha$라 할 때 $\sec^2\alpha$의 값을 구하여라. (단, $0 < \alpha < \frac{\pi}{2}$)

> [!summary]- 풀이
> **1계 도함수**
> 
> $$f'(x) = 2e^{2x}\cos x - e^{2x}\sin x = e^{2x}(2\cos x - \sin x)$$
> 
> **2계 도함수**
> 
> $$f''(x) = 2e^{2x}(2\cos x - \sin x) + e^{2x}(-2\sin x - \cos x)$$
> 
> $$= e^{2x}(4\cos x - 2\sin x - 2\sin x - \cos x)$$
> 
> $$= e^{2x}(3\cos x - 4\sin x)$$
> 
> **$f''(\alpha) = 0$ 조건**
> 
> $$e^{2\alpha}(3\cos\alpha - 4\sin\alpha) = 0$$
> 
> $e^{2\alpha} \neq 0$이므로
> 
> $$3\cos\alpha = 4\sin\alpha$$
> 
> $$\tan\alpha = \frac{3}{4}$$
> 
> **$\sec^2\alpha$ 계산**
> 
> $$\sec^2\alpha = 1 + \tan^2\alpha = 1 + \frac{9}{16} = \frac{25}{16}$$

---

### 예제 166

함수 $f(x) = \ln x$의 $n$계 도함수를 구하여라.

> [!summary]- 풀이
> $$f'(x) = \frac{1}{x} = x^{-1}$$
> 
> $$f''(x) = -x^{-2} = -\frac{1}{x^2}$$
> 
> $$f'''(x) = 2x^{-3} = \frac{2}{x^3} = \frac{2!}{x^3}$$
> 
> $$f^{(4)}(x) = -6x^{-4} = -\frac{6}{x^4} = -\frac{3!}{x^4}$$
> 
> 규칙을 관찰하면
> 
> $$\therefore f^{(n)}(x) = \frac{(-1)^{n-1}(n-1)!}{x^n} \quad (n \geq 1)$$

---

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 역함수 미분법, 다항식 나눗셈과 미분의 관계, n계도함수의 규칙을 숙지하시오.)

---

## 관련 주제

- [[26-differentiation-methods-2|여러가지 함수의 미분법(2)]]
- [[28-mean-value-theorem|롤의 정리, 평균값 정리]]

---

**학습 포인트:**
1. **함수 방정식의 미분**: 관계식 양변을 미분하여 도함수 값 찾기
2. **역함수 미분법**: $(f^{-1})'(x) = \frac{1}{f'(y)}$, $f(\alpha) = x$인 $\alpha$ 찾기가 핵심
3. **다항식 나눗셈**: $(x-a)^2$으로 나누어 떨어지면 $f(a) = 0$, $f'(a) = 0$
4. **n계도함수**: 규칙을 찾아 일반항으로 표현, 수학적 귀납법으로 증명
5. **주요 n계도함수**: $(e^{ax})^{(n)} = a^n e^{ax}$, $(\ln x)^{(n)} = \frac{(-1)^{n-1}(n-1)!}{x^n}$
