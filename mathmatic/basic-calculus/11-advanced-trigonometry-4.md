---
id: 8b4f2e91-3c5a-4f2b-8d1a-9e6f3a5c7d8b
aliases:
  - 심화삼각함수(4)
  - 삼각함수 기타공식
  - 곱을 합차로
  - 합차를 곱으로
tags:
  - 삼각함수
  - 곱셈공식
  - 합차공식
  - 삼각함수변환
  - 중급
pages: 30-32
subject: 대학기초수학
title: 심화삼각함수(4) - 기타공식
topics:
  - 삼각함수의 곱을 합차로 변환
  - 삼각함수의 합차를 곱으로 변환
  - 기타공식 응용
---

# 심화삼각함수(4) - 기타공식

## 1. Thm (16): 기타공식

삼각함수의 곱을 합차로 변환하거나 합차를 곱으로 변환하는 공식들입니다.

### 합차를 곱으로 변환하는 공식

**(1) 사인의 합**

$$\sin A + \sin B = 2\sin\frac{A+B}{2}\cos\frac{A-B}{2}$$

**대응되는 곱셈 공식:**

$$\sin\alpha\cos\beta = \frac{1}{2}\{\sin(\alpha+\beta)+\sin(\alpha-\beta)\}$$

---

**(2) 사인의 차**

$$\sin A - \sin B = 2\cos\frac{A+B}{2}\sin\frac{A-B}{2}$$

**대응되는 곱셈 공식:**

$$\cos\alpha\sin\beta = \frac{1}{2}\{\sin(\alpha+\beta)-\sin(\alpha-\beta)\}$$

---

**(3) 코사인의 합**

$$\cos A + \cos B = 2\cos\frac{A+B}{2}\cos\frac{A-B}{2}$$

**대응되는 곱셈 공식:**

$$\cos\alpha\cos\beta = \frac{1}{2}\{\cos(\alpha+\beta)+\cos(\alpha-\beta)\}$$

---

**(4) 코사인의 차**

$$\cos A - \cos B = -2\sin\frac{A+B}{2}\sin\frac{A-B}{2}$$

**대응되는 곱셈 공식:**

$$\sin\alpha\sin\beta = -\frac{1}{2}\{\cos(\alpha+\beta)-\cos(\alpha-\beta)\}$$

### 공식 유도 과정

#### (1)과 (2)의 증명: 덧셈정리를 이용한 유도

**덧셈정리로부터:**

$\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta \quad \cdots \text{(ㄱ)}$

$\sin(\alpha-\beta) = \sin\alpha\cos\beta - \cos\alpha\sin\beta \quad \cdots \text{(ㄴ)}$

**(ㄱ) + (ㄴ):** 두 식을 더하면

$\sin(\alpha+\beta) + \sin(\alpha-\beta) = 2\sin\alpha\cos\beta \quad \cdots \text{(ㄷ)}$

따라서:

$\sin\alpha\cos\beta = \frac{1}{2}\{\sin(\alpha+\beta) + \sin(\alpha-\beta)\}$

**(ㄱ) - (ㄴ):** 두 식을 빼면

$\sin(\alpha+\beta) - \sin(\alpha-\beta) = 2\cos\alpha\sin\beta \quad \cdots \text{(ㄹ)}$

따라서:

$\cos\alpha\sin\beta = \frac{1}{2}\{\sin(\alpha+\beta) - \sin(\alpha-\beta)\}$

**변수 치환을 통한 합차 공식 유도:**

(ㄷ)에서 $\alpha + \beta = A$, $\alpha - \beta = B$로 놓으면:

- $\alpha = \frac{A+B}{2}$
- $\beta = \frac{A-B}{2}$

따라서:

$\sin A + \sin B = 2\sin\frac{A+B}{2}\cos\frac{A-B}{2}$

(ㄹ)에서 같은 치환을 하면:

$\sin A - \sin B = 2\cos\frac{A+B}{2}\sin\frac{A-B}{2}$

---

#### (3)과 (4)의 증명: 코사인 덧셈정리를 이용

**덧셈정리로부터:**

$\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta \quad \cdots \text{(ㅁ)}$

$\cos(\alpha-\beta) = \cos\alpha\cos\beta + \sin\alpha\sin\beta \quad \cdots \text{(ㅂ)}$

**(ㅁ) + (ㅂ):** 두 식을 더하면

$\cos(\alpha+\beta) + \cos(\alpha-\beta) = 2\cos\alpha\cos\beta \quad \cdots \text{(ㅅ)}$

따라서:

$\cos\alpha\cos\beta = \frac{1}{2}\{\cos(\alpha+\beta) + \cos(\alpha-\beta)\}$

**(ㅁ) - (ㅂ):** 두 식을 빼면

$\cos(\alpha+\beta) - \cos(\alpha-\beta) = -2\sin\alpha\sin\beta \quad \cdots \text{(ㅇ)}$

따라서:

$\sin\alpha\sin\beta = -\frac{1}{2}\{\cos(\alpha+\beta) - \cos(\alpha-\beta)\}$

**변수 치환을 통한 합차 공식 유도:**

(ㅅ)에서 $\alpha + \beta = A$, $\alpha - \beta = B$로 놓으면:

$\cos A + \cos B = 2\cos\frac{A+B}{2}\cos\frac{A-B}{2}$

(ㅇ)에서 같은 치환을 하면:

$\cos A - \cos B = -2\sin\frac{A+B}{2}\sin\frac{A-B}{2}$

---

### 공식의 활용

**합차를 곱으로**: $A = \alpha + \beta$, $B = \alpha - \beta$로 치환하면

- $\frac{A+B}{2} = \alpha$
- $\frac{A-B}{2} = \beta$

**곱을 합차로**: 덧셈정리를 활용하여 곱셈을 합차로 변환

---

## 2. 예제

### 예제 60

삼각형 $ABC$에서 $\sin(A+B)\sin(A-B)=\sin^2 C$일 때 $\angle A$의 크기는?

> [!summary]- 풀이
> 곱을 합차로 변환하는 공식을 사용:
> $\sin(A+B)\sin(A-B) = -\frac{1}{2}\{\cos 2A - \cos 2B\}$
>
> 삼각형의 내각의 합에서 $A + B + C = \pi$이므로:
> $\sin^2 A - \sin^2 B = \sin^2 C$
>
> 삼각형에서 사인 법칙을 적용하면:
> $\sin A = \sin B + \sin C$
>
> 이를 정리하면:
> $\left(\frac{a}{2R}\right)^2 = \left(\frac{b}{2R}\right)^2 + \left(\frac{c}{2R}\right)^2$
>
> 따라서 $a^2 = b^2 + c^2$
>
> 피타고라스 정리에 의해 삼각형 $ABC$는 직각삼각형이고:
> $\angle A = \frac{\pi}{2} \text{ (직각)}$
>
> 또는 삼각형에서:
> $\sin A = \frac{a}{2R}, \quad \sin B = \frac{b}{2R}, \quad \sin C = \frac{c}{2R}$
>
> 따라서 $\angle A = 90°$

---

### 예제 61

$\sin20° \sin40° \sin80°$의 값을 구하여라.

> [!summary]- 풀이
> 먼저 곱을 합차로 변환:
> $\sin40° \sin20° = -\frac{1}{2}\{\cos60° - \cos20°\}$
> $= -\frac{1}{2}\left\{\frac{1}{2} - \cos20°\right\}$
> $= -\frac{1}{4} + \frac{1}{2}\cos20°$
>
> 따라서:
> $\sin20° \sin40° \sin80° = \left(-\frac{1}{4} + \frac{1}{2}\cos20°\right)\sin80°$
> $= -\frac{1}{4}\sin80° + \frac{1}{2}\cos20°\sin80°$
>
> $\sin\alpha\cos\beta = \frac{1}{2}\{\sin(\alpha+\beta) + \sin(\alpha-\beta)\}$를 사용:
> $= -\frac{1}{4}\sin80° + \frac{1}{2} \cdot \frac{1}{2}\{\sin100° + \sin60°\}$
> $= -\frac{1}{4}\sin80° + \frac{1}{4}\sin100° + \frac{\sqrt{3}}{8}$
>
> $\sin100° = \sin(180° - 80°) = \sin80°$이므로:
> $= -\frac{1}{4}\sin80° + \frac{1}{4}\sin80° + \frac{\sqrt{3}}{8}$
> $= \frac{\sqrt{3}}{8}$

---

### 예제 62

$\alpha = \frac{\pi}{18}$일 때 $\frac{\sin\alpha + \sin3\alpha + \sin5\alpha}{\cos\alpha + \cos3\alpha + \cos5\alpha}$의 값을 구하여라.

(힌트: 분모, 분자에 $\sin\alpha$를 곱하여라.)

> [!summary]- 풀이
> **분자:** $\sin\alpha + \sin3\alpha + \sin5\alpha$를 계산
>
> 곱을 합차로 변환하면:
> $X \cdot \sin\alpha = \sin^2\alpha + \sin\alpha\sin3\alpha + \sin\alpha\sin5\alpha$
> $= -\frac{1}{2}\{(\cos2\alpha - \cos0) + (\cos4\alpha - \cos2\alpha) + (\cos6\alpha - \cos4\alpha)\}$
> $= -\frac{1}{2}\{-1 + \cos6\alpha\} = -\frac{1}{2}\left\{-1 + \cos\frac{\pi}{3}\right\} = \frac{1}{4}$
>
> **분모:** $\cos\alpha + \cos3\alpha + \cos5\alpha$를 계산
>
> 마찬가지로:
> $Y \cdot \sin\alpha = \sin\alpha\cos\alpha + \sin\alpha\cos3\alpha + \sin\alpha\cos5\alpha$
> $= \frac{1}{2}\{(\sin2\alpha - \sin0) + (\sin4\alpha - \sin2\alpha) + (\sin6\alpha - \sin4\alpha)\}$
> $= \frac{1}{2}\sin6\alpha = \frac{1}{2} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{3}}{4}$
>
> 따라서:
> $\frac{\sin\alpha + \sin3\alpha + \sin5\alpha}{\cos\alpha + \cos3\alpha + \cos5\alpha} = \frac{X}{Y} = \frac{1/\sqrt{3}}{1} = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$

---

### 예제 63

$\sin x + \sin y = \frac{2}{3}$, $\cos x \cos y = \frac{1}{2}$일 때 $\sin\frac{x+y}{2}$의 값을 구하여라.

> [!summary]- 풀이
> 합차 공식을 사용:
> $\sin x + \sin y = 2\sin\frac{x+y}{2}\cos\frac{x-y}{2} = \frac{2}{3}$
>
> 따라서:
> $\sin\frac{x+y}{2}\cos\frac{x-y}{2} = \frac{1}{3} \quad \cdots \text{(ㄱ)}$
>
> 곱을 합차로 변환:
> $\cos x \cos y = \frac{1}{2}\{\cos(x+y) + \cos(x-y)\} = \frac{1}{2}$
>
> 따라서:
> $\cos(x+y) + \cos(x-y) = 1$
>
> 합차를 곱으로 변환:
> $2\cos\frac{x+y}{2}\cos\frac{x-y}{2} = 1$
> $\cos\frac{x+y}{2}\cos\frac{x-y}{2} = \frac{1}{2} \quad \cdots \text{(ㄴ)}$
>
> (ㄱ)과 (ㄴ)에서:
> $X \cdot Y = \frac{1}{3}, \quad \text{여기서 } X = \sin\frac{x+y}{2}, Y = \cos\frac{x-y}{2}$
>
> 이를 정리하면:
> $2X^2 - \frac{2}{9X^2} + 1 = 0$
> $18X^4 + 9X^2 - 2 = 0$
>
> $X^2 = \frac{1}{6}$ 또는 $X^2 = \frac{-1}{3}$ (음수 제외)
>
> 따라서:
> $\sin\frac{x+y}{2} = \pm\frac{1}{\sqrt{6}}$

---

### 예제 64

$\theta = \frac{\pi}{10}$일 때 $\sin\theta\sin\theta + \sin3\theta\sin\theta + \sin5\theta\sin\theta + \cdots + \sin9\theta\sin\theta$를 구하여라.

> [!summary]- 풀이
> $\theta = \frac{\pi}{10}$이고, 구하려는 식을 $S$라 하면:
> $S = \sin\theta\sin\theta + \sin3\theta\sin\theta + \sin5\theta\sin\theta + \sin7\theta\sin\theta + \sin9\theta\sin\theta$
>
> 각 항을 곱을 합차로 변환:
> $\sin n\theta \sin\theta = -\frac{1}{2}\{\cos((n+1)\theta) - \cos((n-1)\theta)\}$
>
> 따라서:
> $S = -\frac{1}{2}\{(\cos2\theta - \cos0) + (\cos4\theta - \cos2\theta) + (\cos6\theta - \cos4\theta)$
> $+ (\cos8\theta - \cos6\theta) + (\cos10\theta - \cos8\theta)\}$
>
> 이는 망원급수(telescoping series)가 되어:
> $S = -\frac{1}{2}\{\cos10\theta - \cos0\}$
> $= -\frac{1}{2}\{\cos\pi - 1\}$
> $= -\frac{1}{2}\{-1 - 1\}$
> $= -\frac{1}{2} \times (-2)$
> $= 1$
>
> **Note**: 여기서 각 항들이 연쇄적으로 소거되어 처음과 마지막 항만 남는 망원급수의 특성을 활용했습니다.

---

## 3. 공식 정리

### 합차를 곱으로 (Thm 16)

| 공식              | 형태                                   |
| ----------------- | -------------------------------------- |
| $\sin A + \sin B$ | $2\sin\frac{A+B}{2}\cos\frac{A-B}{2}$  |
| $\sin A - \sin B$ | $2\cos\frac{A+B}{2}\sin\frac{A-B}{2}$  |
| $\cos A + \cos B$ | $2\cos\frac{A+B}{2}\cos\frac{A-B}{2}$  |
| $\cos A - \cos B$ | $-2\sin\frac{A+B}{2}\sin\frac{A-B}{2}$ |

### 곱을 합차로

| 공식                  | 형태                                                    |
| --------------------- | ------------------------------------------------------- |
| $\sin\alpha\cos\beta$ | $\frac{1}{2}\{\sin(\alpha+\beta)+\sin(\alpha-\beta)\}$  |
| $\cos\alpha\sin\beta$ | $\frac{1}{2}\{\sin(\alpha+\beta)-\sin(\alpha-\beta)\}$  |
| $\cos\alpha\cos\beta$ | $\frac{1}{2}\{\cos(\alpha+\beta)+\cos(\alpha-\beta)\}$  |
| $\sin\alpha\sin\beta$ | $-\frac{1}{2}\{\cos(\alpha+\beta)-\cos(\alpha-\beta)\}$ |

---

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 합차공식과 곱셈공식의 상호변환을 숙지하시오.)

1. 합차를 곱으로 변환하는 공식 4개를 유도할 수 있는가?
2. 곱을 합차로 변환하는 공식 4개를 유도할 수 있는가?
3. 두 공식의 관계를 이해하고 상황에 맞게 적용할 수 있는가?

---

## 관련 주제

- [[08-advanced-trigonometry-1|심화삼각함수(1) - 덧셈정리]]
- [[09-advanced-trigonometry-2|심화삼각함수(2) - 덧셈정리 응용, 배각공식]]
- [[10-advanced-trigonometry-3|심화삼각함수(3) - 배각공식 문제풀이]]
- [[12-advanced-trigonometry-5|심화삼각함수(5) - 삼각함수의 합성]]

---

**학습 포인트:**

1. **합차를 곱으로**: $A = \alpha + \beta$, $B = \alpha - \beta$ 치환을 통해 유도
2. **곱을 합차로**: 덧셈정리의 역활용으로 복잡한 곱셈을 간단한 합차로 변환
3. **응용**: 삼각함수의 곱이나 합을 포함한 복잡한 식을 단순화하는 강력한 도구
4. **패턴 인식**: 언제 어떤 공식을 사용할지 판단하는 능력 배양
