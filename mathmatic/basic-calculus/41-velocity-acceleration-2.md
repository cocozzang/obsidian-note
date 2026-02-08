---
id: 7e4d9b3f-2c8a-4f1e-9b6d-8a3e5c7f4b2a
aliases:
  - 속도, 가속도와 미분(2)
  - 평면운동
  - 벡터의 미분
  - 공간운동
tags:
  - 속도
  - 가속도
  - 미분
  - 평면운동
  - 공간운동
  - 벡터
  - 내적
  - 속력
  - 관련변화율
pages: 122-124
subject: 대학기초수학
title: 속도, 가속도와 미분(2) - 평면운동
topics:
  - 평면운동의 속도와 가속도
  - 벡터의 크기와 내적
  - 속력 계산
  - 공간운동
  - 수직 조건
---

# 속도, 가속도와 미분(2) - 평면운동

## Thm 41: 속도와 가속도의 미분 (평면운동)

좌표평면 위를 움직이는 점 $P(x, y)$가 시각 $t$에 대한 함수 $x = f(t)$, $y = g(t)$로 나타내어질 때:

### ① 속도 벡터 (Velocity Vector)

$$\vec{v} = \left(\frac{dx}{dt}, \frac{dy}{dt}\right) = (f'(t), g'(t))$$

### ② 속력 (Speed)

$$|\vec{v}| = \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} = \sqrt{\{f'(t)\}^2 + \{g'(t)\}^2}$$

### ③ 가속도 벡터 (Acceleration Vector)

$$\vec{a} = \left(\frac{d^2x}{dt^2}, \frac{d^2y}{dt^2}\right) = (f''(t), g''(t))$$

### ④ 가속도의 크기

$$|\vec{a}| = \sqrt{\left(\frac{d^2x}{dt^2}\right)^2 + \left(\frac{d^2y}{dt^2}\right)^2} = \sqrt{\{f''(t)\}^2 + \{g''(t)\}^2}$$

---

## 벡터의 기본 성질

$\vec{a} = (a_1, a_2)$, $\vec{b} = (b_1, b_2)$일 때:

### ① 벡터의 크기

$$|\vec{a}| = \sqrt{a_1^2 + a_2^2}, \quad |\vec{b}| = \sqrt{b_1^2 + b_2^2}$$

### ② 내적 (Dot Product)

$$\vec{a} \cdot \vec{b} = a_1b_1 + a_2b_2$$

### ③ 수직 조건

$$\vec{a} \perp \vec{b} \iff \vec{a} \cdot \vec{b} = 0$$

---

## 예제

### 예제 261

좌표평면 위의 점 $P(x, y)$의 시각 $t$에서의 좌표가 $x = \sin t + \cos t$, $y = 2\cos t$로 주어질 때, 시각 $t = \frac{\pi}{3}$에서의 **속력**과 **가속도의 크기**를 각각 구하여라.

> [!summary]- 풀이
> **Step 1**: 위치 벡터 정의
> 
> $$\vec{r}(t) = (x, y) = (\sin t + \cos t, 2\cos t)$$
> 
> **Step 2**: 속도 벡터 계산
> 
> $$\vec{v}(t) = \vec{r}'(t) = (\cos t - \sin t, -2\sin t)$$
> 
> $t = \frac{\pi}{3}$일 때:
> 
> $$\vec{v}\left(\frac{\pi}{3}\right) = \left(\cos\frac{\pi}{3} - \sin\frac{\pi}{3}, -2\sin\frac{\pi}{3}\right)$$
> 
> $$= \left(\frac{1}{2} - \frac{\sqrt{3}}{2}, -2 \cdot \frac{\sqrt{3}}{2}\right)$$
> 
> $$= \left(\frac{1-\sqrt{3}}{2}, -\sqrt{3}\right)$$
> 
> **Step 3**: 속력 계산
> 
> $$|\vec{v}| = \sqrt{\left(\frac{1-\sqrt{3}}{2}\right)^2 + (-\sqrt{3})^2}$$
> 
> $$= \sqrt{\frac{(1-\sqrt{3})^2}{4} + 3}$$
> 
> $$= \sqrt{\frac{1 - 2\sqrt{3} + 3}{4} + 3}$$
> 
> $$= \sqrt{\frac{4 - 2\sqrt{3}}{4} + \frac{12}{4}}$$
> 
> $$= \sqrt{\frac{16 - 2\sqrt{3}}{4}}$$
> 
> $$= \frac{\sqrt{16 - 2\sqrt{3}}}{2}$$
> 
> **Step 4**: 가속도 벡터 계산
> 
> $$\vec{a}(t) = \vec{r}''(t) = (-\sin t - \cos t, -2\cos t)$$
> 
> $t = \frac{\pi}{3}$일 때:
> 
> $$\vec{a}\left(\frac{\pi}{3}\right) = \left(-\sin\frac{\pi}{3} - \cos\frac{\pi}{3}, -2\cos\frac{\pi}{3}\right)$$
> 
> $$= \left(-\frac{\sqrt{3}}{2} - \frac{1}{2}, -2 \cdot \frac{1}{2}\right)$$
> 
> $$= \left(\frac{-\sqrt{3}-1}{2}, -1\right)$$
> 
> **Step 5**: 가속도의 크기
> 
> $$|\vec{a}| = \sqrt{\left(\frac{-\sqrt{3}-1}{2}\right)^2 + (-1)^2}$$
> 
> $$= \sqrt{\frac{(\sqrt{3}+1)^2}{4} + 1}$$
> 
> $$= \sqrt{\frac{3 + 2\sqrt{3} + 1}{4} + 1}$$
> 
> $$= \sqrt{\frac{4 + 2\sqrt{3} + 4}{4}}$$
> 
> $$= \sqrt{\frac{8 + 2\sqrt{3}}{4}}$$
> 
> $$= \frac{\sqrt{8 + 2\sqrt{3}}}{2}$$

---

### 예제 262

좌표평면 위를 움직이는 점 $P$의 시각 $t$에서의 위치가 $P(t - \sin t, 1 - \cos t)$일 때, 시각 $t = \frac{\pi}{6}$에서의 속도 $\vec{v}$와 가속도 $\vec{a}$의 **내적** $\vec{v} \cdot \vec{a}$를 구하시오.

> [!summary]- 풀이
> **Step 1**: 위치 벡터 정의
> 
> $$\vec{r}(t) = (t - \sin t, 1 - \cos t)$$
> 
> **Step 2**: 속도 벡터 계산
> 
> $$\vec{v}(t) = \vec{r}'(t) = (1 - \cos t, \sin t)$$
> 
> $t = \frac{\pi}{6}$일 때:
> 
> $$\vec{v}\left(\frac{\pi}{6}\right) = \left(1 - \cos\frac{\pi}{6}, \sin\frac{\pi}{6}\right)$$
> 
> $$= \left(1 - \frac{\sqrt{3}}{2}, \frac{1}{2}\right)$$
> 
> $$= \left(\frac{2-\sqrt{3}}{2}, \frac{1}{2}\right)$$
> 
> **Step 3**: 가속도 벡터 계산
> 
> $$\vec{a}(t) = \vec{r}''(t) = (\sin t, \cos t)$$
> 
> $t = \frac{\pi}{6}$일 때:
> 
> $$\vec{a}\left(\frac{\pi}{6}\right) = \left(\sin\frac{\pi}{6}, \cos\frac{\pi}{6}\right)$$
> 
> $$= \left(\frac{1}{2}, \frac{\sqrt{3}}{2}\right)$$
> 
> **Step 4**: 내적 계산
> 
> $$\vec{v} \cdot \vec{a} = \frac{2-\sqrt{3}}{2} \cdot \frac{1}{2} + \frac{1}{2} \cdot \frac{\sqrt{3}}{2}$$
> 
> $$= \frac{2-\sqrt{3}}{4} + \frac{\sqrt{3}}{4}$$
> 
> $$= \frac{2-\sqrt{3}+\sqrt{3}}{4}$$
> 
> $$= \frac{2}{4} = \frac{1}{2}$$
> 
> $$\therefore \vec{v} \cdot \vec{a} = \frac{1}{2}$$

---

### 예제 263

좌표평면 위를 움직이는 점 $P$의 위치가 $x = e^{-t}\cos\pi t$, $y = e^{-t}\sin\pi t$로 주어질 때 $t = 1$에서 점 $P$의 속력을 구하여라.

> [!summary]- 풀이
> **Step 1**: 위치 벡터 정의
> 
> $$\vec{r}(t) = (e^{-t}\cos\pi t, e^{-t}\sin\pi t)$$
> 
> **Step 2**: 속도 벡터 계산 (곱의 미분법)
> 
> $x$ 성분:
> 
> $$\frac{dx}{dt} = -e^{-t}\cos\pi t + e^{-t}(-\pi\sin\pi t)$$
> 
> $$= -e^{-t}(\cos\pi t + \pi\sin\pi t)$$
> 
> $y$ 성분:
> 
> $$\frac{dy}{dt} = -e^{-t}\sin\pi t + e^{-t}(\pi\cos\pi t)$$
> 
> $$= e^{-t}(\pi\cos\pi t - \sin\pi t)$$
> 
> 따라서:
> 
> $$\vec{v}(t) = (-e^{-t}(\cos\pi t + \pi\sin\pi t), e^{-t}(\pi\cos\pi t - \sin\pi t))$$
> 
> **Step 3**: $t = 1$에서의 속도 벡터
> 
> $t = 1$일 때: $\cos\pi = -1$, $\sin\pi = 0$
> 
> $$\vec{v}(1) = (-e^{-1}(-1 + 0), e^{-1}(\pi \cdot (-1) - 0))$$
> 
> $$= (-e^{-1} \cdot (-1), e^{-1} \cdot (-\pi))$$
> 
> $$= (e^{-1}, -\pi e^{-1})$$
> 
> $$= \left(\frac{1}{e}, -\frac{\pi}{e}\right)$$
> 
> **Step 4**: 속력 계산
> 
> $$|\vec{v}| = \sqrt{(e^{-1})^2 + (-\pi e^{-1})^2}$$
> 
> $$= \sqrt{e^{-2} + \pi^2 e^{-2}}$$
> 
> $$= \sqrt{e^{-2}(1 + \pi^2)}$$
> 
> $$= e^{-1}\sqrt{1 + \pi^2}$$
> 
> $$= \frac{\sqrt{1 + \pi^2}}{e}$$

---

### 예제 264

아래 그림과 같이 반지름의 길이가 2인 원 위를 움직이고 있는 점 $P$가 있다. 점 $P$를 $x$축 위로 정사영시킨 점 $Q$는 $x$축 위를 매초 1의 일정한 속력으로 움직이고 있다. $\angle POQ = \frac{\pi}{3}$일 때, 점 $P$의 **속력**을 구하여라.

![exer264-1|300](./images/03-calculus/exer264-1.png)

> [!summary]- 풀이
> **Step 1**: 주어진 조건
> 
> - 점 $Q$의 속력: $\frac{dx}{dt} = -1$ (음의 방향)
> - $\angle POQ = \frac{\pi}{3}$일 때, 점 $P$의 좌표:
> 
> $$P = \left(2\cos\frac{\pi}{3}, 2\sin\frac{\pi}{3}\right) = (1, \sqrt{3})$$
> 
> **Step 2**: 점 $P$의 위치 함수
> 
> $$P(\theta) = (2\cos\theta, 2\sin\theta)$$
> 
> **Step 3**: $x$ 좌표의 변화율로부터 $\frac{d\theta}{dt}$ 구하기
> 
> $$\frac{dx}{dt} = \frac{d}{dt}(2\cos\theta) = -2\sin\theta \cdot \frac{d\theta}{dt}$$
> 
> $\theta = \frac{\pi}{3}$일 때:
> 
> $$-1 = -2\sin\frac{\pi}{3} \cdot \frac{d\theta}{dt}$$
> 
> $$-1 = -2 \cdot \frac{\sqrt{3}}{2} \cdot \frac{d\theta}{dt}$$
> 
> $$-1 = -\sqrt{3} \cdot \frac{d\theta}{dt}$$
> 
> $$\frac{d\theta}{dt} = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$$
> 
> **Step 4**: $y$ 좌표의 변화율
> 
> $$\frac{dy}{dt} = \frac{d}{dt}(2\sin\theta) = 2\cos\theta \cdot \frac{d\theta}{dt}$$
> 
> $\theta = \frac{\pi}{3}$일 때:
> 
> $$\frac{dy}{dt} = 2\cos\frac{\pi}{3} \cdot \frac{\sqrt{3}}{3}$$
> 
> $$= 2 \cdot \frac{1}{2} \cdot \frac{\sqrt{3}}{3}$$
> 
> $$= \frac{\sqrt{3}}{3}$$
> 
> **Step 5**: 속도 벡터와 속력
> 
> $$\vec{v} = \left(-1, \frac{\sqrt{3}}{3}\right)$$
> 
> $$|\vec{v}| = \sqrt{(-1)^2 + \left(\frac{\sqrt{3}}{3}\right)^2}$$
> 
> $$= \sqrt{1 + \frac{3}{9}}$$
> 
> $$= \sqrt{1 + \frac{1}{3}}$$
> 
> $$= \sqrt{\frac{4}{3}}$$
> 
> $$= \frac{2}{\sqrt{3}} = \frac{2\sqrt{3}}{3}$$

---

### 예제 265

공간 위를 움직이는 점 $P$의 시각 $t$에서의 위치가 $(1 + t^3, t, \sin 2t)$일 때 시각 $t = \frac{\pi}{6}$에서의 속력을 구하여라.

> [!summary]- 풀이
> **Step 1**: 위치 벡터 정의 (3차원)
> 
> $$\vec{r}(t) = (f(t), g(t), h(t)) = (1 + t^3, t, \sin 2t)$$
> 
> **Step 2**: 속도 벡터 계산
> 
> $$\vec{v}(t) = \vec{r}'(t) = (f'(t), g'(t), h'(t))$$
> 
> $$= (3t^2, 1, 2\cos 2t)$$
> 
> **Step 3**: $t = \frac{\pi}{6}$에서의 속도 벡터
> 
> $$\vec{v}\left(\frac{\pi}{6}\right) = \left(3 \cdot \frac{\pi^2}{36}, 1, 2\cos\frac{\pi}{3}\right)$$
> 
> $$= \left(\frac{\pi^2}{12}, 1, 2 \cdot \frac{1}{2}\right)$$
> 
> $$= \left(\frac{\pi^2}{12}, 1, 1\right)$$
> 
> **Step 4**: 속력 계산 (3차원)
> 
> $$|\vec{v}| = \sqrt{\left(\frac{\pi^2}{12}\right)^2 + 1^2 + 1^2}$$
> 
> $$= \sqrt{\frac{\pi^4}{144} + 1 + 1}$$
> 
> $$= \sqrt{\frac{\pi^4}{144} + 2}$$
> 
> $$= \sqrt{\frac{\pi^4 + 288}{144}}$$

---

### 예제 266

공간 위를 움직이는 점 $P$의 시각 $t$에서의 위치가 $(3\cos t, 3\sin t, t^2)$일 때 다음 물음에 답하여라. (단, $0 \le t \le 4\pi$)

(1) 속도와 가속도 벡터를 구하여라.
(2) 임의의 시각 $t$에서 점 $P$의 속력을 구하여라.
(3) 점 $P$의 가속도가 속도와 수직일 때 시각 $t$를 구하여라.

> [!summary]- 풀이
> **Step 1**: 위치 벡터 정의
> 
> $$\vec{r}(t) = (3\cos t, 3\sin t, t^2)$$
> 
> **(1) 속도와 가속도 벡터**
> 
> 속도 벡터:
> 
> $$\vec{v}(t) = \vec{r}'(t) = (-3\sin t, 3\cos t, 2t)$$
> 
> 가속도 벡터:
> 
> $$\vec{a}(t) = \vec{r}''(t) = (-3\cos t, -3\sin t, 2)$$
> 
> **(2) 임의의 시각 $t$에서의 속력**
> 
> $$|\vec{v}(t)| = \sqrt{(-3\sin t)^2 + (3\cos t)^2 + (2t)^2}$$
> 
> $$= \sqrt{9\sin^2 t + 9\cos^2 t + 4t^2}$$
> 
> $$= \sqrt{9(\sin^2 t + \cos^2 t) + 4t^2}$$
> 
> $$= \sqrt{9 + 4t^2}$$
> 
> **(3) 가속도가 속도와 수직일 때**
> 
> 수직 조건: $\vec{v} \cdot \vec{a} = 0$
> 
> $$\vec{v} \cdot \vec{a} = (-3\sin t)(-3\cos t) + (3\cos t)(-3\sin t) + (2t)(2)$$
> 
> $$= 9\sin t\cos t - 9\sin t\cos t + 4t$$
> 
> $$= 4t$$
> 
> $\vec{v} \cdot \vec{a} = 0$이므로:
> 
> $$4t = 0$$
> 
> $$t = 0$$
> 
> $$\therefore t = 0$$

---

## 연습문제

각 예제를 통해 다음 내용을 복습하시오:

1. 평면운동에서 속도와 가속도 벡터 계산
2. 속력과 가속도의 크기 계산
3. 벡터의 내적 계산
4. 곱의 미분법을 이용한 속도 계산
5. 관련 변화율 (원운동과 정사영)
6. 공간운동의 속도와 속력
7. 수직 조건 ($\vec{v} \perp \vec{a}$)

---

## 관련 주제

- [[40-velocity-acceleration-1|속도, 가속도와 미분(1)]]
- [[22-transcendental-derivative-1|초월함수의 도함수(1)]]
- [[20-derivative-applications|도함수의 활용]]

---

**학습 포인트:**

1. **평면운동**: 속도 벡터 $\vec{v} = (f'(t), g'(t))$, 가속도 벡터 $\vec{a} = (f''(t), g''(t))$
2. **속력**: 속도 벡터의 크기 $|\vec{v}| = \sqrt{(f'(t))^2 + (g'(t))^2}$
3. **내적**: $\vec{v} \cdot \vec{a} = v_1a_1 + v_2a_2$
4. **수직 조건**: $\vec{v} \perp \vec{a} \iff \vec{v} \cdot \vec{a} = 0$
5. **곱의 미분법**: $e^{-t}\cos\pi t$와 같은 합성 형태 미분 시 주의
6. **관련 변화율**: 연쇄법칙 $\frac{dy}{dt} = \frac{dy}{d\theta} \cdot \frac{d\theta}{dt}$
7. **공간운동**: 3차원 벡터 $(f(t), g(t), h(t))$로 확장
