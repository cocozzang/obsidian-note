---
id: 59550a86-8668-44a4-9b05-b84a0a8f26f4
aliases:
  - 심화삼각함수(2)
  - 덧셈정리의 응용
  - 배각공식
tags:
  - 삼각함수
  - 덧셈정리
  - 배각공식
  - 반각공식
  - 2배각공식
  - 3배각공식
  - 직선의예각
pages: 24-26
subject: 대학기초수학
title: 심화삼각함수(2) - 덧셈정리의 응용, 배각공식
topics:
  - 정삼각형의 응용
  - 덧셈정리를 이용한 특수각 관계
  - 두 직선이 이루는 예각
  - 2배각 공식
  - 3배각 공식
  - 반각 공식
---

# 심화삼각함수(2) - 덧셈정리의 응용, 배각공식

### Thm (14): 덧셈정리의 응용

#### (1) α + β = π/2 일 때

$$\alpha + \beta = \frac{\pi}{2}$$

이면 다음이 성립한다:

$$
\begin{cases}
\sin^2\alpha + \sin^2\beta = 1 \\
\cos^2\alpha + \cos^2\beta = 1 \\
\tan\alpha \tan\beta = 1
\end{cases}
$$

**의미**: 두 각이 서로 여각 관계일 때의 삼각함수 성질

#### (2) α + β = π/4 또는 3π/4 일 때

**① α + β = π/4 일 때:**

$$(1 + \tan\alpha)(1 + \tan\beta) = 2$$

**② α + β = 3π/4 일 때:**

$$(1 - \tan\alpha)(1 - \tan\beta) = 2$$

**의미**: 두 각의 합이 45° 또는 135°일 때의 탄젠트 관계

#### (3) 두 직선이 이루는 예각

두 직선 $l_1$, $l_2$가 이루는 예각 $\theta$에 대하여:

$$\tan\theta = |\tan(\alpha - \beta)| = \left|\frac{m_1 - m_2}{1 + m_1 \times m_2}\right|$$

여기서:

- $m_1$: 직선 $l_1$의 기울기
- $m_2$: 직선 $l_2$의 기울기
- $\alpha$, $\beta$: 각 직선이 $x$축의 양의 방향과 이루는 각

**응용**: 두 직선 사이의 각도를 구할 때 사용

---

## 2. 예제 - 덧셈정리 응용

### 예제 46

다음 각 식의 값을 구하여라.

**(1)** $\sin^2 1° + \sin^2 2° + \cdots + \sin^2 88° + \sin^2 89° + \sin^2 90°$

> [!summary]- 풀이
> $\alpha + \beta = 90°$일 때 $\sin^2\alpha + \sin^2\beta = 1$을 이용한다.
>
> 각도를 쌍으로 묶으면:
>
> - $(\sin^2 1° + \sin^2 89°) = 1$
> - $(\sin^2 2° + \sin^2 88°) = 1$
> - $\vdots$
> - $(\sin^2 44° + \sin^2 46°) = 1$
> - $\sin^2 45° = \left(\frac{\sqrt{2}}{2}\right)^2 = \frac{1}{2}$
> - $\sin^2 90° = 1$
>
> 따라서:
>
> $$
> \begin{align}
> &= 44 \times 1 + \frac{1}{2} + 1 \\
> &= 44 + 0.5 + 1 \\
> &= 45.5 = \frac{91}{2}
> \end{align}
> $$

**(2)** $\tan 1° \times \tan 2° \times \cdots \times \tan 88° \times \tan 89°$

> [!summary]- 풀이
> $\alpha + \beta = 90°$일 때 $\tan\alpha \tan\beta = 1$을 이용한다.
>
> 각도를 쌍으로 묶으면:
>
> - $(\tan 1° \times \tan 89°) = 1$
> - $(\tan 2° \times \tan 88°) = 1$
> - $\vdots$
> - $(\tan 44° \times \tan 46°) = 1$
> - $\tan 45° = 1$
>
> 따라서:
> $$= 1^{44} \times 1 = 1$$

**(3)** $(1+\tan 1°)(1+\tan 2°) \times \cdots \times (1+\tan 44°)(1+\tan 45°)$

> [!summary]- 풀이
> $\alpha + \beta = 45°$일 때 $(1+\tan\alpha)(1+\tan\beta) = 2$를 이용한다.
>
> 각도를 쌍으로 묶으면:
>
> - $(1+\tan 1°)(1+\tan 44°) = 2$
> - $(1+\tan 2°)(1+\tan 43°) = 2$
> - $\vdots$
> - $(1+\tan 22°)(1+\tan 23°) = 2$
> - $(1+\tan 45°) = 1 + 1 = 2$
>
> 따라서:
> $$= 2^{22} \times 2 = 2^{23}$$

**(4)** $\dfrac{(1+\tan 1°)(1+\tan 2°) \times \cdots \times (1+\tan 43°)(1+\tan 44°)}{(1-\tan 46°)(1-\tan 47°) \times \cdots \times (1-\tan 88°)(1-\tan 89°)}$

> [!summary]- 풀이
>
> - 분자: $\alpha + \beta = 45°$일 때 $(1+\tan\alpha)(1+\tan\beta) = 2$
> - 분모: $\alpha + \beta = 135°$일 때 $(1-\tan\alpha)(1-\tan\beta) = 2$
>
> **분자 계산:**
>
> - $(1+\tan 1°)(1+\tan 44°) = 2$
> - $(1+\tan 2°)(1+\tan 43°) = 2$
> - $\vdots$
> - 총 22쌍이므로: $2^{22}$
>
> **분모 계산:**
>
> - $(1-\tan 46°)(1-\tan 89°) = 2$ ($46° + 89° = 135°$)
> - $(1-\tan 47°)(1-\tan 88°) = 2$ ($47° + 88° = 135°$)
> - $\vdots$
> - 총 22쌍이므로: $2^{22}$
>
> 따라서:
> $$\frac{2^{22}}{2^{22}} = 1$$

---

### 예제 47

두 직선 $y = 3x + 2$, $y = -2x + 1$이 이루는 예각의 크기를 $\theta$라 할 때, $\sec^2\theta$의 값을 구하여라.

> [!summary]- 풀이
> 두 직선의 기울기는 $m_1 = 3$, $m_2 = -2$이다.
>
> 두 직선이 이루는 예각 $\theta$에 대하여:
> $$\tan\theta = \left|\frac{m_1 - m_2}{1 + m_1 m_2}\right|$$
>
> 대입하면:
>
> $$
> \begin{align}
> \tan\theta &= \left|\frac{3 - (-2)}{1 + 3 \times (-2)}\right| \\
> &= \left|\frac{5}{1 - 6}\right| \\
> &= \left|\frac{5}{-5}\right| \\
> &= |-1| = 1
> \end{align}
> $$
>
> 따라서 $\tan\theta = 1$이고,
>
> $\sec^2\theta$는 삼각함수 항등식 $1 + \tan^2\theta = \sec^2\theta$을 이용하면:
> $$\sec^2\theta = 1 + \tan^2\theta = 1 + 1^2 = 2$$

---

### 예제 48

두 직선 $y = mx + 1$과 $y = \dfrac{1}{3}x + 4$가 이루는 예각 $\theta$의 크기가 $\dfrac{\pi}{4}$일 때, 상수 $m$의 값을 구하여라.

> [!summary]- 풀이
> 두 직선의 기울기는 $m_1 = m$, $m_2 = \frac{1}{3}$이다.
>
> $\theta = \frac{\pi}{4}$이므로 $\tan\theta = \tan\frac{\pi}{4} = 1$
>
> 두 직선이 이루는 예각 공식:
> $$\tan\theta = \left|\frac{m_1 - m_2}{1 + m_1 m_2}\right|$$
>
> 대입하면:
> $$1 = \left|\frac{m - \frac{1}{3}}{1 + m \cdot \frac{1}{3}}\right|$$
>
> 절댓값을 풀면 두 경우:
>
> **경우 1:** $\dfrac{m - \frac{1}{3}}{1 + \frac{m}{3}} = 1$
>
> $$
> \begin{align}
> m - \frac{1}{3} &= 1 + \frac{m}{3} \\
> m - \frac{m}{3} &= 1 + \frac{1}{3} \\
> \frac{2m}{3} &= \frac{4}{3} \\
> m &= 2
> \end{align}
> $$
>
> **경우 2:** $\dfrac{m - \frac{1}{3}}{1 + \frac{m}{3}} = -1$
>
> $$
> \begin{align}
> m - \frac{1}{3} &= -1 - \frac{m}{3} \\
> m + \frac{m}{3} &= -1 + \frac{1}{3} \\
> \frac{4m}{3} &= -\frac{2}{3} \\
> m &= -\frac{1}{2}
> \end{align}
> $$
>
> 따라서 $m = 2$ 또는 $m = -\dfrac{1}{2}$

---

## 3. 배각공식

### Thm (15): 배각공식

#### (1) 2배각 공식

**사인:**
$$\sin 2\theta = 2\sin\theta\cos\theta = \frac{2\tan\theta}{1+\tan^2\theta}$$

**코사인:**
$$\cos 2\theta = \cos^2\theta - \sin^2\theta = 2\cos^2\theta - 1 = 1 - 2\sin^2\theta = \frac{1-\tan^2\theta}{1+\tan^2\theta}$$

**탄젠트:**
$$\tan 2\theta = \frac{2\tan\theta}{1-\tan^2\theta}$$

**유도 과정:**

- $\sin 2\theta = \sin(\theta + \theta) = \sin\theta\cos\theta + \cos\theta\sin\theta = 2\sin\theta\cos\theta$
- $\cos 2\theta = \cos(\theta + \theta) = \cos\theta\cos\theta - \sin\theta\sin\theta = \cos^2\theta - \sin^2\theta$
- $\tan 2\theta = \tan(\theta + \theta) = \dfrac{\tan\theta + \tan\theta}{1 - \tan\theta\tan\theta} = \dfrac{2\tan\theta}{1-\tan^2\theta}$

#### (2) 3배각 공식

**사인:**
$$\sin 3\theta = 3\sin\theta - 4\sin^3\theta$$

**코사인:**
$$\cos 3\theta = 4\cos^3\theta - 3\cos\theta$$

**유도 과정:**

- $\sin 3\theta = \sin(2\theta + \theta)$를 덧셈정리로 전개 후 $\sin(2\theta)\;\cos(2\theta)$는 2배각공식 적용
- $\cos 3\theta = \cos(2\theta + \theta)$를 덧셈정리로 전개 후 $\sin(2\theta)\;\cos(2\theta)$는 2배각공식 적용

#### (3) 반각 공식

**사인의 제곱:**
$$\sin^2\frac{\theta}{2} = \frac{1-\cos\theta}{2}$$

**코사인의 제곱:**
$$\cos^2\frac{\theta}{2} = \frac{1+\cos\theta}{2}$$

**탄젠트의 제곱:**
$$\tan^2\frac{\theta}{2} = \frac{1-\cos\theta}{1+\cos\theta}$$

**유도 과정:**

- $\cos 2\theta = 1 - 2\sin^2\theta$에서 $\theta$를 $\frac{\theta}{2}$로 치환
- $\cos 2\theta = 2\cos^2\theta - 1$에서 $\theta$를 $\frac{\theta}{2}$로 치환
- $\tan^2\frac{\theta}{2} = \dfrac{\sin^2\frac{\theta}{2}}{\cos^2\frac{\theta}{2}}$를 이용

---

## 4. 배각공식의 의미

### 기하학적 해석

**2배각:**

- 각도가 2배가 될 때 삼각함수 값의 변화
- $\sin 2\theta$는 단위원에서 각 $2\theta$에 대응하는 $y$ 좌표

**반각:**

- 각도가 절반이 될 때 삼각함수 값의 관계
- $\cos\theta$를 알면 $\sin\frac{\theta}{2}$와 $\cos\frac{\theta}{2}$를 구할 수 있음

### 실용적 활용

1. **복잡한 각도 계산**: $\sin 30° = \frac{1}{2}$를 이용하여 $\sin 15°$, $\sin 60°$ 계산
2. **삼각방정식 해결**: $\sin 2x = \cos x$ 형태의 방정식
3. **적분 계산**: $\int \sin^2 x \, dx$ 계산 시 반각공식 활용
4. **물리학 응용**: 진동, 파동 현상의 주기 변환

---

## 연습문제

1. $\alpha + \beta = \frac{\pi}{3}$일 때, $\sin^2\alpha + \sin^2\beta$의 값을 구하시오.

2. 두 직선 $y = 2x - 1$과 $y = -\frac{1}{2}x + 3$이 이루는 예각을 구하시오.

3. $\cos\theta = \frac{3}{5}$일 때, $\sin 2\theta$와 $\cos 2\theta$의 값을 구하시오.

4. $\tan\frac{\pi}{8}$의 값을 구하시오. (힌트: 반각공식 사용)

---

## 관련 주제

- [[08-advanced-trigonometry-1|심화삼각함수(1) - 덧셈정리]]
- [[10-advanced-trigonometry-3|심화삼각함수(3) - 배각공식 문제풀이]]
- [[11-advanced-trigonometry-4|심화삼각함수(4) - 기타공식]]

---

## 학습 포인트

1. **정삼각형 응용**: 특수각 관계($\frac{\pi}{2}$, $\frac{\pi}{4}$, $\frac{3\pi}{4}$)에서의 삼각함수 성질을 이해하고 활용할 수 있다.

2. **두 직선의 예각**: 두 직선의 기울기로부터 이루는 각을 구하는 공식을 이해하고, 실제 문제에 적용할 수 있다.

3. **2배각 공식**: $\sin 2\theta$, $\cos 2\theta$, $\tan 2\theta$의 여러 형태를 외우고, 상황에 맞게 선택하여 사용할 수 있다.

4. **반각 공식**: $\cos\theta$를 이용하여 $\sin\frac{\theta}{2}$와 $\cos\frac{\theta}{2}$를 구할 수 있으며, 이를 활용하여 특수각의 값을 계산할 수 있다.

5. **3배각 공식**: 고차 다항식 형태의 공식을 이해하고, 필요시 유도할 수 있다.
