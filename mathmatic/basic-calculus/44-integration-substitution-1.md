---
id: a7f3b214-9e5d-4c82-b0f1-3e84d7c12a9f
aliases:
  - 초월함수의 부정적분(2)
  - 치환적분(1)
  - 치환적분법
  - 삼각함수의 치환적분
tags:
  - 치환적분
  - 초월함수의적분
  - 삼각함수의적분
  - 지수함수의적분
  - 로그함수의적분
  - 적분법
  - 중급
pages: 131-135
subject: 대학기초수학
title: 초월함수의 부정적분(2), 치환적분(1)
topics:
  - 치환적분법 (Thm 45)
  - 중요한 치환적분 패턴
  - 삼각함수 홀수 거듭제곱 적분
  - 지수·로그함수의 치환적분
  - 치환적분 응용 예제
---

# 44강: 초월함수의 부정적분(2), 치환적분(1)

## 1. 치환적분법

### Thm (45): 치환적분

$$
\int f(g(x))\,g'(x)\,dx \quad \text{(에서 } g(x) = t \Rightarrow g'(x)\,dx = dt\text{)}
$$

$$
= \int f(t)\,dt
$$

> [!note] 핵심 아이디어
> 복잡한 합성함수의 적분을 치환 $g(x) = t$를 통해 단순한 형태 $\int f(t)\,dt$로 변환한다.
> - **치환 선택 기준**: 피적분함수 안의 복잡한 부분 또는 도함수가 옆에 등장하는 부분을 $t$로 놓는다.

---

## 2. 중요한 치환적분

> [!tip] 삼각함수 홀수 거듭제곱 적분 전략
> $\sin^{홀수} x$ 또는 $\cos^{홀수} x$ 꼴: 하나를 분리 후 $\sin^2 + \cos^2 = 1$ 항등식 적용

### ① $\int \cos^3 x\,dx$

$$
\int \cos^3 x\,dx = \int \cos x \cdot \cos^2 x\,dx = \int \cos x(1 - \sin^2 x)\,dx
$$

$\sin x = t$ 로 치환 $\Rightarrow \cos x\,dx = dt$

$$
= \int (1 - t^2)\,dt = t - \frac{1}{3}t^3 + C = \sin x - \frac{1}{3}\sin^3 x + C
$$

---

### ② $\int \sin^5 x\,dx$

$$
\int \sin^5 x\,dx = \int \sin x \cdot \sin^4 x\,dx = \int \sin x(1 - \cos^2 x)^2\,dx
$$

$\cos x = t$ 로 치환 $\Rightarrow \sin x\,dx = -dt$ (부호 주의!)

$$
= \int (1-t^2)^2\,(-dt) = -\int (1 - 2t^2 + t^4)\,dt
$$

$$
= -t + \frac{2}{3}t^3 - \frac{1}{5}t^5 + C
$$

$$
= -\cos x + \frac{2}{3}\cos^3 x - \frac{1}{5}\cos^5 x + C
$$

---

### ③ $\int xe^{x^2}\,dx$

$x^2 = t$ 로 치환 $\Rightarrow 2x\,dx = dt$

$$
\int xe^{x^2}\,dx = \frac{1}{2}\int 2xe^{x^2}\,dx = \frac{1}{2}\int e^t\,dt = \frac{1}{2}e^t + C = \frac{1}{2}e^{x^2} + C
$$

---

### ④ $\int \frac{\ln x}{x}\,dx$

$\ln x = t$ 로 치환 $\Rightarrow \frac{1}{x}\,dx = dt$

$$
\int \frac{\ln x}{x}\,dx = \int t\,dt = \frac{1}{2}t^2 + C = \frac{1}{2}(\ln x)^2 + C
$$

---

## 3. 예제

### 예제 284

함수 $f(x) = \displaystyle\int xe^{x^2}\,dx$에 대하여 $f(0) = 0$일 때, $f(2)$의 값을 구하여라.

> [!summary]- 풀이
> $x^2 = t$ 로 치환 $\Rightarrow 2x\,dx = dt$:
>
> $$f(x) = \int xe^{x^2}\,dx = \frac{1}{2}\int 2xe^{x^2}\,dx = \frac{1}{2}\int e^t\,dt = \frac{1}{2}e^t + C = \frac{1}{2}e^{x^2} + C$$
>
> 초기조건 $f(0) = 0$ 대입:
>
> $$f(0) = \frac{1}{2}e^0 + C = \frac{1}{2} + C = 0 \implies C = -\frac{1}{2}$$
>
> $$f(x) = \frac{1}{2}e^{x^2} - \frac{1}{2}$$
>
> $$f(2) = \frac{1}{2}e^4 - \frac{1}{2} = \boxed{\frac{e^4 - 1}{2}}$$

---

### 예제 285

함수 $f(x) = \displaystyle\int \frac{\cos(\ln x)}{x}\,dx$에 대하여 $f(1) = 1$일 때, $f\!\left(e^{\frac{\pi}{2}}\right)$의 값을 구하여라.

> [!summary]- 풀이
> $\ln x = t$ 로 치환 $\Rightarrow \frac{1}{x}\,dx = dt$:
>
> $$f(x) = \int \frac{\cos(\ln x)}{x}\,dx = \int \cos t\,dt = \sin t + C = \sin(\ln x) + C$$
>
> 초기조건 $f(1) = 1$ 대입:
>
> $$f(1) = \sin(\ln 1) + C = \sin 0 + C = C = 1$$
>
> $$f(x) = \sin(\ln x) + 1$$
>
> $x = e^{\pi/2}$ 대입:
>
> $$f\!\left(e^{\frac{\pi}{2}}\right) = \sin\!\left(\ln e^{\frac{\pi}{2}}\right) + 1 = \sin\frac{\pi}{2} + 1 = 1 + 1 = \boxed{2}$$

---

### 예제 286

$\displaystyle\int (1 - \cos^3 x)\cos x \sin x\,dx$ 를 구하여라.

> [!summary]- 풀이
> $\cos x = t$ 로 치환 $\Rightarrow -\sin x\,dx = dt$, 즉 $\sin x\,dx = -dt$:
>
> $$\int (1 - \cos^3 x)\cos x \sin x\,dx = \int (1-t^3) \cdot t \cdot (-dt) = \int (t^4 - t)\,dt$$
>
> $$= \frac{1}{5}t^5 - \frac{1}{2}t^2 + C$$
>
> $$= \frac{1}{5}\cos^5 x - \frac{1}{2}\cos^2 x + C$$

---

### 예제 287

$\displaystyle\int 2xe^{x^2}\,dx$ 를 구하여라.

> [!summary]- 풀이
> $x^2 = t$ 로 치환 $\Rightarrow 2x\,dx = dt$:
>
> $$\int 2xe^{x^2}\,dx = \int e^t\,dt = e^t + C = e^{x^2} + C$$

---

### 예제 288

$\displaystyle\int \frac{3(\ln x)^2}{x}\,dx$ 를 구하여라.

> [!summary]- 풀이
> $\ln x = t$ 로 치환 $\Rightarrow \frac{1}{x}\,dx = dt$:
>
> $$\int \frac{3(\ln x)^2}{x}\,dx = \int 3t^2\,dt = t^3 + C = (\ln x)^3 + C$$

---

### 예제 289

$\displaystyle\int (\sin^3 x + 1)\cos x\,dx$ 를 구하여라.

> [!summary]- 풀이
> $\sin x = t$ 로 치환 $\Rightarrow \cos x\,dx = dt$:
>
> $$\int (\sin^3 x + 1)\cos x\,dx = \int (t^3 + 1)\,dt = \frac{1}{4}t^4 + t + C$$
>
> $$= \frac{1}{4}\sin^4 x + \sin x + C$$

---

### 예제 290

$\displaystyle\int \frac{\sqrt{\ln x}}{x}\,dx$ 를 구하여라.

> [!summary]- 풀이
> $\ln x = t$ 로 치환 $\Rightarrow \frac{1}{x}\,dx = dt$:
>
> $$\int \frac{\sqrt{\ln x}}{x}\,dx = \int \sqrt{t}\,dt = \int t^{\frac{1}{2}}\,dt = \frac{2}{3}t^{\frac{3}{2}} + C$$
>
> $$= \frac{2}{3}(\ln x)^{\frac{3}{2}} + C = \frac{2}{3}\ln x \cdot \sqrt{\ln x} + C$$

---

### 예제 291

$f(x) = \displaystyle\int \frac{x}{\sqrt{x+1}}\,dx$이고 $f(0) = 1$일 때 $f(3)$을 구하여라.

> [!summary]- 풀이
> $\sqrt{x+1} = t$ 로 치환 $\Rightarrow x+1 = t^2 \Rightarrow x = t^2-1$
>
> 양변 미분: $1 = 2t \cdot \frac{dt}{dx} \Rightarrow dx = 2t\,dt$
>
> $$f(x) = \int \frac{t^2-1}{t} \cdot 2t\,dt = \int (2t^2 - 2)\,dt = \frac{2}{3}t^3 - 2t + C$$
>
> $t = \sqrt{x+1}$ 로 역치환:
>
> $$f(x) = \frac{2}{3}(x+1)\sqrt{x+1} - 2\sqrt{x+1} + C$$
>
> 초기조건 $f(0) = 1$ 대입:
>
> $$f(0) = \frac{2}{3}(1)(1) - 2(1) + C = \frac{2}{3} - 2 + C = 1$$
>
> $$C = 1 + 2 - \frac{2}{3} = 3 - \frac{2}{3} = \frac{7}{3}$$
>
> $$f(x) = \frac{2}{3}(x+1)\sqrt{x+1} - 2\sqrt{x+1} + \frac{7}{3}$$
>
> $x = 3$ 대입:
>
> $$f(3) = \frac{2}{3}(4)(2) - 2(2) + \frac{7}{3} = \frac{16}{3} - 4 + \frac{7}{3} = \frac{23}{3} - \frac{12}{3} = \boxed{\frac{11}{3}}$$

---

### 예제 292

$f'(x) = \dfrac{x-3}{(x-1)^3}$이고 $f(0) = 2$일 때 $f(2)$의 값을 구하여라.

> [!summary]- 풀이
> $x-1 = t$ 로 치환 $\Rightarrow x = t+1$, $dx = dt$:
>
> $$f(x) = \int \frac{x-3}{(x-1)^3}\,dx = \int \frac{(t+1)-3}{t^3}\,dt = \int \frac{t-2}{t^3}\,dt$$
>
> $$= \int (t^{-2} - 2t^{-3})\,dt = -t^{-1} + t^{-2} + C$$
>
> $t = x-1$ 로 역치환:
>
> $$f(x) = -\frac{1}{x-1} + \frac{1}{(x-1)^2} + C$$
>
> 초기조건 $f(0) = 2$ 대입:
>
> $$f(0) = -\frac{1}{-1} + \frac{1}{(-1)^2} + C = 1 + 1 + C = 2 \implies C = 0$$
>
> $$f(x) = -\frac{1}{x-1} + \frac{1}{(x-1)^2}$$
>
> $$f(2) = -\frac{1}{1} + \frac{1}{1} = \boxed{0}$$

---

### 예제 293

$f(x) = \displaystyle\int \frac{2}{1-e^x}\,dx$일 때, $f(2) - f(1)$의 값을 구하여라.

> [!summary]- 풀이
> $1 - e^x = t$ 로 치환 $\Rightarrow -e^x\,dx = dt$, $e^x = 1-t$:
>
> $$dx = \frac{dt}{-e^x} = \frac{dt}{-(1-t)} = \frac{dt}{t-1}$$
>
> $$f(x) = \int \frac{2}{t} \cdot \frac{dt}{t-1} = 2\int \frac{1}{t(t-1)}\,dt$$
>
> 부분분수 분해: $\frac{1}{t(t-1)} = \frac{-1}{t} + \frac{1}{t-1}$ (분자비교: $\frac{1}{t(t-1)} = \frac{A}{t} + \frac{B}{t-1}$ $\Rightarrow$ $A=-1, B=1$)
>
> $$f(x) = 2\int \left(\frac{-1}{t} + \frac{1}{t-1}\right)dt = 2(-\ln|t| + \ln|t-1|) + C$$
>
> $$= 2\ln\left|\frac{t-1}{t}\right| + C$$
>
> $t = 1-e^x$ 로 역치환, $t-1 = -e^x$:
>
> $$= 2\ln\left|\frac{-e^x}{1-e^x}\right| + C = 2\ln\left|\frac{e^x}{e^x-1}\right| + C$$
>
> 상수 $C$는 $f(2)-f(1)$ 계산 시 소거:
>
> $$f(2) - f(1) = 2\ln\frac{e^2}{e^2-1} - 2\ln\frac{e}{e-1}$$
>
> $$= 2\ln\left(\frac{e^2}{e^2-1} \cdot \frac{e-1}{e}\right) = 2\ln\left(\frac{e^2}{(e-1)(e+1)} \cdot \frac{e-1}{e}\right)$$
>
> $$= 2\ln\frac{e}{e+1} = \boxed{2\ln\frac{e}{e+1}}$$

---

## 관련 주제

- [[43-indefinite-integral-1|43강: 부정적분, 초월함수의 부정적분(1)]]
- [[45-integration-by-parts|45강: 부분적분]]

---

**학습 포인트:**
1. **치환적분 기본 원리**: $g(x) = t$ 치환 시 $g'(x)\,dx = dt$ 로 변환
2. **삼각함수 홀수 거듭제곱**: 하나를 분리 후 피타고라스 항등식으로 변환, 나머지를 $t$로 치환
3. **$e^{f(x)}$ 꼴**: 지수 부분을 $t$로 치환, 도함수가 옆에 있는지 확인
4. **$\ln x$ 포함**: $\ln x = t$ 치환 시 $\frac{1}{x}\,dx = dt$ 로 자연스럽게 정리
5. **$\sqrt{ax+b}$ 꼴**: $\sqrt{ax+b} = t$ 로 직접 치환, $dx = \frac{2t}{a}\,dt$ 유도
6. **부분분수 분해 활용**: 유리함수 치환 후 분모 인수분해가 필요한 경우 적용
