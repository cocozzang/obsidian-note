---
id: b2f3e1a4-9c7d-4f8e-a1b2-3c4d5e6f7a8b
aliases:
  - 정적분의 정의와 무한급수
  - 정적분의 정의
  - 무한급수와 정적분 변환
  - Def(5)
  - Thm47
tags:
  - 정적분
  - 무한급수
  - 리만합
  - 적분구간
  - 극한과적분
pages: 139
subject: 대학기초수학
title: 정적분의 정의와 무한급수
topics:
  - 정적분의 정의 (Def 5)
  - 직사각형 넓이의 합과 극한
  - 무한급수를 정적분으로 변환하는 방법
  - 정적분과 무한급수 (Thm 47)
---

# 46강: 정적분의 정의와 무한급수

## 1. 정적분의 정의

### Def (5): 정적분의 정의

함수 $f(x)$가 구간 $[a, b]$에서 연속일 때, 그 구간을 $n$등분하여 양쪽 끝과 각 분점의 $x$좌표를

$$x_0(=a),\ x_1,\ x_2,\ \cdots,\ x_{n-1},\ x_n(=b)$$

이라 하고 $\frac{b-a}{n} = \Delta x$라 할 때,

$$\lim_{n \to \infty} \sum_{k=1}^{n} f(x_k)\Delta x$$

의 값을 함수 $f(x)$의 $a$에서 $b$까지의 **정적분**이라 하고, 그 값을 $\int_{a}^{b} f(x)\,dx$로 나타낸다.

$$\boxed{\lim_{n \to \infty} \sum_{k=1}^{n} f(x_k)\Delta x = \int_{a}^{b} f(x)\,dx}$$

---

### 직사각형 넓이의 합 (전개)

구간 $[a, b]$를 $n$등분하면 $\Delta x = \frac{b-a}{n}$이고, 각 소구간의 오른쪽 끝점에서 함수값을 취한 직사각형 넓이의 합은 다음과 같다.

$$\frac{b-a}{n}\left\{f\!\left(a+\frac{b-a}{n}\right)+f\!\left(a+\frac{b-a}{n}\cdot 2\right)+\cdots+f\!\left(a+\frac{b-a}{n}\cdot n\right)\right\}$$

$$= \sum_{k=1}^{n} \frac{b-a}{n}\,f\!\left(a+\frac{b-a}{n}k\right)$$

따라서:

$$\lim_{n \to \infty}\sum_{k=1}^{n}\frac{b-a}{n}\,f\!\left(a+\frac{b-a}{n}k\right) = \int_{a}^{b}f(x)\,dx$$

> [!note] 핵심 2 — 정적분의 기하학적 의미
> $\int_{a}^{b}f(x)\,dx$는 **부호가 있는 직사각형 넓이의 합의 극한값**이다.
> - $f(x) > 0$인 구간 → 양(+)의 넓이
> - $f(x) < 0$인 구간 → 음(−)의 넓이
> - 결국 부호를 고려한 넓이의 합이다.

---

## 2. 핵심 1 — 무한급수 → 정적분으로 변환하는 기본 방식

### 변환 대응표

$$\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+\frac{b-a}{n}k\right)\cdot\frac{b-a}{n}$$

| 무한급수 요소 | 정적분 요소 |
|---|---|
| $\lim\sum$ | $\int$ |
| $a+\frac{b-a}{n}k$ | $x$ |
| $\frac{b-a}{n}$ | $dx$ |

### 적분구간 결정 원리

$dx = \Delta x$는 연속된 두 분점의 차이다:

$$dx = \Delta x = \left(a+\frac{b-a}{n}\cdot 2\right)-\left(a+\frac{b-a}{n}\cdot 1\right)=\frac{b-a}{n}$$

**적분 구간**은 무한급수에서 $k$의 첫 번째 값($k=1$)과 마지막 값($k=n$)을 대입하여 결정한다:

$$k=1 \text{ 일 때}: \quad a+\frac{b-a}{n}\cdot 1\ \xrightarrow{n\to\infty}\ a \quad \Rightarrow \text{아래끝}$$

$$k=n \text{ 일 때}: \quad a+\frac{b-a}{n}\cdot n = b \quad \Rightarrow \text{위끝}$$

$$\therefore \quad \int_{a}^{b}f(x)\,dx$$

---

## 3. Thm (47): 정적분과 무한급수

$$\boxed{\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+\frac{p}{n}k\right)\cdot\frac{p}{n} = \int_{a}^{a+p}f(x)\,dx = \int_{0}^{p}f(a+x)\,dx = p\int_{0}^{1}f(a+px)\,dx}$$

---

### 변환 방법 (1): $a+\frac{p}{n}k = x$로 치환

$$dx = \left(a+\frac{p}{n}\cdot 2\right)-\left(a+\frac{p}{n}\cdot 1\right) = \frac{p}{n}$$

적분구간:
$$k=1:\ a+\frac{p}{n}\cdot 1 \xrightarrow{n\to\infty} a \qquad k=n:\ a+\frac{p}{n}\cdot n = a+p$$

$$\therefore \quad \int_{a}^{a+p}f(x)\,dx$$

---

### 변환 방법 (2): $\frac{p}{n}k = x$로 치환

$$dx = \frac{p}{n}\cdot 2 - \frac{p}{n}\cdot 1 = \frac{p}{n}$$

적분구간:
$$k=1:\ \frac{p}{n}\cdot 1 \xrightarrow{n\to\infty} 0 \qquad k=n:\ \frac{p}{n}\cdot n = p$$

$$\therefore \quad \int_{0}^{p}f(a+x)\,dx$$

> [!note] 방법 (1) → (2) 관계
> (2)는 (1)에서 $x$를 $-a$만큼 평행이동한 것이다. 아래끝·위끝도 각각 $-a$만큼 줄어든다.

---

### 변환 방법 (3): $\frac{k}{n} = x$로 치환

$$dx = \frac{1}{n}\cdot 2 - \frac{1}{n}\cdot 1 = \frac{1}{n}$$

준식을 변형하면:

$$\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+\frac{p}{n}k\right)\cdot\frac{p}{n} = \lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+p\cdot\frac{k}{n}\right)\cdot p\cdot\frac{1}{n}$$

적분구간:
$$k=1:\ \frac{1}{n}\cdot 1 \xrightarrow{n\to\infty} 0 \qquad k=n:\ \frac{1}{n}\cdot n = 1$$

$$\therefore \quad p\int_{0}^{1}f(a+px)\,dx$$

---

### 변환 방법 (4): $\frac{k}{2n} = x$로 치환 (심화)

준식을 변형:

$$\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+\frac{p}{n}k\right)\cdot\frac{p}{n} = \lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(a+2p\cdot\frac{k}{2n}\right)\cdot\frac{2p}{2n}$$

$$dx = \frac{1}{2n}$$

적분구간:
$$k=1:\ \frac{1}{2n} \xrightarrow{n\to\infty} 0 \qquad k=n:\ \frac{n}{2n} = \frac{1}{2}$$

$$\therefore \quad 2p\int_{0}^{\frac{1}{2}}f(a+2px)\,dx$$

> [!note] 방법 (3) vs (4)
> (4)는 (3)에서 $f(x)$ 그래프가 $x$축 방향으로 $\frac{1}{2}$배 압축된 것에 해당한다 ($x$의 계수가 $p \to 2p$로 변함).

---

## 4. 예제

### 예제 — 간단 변환 연습

$$\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(1+\frac{5}{n}k\right)\cdot\frac{1}{n}$$

위 무한급수식을 정적분으로 바꾸어라.

> [!summary]- 풀이
>
> **준식 변형**: $\frac{1}{n} = \frac{1}{5}\cdot\frac{5}{n}$이므로
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(1+\frac{5}{n}k\right)\cdot\frac{1}{n} = \frac{1}{5}\lim_{n \to \infty}\sum_{k=1}^{n}f\!\left(1+\frac{5}{n}k\right)\cdot\frac{5}{n}$$
>
> ---
>
> **방법 (1)**: $1+\frac{5}{n}k = x$로 치환
>
> $$dx = \frac{5}{n}, \quad \text{아래끝}=1,\ \text{위끝}=6$$
>
> $$= \frac{1}{5}\int_{1}^{6}f(x)\,dx$$
>
> ---
>
> **방법 (2)**: $\frac{5}{n}k = x$로 치환
>
> $$\frac{1}{5}\int_{0}^{5}f(1+x)\,dx$$
>
> ---
>
> **방법 (3)**: $\frac{k}{n} = x$로 치환
>
> $$\int_{0}^{1}f(1+5x)\,dx$$

---

## 관련 주제

- [[45-integration-by-parts|45강: 부분적분]]
- [[47-fundamental-theorem|47강: 정적분과 부정적분의 관계]]
- [[48-integral-series-2|48강: 정적분과 무한급수 (2)]]

---

**학습 포인트:**
1. $\lim\sum \Rightarrow \int$, $\frac{b-a}{n} \Rightarrow dx$ — 무한급수와 정적분의 대응 관계를 정확히 암기한다.
2. 적분구간은 $k=1$과 $k=n$을 대입하여 $n\to\infty$ 극한으로 결정한다.
3. Thm 47의 세 가지 변환 방법은 모두 동치이며, 문제 형태에 따라 편리한 방법을 선택한다.
