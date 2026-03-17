---
id: c9e2d471-5f8a-4b31-a6e0-8d47f3b20c5e
aliases:
  - 부분적분
  - 부분적분법
  - 부분적분 유형
  - 그적미적
tags:
  - 부분적분
  - 적분법
  - 지수함수의적분
  - 삼각함수의적분
  - 로그함수의적분
  - 중급
pages: 136-138
subject: 대학기초수학
title: 부분적분
topics:
  - 부분적분법 (Thm 46)
  - 유형1 다항함수×지수함수
  - 유형2 다항함수×삼각함수
  - 유형3 다항함수×로그함수
  - 유형4 지수함수×삼각함수
  - 부분적분 응용 예제
---

# 45강: 부분적분

## 1. 부분적분법

### Thm (46): 부분적분

$$
\int f'(x)g(x)\,dx = f(x)g(x) - \int f(x)g'(x)\,dx
$$

> [!note] 공식 유도
> 곱의 미분법 $(f(x) \cdot g(x))' = f'(x)g(x) + f(x)g'(x)$ 에서:
>
> $$f'(x)g(x) = (f(x)g(x))' - f(x)g'(x)$$
>
> 양변을 적분하면 Thm (46)이 유도된다.

> [!tip] 암기법: **그·적 − 미·적**
> - **그·적**: 그대로 × 적분
> - **미·적**: 미분 × 적분
>
> $$\underbrace{f'(x)}_{\text{적분}} \cdot \underbrace{g(x)}_{\text{그대로}} \longrightarrow \underbrace{f(x)}_{\text{적·그}} \cdot g(x) - \int \underbrace{f(x)}_{\text{적·미}} \cdot g'(x)\,dx$$

---

## 2. 적분 우선순위와 유형 분류

> [!tip] 부분적분 적분 우선순위
> **지수함수 > 삼각함수 > 다항함수 > 로그함수**
>
> 우선순위가 **낮은** 함수를 $g(x)$ (그대로 쪽)로, **높은** 함수를 $f'(x)$ (적분 쪽)로 설정한다.
>
> 예) $\int x \ln x\,dx$ → $x$를 적분(다항), $\ln x$를 그대로(로그) → $f'(x) = x$, $g(x) = \ln x$

---

## 3. 유형별 예제

### 유형 1: 다항함수 × 지수함수

다항함수를 $g(x)$ (그대로), 지수함수를 $f'(x)$ (적분)로 설정

#### ① $\int xe^{2x}\,dx$

$$
= x \cdot \frac{1}{2}e^{2x} - \int 1 \cdot \frac{1}{2}e^{2x}\,dx
= \frac{1}{2}xe^{2x} - \frac{1}{4}e^{2x} + C
$$

---

#### ② $\int x^2 e^{3x}\,dx$

$x^2$이 2차이므로 부분적분을 2회 적용:

$$
= x^2 \cdot \frac{1}{3}e^{3x} - \int 2x \cdot \frac{1}{3}e^{3x}\,dx
$$

$$
= \frac{1}{3}x^2e^{3x} - \left\{2x \cdot \frac{1}{9}e^{3x} - \int 2 \cdot \frac{1}{9}e^{3x}\,dx\right\}
$$

$$
= \frac{1}{3}x^2e^{3x} - \frac{2}{9}xe^{3x} + \frac{2}{27}e^{3x} + C
$$

---

### 유형 2: 다항함수 × 삼각함수

다항함수를 $g(x)$ (그대로), 삼각함수를 $f'(x)$ (적분)로 설정

#### ① $\int x\sin 3x\,dx$

$$
= x \cdot \left(-\frac{1}{3}\cos 3x\right) - \int 1 \cdot \left(-\frac{1}{3}\cos 3x\right)dx
$$

$$
= -\frac{1}{3}x\cos 3x + \frac{1}{9}\sin 3x + C
$$

---

#### ② $\int x^3 \cos x\,dx$

> [!tip] 고차 다항 × 삼각/지수 — **그·적−미·적+미적−미·적+⋯ 반복법**
> 다항함수의 차수만큼 부분적분을 반복하므로, 부호를 교대하며 한 번에 전개한다.

$$
= x^3\sin x - 3x^2(-\cos x) + 6x(-\sin x) - 6\cos x + C
$$

$$
= x^3\sin x + 3x^2\cos x - 6x\sin x - 6\cos x + C
$$

---

### 유형 3: 다항함수 × 로그함수 (원래 공식대로!)

로그함수를 $g(x)$ (그대로), 다항함수를 $f'(x)$ (적분)로 설정

#### ① $\int \ln x\,dx$

$$
= x\ln x - \int x \cdot \frac{1}{x}\,dx = x\ln x - x + C
$$

---

#### ② $\int x\ln x\,dx$

$$
= \frac{1}{2}x^2\ln x - \int \frac{1}{2}x^2 \cdot \frac{1}{x}\,dx = \frac{1}{2}x^2\ln x - \frac{1}{4}x^2 + C
$$

---

#### ③ $\int (\ln x)^2\,dx$

$$
= x(\ln x)^2 - \int x \cdot 2\ln x \cdot \frac{1}{x}\,dx = x(\ln x)^2 - 2\int \ln x\,dx
$$

$$
= x(\ln x)^2 - 2(x\ln x - x) + C = x(\ln x)^2 - 2x\ln x + 2x + C
$$

---

### 유형 4: 지수함수 × 삼각함수 (원래 모양이 나올 때까지 반복!)

> [!warning] 부분적분을 2회 적용하면 원래 적분이 다시 등장 → 방정식으로 풀기

#### $\int e^x \cos x\,dx$

1회 부분적분:

$$
= e^x\cos x - \int e^x(-\sin x)\,dx = e^x\cos x + \int e^x\sin x\,dx
$$

2회 부분적분 (오른쪽 항에 다시 적용):

$$
= e^x\cos x + \left\{e^x\sin x - \int e^x\cos x\,dx\right\}
$$

$$
\int e^x\cos x\,dx = e^x\cos x + e^x\sin x - \int e^x\cos x\,dx
$$

양변에 $\int e^x\cos x\,dx$를 이항:

$$
2\int e^x\cos x\,dx = e^x\cos x + e^x\sin x
$$

$$
\int e^x\cos x\,dx = \frac{1}{2}e^x(\cos x + \sin x) + C
$$

---

## 4. 예제

### 예제 294

곡선 $y = f(x)$ 위의 점 $(x, y)$에서의 접선의 기울기가 $x\ln x$이고 $f(1) = \dfrac{3}{4}$일 때, $f(4)$를 구하여라.

> [!summary]- 풀이
> 접선의 기울기 $= f'(x) = x\ln x$ 이므로 부분적분 (유형 3) 적용:
>
> $$f(x) = \int x\ln x\,dx = \frac{1}{2}x^2\ln x - \int \frac{1}{2}x^2 \cdot \frac{1}{x}\,dx = \frac{1}{2}x^2\ln x - \frac{1}{4}x^2 + C$$
>
> 초기조건 $f(1) = \dfrac{3}{4}$ 대입:
>
> $$f(1) = \frac{1}{2}(1)\ln 1 - \frac{1}{4}(1) + C = 0 - \frac{1}{4} + C = \frac{3}{4}$$
>
> $$C = 1$$
>
> $$f(x) = \frac{1}{2}x^2\ln x - \frac{1}{4}x^2 + 1$$
>
> $x = 4$ 대입:
>
> $$f(4) = \frac{1}{2}(16)\ln 4 - \frac{1}{4}(16) + 1 = 8\ln 4 - 4 + 1$$
>
> $$= 8\ln 4 - 3 = 8 \cdot 2\ln 2 - 3 = \boxed{16\ln 2 - 3}$$

---

### 예제 295

$f'(x) = \cos x \ln(\sin x)$이고 $f\!\left(\dfrac{\pi}{2}\right) = 0$일 때, $f\!\left(\dfrac{\pi}{6}\right)$을 구하여라.

> [!summary]- 풀이
> **치환적분 먼저**: $\sin x = t$ 로 치환 $\Rightarrow \cos x\,dx = dt$
>
> $$f(x) = \int \cos x\ln(\sin x)\,dx = \int \ln t\,dt$$
>
> **부분적분 (유형 3)** 적용:
>
> $$= t\ln t - t + C = \sin x\ln(\sin x) - \sin x + C$$
>
> 초기조건 $f\!\left(\dfrac{\pi}{2}\right) = 0$ 대입:
>
> $$f\!\left(\frac{\pi}{2}\right) = \sin\frac{\pi}{2}\ln\!\left(\sin\frac{\pi}{2}\right) - \sin\frac{\pi}{2} + C = 1 \cdot \ln 1 - 1 + C = -1 + C = 0$$
>
> $$C = 1$$
>
> $$f(x) = \sin x\ln(\sin x) - \sin x + 1$$
>
> $x = \dfrac{\pi}{6}$ 대입 ($\sin\dfrac{\pi}{6} = \dfrac{1}{2}$):
>
> $$f\!\left(\frac{\pi}{6}\right) = \frac{1}{2}\ln\frac{1}{2} - \frac{1}{2} + 1 = -\frac{1}{2}\ln 2 + \frac{1}{2}$$
>
> $$= \frac{1}{2}(1 - \ln 2) = \frac{1}{2}(\ln e - \ln 2) = \boxed{\frac{1}{2}\ln\frac{e}{2}}$$

---

### 예제 296

$f'(x) = e^x\sin x$이고 $f(0) = \dfrac{1}{2}$일 때, $f(\pi)$를 구하여라.

> [!summary]- 풀이
> **유형 4** (지수 × 삼각) 적용. $I = \int e^x\sin x\,dx$ 로 놓으면:
>
> 1회 부분적분:
>
> $$I = e^x\sin x - \int e^x\cos x\,dx$$
>
> 2회 부분적분:
>
> $$= e^x\sin x - \left\{e^x\cos x - \int e^x(-\sin x)\,dx\right\}$$
>
> $$= e^x\sin x - e^x\cos x - \int e^x\sin x\,dx$$
>
> $$I = e^x\sin x - e^x\cos x - I$$
>
> $$2I = e^x(\sin x - \cos x)$$
>
> $$f(x) = I + C = \frac{1}{2}e^x(\sin x - \cos x) + C$$
>
> 초기조건 $f(0) = \dfrac{1}{2}$ 대입:
>
> $$f(0) = \frac{1}{2}e^0(\sin 0 - \cos 0) + C = \frac{1}{2}(0-1) + C = -\frac{1}{2} + C = \frac{1}{2}$$
>
> $$C = 1$$
>
> $$f(x) = \frac{1}{2}e^x(\sin x - \cos x) + 1$$
>
> $x = \pi$ 대입 ($\sin\pi = 0$, $\cos\pi = -1$):
>
> $$f(\pi) = \frac{1}{2}e^\pi(0-(-1)) + 1 = \boxed{\frac{1}{2}e^\pi + 1}$$

---

### 예제 297

$f(x) = \displaystyle\int (x-2)e^x\,dx$이고 $f(0) = 3$일 때, $f(x)$를 구하여라.

> [!summary]- 풀이
> **유형 1** (다항 × 지수) 부분적분 1회 적용:
>
> $$\int (x-2)e^x\,dx = (x-2)e^x - \int 1 \cdot e^x\,dx = (x-2)e^x - e^x + C$$
>
> $$= e^x(x-2-1) + C = e^x(x-3) + C$$
>
> 초기조건 $f(0) = 3$ 대입:
>
> $$f(0) = e^0(0-3) + C = -3 + C = 3 \implies C = 6$$
>
> $$\boxed{f(x) = e^x(x-3) + 6}$$

---

### 예제 298

$f(x) = \displaystyle\int x^2\cos 2x\,dx$이고 $f(\pi) = \dfrac{\pi}{2}$일 때, $f(x)$를 구하여라.

> [!summary]- 풀이
> **유형 2** (다항 × 삼각) $x^2$이 2차이므로 **반복법** 적용:
>
> $$f(x) = x^2 \cdot \frac{1}{2}\sin 2x - 2x \cdot \left(-\frac{1}{4}\cos 2x\right) + 2 \cdot \left(-\frac{1}{8}\sin 2x\right) + C$$
>
> $$= \frac{1}{2}x^2\sin 2x + \frac{1}{2}x\cos 2x - \frac{1}{4}\sin 2x + C$$
>
> 초기조건 $f(\pi) = \dfrac{\pi}{2}$ 대입 ($\sin 2\pi = 0$, $\cos 2\pi = 1$):
>
> $$f(\pi) = \frac{1}{2}\pi^2 \cdot 0 + \frac{1}{2}\pi \cdot 1 - \frac{1}{4} \cdot 0 + C = \frac{\pi}{2} + C = \frac{\pi}{2}$$
>
> $$C = 0$$
>
> $$\boxed{f(x) = \frac{1}{2}x^2\sin 2x + \frac{1}{2}x\cos 2x - \frac{1}{4}\sin 2x}$$

---

### 예제 299

함수 $f(x) = e^{2x-1}$일 때, $\displaystyle\int f^{-1}(x)\,dx$를 구하여라.

> [!summary]- 풀이
> **Step 1**: 역함수 $f^{-1}(x)$ 구하기
>
> $y = e^{2x-1}$에서 $x$와 $y$를 교환:
>
> $$x = e^{2y-1} \implies \ln x = 2y-1 \implies y = \frac{1}{2}\ln x + \frac{1}{2}$$
>
> $$f^{-1}(x) = \frac{1}{2}\ln x + \frac{1}{2}$$
>
> **Step 2**: 부분적분 (유형 3) 적용:
>
> $$\int f^{-1}(x)\,dx = \int \left(\frac{1}{2}\ln x + \frac{1}{2}\right)dx = \frac{1}{2}\int (\ln x + 1)\,dx$$
>
> $$= \frac{1}{2}\left(\int \ln x\,dx + \int 1\,dx\right) = \frac{1}{2}(x\ln x - x + x) + C$$
>
> $$= \boxed{\frac{1}{2}x\ln x + C}$$

---

## 관련 주제

- [[44-integration-substitution-1|44강: 초월함수의 부정적분(2), 치환적분(1)]]
- [[46-definite-integral-intro|46강: 정적분의 정의와 무한급수]]

---

**학습 포인트:**
1. **부분적분 공식**: $\int f'(x)g(x)\,dx = f(x)g(x) - \int f(x)g'(x)\,dx$ (그·적 − 미·적)
2. **적분 우선순위**: 지수 > 삼각 > 다항 > 로그 → 우선순위 낮은 쪽을 $g(x)$ (그대로)로
3. **유형 1·2 고차**: 다항함수 차수만큼 반복 — 부호 교대하며 한 번에 전개
4. **유형 3 로그**: $\ln x$는 반드시 그대로 쪽, 다항 부분을 적분
5. **유형 4 지수×삼각**: 2회 반복 후 원래 적분이 등장 → 방정식으로 이항하여 풀기
6. **치환 후 부분적분**: 치환으로 $\int \ln t\,dt$ 꼴로 변환 후 부분적분 적용 (예제 295)
