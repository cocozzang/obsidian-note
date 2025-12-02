---
id: e9e77ccc-b1a4-4fd1-aa36-c96a920599e1
aliases:
  - 심화삼각함수(5)
  - 삼각함수의 합성
  - 삼각합수의 합성공식
tags:
  - 삼각함수합성
  - 삼각함수
  - 삼각함수덧셈정리
  - 심화삼각함수
pages: 33-35
subject: 대학기초수학
title: 심화삼각함수(5) - 삼각함수의 합성
topics:
  - 삼각함수의 합성
  - 삼각함수의 합성공식
  - 삼각함수의 합성 표현
---

# 심화삼각함수(5) - 삼각함수의 합성

## 1. 삼각함수의 합성

### Thm (17): 삼각함수의 합성

각이 같은 $\sin$, $\cos$의 합을 하나의 $\sin$ 또는 $\cos$으로 고치는 과정이다.

#### (1) $a\sin\theta + b\cos\theta$를 $\sin$의 합성으로 변환

$$a\sin\theta + b\cos\theta = \sqrt{a^2 + b^2} \sin(\theta + \alpha)$$

단, $\tan\alpha = \frac{b}{a}$ 이다.

**조건에 따른 $\alpha$의 범위:**

① $a > 0, b > 0 : 0 < \alpha < \frac{\pi}{2}$

② $a < 0, b > 0 : \frac{\pi}{2} < \alpha < \pi$

③ $a < 0, b < 0 : \pi < \alpha < \frac{3}{2}\pi$

④ $a > 0, b < 0 : \frac{3}{2}\pi < \alpha < 2\pi$

#### (2) $a\sin\theta + b\cos\theta$를 $\cos$의 합성으로 변환

$$a\sin\theta + b\cos\theta = \sqrt{a^2 + b^2} \cos(\theta - \beta)$$

단, $\tan\beta = \frac{a}{b}$ 이다.

**조건에 따른 $\beta$의 범위:**

① $b > 0, a > 0 : 0 < \beta < \frac{\pi}{2}$

② $b < 0, a > 0 : \frac{\pi}{2} < \beta < \pi$

③ $b < 0, a < 0 : \pi < \beta < \frac{3}{2}\pi$

④ $b > 0, a < 0 : \frac{3}{2}\pi < \beta < 2\pi$

#### (3) 합성의 도형으로의 해석 → 벡터의 내적과 같다

$$a\sin\theta + b\cos\theta = (\cos\theta, \sin\theta) \cdot (b, a) = \vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\gamma$$

여기서 $\gamma$는 $\vec{a}$와 $\vec{b}$가 이루는 각이고 $\gamma = 0°$ 즉 $\vec{a}$와 $\vec{b}$가 일치할 때 내적은 최댓값을 가진다.

### 합성 공식의 유도

#### (1)의 증명: $a\sin\theta + b\cos\theta = \sqrt{a^2 + b^2} \sin(\theta + \alpha)$

직각삼각형을 이용한 기하학적 유도:

```

               /|
              / |
    √(a²+b²) /  | a
            /   |
           /α   |
          /_____|
              b
```

위 직각삼각형에서:

- 빗변: $\sqrt{a^2 + b^2}$
- 밑변: $b$
- 높이: $a$
- $\tan\alpha = \frac{a}{b}$

**유도 과정:**

$$
\begin{align}
a\sin\theta + b\cos\theta &= \sqrt{a^2 + b^2} \left(\frac{a}{\sqrt{a^2 + b^2}}\sin\theta + \frac{b}{\sqrt{a^2 + b^2}}\cos\theta\right) \\
&= \sqrt{a^2 + b^2} (\cos\alpha \cdot \sin\theta + \sin\alpha \cdot \cos\theta) \\
&= \sqrt{a^2 + b^2} \sin(\theta + \alpha)
\end{align}
$$

단, $\tan\alpha = \frac{b}{a}$ 이다.

#### (2)의 증명: $a\sin\theta + b\cos\theta = \sqrt{a^2 + b^2} \cos(\theta - \beta)$

같은 직각삼각형을 이용하되, 각도를 다르게 설정:

```

             /|
            / |
  √(a²+b²) /  |a
          /   |
         / β  |
        /_____|
            b
```

$\tan\beta = \frac{a}{b}$로 설정

**유도 과정:**

$$
\begin{align}
a\sin\theta + b\cos\theta &= b\cos\theta + a\sin\theta \\
&= \sqrt{a^2 + b^2} \left(\frac{b}{\sqrt{a^2 + b^2}}\cos\theta + \frac{a}{\sqrt{a^2 + b^2}}\sin\theta\right) \\
&= \sqrt{a^2 + b^2} (\cos\beta \cdot \cos\theta + \sin\beta \cdot \sin\theta) \\
&= \sqrt{a^2 + b^2} \cos(\theta - \beta)
\end{align}
$$

단, $\tan\beta = \frac{a}{b}$ 이다.

#### (3)의 벡터 해석

벡터의 내적을 이용한 기하학적 해석:

$$a\sin\theta + b\cos\theta = (\cos\theta, \sin\theta) \cdot (b, a)$$

**벡터로 표현:**

- $\vec{a} = (\cos\theta, \sin\theta)$ (단위 벡터)
- $\vec{b} = (b, a)$

**내적 공식:**

$$\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\gamma$$

여기서:

- $|\vec{a}| = \sqrt{\cos^2\theta + \sin^2\theta} = 1$
- $|\vec{b}| = \sqrt{b^2 + a^2}$
- $\cos\gamma = 1$ (최댓값)

따라서:

$$a\sin\theta + b\cos\theta = |\vec{a}||\vec{b}|\cos\gamma = \sqrt{a^2 + b^2} \cdot \cos\gamma$$

$\gamma = 0°$ 즉 $\vec{a}$와 $\vec{b}$가 일치할 때 내적은 최댓값을 가진다.

**기하학적 의미:**

```
    y
    |
    |  (cosθ, sinθ)
    | /
    |/_____ θ
----+-------- x
    |
    |(b, a)
    |
```

① $\vec{a} = (a_1, a_2)$, $\vec{b} = (b_1, b_2)$ 라 두면

$$\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\gamma$$

일 때

$$\vec{a} \cdot \vec{b} = (a_1b_1 + a_2b_2)$$

② $\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\gamma$ 로부터

$$\cos\gamma = 1$$

즉, $\gamma = 0°$ 일 때 최댓값

---

## 2. 예제

### 예제 65

함수 $y = 3\sin x - 2\cos\left(x - \frac{\pi}{6}\right) + 1$의 최댓값과 최솟값의 곱을 구하여라.

> [!summary]- 풀이 1: $\sin$의 합성으로 변환
>
> **Step 1**: 삼각함수 덧셈정리를 이용하여 전개
>
> $\begin{align}
> y &= 3\sin x - 2\cos\left(x - \frac{\pi}{6}\right) + 1 \\
> &= 3\sin x - 2\left(\cos x \cos\frac{\pi}{6} + \sin x \sin\frac{\pi}{6}\right) + 1 \\
> &= 3\sin x - 2\left(\frac{\sqrt{3}}{2}\cos x + \frac{1}{2}\sin x\right) + 1 \\
> &= 3\sin x - \sqrt{3}\cos x - \sin x + 1 \\
> &= 2\sin x - \sqrt{3}\cos x + 1
> \end{align}$
>
> **Step 2**: $2\sin x - \sqrt{3}\cos x$를 $\sin$의 합성으로 변환
>
> $2\sin x + (-\sqrt{3})\cos x = \sqrt{2^2 + (-\sqrt{3})^2} \sin(x + \alpha)$
>
> 여기서:
>
> - $a = 2$, $b = -\sqrt{3}$
> - $\sqrt{a^2 + b^2} = \sqrt{4 + 3} = \sqrt{7}$
> - $\tan\alpha = \frac{b}{a} = \frac{-\sqrt{3}}{2}$
>
> **Step 3**: 최댓값과 최솟값 구하기
>
> $y = \sqrt{7}\sin(x + \alpha) + 1$
>
> - 최댓값: $k = \sqrt{7} + 1$ (when $\sin(x + \alpha) = 1$)
> - 최솟값: $m = -\sqrt{7} + 1$ (when $\sin(x + \alpha) = -1$)
>
> **Step 4**: 최댓값과 최솟값의 곱
>
> $\begin{align}
> k \cdot m &= (\sqrt{7} + 1)(-\sqrt{7} + 1) \\
> &= (1 + \sqrt{7})(1 - \sqrt{7}) \\
> &= 1 - 7 \\
> &= -6
> \end{align}$

> [!summary]- 풀이 2: 벡터 내적 이용
>
> **Step 1**: 같은 방식으로 전개하여
>
> $y = 2\sin x - \sqrt{3}\cos x + 1$
>
> **Step 2**: 벡터 내적으로 표현
>
> $2\sin x + (-\sqrt{3})\cos x = (\cos x, \sin x) \cdot (-\sqrt{3}, 2)$
>
> 벡터 $\vec{a} = (\cos x, \sin x)$, $\vec{b} = (-\sqrt{3}, 2)$
>
> **Step 3**: 내적의 최댓값과 최솟값
>
> $\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\gamma$
>
> 여기서:
>
> - $|\vec{a}| = 1$ (단위 벡터)
> - $|\vec{b}| = \sqrt{(-\sqrt{3})^2 + 2^2} = \sqrt{3 + 4} = \sqrt{7}$
>
> 따라서:
>
> - $\gamma = 0°$일 때 최댓값: $|\vec{a}||\vec{b}| = \sqrt{7}$
> - $\gamma = 180°$일 때 최솟값: $-|\vec{a}||\vec{b}| = -\sqrt{7}$
>
> **Step 4**: $y$의 최댓값과 최솟값
>
> - 최댓값: $k = \sqrt{7} + 1$
> - 최솟값: $m = -\sqrt{7} + 1$
> - 곱: $k \cdot m = (\sqrt{7} + 1)(-\sqrt{7} + 1) = 1 - 7 = -6$

### 예제 66

폐구간 $[0, \pi]$에서 정의된 함수 $f(x) = 3\sin x - 4\cos x$가 $x = \theta$에서 최댓값을 가질 때 $\sin\theta + \cos\theta$을 구하여라.

> [!summary]- 풀이
>
> **Step 1**: $f(x) = 3\sin x - 4\cos x$를 $\cos$의 합성으로 변환
>
> $0 \leq x \leq \pi$이므로, $f(x) = 3\sin x - 4\cos x$를 $\cos(x - \beta)$ 형태로 합성
>
> $f(x) = 3\sin x - 4\cos x = (-4)\cos x + 3\sin x$
>
> $= \sqrt{(-4)^2 + 3^2} \cos(x - \beta) = 5\cos(x - \beta)$
>
> 여기서 $\tan\beta = \frac{3}{-4}$이고, $b < 0$, $a > 0$이므로 $\frac{\pi}{2} < \beta < \pi$
>
> **Step 2**: 최댓값 조건
>
> $\cos(x - \beta) = -1$일 때 최댓값 (계수가 음수이므로)
>
> $x - \beta = 0 \text{ 또는 } x = \beta$
>
> 따라서 $x = \theta$일 때 $\theta = \beta$이고, $\sin\theta + \cos\theta = \sin\beta + \cos\beta$
>
> **Step 3**: $\sin\beta$와 $\cos\beta$ 구하기
>
> ```
>
>      /|
>   5 / |
>    /  | 3
>   /β  |
>  /____|
>    -4
> ```
>
> $\tan\beta = \frac{3}{-4}$이고 $\frac{\pi}{2} < \beta < \pi$이므로:
>
> - $\sin\beta = \frac{3}{5}$
> - $\cos\beta = -\frac{4}{5}$
>
> **Step 4**: 답 구하기
>
> $\sin\theta + \cos\theta = \sin\beta + \cos\beta = \frac{3}{5} + \left(-\frac{4}{5}\right) = -\frac{1}{5}$

### 예제 67

함수 $f(x) = \sqrt{3}\cos x + (2k - 1)\sin x$ $(0 \leq \theta \leq 2\pi)$가 $x = \frac{4}{3}\pi$에서 최솟값을 가질 때, 실수 $k$의 값을 구하여라.

> [!summary]- 풀이
>
> **Step 1**: $f(x)$를 $\cos$의 합성으로 변환
>
> $f(x) = \sqrt{3}\cos x + (2k - 1)\sin x$
>
> $= \sqrt{3 + (2k - 1)^2} \cos(x - \beta)$
>
> 여기서 $\tan\beta = \frac{2k - 1}{\sqrt{3}}$
>
> **Step 2**: 최솟값 조건
>
> $\cos(x - \beta) = -1$일 때 최솟값
>
> $x - \beta = \pi \Rightarrow x = \pi + \beta$
>
> 주어진 조건에서 $x = \frac{4}{3}\pi$이므로:
>
> $\frac{4}{3}\pi = \pi + \beta \Rightarrow \beta = \frac{\pi}{3}$
>
> **Step 3**: $k$ 구하기
>
> ```
>     √(3+(2k-1)²)
>         /|
>        / |
>  2k-1 /  | √3
>      /   |
>     / π/3|
>    /_____|
>      √3
> ```
>
> $\tan\beta = \tan\frac{\pi}{3} = \sqrt{3}$
>
> 따라서:
>
> $\frac{2k - 1}{\sqrt{3}} = \sqrt{3}$
>
> $2k - 1 = 3$
>
> $2k = 4$
>
> $k = 2$

### 예제 68

함수 $f(x) = a\cos^2 x + (a - b)\sin x \cos x + b\sin^2 x$의 최댓값이 $1 + \sqrt{2}$, 최솟값이 $1 - \sqrt{2}$일 때 $a + b$의 값을 구하여라. (단, $a > b$이다.)

> [!summary]- 풀이
>
> **Step 1**: $f(x)$를 정리 (배각공식 이용)
>
> 주어진 조건: 최댓값 $M = 1 + \sqrt{2}$, 최솟값 $m = 1 - \sqrt{2}$
>
> $M + m = |a + b| = (1 + \sqrt{2}) + (1 - \sqrt{2}) = 2$
>
> **Step 2**: 반각공식 적용
>
> $\begin{align}
> f(x) &= a\cos^2 x + (a - b)\sin x \cos x + b\sin^2 x \\
> &= \frac{1}{2}a + \frac{a}{2}\cos 2x + \frac{(a - b)}{2}\sin 2x + \frac{b}{2} - \frac{b}{2}\cos 2x \\
> &= \frac{(a - b)}{2}\sin 2x + \frac{(a - b)}{2}\cos 2x + \frac{a + b}{2}
> \end{align}$
>
> **Step 3**: 합성하기
>
> $f(x) = \frac{(a - b)}{2}\sin 2x + \frac{(a - b)}{2}\cos 2x + \frac{a + b}{2}$
>
> $= \frac{\sqrt{2}}{2}(a - b)(\sin 2x + \cos 2x) + \frac{a + b}{2}$
>
> 여기서 $x = \frac{\pi}{4}$일 때:
>
> $\sin 2x + \cos 2x = \sin\frac{\pi}{2} + \cos\frac{\pi}{2} = 1 + 0 = 1$
>
> **Step 4**: 최댓값과 최솟값 표현
>
> - $\sin 2x + \cos 2x$의 최댓값: $\sqrt{2}$ (when $\tan d = 1$)
> - $\sin 2x + \cos 2x$의 최솟값: $-\sqrt{2}$
>
> 따라서:
>
> - 최댓값: $M = \frac{\sqrt{2}}{2}(a - b) \cdot \sqrt{2} + \frac{a + b}{2} = (a - b) + \frac{a + b}{2}$
> - 최솟값: $m = -\frac{\sqrt{2}}{2}(a - b) \cdot \sqrt{2} + \frac{a + b}{2} = -(a - b) + \frac{a + b}{2}$
>
> **Step 5**: 연립방정식 풀이
>
> $M = \frac{\sqrt{2}}{2}(a - b) + \frac{a + b}{2} = 1 + \sqrt{2}$
>
> $m = -\frac{\sqrt{2}}{2}(a - b) + \frac{a + b}{2} = 1 - \sqrt{2}$
>
> 두 식을 더하면:
>
> $a + b = 2$

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 삼각함수의 합성 공식을 다양한 상황에 적용하는 능력을 숙지하시오.)

## 관련 주제

- [[11-advanced-trigonometry-4|심화삼각함수(4) - 기타공식]]
- [[13-transcendental-limit-1|초월함수의 극한(1)]]

---

**학습 포인트:**

1. 삼각함수의 합성은 $\sin$, $\cos$의 합을 하나의 삼각함수로 표현
2. 합성 공식의 계수는 $\sqrt{a^2 + b^2}$
3. 합성 각도는 $\tan\alpha = \frac{b}{a}$ 또는 $\tan\beta = \frac{a}{b}$로 결정
4. 벡터의 내적으로 해석 가능하며, 최댓값은 두 벡터가 평행할 때
5. $a$, $b$의 부호에 따라 각도 $\alpha$, $\beta$의 범위가 결정됨
6. 최댓값과 최솟값 문제에서 합성 공식을 활용하여 효과적으로 해결
