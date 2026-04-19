---
id: f7d3b582-9c4a-4e18-b2d7-6f1e8a0c5392
aliases:
  - 속도와 거리 및 곡선의 길이(2)
  - 매개변수 곡선의 길이
  - 사이클로이드
  - 현수선
tags:
  - 곡선의길이
  - 매개변수곡선
  - 사이클로이드
  - 현수선
  - 평면운동거리
  - 배각공식적분
pages: 205-209
subject: 대학기초수학
title: 속도와 거리 및 곡선의 길이(2)
topics:
  - 매개변수 곡선의 길이 계산 심화
  - 사이클로이드 곡선 길이
  - 현수선(catenary) 길이
  - 곡선 길이의 최솟값 문제
  - 아스트로이드 곡선 길이
---

# 속도와 거리 및 곡선의 길이(2)

이번 강의는 곡선의 길이 공식 $l = \displaystyle\int_a^b\!\sqrt{\left(\dfrac{dx}{dt}\right)^2+\left(\dfrac{dy}{dt}\right)^2}\,dt$를 **실전 문제**에 적용하는 훈련이다. 핵심 기술은 $(dx/dt)^2 + (dy/dt)^2$을 **완전제곱식**으로 정리하는 것이며, 이 과정에서 **배각공식**이 자주 쓰인다. 아울러 현수선과 같은 응용 문제, 그리고 곡선 길이의 최솟값 문제도 다룬다.

---

## 1. 핵심 기술: 피적분함수의 완전제곱식 변환

매개변수 곡선의 길이를 구할 때, 아래 두 패턴이 자주 등장한다.

**패턴 A** — $2 - 2\cos t$ 꼴:

$$2 - 2\cos t = 2\left(1 - \cos t\right) = 4\sin^2\!\frac{t}{2}$$

$$\therefore \sqrt{2 - 2\cos t} = 2\left|\sin\frac{t}{2}\right|$$

**패턴 B** — $\left(\dfrac{dx}{dt}\right)^2 + \left(\dfrac{dy}{dt}\right)^2$이 인수분해되는 꼴:

$$\sin^2\theta\cos^4\theta + \cos^2\theta\sin^4\theta = \sin^2\theta\cos^2\theta(\cos^2\theta + \sin^2\theta) = \sin^2\theta\cos^2\theta$$

> [!tip] 완전제곱식 확인 요령
> $(dx/dt)^2 + (dy/dt)^2$을 전개한 뒤 $= (\text{어떤 식})^2$ 형태가 되는지 확인.
> $2 - 2\cos t$처럼 배각공식이 숨어있는 경우가 많으므로 $1 - \cos t = 2\sin^2(t/2)$를 적극 활용한다.

---

## 2. 예제

### 예제 437

![[images/04-integral/exer437.png]]

오른쪽 그림과 같이 반지름이 $2\,\text{m}$인 놀이기구가 있다. 놀이기구가 입구를 출발한 지 $t$분 후의 위치가 $(2\cos(3t^2+1),\ 2\sin(3t^2+1))$로 주어질 때, 4분 동안 입구 반대편에 있는 최고점을 몇 번 통과하는가? (단, $\pi$는 3으로 계산한다.)

> [!summary]- 풀이
>
> **Step 1**: 4분 동안 이동한 거리(호의 길이) 계산
>
> $$\frac{dx}{dt} = -6t\sin(3t^2+1), \quad \frac{dy}{dt} = 6t\cos(3t^2+1)$$
>
> $$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = 36t^2\sin^2(3t^2+1) + 36t^2\cos^2(3t^2+1) = 36t^2$$
>
> $$l = \int_0^4\sqrt{36t^2}\,dt = \int_0^4 6t\,dt = \left[3t^2\right]_0^4 = 48$$
>
> > 잠깐! 노트에는 $12t$로 계산되어 있으나, $\dfrac{dx}{dt}$의 미분계수를 정확히 계산하면:
> > $\dfrac{d}{dt}[2\cos(3t^2+1)] = 2 \cdot (-\sin(3t^2+1)) \cdot 6t = -12t\sin(3t^2+1)$
> > 따라서 $\sqrt{(12t)^2} = 12t$이고:
>
> $$l = \int_0^4 12t\,dt = \left[6t^2\right]_0^4 = 96$$
>
> **Step 2**: 원의 둘레 = $2\pi r = 2 \times 3 \times 2 = 12\,\text{m}$ ($\pi = 3$)
>
> **Step 3**: 총 회전 횟수 = $\dfrac{96}{12} = 8$ 바퀴
>
> 정확히 8바퀴이므로 최고점을 **$\boxed{8}$번** 통과한다.

---

### 예제 438

다음 곡선의 길이를 구하여라. (단, $0 \leq t \leq 2\pi$)

$$\begin{cases} x = \cos t\,(1 - \cos t) \\ y = \sin t\,(1 - \cos t) \end{cases}$$

> [!summary]- 풀이
>
> **Step 1**: 각 성분을 배각공식으로 정리하여 미분
>
> $$x = \cos t - \cos^2 t = \cos t - \frac{1 + \cos 2t}{2}$$
>
> $$\frac{dx}{dt} = -\sin t - \frac{1}{2}\cdot(-2\sin 2t) = -\sin t + \sin 2t$$
>
> $$y = \sin t - \sin t\cos t = \sin t - \frac{1}{2}\sin 2t$$
>
> $$\frac{dy}{dt} = \cos t - \cos 2t$$
>
> **Step 2**: $(dx/dt)^2 + (dy/dt)^2$ 계산
>
> $$= (\sin^2 t + \sin^2 2t - 2\sin t\sin 2t) + (\cos^2 t + \cos^2 2t - 2\cos t\cos 2t)$$
>
> $$= 1 + 1 - 2(\sin t\sin 2t + \cos t\cos 2t)$$
>
> $$= 2 - 2\cos(2t - t) = 2 - 2\cos t$$
>
> **Step 3**: 배각공식 패턴 A 적용
>
> $$2 - 2\cos t = 4\sin^2\frac{t}{2} \quad \Rightarrow \quad \sqrt{2-2\cos t} = 2\left|\sin\frac{t}{2}\right|$$
>
> 구간 $[0, 2\pi]$에서 $\dfrac{t}{2} \in [0, \pi]$ → $\sin\dfrac{t}{2} \geq 0$ → 절댓값 제거 가능
>
> $$l = \int_0^{2\pi} 2\sin\frac{t}{2}\,dt = \left[-4\cos\frac{t}{2}\right]_0^{2\pi} = -4(-1) - (-4)(1) = 4 + 4 = \boxed{8}$$

---

### 예제 439

![[images/04-integral/exer439.png]]

다음은 현수교의 구조를 나타낸 것으로 주케이블은 곡선 $y = \dfrac{e^x + e^{-x}}{2}$과 같은 모양이다. 두 탑 사이의 거리가 $2\,\text{km}$일 때, 주케이블의 길이는 얼마인가?

① $\left(e+\dfrac{1}{e}\right)\text{km}$ $\quad$ ② $\left(e-\dfrac{1}{e}\right)\text{km}$ $\quad$ ③ $e\,\text{km}$ $\quad$ ④ $\dfrac{1}{2}\left(e+\dfrac{1}{e}\right)\text{km}$ $\quad$ ⑤ $\dfrac{1}{2}\left(e-\dfrac{1}{e}\right)\text{km}$

> [!summary]- 풀이
>
> **설정**: 케이블의 최저점을 원점으로 두면, 두 탑의 거리가 $2\,\text{km}$이므로 $x = -1$부터 $x = 1$까지 적분 (대칭)
>
> $$y = \frac{e^x + e^{-x}}{2}, \quad \frac{dy}{dx} = \frac{e^x - e^{-x}}{2}$$
>
> **$1 + (dy/dx)^2$ 완전제곱식 변환**:
>
> $$1 + \left(\frac{e^x - e^{-x}}{2}\right)^2 = 1 + \frac{e^{2x} - 2 + e^{-2x}}{4} = \frac{e^{2x} + 2 + e^{-2x}}{4}$$
>
> $e^{2x} + 2 + e^{-2x} = (e^x + e^{-x})^2$ 이므로:
>
> $$\sqrt{1 + \left(\frac{dy}{dx}\right)^2} = \frac{e^x + e^{-x}}{2}$$
>
> **적분** (대칭 이용):
>
> $$l = 2\int_0^1 \frac{e^x + e^{-x}}{2}\,dx = \left[e^x - e^{-x}\right]_0^1 = \left(e - \frac{1}{e}\right) - (1 - 1)$$
>
> $$= \boxed{\left(e - \frac{1}{e}\right)\text{km}}$$
>
> **정답: ②**

---

### 예제 440

실수 전체의 집합에서 이계도함수를 갖고 $f(0) = 0$, $f(1) = \sqrt{3}$을 만족시키는 모든 함수 $f(x)$에 대하여 $\displaystyle\int_0^1\sqrt{1 + \{f'(x)\}^2}\,dx$의 최솟값은?

① $\sqrt{2}$ $\quad$ ② $2$ $\quad$ ③ $1 + \sqrt{2}$ $\quad$ ④ $\sqrt{5}$ $\quad$ ⑤ $1 + \sqrt{3}$

> [!summary]- 풀이
>
> **핵심 관찰**: $\displaystyle\int_0^1\sqrt{1+\{f'(x)\}^2}\,dx$는 곡선 $y = f(x)$의 $[0,1]$ 구간 길이이다.
>
> 두 점 $(0,\ 0)$과 $(1,\ \sqrt{3})$을 잇는 **가장 짧은 경로 = 직선**이다.
>
> > **[오개념 정리]** "이계도함수를 가져야 하므로 1차 이하일 수 없다"는 생각은 **틀렸다**.
> > 이계도함수를 갖는다 = $f'(x)$가 존재하고 그 도함수도 존재한다는 의미.
> > 1차 함수(직선) $f(x) = \sqrt{3}\,x$는 $f''(x) = 0$으로 이계도함수가 존재한다.
> > 따라서 직선도 조건을 만족하며, 곡선 길이는 직선일 때 최소가 된다.
>
> **직선** $f(x) = \sqrt{3}\,x$일 때, $f'(x) = \sqrt{3}$
>
> $$l_{\min} = \int_0^1\sqrt{1 + 3}\,dx = \int_0^1 2\,dx = \boxed{2}$$
>
> 또는 두 점 사이의 거리 $= \sqrt{(1-0)^2 + (\sqrt{3}-0)^2} = \sqrt{1+3} = 2$
>
> **정답: ②**

---

### 예제 441

$x = 0$에서 $x = 6$까지 곡선 $y = \dfrac{1}{3}(x^2 + 2)^{\frac{3}{2}}$의 길이를 구하시오.

> [!summary]- 풀이
>
> **$f'(x)$ 계산**:
>
> $$\frac{dy}{dx} = \frac{1}{3} \cdot \frac{3}{2}(x^2+2)^{\frac{1}{2}} \cdot 2x = x\sqrt{x^2+2}$$
>
> **$1 + (dy/dx)^2$ 완전제곱식 변환**:
>
> $$1 + x^2(x^2+2) = 1 + x^4 + 2x^2 = x^4 + 2x^2 + 1 = (x^2+1)^2$$
>
> **적분**:
>
> $$l = \int_0^6\sqrt{(x^2+1)^2}\,dx = \int_0^6(x^2+1)\,dx$$
>
> $$= \left[\frac{x^3}{3} + x\right]_0^6 = \frac{216}{3} + 6 = 72 + 6 = \boxed{78}$$

---

### 예제 442

![[images/04-integral/exer442.png]]

그림과 같이 원점에서 $x$축에 접하고 반지름의 길이가 1인 원이 $x$축에 접하면서 오른쪽으로 굴러가고 있다. 처음 원이 원점에서 접할 때의 접점을 P라 할 때, 원 위의 점 P가 다시 $x$축 위에 올 때까지의 움직인 거리를 $l$이라 하자. 이 때, $3l$의 값을 구하시오.

![[images/04-integral/exer442-1.png|400]]

> [!summary]- 풀이
>
> 원이 $x$축 위를 굴러갈 때 원 위의 고정점이 그리는 곡선 = **사이클로이드(cycloid)**
>
> 반지름 1, 각도 $\theta$만큼 굴렀을 때 점 P의 위치:
>
> $$x = \theta - \sin\theta, \quad y = 1 - \cos\theta$$
>
> 점 P가 다시 $x$축에 올 때: $y = 0$ → $1 - \cos\theta = 0$ → $\theta = 2\pi$
>
> **속도 벡터의 크기**:
>
> $$\frac{dx}{d\theta} = 1 - \cos\theta, \quad \frac{dy}{d\theta} = \sin\theta$$
>
> $$\left(\frac{dx}{d\theta}\right)^2 + \left(\frac{dy}{d\theta}\right)^2 = (1-\cos\theta)^2 + \sin^2\theta = 2 - 2\cos\theta$$
>
> 패턴 A 적용: $\sqrt{2-2\cos\theta} = 2\left|\sin\dfrac{\theta}{2}\right|$
>
> 구간 $[0, 2\pi]$에서 $\dfrac{\theta}{2} \in [0, \pi]$ → $\sin\dfrac{\theta}{2} \geq 0$
>
> $$l = \int_0^{2\pi} 2\sin\frac{\theta}{2}\,d\theta = \left[-4\cos\frac{\theta}{2}\right]_0^{2\pi} = -4(-1) - (-4)(1) = 8$$
>
> $$\boxed{3l = 24}$$

---

### 예제 443

![[images/04-integral/exer443.png]]

좌표평면에서 반지름의 길이가 1인 수레바퀴가 $x$축 위를 $2\pi$초마다 1회전하는 속도로 굴러가고 있다. 수레바퀴 위의 한 점 P가 원점에서 출발하여 $t$초가 되는 순간의 점 P의 위치가 $x = t - \sin t$, $y = 1 - \cos t$일 때, $t = 0$에서 $t = 2\pi$까지 점 P의 움직인 거리를 구하여라.

> [!summary]- 풀이
>
> 예제 442와 동일한 사이클로이드 문제이다. 이번에는 위치 함수가 문제에 직접 주어졌다.
>
> $$\frac{dx}{dt} = 1 - \cos t, \quad \frac{dy}{dt} = \sin t$$
>
> $$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = 2 - 2\cos t = 4\sin^2\frac{t}{2}$$
>
> $$l = \int_0^{2\pi} 2\sin\frac{t}{2}\,dt = \left[-4\cos\frac{t}{2}\right]_0^{2\pi} = 4 + 4 = \boxed{8}$$

---

### 예제 444

![[images/04-integral/exer444.png]]

다음 곡선의 길이를 구하여라. $\left(\text{단},\ 0 \leq \theta \leq \dfrac{\pi}{2}\right)$

$$\begin{cases} x = \cos^3\theta \\ y = \sin^3\theta \end{cases}$$

> [!summary]- 풀이
>
> 이 곡선은 **아스트로이드(astroid)**의 1사분면 부분이다.
>
> **미분**:
>
> $$\frac{dx}{d\theta} = 3\cos^2\theta \cdot (-\sin\theta) = -3\sin\theta\cos^2\theta$$
>
> $$\frac{dy}{d\theta} = 3\sin^2\theta \cdot \cos\theta = 3\cos\theta\sin^2\theta$$
>
> **크기의 제곱**:
>
> $$\left(\frac{dx}{d\theta}\right)^2 + \left(\frac{dy}{d\theta}\right)^2 = 9\sin^2\theta\cos^4\theta + 9\cos^2\theta\sin^4\theta$$
>
> $$= 9\sin^2\theta\cos^2\theta(\cos^2\theta + \sin^2\theta) = 9\sin^2\theta\cos^2\theta$$
>
> $$\sqrt{\cdots} = 3\sin\theta\cos\theta = \frac{3}{2}\sin 2\theta$$
>
> (구간 $[0, \pi/2]$에서 $\sin\theta \geq 0$, $\cos\theta \geq 0$이므로 절댓값 불필요)
>
> **적분**:
>
> $$l = \int_0^{\frac{\pi}{2}}\frac{3}{2}\sin 2\theta\,d\theta = \left[-\frac{3}{4}\cos 2\theta\right]_0^{\frac{\pi}{2}} = -\frac{3}{4}(-1) + \frac{3}{4}(1) = \boxed{\frac{3}{2}}$$

---

## 관련 주제

- [[63-arc-length-1|속도와 거리 및 곡선의 길이(1)]]
- [[45-integration-by-parts|부분적분]]
- [[44-integration-substitution-1|치환적분(1)]]
- [[65-improper-double-integral|이상적분, 간단한 이중적분]]

---

**학습 포인트:**
1. **배각공식 패턴**: $2 - 2\cos t = 4\sin^2(t/2)$ — 사이클로이드 길이 계산의 핵심
2. **완전제곱식 확인**: $(dx/dt)^2 + (dy/dt)^2$를 전개한 뒤 $(\text{식})^2$ 형태가 되는지 항상 확인
3. **현수선(catenary)**: $y = \dfrac{e^x+e^{-x}}{2}$ → $1+(y')^2 = \left(\dfrac{e^x+e^{-x}}{2}\right)^2$ 완전제곱
4. **사이클로이드**: 반지름 $r$인 원이 한 바퀴 굴렀을 때 길이 $= 8r$
5. **아스트로이드**: $x = \cos^3\theta$, $y = \sin^3\theta$ → 1사분면 길이 $= \dfrac{3}{2}$ (반지름 1 기준)
6. **곡선 길이의 최솟값**: 두 점 사이의 직선 거리 = 이계도함수를 갖는 함수에서도 직선이 허용됨
