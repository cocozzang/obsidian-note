---
id: b2f4e891-3c7a-4d58-a1e0-7f62c9d04b3e
aliases:
  - 부정적분
  - 초월함수의 부정적분(1)
  - 부정적분의 계산
  - 초월함수 적분공식
tags:
  - 부정적분
  - 초월함수의적분
  - 삼각함수의적분
  - 지수함수의적분
  - 적분법
  - 중급
pages: 129-131
subject: 대학기초수학
title: 부정적분, 초월함수의 부정적분(1)
topics:
  - 부정적분의 계산 공식
  - 초월함수의 적분공식
  - 기타 중요한 적분
  - 부정적분 응용 예제
---

# 43강: 부정적분, 초월함수의 부정적분(1)

## 1. 부정적분의 계산

### Thm (43): 부정적분의 계산

$$
(1)\ \int k\,dx = kx + C \quad (k\text{는 상수})
$$

$$
(2)\ \int x^n\,dx = \frac{1}{n+1}x^{n+1} + C \quad (n\text{은 양의 정수})
$$

$$
(3)\ \int \{f(x) \pm g(x)\}\,dx = \int f(x)\,dx \pm \int g(x)\,dx \quad (\text{복호동순})
$$

$$
(4)\ \int (ax+b)^n\,dx = \frac{1}{a} \cdot \frac{1}{n+1}(ax+b)^{n+1} + C \quad (a \neq 0\text{이고}\ n\text{이 양의 정수})
$$

---

### Thm (43)-(4) 증명

#### 증명 1) 직접 전개

$$
\int (ax+b)^n\,dx
= \int a^n\left(x + \frac{b}{a}\right)^n dx
= \frac{1}{a} \cdot a^{n+1} \int \left(x + \frac{b}{a}\right)^n dx
$$

$$
= \frac{1}{a} \cdot \frac{1}{n+1} \cdot a^{n+1}\left(x + \frac{b}{a}\right)^{n+1} + C
= \frac{1}{a} \cdot \frac{1}{n+1}(ax+b)^{n+1} + C
$$

#### 증명 2) 치환적분법

$ax + b = t$ 로 놓으면

$$
a = \frac{dt}{dx} \implies dx = \frac{1}{a}\,dt
$$

$$
\int (ax+b)^n\,dx
= \int t^n \cdot \frac{1}{a}\,dt
= \frac{1}{a} \int t^n\,dt
= \frac{1}{a} \cdot \frac{1}{n+1}t^{n+1} + C
= \frac{1}{a} \cdot \frac{1}{n+1}(ax+b)^{n+1} + C
$$

---

## 2. 예제 (Thm 43 적용)

### 예제 276

함수 $f(x)$와 그의 부정적분 $F(x)$ 사이에
$F(x) = xf(x) + x^3 - 4x^2$을 만족할 때, $f(4) - f(2)$의 값을 구하여라.

> [!summary]- 풀이
> $F'(x) = f(x)$ 이므로 양변을 $x$에 대해 미분하면:
>
> $$F'(x) = f(x) + xf'(x) + 3x^2 - 8x$$
>
> $F'(x) = f(x)$ 를 대입하면:
>
> $$f(x) = f(x) + xf'(x) + 3x^2 - 8x$$
>
> $$xf'(x) + 3x^2 - 8x = 0$$
>
> $$f'(x) = -3x + 8$$
>
> 적분하면:
>
> $$f(x) = -\frac{3}{2}x^2 + 8x + C$$
>
> 따라서:
>
> $$f(4) - f(2) = \left(-24 + 32 + C\right) - \left(-6 + 16 + C\right)$$
>
> $$= 8 - 10 = \boxed{-2}$$

---

### 예제 277

$f(x) = \int (x^3 - 2x^2 + x + 1)\,dx$ 일 때, $\displaystyle\lim_{h \to 0} \frac{f(2+h) - f(2-h)}{h}$ 의 값을 구하여라.

> [!summary]- 풀이
> 극한식을 변형한다:
>
> $$\lim_{h \to 0} \frac{f(2+h) - f(2-h)}{h}
> = \lim_{h \to 0} \frac{f(2+h) - f(2-h)}{2h} \cdot 2 = 2f'(2)$$
>
> $f'(x) = x^3 - 2x^2 + x + 1$ 이므로:
>
> $$2f'(2) = 2(8 - 8 + 2 + 1) = \boxed{6}$$

---

### 예제 278

임의의 실수 $x, y$에 대하여 $f(x+y) = f(x) + f(y) + xy + 1$를 만족시키는 함수 $f(x)$가 있다.
$f'(0) = 4$일 때 $f(8)$의 값을 구하여라. (단, $f(x)$는 미분가능)

> [!summary]- 풀이
> $f(x+y) = f(x) + f(y) + xy + 1$ 양변을 $y$에 대해 미분하면:
>
> $$f'(x+y) = f'(y) + x$$
>
> $y = 0$ 대입:
>
> $$f'(x) = f'(0) + x = x + 4$$
>
> 적분하면:
>
> $$f(x) = \int (x+4)\,dx = \frac{1}{2}x^2 + 4x + C$$
>
> 초기값 결정: 원래 조건에 $x = y = 0$ 대입:
>
> $$f(0) = f(0) + f(0) + 1 \implies f(0) = -1$$
>
> $$\therefore C = -1$$
>
> $$f(x) = \frac{1}{2}x^2 + 4x - 1$$
>
> $$f(8) = 32 + 32 - 1 = \boxed{63}$$

---

### 예제 279

삼차함수 $y = f(x)$는 $x = 1$에서 극값을 갖고, 그 그래프가 원점에 대하여 대칭일 때,
이 그래프와 $x$축과의 교점의 $x$좌표 중에서 양수인 값을 구하여라.

> [!summary]- 풀이
> 조건 정리:
> - $x=1$에서 극값 → $f'(1) = 0$
> - 원점 대칭 → 기함수: $f(-x) = -f(x)$ → $f'(x)$는 우함수: $f'(-x) = f'(x)$
> - $f(0) = 0$
>
> $f'(x)$는 우함수이고 $f'(1) = 0$이므로 $f'(-1) = 0$, 따라서:
>
> $$f'(x) = a(x+1)(x-1) = a(x^2 - 1)$$
>
> 적분하면:
>
> $$f(x) = \frac{a}{3}x^3 - ax + C$$
>
> $f(0) = 0$ → $C = 0$
>
> $$f(x) = \frac{a}{3}x^3 - ax$$
>
> $x$축과의 교점: $f(x) = 0$
>
> $$\frac{a}{3}x^3 - ax = 0 \implies x(x^2 - 3) = 0$$
>
> $$x = 0,\ x = \pm\sqrt{3}$$
>
> 이 중 양수인 값은 $\boxed{\sqrt{3}}$

---

### 예제 280

삼차함수 $y = f(x)$의 도함수 $y = f'(x)$의 그래프는 오른쪽과 같다.
$f(0) = 0$일 때, $x$에 대한 방정식 $f(x) = kx$가 서로 다른 세 실근을 갖기 위한 실수 $k$의 값의 범위를 구하여라.

![[./images/03-calculus/exer280.png|300]]

> [!summary]- 풀이
> 그래프에서 $f'(x)$는 $x = \pm 2$에서 영점, $x = 0$에서 최댓값 3을 가짐:
>
> $$f'(x) = -\frac{3}{4}(x+2)(x-2) = -\frac{3}{4}(x^2 - 4) = -\frac{3}{4}x^2 + 3$$
>
> 적분하면:
>
> $$f(x) = -\frac{1}{4}x^3 + 3x + C$$
>
> $f(0) = 0$ → $C = 0$
>
> $$f(x) = -\frac{1}{4}x^3 + 3x$$
>
> 방정식 $f(x) = kx$를 변형:
>
> $$-\frac{1}{4}x^3 + 3x = kx$$
>
> $$x^3 - 12x + 4kx = 0$$
>
> $$x(x^2 - 12 + 4k) = 0$$
>
> $x = 0$은 이미 실근. $x^2 + (4k-12) = 0$이 $x \neq 0$인 서로 다른 두 실근을 가져야 함:
>
> **조건 1**: 판별식 $> 0$
>
> $$\frac{D}{4} = 12 - 4k > 0 \implies k < 3$$
>
> **조건 2**: $x = 0$이 이중근이 아닌 조건
>
> $$4k - 12 \neq 0 \implies k \neq 3$$
>
> (조건 1에 이미 포함됨)
>
> $$\therefore \boxed{k < 3}$$

---

## 3. 초월함수의 부정적분

### Thm (44): 초월함수의 적분공식

$$
(1)\ \int \sin x\,dx = -\cos x + C \qquad (2)\ \int \cos x\,dx = \sin x + C
$$

$$
(3)\ \int \tan x\,dx = -\ln|\cos x| + C \qquad (4)\ \int \sec^2 x\,dx = \tan x + C
$$

$$
(5)\ \int e^x\,dx = e^x + C \qquad (6)\ \int a^x\,dx = \frac{1}{\ln a}\,a^x + C
$$

> [!note] 반각공식 (적분 활용)
> $$\sin^2 kx = \frac{1 - \cos 2kx}{2}, \qquad \cos^2 kx = \frac{1 + \cos 2kx}{2}$$

---

### 핵심 보조공식

$$
\{\ln|f(x)|\}' = \frac{f'(x)}{f(x)} \implies \int \frac{f'(x)}{f(x)}\,dx = \ln|f(x)| + C
$$

---

### Thm (44)-(3) 유도: $\int \tan x\,dx$

$$
\int \tan x\,dx = \int \frac{\sin x}{\cos x}\,dx = -\int \frac{-\sin x}{\cos x}\,dx
$$

$(\cos x)' = -\sin x$ 이므로 보조공식을 적용하면:

$$
= -\ln|\cos x| + C
$$

---

## 4. 기타 중요한 적분

> [!tip] $\sin^2$, $\cos^2$ 적분 원칙
> $\sin^2 x$와 $\cos^2 x$를 직접 적분하는 원함수는 없으므로, **반각공식으로 식을 변형**한 후 Thm (44)-(2)를 적용한다.

### ① $\int \tan^2 x\,dx$

$$
\int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx = \tan x - x + C
$$

---

### ② $\int \sec x\,dx$

분자분모에 $(\sec x + \tan x)$를 곱한다:

$$
\int \sec x\,dx = \int \frac{\sec x(\sec x + \tan x)}{\sec x + \tan x}\,dx
$$

$(\sec x + \tan x)' = \sec x \tan x + \sec^2 x = \sec x(\sec x + \tan x)$ 이므로:

$$
\int \sec x\,dx = \ln|\sec x + \tan x| + C
$$

---

### ③ $\int \cot x\,dx$

$$
\int \cot x\,dx = \int \frac{\cos x}{\sin x}\,dx = \ln|\sin x| + C
$$

---

### ④ $\int \csc^2 x\,dx$

$(\cot x)' = -\csc^2 x$ 이므로:

$$
\int \csc^2 x\,dx = -\cot x + C
$$

---

### ⑤ $\int \cot^2 x\,dx$

삼각항등식 $1 + \cot^2 x = \csc^2 x$ → $\cot^2 x = \csc^2 x - 1$ 을 이용:

$$
\int \cot^2 x\,dx = \int (\csc^2 x - 1)\,dx = -\cot x - x + C
$$

---

### ⑥ $\int \csc x\,dx$

분자분모에 $(\csc x + \cot x)$를 곱한다:

$$
\int \csc x\,dx = \int \frac{\csc x(\csc x + \cot x)}{\csc x + \cot x}\,dx = -\int \frac{-\csc x(\csc x + \cot x)}{\csc x + \cot x}\,dx
$$

$(\csc x + \cot x)' = -\csc x \cot x - \csc^2 x = -\csc x(\csc x + \cot x)$ 이므로:

$$
\int \csc x\,dx = -\ln|\csc x + \cot x| + C
$$

---

### ⑦ $\int \sin^2 x\,dx$

반각공식 $\sin^2 x = \frac{1 - \cos 2x}{2}$ 를 적용:

$$
\int \sin^2 x\,dx = \int \frac{1 - \cos 2x}{2}\,dx = \frac{1}{2}x - \frac{1}{4}\sin 2x + C
$$

---

### ⑧ $\int \cos^2 x\,dx$

반각공식 $\cos^2 x = \frac{1 + \cos 2x}{2}$ 를 적용:

$$
\int \cos^2 x\,dx = \int \frac{1 + \cos 2x}{2}\,dx = \frac{1}{2}x + \frac{1}{4}\sin 2x + C
$$

---

### ⑨ $\int \sin^3 x\,dx$

#### 방법 1) 3배각공식 활용

3배각공식 $\sin 3x = 3\sin x - 4\sin^3 x$ 를 변형:

$$
\sin^3 x = \frac{3}{4}\sin x - \frac{1}{4}\sin 3x
$$

$$
\int \sin^3 x\,dx = \int \left(\frac{3}{4}\sin x - \frac{1}{4}\sin 3x\right)dx
= -\frac{3}{4}\cos x + \frac{1}{12}\cos 3x + C
$$

#### 방법 2) 치환적분법 활용

$$
\int \sin^3 x\,dx = \int \sin x \cdot \sin^2 x\,dx = \int \sin x(1 - \cos^2 x)\,dx
$$

$\cos x = t$ 로 치환하면 $-\sin x\,dx = dt$, 즉 $\sin x\,dx = -dt$:

$$
= \int (1 - t^2)(-dt) = \int (t^2 - 1)\,dt = \frac{1}{3}t^3 - t + C
$$

$$
= \frac{1}{3}\cos^3 x - \cos x + C
$$

---

## 5. 예제 (Thm 44 적용)

### 예제 281

다음 부정적분을 구하여라.

**(1)** $\displaystyle\int \sin^2 \frac{x}{2}\,dx$

**(2)** $\displaystyle\int \cos 3x \sin x\,dx$

**(3)** $\displaystyle\int \tan 2x\,dx$

> [!summary]- 풀이 (1)
> 반각공식 $\sin^2 \frac{x}{2} = \frac{1 - \cos x}{2}$ 를 적용:
>
> $\int \sin^2 \frac{x}{2}\,dx = \int \frac{1-\cos x}{2}\,dx = \frac{1}{2}x - \frac{1}{2}\sin x + C$

> [!summary]- 풀이 (2)
> 적화공식 $\cos\alpha \sin\beta = \frac{1}{2}(\sin(\alpha+\beta) - \sin(\alpha-\beta))$ 를 적용:
>
> $\cos 3x \sin x = \frac{1}{2}(\sin 4x - \sin 2x)$
>
> $\int \cos 3x \sin x\,dx = \int \frac{1}{2}(\sin 4x - \sin 2x)\,dx$
>
> $= \frac{1}{2}\left(-\frac{1}{4}\cos 4x + \frac{1}{2}\cos 2x\right) + C$
>
> $= -\frac{1}{8}\cos 4x + \frac{1}{4}\cos 2x + C$

> [!summary]- 풀이 (3)
> $\tan 2x = \frac{\sin 2x}{\cos 2x}$ 로 변형, 보조공식 $\int \frac{f'}{f}\,dx = \ln|f| + C$ 를 적용:
>
> $\int \tan 2x\,dx = \int \frac{\sin 2x}{\cos 2x}\,dx = -\frac{1}{2}\int \frac{-2\sin 2x}{\cos 2x}\,dx$
>
> $= -\frac{1}{2}\ln|\cos 2x| + C$

---

### 예제 282

점 $(0, 1)$을 지나는 곡선 $y = f(x)$ 위의 임의의 점 $(x, y)$에서의 접선의 기울기가 $2\cos x + e^x$일 때, $f(x)$를 구하여라.

> [!summary]- 풀이
> 접선의 기울기 = $f'(x)$ 이므로:
>
> $f(x) = \int (2\cos x + e^x)\,dx = 2\sin x + e^x + C$
>
> 초기조건 $f(0) = 1$ 대입:
>
> $f(0) = 2\sin 0 + e^0 + C = 0 + 1 + C = 1$
>
> $\therefore C = 0$
>
> $\boxed{f(x) = 2\sin x + e^x}$

---

### 예제 283

실수 전체의 집합에서 정의된 함수 $f(x)$에 대하여
$f'(x) = \dfrac{x}{x^2+1}$, $f(0) = 3$일 때 $f(\sqrt{e^2-1})$의 값을 구하여라.

> [!summary]- 풀이
> 보조공식 $\int \frac{f'}{f}\,dx = \ln|f| + C$ 를 적용:
>
> $f(x) = \int \frac{x}{x^2+1}\,dx = \frac{1}{2}\int \frac{2x}{x^2+1}\,dx = \frac{1}{2}\ln|x^2+1| + C$
>
> $x^2 + 1 > 0$ 이므로 절댓값 생략 가능:
>
> $f(x) = \frac{1}{2}\ln(x^2+1) + C$
>
> 초기조건 $f(0) = 3$ 대입:
>
> $f(0) = \frac{1}{2}\ln 1 + C = C = 3$
>
> $f(x) = \frac{1}{2}\ln(x^2+1) + 3$
>
> $x = \sqrt{e^2-1}$ 대입:
>
> $f(\sqrt{e^2-1}) = \frac{1}{2}\ln(e^2-1+1) + 3 = \frac{1}{2}\ln e^2 + 3 = 1 + 3 = \boxed{4}$

---

## 관련 주제

- [[42-partial-derivative|42강: 기본 편도함수]]
- [[44-integration-substitution-1|44강: 초월함수의 부정적분(2), 치환적분(1)]]

---

**학습 포인트:**
1. **Thm (43)-(4)**: $(ax+b)^n$ 꼴의 적분은 $\frac{1}{a} \cdot \frac{1}{n+1}(ax+b)^{n+1} + C$
2. **부정적분과 도함수의 관계**: $F'(x) = f(x)$ 를 이용해 방정식 세우기
3. **초월함수 적분**: $\tan x$, $\sec x$, $\csc x$ 등은 분자분모 변형 또는 보조공식 $\int \frac{f'}{f} = \ln|f|$ 활용
4. **$\sin^2 x$, $\cos^2 x$ 적분**: 반드시 반각공식으로 변환 후 적분
5. **적화공식 활용**: $\cos\alpha\sin\beta$ 꼴은 적화공식으로 분리 후 적분
6. **접선의 기울기 → 부정적분**: $f'(x)$를 적분하여 $f(x)$ 결정 후 초기조건으로 상수 $C$ 결정
