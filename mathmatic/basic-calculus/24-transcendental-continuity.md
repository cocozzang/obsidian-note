---
id: a7f3c8d2-4e91-4b5a-9c6f-8d2e1a3b5c7f
aliases:
  - 초월함수의 연속과 미분가능성
  - 초월함수 연속성
  - 초월함수 미분가능성
tags:
  - 초월함수
  - 연속성
  - 미분가능성
  - 함수방정식
  - 조각함수
pages: 67-69
subject: 대학기초수학
title: 초월함수의 연속과 미분가능성
topics:
  - 함수방정식과 미분
  - 초월함수의 연속조건
  - 초월함수의 미분가능성 판정
  - 도함수의 연속성 조사
---

# 초월함수의 연속과 미분가능성

## 1. 핵심 개념

### 연속성 조건

함수 $f(x)$가 $x = a$에서 연속이 되려면:

$$f(a) = \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$$

### 미분가능성 조건

함수 $f(x)$가 $x = a$에서 미분가능하려면:

1. **연속성**: $x = a$에서 연속
2. **좌미분 = 우미분**: $f'_-(a) = f'_+(a)$

$$f'_-(a) = \lim_{h \to 0^-} \frac{f(a+h) - f(a)}{h}, \quad f'_+(a) = \lim_{h \to 0^+} \frac{f(a+h) - f(a)}{h}$$

### 주요 극한 공식

$$\lim_{x \to 0} (1+x)^{\frac{1}{x}} = e, \quad \lim_{x \to 0} \frac{\sin x}{x} = 1$$

---

## 2. 예제

### 예제 135

모든 실수 $x$에 대하여 미분가능한 함수 $f(x)$가 다음 조건을 만족할 때 $f(2) \times f'(2)$의 값을 구하여라.

(조건 Ⅰ) $f(x) > 0$이고 $f'(0) = 2$이다.

(조건 Ⅱ) 임의의 두 실수 $x, y$에 대하여 $f(x+y) = f(x)f(y)$이다.

> [!summary]- 풀이
> **Step 1: $f(0)$ 구하기**
>
> 조건 Ⅱ에서 $x = y = 0$ 대입:
>
> $$f(0) = f(0) \cdot f(0)$$
>
> $$f(0) = [f(0)]^2$$
>
> $f(x) > 0$이므로 $f(0) \neq 0$, 따라서:
>
> $$f(0) = 1$$
>
> **Step 2: $f'(x)$와 $f(x)$의 관계 유도**
>
> 조건 Ⅱ의 양변을 $y$에 대해 편미분 후 $y = 0$ 대입:
>
> $$f'(x+y) = f(x) \cdot f'(y)$$
>
> $y = 0$ 대입:
>
> $$f'(x) = f(x) \cdot f'(0) = 2f(x)$$
>
> **Step 3: $f(x)$ 결정**
>
> $$\frac{f'(x)}{f(x)} = 2$$
>
> $\frac{f'(x)}{f(x)} = [\ln f(x)]'$이므로:
>
> $$[\ln f(x)]' = 2$$
>
> 양변 적분:
>
> $$\ln f(x) = 2x + C$$
>
> $$f(x) = e^{2x + C}$$
>
> $f(0) = 1$에서 $e^C = 1$이므로 $C = 0$
>
> $$\therefore f(x) = e^{2x}$$
>
> **Step 4: 답 계산**
>
> $$f(2) = e^4, \quad f'(x) = 2e^{2x}, \quad f'(2) = 2e^4$$
>
> $$f(2) \times f'(2) = e^4 \times 2e^4 = 2e^8$$

---

### 예제 136

실수 전체의 집합에서 정의된 함수

$$f(x) = \begin{cases} \frac{a - \cos 2x}{x^2} & (x \neq 0) \\ b & (x = 0) \end{cases}$$

가 $x = 0$에서 연속이 되도록 상수 $a, b$의 값을 정할 때 $a + b$의 값을 구하여라.

> [!summary]- 풀이
> **연속 조건**: $f(0) = \lim_{x \to 0} f(x)$
>
> $$b = \lim_{x \to 0} \frac{a - \cos 2x}{x^2}$$
>
> **Step 1: $a$ 결정**
>
> 극한이 유한확정값 $b$를 가지려면 (분모 → 0이므로 분자도 → 0):
>
> $$\lim_{x \to 0} (a - \cos 2x) = 0$$
>
> $$a - 1 = 0 \quad \therefore a = 1$$
>
> **Step 2: $b$ 계산**
>
> $\cos 2x = 1 - 2\sin^2 x$ 이용:
>
> $$b = \lim_{x \to 0} \frac{1 - \cos 2x}{x^2} = \lim_{x \to 0} \frac{1 - (1 - 2\sin^2 x)}{x^2}$$
>
> $$= \lim_{x \to 0} \frac{2\sin^2 x}{x^2} = 2 \cdot \lim_{x \to 0} \left(\frac{\sin x}{x}\right)^2 = 2 \cdot 1^2 = 2$$
>
> $$\therefore a + b = 1 + 2 = 3$$

---

### 예제 137

함수

$$f(x) = \begin{cases} e^x \cos x & (x \geq 0) \\ 2x^2 + px + q & (x < 0) \end{cases}$$

가 $x = 0$에서 미분가능할 때 $p + q$를 구하여라. (단, $p, q$는 상수)

> [!summary]- 풀이
> **Step 1: 연속성 확인**
>
> $$f(0) = e^0 \cos 0 = 1 \cdot 1 = 1$$
>
> $$\lim_{x \to 0^+} f(x) = \lim_{x \to 0^+} e^x \cos x = 1$$
>
> $$\lim_{x \to 0^-} f(x) = \lim_{x \to 0^-} (2x^2 + px + q) = q$$
>
> 연속이려면 $q = 1$
>
> **Step 2: 좌미분과 우미분 비교**
>
> 우미분 ($x \geq 0$에서 $f(x) = e^x \cos x$):
>
> $$f'(x) = e^x \cos x - e^x \sin x$$
>
> $$f'_+(0) = 1 \cdot 1 - 1 \cdot 0 = 1$$
>
> 좌미분 ($x < 0$에서 $f(x) = 2x^2 + px + q$):
>
> $$f'(x) = 4x + p$$
>
> $$f'_-(0) = p$$
>
> 미분가능하려면 $f'_-(0) = f'_+(0)$:
>
> $$p = 1$$
>
> $$\therefore p + q = 1 + 1 = 2$$

---

### 예제 138

함수

$$f(x) = \begin{cases} (1+x)^{\frac{1}{\sin x}} & (-\pi < x < \pi, \ x \neq 0) \\ k & (x = 0) \end{cases}$$

가 $x = 0$에서 연속일 때 $k$의 값을 구하여라.

> [!summary]- 풀이
> **연속 조건**: $f(0) = \lim_{x \to 0} f(x)$
>
> $$\lim_{x \to 0} (1+x)^{\frac{1}{\sin x}}$$
>
> $x \to 0$일 때 $\sin x \approx x$이므로:
>
> $$= \lim_{x \to 0} (1+x)^{\frac{1}{x} \cdot \frac{x}{\sin x}}$$
>
> $$= \left[\lim_{x \to 0} (1+x)^{\frac{1}{x}}\right]^{\lim_{x \to 0} \frac{x}{\sin x}}$$
>
> $$= e^1 = e$$
>
> $$\therefore k = e$$

---

### 예제 139

구간 $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$에서 연속인 함수 $f(x) = \frac{2x}{\ln(1 + \sin x)}$일 때 $f(0)$의 값을 구하여라.

> [!summary]- 풀이
> $x = 0$에서 직접 대입하면 $\frac{0}{0}$ 꼴이므로 극한으로 계산:
>
> $$f(0) = \lim_{x \to 0} \frac{2x}{\ln(1 + \sin x)}$$
>
> 지수 형태로 변형:
>
> $$= \lim_{x \to 0} \frac{1}{\ln(1 + \sin x)^{\frac{1}{2x}}}$$
>
> $$= \lim_{x \to 0} \frac{1}{\ln\left[(1 + \sin x)^{\frac{1}{\sin x}}\right]^{\frac{\sin x}{2x}}}$$
>
> $\lim_{t \to 0} (1+t)^{\frac{1}{t}} = e$ 이용:
>
> $$= \frac{1}{\ln e^{\frac{1}{2}}} = \frac{1}{\frac{1}{2}} = 2$$
>
> $$\therefore f(0) = 2$$

---

### 예제 140

함수

$$f(x) = \begin{cases} e^x & (x \leq 1) \\ a \sin \pi x + b & (x > 1) \end{cases}$$

가 $x = 1$에서 미분가능하도록 상수 $a, b$의 값을 정할 때 $\frac{b}{a}$의 값을 구하여라.

> [!summary]- 풀이
> **Step 1: 연속성**
>
> $$f(1) = e^1 = e$$
>
> $$\lim_{x \to 1^-} f(x) = e^1 = e$$
>
> $$\lim_{x \to 1^+} f(x) = a \sin \pi + b = a \cdot 0 + b = b$$
>
> 연속이려면 $b = e$
>
> **Step 2: 좌미분과 우미분 비교**
>
> $$f'(x) = \begin{cases} e^x & (x < 1) \\ a\pi \cos \pi x & (x > 1) \end{cases}$$
>
> $$f'_-(1) = e^1 = e$$
>
> $$f'_+(1) = a\pi \cos \pi = a\pi \cdot (-1) = -a\pi$$
>
> 미분가능하려면:
>
> $$e = -a\pi \quad \therefore a = -\frac{e}{\pi}$$
>
> **Step 3: 답 계산**
>
> $$\frac{b}{a} = \frac{e}{-\frac{e}{\pi}} = -\pi$$

---

### 예제 141

함수

$$f(x) = \begin{cases} e^{x-a} & (x < 1) \\ \ln x + b & (x \geq 1) \end{cases}$$

가 $x = 1$에서 미분가능하기 위한 $a + \ln b$의 값을 구하여라. (단, $a, b$는 상수)

> [!summary]- 풀이
> **Step 1: 연속성**
>
> $$f(1) = \ln 1 + b = b$$
>
> $$\lim_{x \to 1^-} f(x) = e^{1-a}$$
>
> $$\lim_{x \to 1^+} f(x) = \ln 1 + b = b$$
>
> 연속이려면:
>
> $$e^{1-a} = b \quad \cdots (*)$$
>
> **Step 2: 좌미분과 우미분 비교**
>
> $$f'(x) = \begin{cases} e^{x-a} & (x < 1) \\ \frac{1}{x} & (x > 1) \end{cases}$$
>
> $$f'_-(1) = e^{1-a}, \quad f'_+(1) = \frac{1}{1} = 1$$
>
> 미분가능하려면:
>
> $$e^{1-a} = 1$$
>
> $$1 - a = 0 \quad \therefore a = 1$$
>
> **Step 3: $b$ 결정**
>
> $(*)$에서: $b = e^{1-1} = e^0 = 1$
>
> $$\therefore \ln b = \ln 1 = 0$$
>
> $$a + \ln b = 1 + 0 = 1$$

---

### 예제 142

함수

$$f(x) = \begin{cases} \frac{\sin(x^2)}{x} & (x \neq 0) \\ 0 & (x = 0) \end{cases}$$

일 때 $f'(x)$의 $x = 0$에서의 연속성을 조사하여라.

> [!summary]- 풀이
> **$f'(x)$가 $x = 0$에서 연속이려면**: $f'(0) = \lim_{x \to 0} f'(x)$
>
> **Step 1: $f'(0)$ 계산 (미분계수 정의 이용)**
>
> $$f'(0) = \lim_{h \to 0} \frac{f(0+h) - f(0)}{h} = \lim_{h \to 0} \frac{\frac{\sin h^2}{h} - 0}{h}$$
>
> $$= \lim_{h \to 0} \frac{\sin h^2}{h^2} = 1$$
>
> **Step 2: $\lim_{x \to 0} f'(x)$ 계산**
>
> $x \neq 0$에서 $f(x) = \frac{\sin(x^2)}{x}$의 도함수:
>
> $$f'(x) = \frac{2x \cdot x \cdot \cos(x^2) - \sin(x^2)}{x^2} = \frac{2x^2 \cos(x^2) - \sin(x^2)}{x^2}$$
>
> $$\lim_{x \to 0} f'(x) = \lim_{x \to 0} \left(2\cos(x^2) - \frac{\sin(x^2)}{x^2}\right)$$
>
> $$= 2 \cdot 1 - 1 = 1$$
>
> **결론**
>
> $$f'(0) = 1 = \lim_{x \to 0} f'(x)$$
>
> $\therefore$ **$f'(x)$는 $x = 0$에서 연속이다.**

---

### 예제 143

함수

$$f(x) = \begin{cases} x \sin \frac{1}{x} & (x \neq 0) \\ 0 & (x = 0) \end{cases}$$

일 때 $f(x)$의 $x = 0$에서의 연속성과 미분가능성을 조사하여라.

> [!summary]- 풀이
> **Part 1: 연속성 조사**
>
> 연속 조건: $f(0) = \lim_{x \to 0} f(x)$
>
> $\lim_{x \to 0} x \sin \frac{1}{x}$에서 $\sin \frac{1}{x}$는 진동하므로 샌드위치 정리 적용:
>
> $$-1 \leq \sin \frac{1}{x} \leq 1$$
>
> $x > 0$일 때: $-x \leq x \sin \frac{1}{x} \leq x$
>
> $x \to 0^+$일 때: $0 \leq \lim_{x \to 0^+} x \sin \frac{1}{x} \leq 0$
>
> $$\therefore \lim_{x \to 0^+} x \sin \frac{1}{x} = 0$$
>
> $x < 0$일 때: $-x \geq x \sin \frac{1}{x} \geq x$ (부등호 방향 반전)
>
> $x \to 0^-$일 때: $0 \geq \lim_{x \to 0^-} x \sin \frac{1}{x} \geq 0$
>
> $$\therefore \lim_{x \to 0^-} x \sin \frac{1}{x} = 0$$
>
> $f(0) = 0$이므로:
>
> $$\therefore \textbf{f(x)는 x = 0에서 연속이다.}$$
>
> ---
>
> **Part 2: 미분가능성 조사**
>
> 미분계수 정의로 $f'(0)$ 계산:
>
> $$f'(0) = \lim_{h \to 0} \frac{f(0+h) - f(0)}{h} = \lim_{h \to 0} \frac{h \sin \frac{1}{h} - 0}{h}$$
>
> $$= \lim_{h \to 0} \sin \frac{1}{h}$$
>
> $h \to 0$일 때 $\frac{1}{h} \to \pm\infty$이므로 $\sin \frac{1}{h}$는 $-1$과 $1$ 사이에서 무한히 진동한다.
>
> **극한값이 존재하지 않는다** → $f'(0)$이 존재하지 않는다.
>
> $$\therefore \textbf{f(x)는 x = 0에서 미분불가능하다.}$$

---

## 3. 핵심 정리

### 연속이지만 미분불가능한 함수

예제 143의 $f(x) = x \sin \frac{1}{x}$는 $x = 0$에서:

- **연속**: 샌드위치 정리로 극한값 0 확인
- **미분불가능**: $\sin \frac{1}{x}$의 진동으로 미분계수 극한 미존재

### 도함수의 연속성

함수 $f(x)$가 미분가능하더라도 $f'(x)$가 연속이 아닐 수 있다. (예제 142는 연속인 경우)

도함수의 연속성 조사: $f'(a) = \lim_{x \to a} f'(x)$ 확인

### 미분가능성 판정 순서

1. **연속성 확인**: $f(a) = \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$
2. **좌미분 = 우미분**: $f'_-(a) = f'_+(a)$

---

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 초월함수의 연속성과 미분가능성 판정법을 숙지하시오.)

---

## 관련 주제

- [[23-transcendental-derivative-2|초월함수의 도함수(2)]]
- [[25-differentiation-methods-1|여러가지 함수의 미분법(1)]]
- [[21-differentiability|미분가능성]]

---

**학습 포인트:**

1. 조각함수의 연속성: 경계점에서 좌극한 = 우극한 = 함수값
2. 조각함수의 미분가능성: 연속 + 좌미분 = 우미분
3. 함수방정식 문제: 특정 값 대입으로 $f(0)$ 등 기본값 결정
4. 도함수의 연속성: $f'(a)$와 $\lim_{x \to a} f'(x)$ 비교
5. 샌드위치 정리: 진동하는 함수의 극한 계산에 활용
