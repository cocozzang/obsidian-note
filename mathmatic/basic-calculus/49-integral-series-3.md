---
id: b3e2f1a4-9c7d-4e58-8b21-6f03d2a85c19
aliases:
  - 정적분과 무한급수(3)
  - 리만합 정적분 변환
  - 구간변환 리만합
  - 도형 무한급수
tags:
  - 정적분
  - 무한급수
  - 리만합
  - 구간변환
  - 치환적분
  - 도형과정적분
pages: 146-149
subject: 대학기초수학
title: 정적분과 무한급수(3)
topics:
  - 리만합의 정적분 변환 응용
  - 구간이 [0,1]이 아닌 경우의 변환
  - 도형의 길이·넓이를 무한급수로 표현 후 정적분 변환
---

# 정적분과 무한급수(3)

> 이 강에서는 [[48-integral-series-2|정적분과 무한급수(2)]]에서 학습한 리만합–정적분 변환 공식을 다양한 유형에 적용한다.
> 구간이 $[0,1]$이 아닌 경우, 삼각·지수·로그함수, 그리고 도형을 매개로 한 응용 문제를 집중적으로 다룬다.

---

## 1. 핵심 공식 복습

이전 강에서 확립한 핵심 변환 공식:

$$
\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} f\!\left(\frac{k}{n}\right) = \int_{0}^{1} f(x)\, dx
$$

**구간이 $[a, b]$인 경우** — $x_k = a + \frac{(b-a)k}{n}$으로 치환:

$$
\lim_{n \to \infty} \frac{b-a}{n} \sum_{k=1}^{n} f\!\left(a + \frac{(b-a)k}{n}\right) = \int_{a}^{b} f(x)\, dx
$$

따라서 공통인수 $\frac{1}{n}$을 먼저 분리한 뒤, $\frac{k}{n} \to x$로 대응시켜 구간을 결정한다.

---

## 2. 패턴별 변환 정리

### 패턴 ①: $\frac{1}{n}\sum f\!\left(\frac{k}{n}\right)$ → 구간 $[0,1]$

$$
\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} f\!\left(\frac{k}{n}\right) = \int_{0}^{1} f(x)\, dx
$$

### 패턴 ②: $\frac{\pi}{n}\sum f\!\left(\frac{k\pi}{n}\right)$ → 구간 $[0,\pi]$

$t = \frac{k\pi}{n}$으로 놓으면 $\frac{\pi}{n} = \Delta t$이므로:

$$
\lim_{n \to \infty} \frac{\pi}{n} \sum_{k=1}^{n} f\!\left(\frac{k\pi}{n}\right) = \int_{0}^{\pi} f(x)\, dx
$$

### 패턴 ③: $\frac{1}{n}\sum f\!\left(a + \frac{(b-a)k}{n}\right)$ → 스케일 조정

$$
\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} f\!\left(a + \frac{(b-a)k}{n}\right) = \frac{1}{b-a}\int_{a}^{b} f(x)\, dx
$$

---

## 3. 예제

### 예제 310

$$
\lim_{n \to \infty} \frac{1}{n} \left( \sqrt{\frac{1}{n}} + \sqrt{\frac{2}{n}} + \sqrt{\frac{3}{n}} + \cdots + \sqrt{\frac{n}{n}} \right)
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> 시그마 형태로 정리:
>
> $$\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \sqrt{\frac{k}{n}}$$
>
> $f(x) = \sqrt{x}$, 구간 $[0, 1]$의 리만합이므로:
>
> $$= \int_{0}^{1} \sqrt{x}\, dx = \int_{0}^{1} x^{\frac{1}{2}}\, dx = \left[ \frac{2}{3} x^{\frac{3}{2}} \right]_{0}^{1}$$
>
> $$= \frac{2}{3} - 0 = \boxed{\frac{2}{3}}$$

---

### 예제 311

$$
\lim_{n \to \infty} \frac{1}{n}\left( \sin\frac{\pi}{n} + \sin\frac{2\pi}{n} + \sin\frac{3\pi}{n} + \cdots + \sin\frac{n\pi}{n} \right)
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> 시그마 형태로 정리:
>
> $$\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \sin\frac{k\pi}{n}$$
>
> $\frac{k\pi}{n} = \pi \cdot \frac{k}{n}$이므로 $f(x) = \sin(\pi x)$, 구간 $[0,1]$로 볼 수도 있고,
> 또는 $\frac{\pi}{n}$를 인수로 묶어 구간 $[0, \pi]$로 변환:
>
> $$= \frac{1}{\pi} \int_{0}^{\pi} \sin x\, dx = \frac{1}{\pi} \left[ -\cos x \right]_{0}^{\pi}$$
>
> $$= \frac{1}{\pi}(1 - (-1)) = \boxed{\frac{2}{\pi}}$$

---

### 예제 312

$$
\lim_{n \to \infty} \frac{\pi}{n}\left\{ \sin\!\left(\pi + \frac{\pi}{n}\right) + \sin\!\left(\pi + \frac{2\pi}{n}\right) + \cdots + \sin\!\left(\pi + \frac{n\pi}{n}\right) \right\}
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> 시그마 형태로 정리:
>
> $$\lim_{n \to \infty} \frac{\pi}{n} \sum_{k=1}^{n} \sin\!\left(\pi + \frac{k\pi}{n}\right)$$
>
> $\frac{\pi}{n} = \Delta x$, $x_k = \pi + \frac{k\pi}{n}$이므로 $x$는 $\pi \to 2\pi$ 범위:
>
> $$= \int_{\pi}^{2\pi} \sin x\, dx = \left[ -\cos x \right]_{\pi}^{2\pi}$$
>
> $$= (-\cos 2\pi) - (-\cos \pi) = -1 + (-1) = \boxed{0}$$

---

### 예제 313

$$
\lim_{n \to \infty} \left( \ln\!\sqrt[n]{\frac{n+1}{n}} + \ln\!\sqrt[n]{\frac{n+2}{n}} + \ln\!\sqrt[n]{\frac{n+3}{n}} + \cdots + \ln\!\sqrt[n]{\frac{n+n}{n}} \right)
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> $\ln\!\sqrt[n]{A} = \frac{1}{n}\ln A$ 이므로 각 항을 변환:
>
> $$\ln\!\sqrt[n]{\frac{n+k}{n}} = \frac{1}{n}\ln\frac{n+k}{n} = \frac{1}{n}\ln\!\left(1 + \frac{k}{n}\right)$$
>
> 따라서 전체 합은:
>
> $$\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \ln\!\left(1 + \frac{k}{n}\right)$$
>
> $f(x) = \ln(1+x)$, 구간 $[0,1]$의 리만합 → $x \to (1+x)$로 치환하면 구간 $[1, 2]$:
>
> $$= \int_{1}^{2} \ln x\, dx = \left[ x\ln x - x \right]_{1}^{2}$$
>
> $$= (2\ln 2 - 2) - (0 - 1) = 2\ln 2 - 2 + 1 = \boxed{2\ln 2 - 1}$$

---

### 예제 314

오른쪽 그림과 같이 곡선 $y = f(x)$와 $x$축 및 두 직선 $x=1$, $x=3$으로 둘러싸인 부분의 넓이를 $A$라 하자. 이 때, $\displaystyle\lim_{n \to \infty} \sum_{k=1}^{n} f\!\left(1 + \frac{2k}{n}\right)\frac{1}{n}$의 값을 $A$로 나타내면?

![exer314|1000](./images/04-integral/exer314.png)

> [!summary]- 풀이
>
> 주어진 합에서 $\frac{2}{n}$을 인수로 나타내기:
>
> $$
> \lim_{n \to \infty} \sum_{k=1}^{n} f\!\left(1 + \frac{2k}{n}\right) \frac{1}{n}
> = \lim_{n \to \infty} \frac{1}{2} \cdot \frac{2}{n} \sum_{k=1}^{n} f\!\left(1 + \frac{2k}{n}\right)
> $$
>
> $x_k = 1 + \frac{2k}{n}$, $\Delta x = \frac{2}{n}$이므로 $x$: $1 \to 3$:
>
> $$= \frac{1}{2} \int_{1}^{3} f(x)\, dx = \frac{A}{2}$$
>
> **정답**: ① $\dfrac{A}{2}$

---

### 예제 315

다음 그림과 같이 지름의 길이가 2인 반원의 호 AB를 $n$등분한 점을 차례로 $C_0$, $C_1$, $C_2$, $\cdots$, $C_n(=\text{B})$이라 할 때, $\displaystyle\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n}\overline{AC_k}$의 값을 구하는 식은?

![exer315|1000](./images/04-integral/exer315.png)

> [!summary]- 풀이
>
> 반원의 지름 $\overline{AB} = 2$이므로 반지름 = 1. 중심각을 기준으로 $C_k$의 위치 분석.
>
> 호 AB 전체의 중심각 = $\pi$이고, $n$등분하므로 각 구간의 중심각 = $\frac{\pi}{n}$.
> $C_k$에 대한 $\angle AOC_k = \frac{\pi}{n} \cdot k$ (A에서부터 측정).
>
> 코사인 법칙 적용 ($\overline{OA} = \overline{OC_k} = 1$):
>
> $$\overline{AC_k}^2 = 1^2 + 1^2 - 2 \cdot 1 \cdot 1 \cdot \cos\frac{\pi k}{n} = 2 - 2\cos\frac{\pi k}{n}$$
>
> $$\overline{AC_k} = \sqrt{2 - 2\cos\frac{\pi k}{n}}$$
>
> 따라서:
>
> $$\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \sqrt{2 - 2\cos\frac{\pi k}{n}} = \int_{0}^{1} \sqrt{2 - 2\cos\pi x}\, dx$$
>
> **정답**: ④ $\displaystyle\int_{0}^{1} \sqrt{2 - 2\cos\pi x}\, dx$

---

### 예제 316

좌표평면 위에 중심이 원점이고 반지름의 길이가 $a$인 원이 있다. 이 원에 내접하는 정 $n$각형의 꼭지점들을 $P_0, P_1, P_2, \cdots, P_{n-1}$로 나타내자. 선분 $\overline{P_0 P_k}$의 길이를 $L_k$로 할 때, $\displaystyle\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n-1} L_k$을 구하여라. (단, $P_0(a,\,0)$)

![exer316|1000](./images/04-integral/exer316.png)

![exer316-2|1000](./images/04-integral/exer316-2.png)

> [!summary]- 풀이
>
> $P_0 = (a, 0)$이고 정 $n$각형의 꼭지점이므로 $P_k$의 중심각은 $\frac{2\pi k}{n}$.
>
> 코사인 법칙 ($\overline{OP_0} = \overline{OP_k} = a$, 사이각 = $\frac{2\pi k}{n}$):
>
> $$L_k = \overline{P_0 P_k} = \sqrt{a^2 + a^2 - 2a^2\cos\frac{2\pi k}{n}} = a\sqrt{2 - 2\cos\frac{2\pi k}{n}}$$
>
> 반각 공식 $2 - 2\cos\theta = 4\sin^2\frac{\theta}{2}$ 적용:
>
> $$L_k = 2a\sin\frac{\pi k}{n}$$
>
> 따라서:
>
> $$
> \lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n-1} 2a\sin\frac{\pi k}{n}
> = \frac{1}{\pi} \int_{0}^{\pi} 2a\sin x\, dx
> $$
>
> $$= \frac{2a}{\pi}\left[-\cos x\right]_{0}^{\pi} = \frac{2a}{\pi}(1 - (-1)) = \boxed{\frac{4a}{\pi}}$$
>
> **정답**: ⑤ $\dfrac{4a}{\pi}$

---

### 예제 317

길이가 2인 선분 $\overline{AB}$를 지름으로 하는 반원의 호를 $n$등분하여 각 점을 차례로 $P_0$, $P_1$, $P_2$, $\cdots$, $P_{n-1}$이라 하고, $\triangle ABP_k$의 넓이를 $S_k$라 할 때, $\displaystyle\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n-1} S_k$의 값은?

![exer317|1000](./images/04-integral/exer317.png)

> [!summary]- 풀이
>
> ![exer317-2|1000](./images/04-integral/exer317-2.png)
>
> 반원의 지름 $\overline{AB} = 2$이므로 반지름 = 1, 중심 O.
>
> **탈레스의 정리**: 지름에 대한 원주각은 직각이므로 $\angle AP_k B = \frac{\pi}{2}$.
>
> 호를 $n$등분 → 중심각 $\angle P_k OB = \frac{\pi k}{n}$
>
> 원주각은 중심각의 절반이므로: $\angle P_k AB = \frac{\pi k}{2n}$
>
> 따라서:
>
> - $\overline{AP_k} = 2\cos\frac{\pi k}{2n}$ &emsp; ($\overline{AB} = 2$, $\cos$ 관계)
> - $\overline{BP_k} = 2\sin\frac{\pi k}{2n}$
>
> 직각삼각형 $\triangle ABP_k$의 넓이:
>
> $$
> S_k = \frac{1}{2} \cdot \overline{AP_k} \cdot \overline{BP_k}
> = \frac{1}{2} \cdot 2\cos\frac{\pi k}{2n} \cdot 2\sin\frac{\pi k}{2n}
> $$
>
> $2\sin\theta\cos\theta = \sin 2\theta$ 배각 공식 적용:
>
> $$= 2\sin\frac{\pi k}{2n}\cos\frac{\pi k}{2n} = \sin\frac{\pi k}{n}$$
>
> 따라서:
>
> $$
> \lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n-1} \sin\frac{\pi k}{n}
> = \frac{1}{\pi}\int_{0}^{\pi} \sin x\, dx
> = \frac{1}{\pi}\left[-\cos x\right]_{0}^{\pi}
> $$
>
> $$= \frac{1}{\pi}(1 - (-1)) = \boxed{\frac{2}{\pi}}$$
>
> **정답**: ② $\dfrac{2}{\pi}$

---

### 예제 318

$$
\lim_{n \to \infty} \sum_{k=1}^{n} \frac{\pi}{n}\sin^2\frac{k\pi}{2n}
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> $\frac{\pi}{n} = \Delta x$, $x_k = \frac{k\pi}{n}$이므로 구간 $[0, \pi]$의 리만합.
> 단, $\sin^2$의 인수가 $\frac{k\pi}{2n} = \frac{x_k}{2}$이므로 $f(x) = \sin^2\frac{x}{2}$.
>
> 구간 $[0, \pi]$를 $x = 2t$로 치환하면 구간 $[0, \frac{\pi}{2}]$:
>
> $$= 2\int_{0}^{\frac{\pi}{2}} \sin^2 x\, dx$$
>
> 반각 공식 $\sin^2 x = \frac{1 - \cos 2x}{2}$ 적용:
>
> $$= 2\int_{0}^{\frac{\pi}{2}} \frac{1-\cos 2x}{2}\, dx = \int_{0}^{\frac{\pi}{2}} (1 - \cos 2x)\, dx$$
>
> $$= \left[ x - \frac{1}{2}\sin 2x \right]_{0}^{\frac{\pi}{2}} = \frac{\pi}{2} - 0 = \boxed{\frac{\pi}{2}}$$

---

### 예제 319

$$
\lim_{n \to \infty} \sum_{k=1}^{n} \frac{k^2}{n^3 + k^3}
$$

의 값을 구하여라.

> [!summary]- 풀이
>
> 분모·분자를 $\frac{1}{n^3}$으로 나누어 $\frac{k}{n}$ 꼴로 변환:
>
> $$\frac{k^2}{n^3+k^3} = \frac{\frac{k^2}{n^3}}{1 + \frac{k^3}{n^3}} = \frac{1}{n} \cdot \frac{\left(\frac{k}{n}\right)^2}{1 + \left(\frac{k}{n}\right)^3}$$
>
> 따라서:
>
> $$\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \frac{\left(\frac{k}{n}\right)^2}{1+\left(\frac{k}{n}\right)^3} = \int_{0}^{1} \frac{x^2}{1+x^3}\, dx$$
>
> $u = 1 + x^3$으로 치환, $du = 3x^2\, dx$:
>
> $$= \frac{1}{3}\int_{0}^{1} \frac{3x^2}{1+x^3}\, dx = \frac{1}{3}\left[\ln|1+x^3|\right]_{0}^{1}$$
>
> $$= \frac{1}{3}(\ln 2 - 0) = \boxed{\frac{\ln 2}{3}}$$

---

### 예제 320

$f(x) = e^{3x}$일 때, $\displaystyle\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n} f\!\left(\frac{2k}{n}\right)$의 값을 구하여라.

> [!summary]- 풀이
>
> $f\!\left(\frac{2k}{n}\right) = e^{3 \cdot \frac{2k}{n}}$이고, $x_k = \frac{2k}{n}$으로 구간 $[0, 2]$의 리만합.
>
> $\frac{2}{n}$을 인수로 분리:
>
> $$
> \lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n} f\!\left(\frac{2k}{n}\right)
> = \frac{1}{2} \int_{0}^{2} f(x)\, dx = \frac{1}{2}\int_{0}^{2} e^{3x}\, dx
> $$
>
> $$= \frac{1}{2}\left[\frac{1}{3}e^{3x}\right]_{0}^{2} = \frac{1}{2}\left(\frac{1}{3}e^6 - \frac{1}{3}\right) = \boxed{\frac{e^6 - 1}{6}}$$

---

## 관련 주제

- [[48-integral-series-2|정적분과 무한급수(2)]]
- [[50-integral-techniques-1|정적분의 계산기법(1)]]
- [[45-integration-by-parts|부분적분]]

---

**학습 포인트:**

1. $\frac{1}{n}$을 공통 인수로 분리한 뒤 $\frac{k}{n} \to x$로 대응시켜 구간 $[a,b]$를 결정한다.
2. $\frac{\pi}{n}$이 앞에 있으면 구간 $[0, \pi]$, $\frac{b-a}{n}$이면 구간 $[a, b]$임을 파악한다.
3. 도형 문제는 코사인 법칙·반각 공식·탈레스 정리를 이용해 $L_k$ 또는 $S_k$를 $\sin$ / $\cos$으로 표현한 후 리만합으로 변환한다.
4. $\int \ln x\, dx = x\ln x - x + C$ (부분적분), $\int \frac{x^2}{1+x^3}dx$ (치환적분) 등 기본 적분 공식을 숙지한다.
