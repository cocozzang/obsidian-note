---
id: 5a6b7c8d-9e0f-1a2b-3c4d-5e6f7a8b9c0d
aliases:
  - 삼각함수1
  - 일반각과 호도법
  - 삼각함수의 정의
tags:
  - 삼각함수
  - 호도법
  - 라디안
  - 삼각비
lecture: 큐스터디 썡기초수학
title: 5강 삼각함수(1) - 일반각과 삼각함수
topics:
  - 일반각과 호도법
  - 60분법과 호도법의 변환
  - 부채꼴의 호의 길이와 넓이
  - 삼각함수의 정의
  - 삼각함수의 부호
  - 삼각함수 사이의 관계
  - 삼각함수의 각변형 (주기공식, 음각공식, 보각공식, 여각공식)
---

# 9. 삼각함수(1)

## 01 일반각과 호도법

### (1) 일반각

**정의**: 시초선 $\overrightarrow{OX}$와 동경 $\overrightarrow{OP}$가 나타내는 양의 최소각을 $\alpha$라고 할 때, $\angle XOP$의 일반각 $\theta$는

$$\theta = 360° \times n + \alpha \quad (n\text{은 정수}, 0 \leq \alpha < 360°)$$

```
    P : 동경
   /
  /
 / α
O────────→ X : 시초선
```

**예시**:

- $45°$의 일반각: $360°n + 45°$
- $-30°$의 일반각: $360°n - 30°$ 또는 $360°n + 330°$

---

### (2) 호도법

**정의**: 호의 길이로 각을 표현하는 방법

$$\theta = \frac{l}{r} \text{ (rad)}$$

여기서 $l$은 호의 길이, $r$은 반지름

```
      r
    ←─┐
   /   │r
  /  θ │
 /______│
O   l
```

#### 1호도(radian)의 정의

반지름 = 호의 길이일 때 정의되는 각

```
    1
   ←─┐
  /   │1
 / 1  │
/_____|
  1
```

$\theta = \frac{1}{1} = 1$ (rad)

---

### (3) 60분법과 호도법의 변환

#### ① 반원(180°)의 호도법

- 반원의 호의 길이: $l = \pi r$
- 각: $\theta = \frac{l}{r} = \frac{\pi r}{r} = \pi$ (rad)

**결론**: $180° = \pi$ (rad)

따라서:
$$1° = \frac{\pi}{180} \text{ rad}$$
$$1 \text{ rad} = \frac{180°}{\pi} \approx 57°17'45''$$

#### ② 주요 각도 변환

**60분법 → 호도법**:

| 각도     | 호도법               |
| ------ | ----------------- |
| $30°$  | $\frac{\pi}{6}$   |
| $45°$  | $\frac{\pi}{4}$   |
| $60°$  | $\frac{\pi}{3}$   |
| $90°$  | $\frac{\pi}{2}$   |
| $120°$ | $\frac{2\pi}{3}$  |
| $135°$ | $\frac{3\pi}{4}$  |
| $150°$ | $\frac{5\pi}{6}$  |
| $180°$ | $\pi$             |
| $270°$ | $\frac{3\pi}{2}$  |
| $300°$ | $\frac{5\pi}{3}$  |
| $315°$ | $\frac{7\pi}{4}$  |
| $330°$ | $\frac{11\pi}{6}$ |
| $360°$ | $2\pi$            |

### 📝 예제

**예제 1**: 60분법을 호도법으로, 호도법을 60분법으로 바꾸어라.

① $30° = 30 \times \frac{\pi}{180} = \frac{\pi}{6}$ (rad)

② $120° = 120 \times \frac{\pi}{180} = \frac{2\pi}{3}$ (rad)

③ $\frac{3\pi}{2} = \frac{3\pi}{2} \times \frac{180°}{\pi} = 270°$

④ $\frac{4\pi}{3} = \frac{4\pi}{3} \times \frac{180°}{\pi} = 240°$

---

**예제 2**: $50°$를 호도법으로 나타내어라.

**풀이**:
$$50° = 50 \times \frac{\pi}{180} = \frac{50\pi}{180} = \frac{5\pi}{18}$$

---

### (4) 특수각 (계열각)

#### 30° 계열

| 각도   | $30°$           | $150°$           | $210°$           | $330°$            |
| ------ | --------------- | ---------------- | ---------------- | ----------------- |
| 호도법 | $\frac{\pi}{6}$ | $\frac{5\pi}{6}$ | $\frac{7\pi}{6}$ | $\frac{11\pi}{6}$ |

#### 45° 계열

| 각도   | $45°$           | $135°$           | $225°$           | $315°$           |
| ------ | --------------- | ---------------- | ---------------- | ---------------- |
| 호도법 | $\frac{\pi}{4}$ | $\frac{3\pi}{4}$ | $\frac{5\pi}{4}$ | $\frac{7\pi}{4}$ |

#### 60° 계열

| 각도   | $60°$           | $120°$           | $240°$           | $300°$           |
| ------ | --------------- | ---------------- | ---------------- | ---------------- |
| 호도법 | $\frac{\pi}{3}$ | $\frac{2\pi}{3}$ | $\frac{4\pi}{3}$ | $\frac{5\pi}{3}$ |

---

### (5) 삼각비와 특수각의 삼각비

#### ① 직각삼각형의 삼각비

```
      c
     /|
    / |
   /  |b
  /   |
 /θ___|
a
```

- $\sin\theta = \frac{b}{c}$ (대변/빗변)
- $\cos\theta = \frac{a}{c}$ (밑변/빗변)
- $\tan\theta = \frac{b}{a}$ (대변/밑변)
- $\csc\theta = \frac{c}{b}$ (빗변/대변)
- $\sec\theta = \frac{c}{a}$ (빗변/밑변)
- $\cot\theta = \frac{a}{b}$ (밑변/대변)

#### ② 특수각의 삼각비

**30° ($\frac{\pi}{6}$)**

```
    2
   /|
  / |
 /30°|1
/_____|
  √3
```

- $\sin 30° = \sin\frac{\pi}{6} = \frac{1}{2}$
- $\cos 30° = \cos\frac{\pi}{6} = \frac{\sqrt{3}}{2}$
- $\tan 30° = \tan\frac{\pi}{6} = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$

**45° ($\frac{\pi}{4}$)**

```
   √2
   /|
  / |
 /45°|1
/_____|
   1
```

- $\sin 45° = \sin\frac{\pi}{4} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$
- $\cos 45° = \cos\frac{\pi}{4} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$
- $\tan 45° = \tan\frac{\pi}{4} = 1$

**60° ($\frac{\pi}{3}$)**

```
    2
   /|
  / |
 /60°|√3
/_____|
   1
```

- $\sin 60° = \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}$
- $\cos 60° = \cos\frac{\pi}{3} = \frac{1}{2}$
- $\tan 60° = \tan\frac{\pi}{3} = \sqrt{3}$

#### ③ 특수각 삼각비 표

| 각           | $0°$ $(0)$ | $30°$ $\left(\frac{\pi}{6}\right)$ | $45°$ $\left(\frac{\pi}{4}\right)$ | $60°$ $\left(\frac{\pi}{3}\right)$ | $90°$ $\left(\frac{\pi}{2}\right)$ |
| ------------ | ---------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| $\sin\theta$ | $0$        | $\frac{1}{2}$                      | $\frac{\sqrt{2}}{2}$               | $\frac{\sqrt{3}}{2}$               | $1$                                |
| $\cos\theta$ | $1$        | $\frac{\sqrt{3}}{2}$               | $\frac{\sqrt{2}}{2}$               | $\frac{1}{2}$                      | $0$                                |
| $\tan\theta$ | $0$        | $\frac{\sqrt{3}}{3}$               | $1$                                | $\sqrt{3}$                         | $\infty$                           |

---

### (6) 부채꼴의 호의 길이와 넓이

반지름의 길이가 $r$, 중심각의 크기가 $\theta$ (라디안)인 부채꼴에서

```
    ╱─╲
   ╱ θ ╲
  ╱     ╲
 ╱───l───╲
  r     r
```

① **호의 길이**: $l = r\theta$

② **부채꼴 넓이**: $S = \frac{1}{2}r^2\theta = \frac{1}{2}rl$

### 📝 예제

**예제 1**: 반지름이 6cm, 중심각이 $\frac{2\pi}{3}$인 부채꼴의 호의 길이와 넓이를 구하여라.

**풀이**:

- 호의 길이: $l = r\theta = 6 \times \frac{2\pi}{3} = 4\pi$ (cm)
- 넓이: $S = \frac{1}{2}r^2\theta = \frac{1}{2} \times 6^2 \times \frac{2\pi}{3} = \frac{1}{2} \times 36 \times \frac{2\pi}{3} = 12\pi$ (cm²)

또는: $S = \frac{1}{2}rl = \frac{1}{2} \times 6 \times 4\pi = 12\pi$ (cm²)

---

**예제 2**: 호의 길이가 $8\pi$cm, 넓이가 $48\pi$cm²인 부채꼴의 반지름과 중심각을 구하여라.

**풀이**:
$$S = \frac{1}{2}rl$$
$$48\pi = \frac{1}{2} \times r \times 8\pi$$
$$48\pi = 4\pi r$$
$$r = 12 \text{ (cm)}$$

$$l = r\theta$$
$$8\pi = 12\theta$$
$$\theta = \frac{8\pi}{12} = \frac{2\pi}{3} \text{ (rad)}$$

---

## 02 삼각함수의 정의

### (1) 삼각함수의 정의

좌표평면에서 동경이 나타내는 각의 크기를 $\theta$, 동경과 반지름의 길이가 $r$인 원과의 교점을 $P(x, y)$라고 할 때:

```
      y
      |
      |P(x,y)
      |/|
      |/ |y
      |/θ_|_____ x
    O   x   r
```

① $\sin\theta = \frac{y}{r}$을 $\sin\theta$ 값으로 정의
② $\cos\theta = \frac{x}{r}$을 $\cos\theta$ 값으로 정의
③ $\tan\theta = \frac{y}{x}$ $(x \neq 0)$을 $\tan\theta$ 값으로 정의
④ $\csc\theta = \frac{r}{y}$ $(y \neq 0)$
⑤ $\sec\theta = \frac{r}{x}$ $(x \neq 0)$
⑥ $\cot\theta = \frac{x}{y}$ $(y \neq 0)$

**단위원 ($r = 1$)에서**:

- $\sin\theta = y$
- $\cos\theta = x$
- $\tan\theta = \frac{y}{x}$

---

### (2) 삼각함수의 부호

사분면에 따른 삼각함수의 부호:

```
        y
        |
   2분면 | 1분면
  sin+  | sin+
  cos-  | cos+
  tan-  | tan+
________|________x
   3분면 | 4분면
  sin-  | sin-
  cos-  | cos+
  tan+  | tan-
        |
```

**외우기**: "**1 All, 2 Sin, 3 Tan, 4 Cos**" (양수인 것)

| 사분면 | $\sin$ | $\cos$ | $\tan$ |
| ------ | ------ | ------ | ------ |
| 1분면  | $+$    | $+$    | $+$    |
| 2분면  | $+$    | $-$    | $-$    |
| 3분면  | $-$    | $-$    | $+$    |
| 4분면  | $-$    | $+$    | $-$    |

### 📝 예제

**예제 1**: 원점과 점 $(3, 4)$를 잇는 선분을 동경으로 하는 각을 $\theta$라 할 때 $\sin\theta$, $\cos\theta$, $\tan\theta$를 구하여라.

**풀이**:

- $x = 3$, $y = 4$
- $r = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$

$$\sin\theta = \frac{y}{r} = \frac{4}{5}$$
$$\cos\theta = \frac{x}{r} = \frac{3}{5}$$
$$\tan\theta = \frac{y}{x} = \frac{4}{3}$$

---

**예제 2**: 원점과 점 $(-2, 3)$를 잇는 선분을 동경으로 하는 각을 $\theta$라 할 때 $\sin\theta$, $\cos\theta$, $\tan\theta$를 구하여라.

**풀이**:

- $x = -2$, $y = 3$
- $r = \sqrt{(-2)^2 + 3^2} = \sqrt{4 + 9} = \sqrt{13}$

$$\sin\theta = \frac{y}{r} = \frac{3}{\sqrt{13}} = \frac{3\sqrt{13}}{13}$$
$$\cos\theta = \frac{x}{r} = \frac{-2}{\sqrt{13}} = \frac{-2\sqrt{13}}{13}$$
$$\tan\theta = \frac{y}{x} = \frac{3}{-2} = -\frac{3}{2}$$

---

### (3) 삼각함수 사이의 관계

#### ① 역수 관계

$$\csc\theta = \frac{1}{\sin\theta}, \quad \sec\theta = \frac{1}{\cos\theta}, \quad \cot\theta = \frac{1}{\tan\theta}$$

#### ② 상제 관계

$$\tan\theta = \frac{\sin\theta}{\cos\theta}, \quad \cot\theta = \frac{\cos\theta}{\sin\theta}$$

#### ③ 제곱 관계

- $\sin^2\theta + \cos^2\theta = 1$
- $\tan^2\theta + 1 = \sec^2\theta$
- $1 + \cot^2\theta = \csc^2\theta$

**증명** ($\sin^2\theta + \cos^2\theta = 1$):
$$\sin^2\theta + \cos^2\theta = \frac{y^2}{r^2} + \frac{x^2}{r^2} = \frac{x^2 + y^2}{r^2} = \frac{r^2}{r^2} = 1$$

### 📝 예제

**예제**: $\sin\theta = \frac{3}{5}$이고 $\frac{\pi}{2} < \theta < \pi$일 때, $\cos\theta$와 $\tan\theta$를 구하여라.

**풀이**:

$\sin^2\theta + \cos^2\theta = 1$에서
$$\left(\frac{3}{5}\right)^2 + \cos^2\theta = 1$$
$$\frac{9}{25} + \cos^2\theta = 1$$
$$\cos^2\theta = 1 - \frac{9}{25} = \frac{16}{25}$$
$$\cos\theta = \pm\frac{4}{5}$$

$\frac{\pi}{2} < \theta < \pi$ (2분면)에서 $\cos\theta < 0$이므로
$$\cos\theta = -\frac{4}{5}$$

$$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{\frac{3}{5}}{-\frac{4}{5}} = \frac{3}{5} \times \frac{5}{-4} = -\frac{3}{4}$$

---

## 03 삼각함수의 각변형

### (1) 주기공식: $\theta + 2\pi n$ ($n$은 정수)

$$\sin(\theta + 2\pi n) = \sin\theta$$
$$\cos(\theta + 2\pi n) = \cos\theta$$
$$\tan(\theta + \pi n) = \tan\theta$$

**이유**: 한 바퀴($2\pi$) 돌면 같은 위치로 돌아옴

---

### (2) 음각공식: $-\theta$

$$\sin(-\theta) = -\sin\theta$$
$$\cos(-\theta) = \cos\theta$$
$$\tan(-\theta) = -\tan\theta$$

**이유**: $x$축 대칭

```
      y
      |
      |P(x,y)
______|______x
      |P'(x,-y)
      |
```

---

### (3) 보각공식: $\pi \pm \theta$

$$\sin(\pi - \theta) = \sin\theta$$
$$\cos(\pi - \theta) = -\cos\theta$$
$$\tan(\pi - \theta) = -\tan\theta$$

$$\sin(\pi + \theta) = -\sin\theta$$
$$\cos(\pi + \theta) = -\cos\theta$$
$$\tan(\pi + \theta) = \tan\theta$$

**이유**: $y$축 대칭 또는 원점 대칭

---

### (4) 여각공식: $\frac{\pi}{2} \pm \theta$

$$\sin\left(\frac{\pi}{2} - \theta\right) = \cos\theta$$
$$\cos\left(\frac{\pi}{2} - \theta\right) = \sin\theta$$
$$\tan\left(\frac{\pi}{2} - \theta\right) = \cot\theta$$

$$\sin\left(\frac{\pi}{2} + \theta\right) = \cos\theta$$
$$\cos\left(\frac{\pi}{2} + \theta\right) = -\sin\theta$$
$$\tan\left(\frac{\pi}{2} + \theta\right) = -\cot\theta$$

**이유**: $y = x$ 대칭 또는 변형

---

### 각변형 공식 정리

**단계 ①**: $\frac{\pi}{2} \times$ (짝수 또는 홀수) 판단

- **짝수** ($\pm 0$, $\pm \pi$, $\pm 2\pi$, ...): 그대로
- **홀수** ($\pm\frac{\pi}{2}$, $\pm\frac{3\pi}{2}$, ...): $\sin \leftrightarrow \cos$, $\tan \leftrightarrow \cot$

**단계 ②**: 동경의 위치에 따라 부호 결정

- $\theta$를 예각으로 간주
- 각 사분면에서의 부호 결정

**기억법**: "$\cos$은 오른쪽(→), $\sin$은 위쪽(↑)"

### 📝 예제

**예제 1**: 다음을 간단히 하여라.

① $\sin\frac{7\pi}{6}$

**풀이**:
$$\sin\frac{7\pi}{6} = \sin\left(\pi + \frac{\pi}{6}\right) = -\sin\frac{\pi}{6} = -\frac{1}{2}$$

② $\cos\frac{5\pi}{4}$

**풀이**:
$$\cos\frac{5\pi}{4} = \cos\left(\pi + \frac{\pi}{4}\right) = -\cos\frac{\pi}{4} = -\frac{\sqrt{2}}{2}$$

③ $\tan\frac{5\pi}{3}$

**풀이**:
$$\tan\frac{5\pi}{3} = \tan\left(2\pi - \frac{\pi}{3}\right) = \tan\left(-\frac{\pi}{3}\right) = -\tan\frac{\pi}{3} = -\sqrt{3}$$

---

**예제 2**: 다음을 간단히 하여라.

① $\sin\frac{2\pi}{3}$

**풀이**:
$$\sin\frac{2\pi}{3} = \sin\left(\pi - \frac{\pi}{3}\right) = \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}$$

② $\cos\frac{7\pi}{6}$

**풀이**:
$$\cos\frac{7\pi}{6} = \cos\left(\pi + \frac{\pi}{6}\right) = -\cos\frac{\pi}{6} = -\frac{\sqrt{3}}{2}$$

③ $\tan\frac{3\pi}{4}$

**풀이**:
$$\tan\frac{3\pi}{4} = \tan\left(\pi - \frac{\pi}{4}\right) = -\tan\frac{\pi}{4} = -1$$

---

**예제 3**: 여각공식 활용

① $\sin\frac{5\pi}{6}$

**풀이**:

방법1 (보각공식):
$$\sin\frac{5\pi}{6} = \sin\left(\pi - \frac{\pi}{6}\right) = \sin\frac{\pi}{6} = \frac{1}{2}$$

방법2 (여각공식):
$$\sin\frac{5\pi}{6} = \sin\left(\frac{\pi}{2} + \frac{\pi}{3}\right) = \cos\frac{\pi}{3} = \frac{1}{2}$$

② $\cos\frac{7\pi}{12}$

**풀이**:
$$\cos\frac{7\pi}{12} = \cos\left(\frac{\pi}{2} + \frac{\pi}{12}\right) = -\sin\frac{\pi}{12}$$

---

## 🔑 핵심 정리

### 호도법

- $180° = \pi$ rad
- $1° = \frac{\pi}{180}$ rad
- $1$ rad $= \frac{180°}{\pi} \approx 57.3°$

### 부채꼴

- 호의 길이: $l = r\theta$
- 넓이: $S = \frac{1}{2}r^2\theta = \frac{1}{2}rl$

### 삼각함수의 정의

- $\sin\theta = \frac{y}{r}$, $\cos\theta = \frac{x}{r}$, $\tan\theta = \frac{y}{x}$

### 삼각함수의 부호

- 1분면: All 양수
- 2분면: Sin만 양수
- 3분면: Tan만 양수
- 4분면: Cos만 양수

### 삼각함수 사이의 관계

- $\sin^2\theta + \cos^2\theta = 1$
- $\tan^2\theta + 1 = \sec^2\theta$
- $\tan\theta = \frac{\sin\theta}{\cos\theta}$

### 각변형 공식

- 주기: $\sin(\theta + 2\pi) = \sin\theta$
- 음각: $\sin(-\theta) = -\sin\theta$, $\cos(-\theta) = \cos\theta$
- 보각: $\sin(\pi - \theta) = \sin\theta$, $\cos(\pi - \theta) = -\cos\theta$
- 여각: $\sin(\frac{\pi}{2} - \theta) = \cos\theta$

---

## 📚 연습문제

### 문제 1

호의 길이가 $6\pi$, 중심각이 $\frac{2\pi}{3}$인 부채꼴의 반지름과 넓이를 구하여라.

---

### 문제 2

$\cos\theta = -\frac{5}{13}$이고 $\pi < \theta < \frac{3\pi}{2}$일 때, $\sin\theta$와 $\tan\theta$를 구하여라.

---

### 문제 3

다음 값을 구하여라.

(1) $\sin\frac{11\pi}{6}$
(2) $\cos\frac{4\pi}{3}$
(3) $\tan\frac{5\pi}{4}$

---

### 문제 4

$\sin\theta + \cos\theta = \frac{1}{2}$일 때, $\sin\theta\cos\theta$의 값을 구하여라.

**힌트**: $(\sin\theta + \cos\theta)^2 = \sin^2\theta + 2\sin\theta\cos\theta + \cos^2\theta$

---

## 🔗 관련 링크

- [[3-shape|3강: 도형의 이동, 함수와 그래프]] - 각도와 좌표
- [[6-trigonometry2|6강: 삼각함수(2)]] - 삼각함수의 그래프
- [[8-trigonometry-law|8강: 사인법칙과 코사인법칙]]

---

_다음 챕터: [[6-trigonometry2|6강 삼각함수(2) - 그래프와 방정식]]_
