---
id: d5e8f3a2-1b4c-4d61-c3e0-4f7a9b2d6e85
aliases:
  - 부피와 적분(2)
  - 회전체 부피 심화
  - 구의 일부 부피
  - 파푸스 정리
tags:
  - 부피와적분
  - 회전체
  - 구의부피
  - 파푸스정리
  - 미분과부피
pages: 192-194
subject: 대학기초수학
title: 부피와 적분(2)
topics:
  - 원뿔대·특수 입체의 회전체 부피
  - 두 곡선 사이 회전체 (와셔법)
  - 파푸스 정리를 이용한 도넛 부피
  - 구의 일부 부피 공식
  - 부피의 시간 변화율 (연속문제)
---

# 부피와 적분(2)

지난 강의의 기본 회전체 공식에서 한 단계 나아가, 이번 강의에서는 **특수한 형태의 입체**(원뿔대, 정사각형 회전, 구의 일부)의 부피를 다룬다. 특히 **파푸스 정리**와 **구의 일부 부피 공식**은 적분 없이도 빠르게 계산할 수 있는 강력한 도구이다. 또한 부피를 시간의 함수로 나타낸 뒤 **미분하여 변화율**을 구하는 응용 문제도 핵심이다.

---

## 1. Thm (56-1): 구의 일부 부피 공식

![[images/04-integral/thm56-1.png|400]]

반지름 $r$인 구를 잘랐을 때, 높이 $h$, 단면 반지름 $a$인 **구의 일부(구관)**의 부피:

$$\boxed{V_{\text{구관}} = \frac{\pi}{2}h\left(a^2 + \frac{1}{3}h^2\right)}$$

- 전체 구의 부피: $V = \dfrac{4}{3}\pi r^3$
- 관계식: $a^2 = r^2 - (r-h)^2 = 2rh - h^2$
> [!note] 활용 전략
> 구의 일부 부피는 적분으로도 구할 수 있지만, 이 공식을 쓰면 훨씬 빠르다. 두 방법의 결과가 일치하는지 확인하는 것도 좋은 학습이다.

### 공식 검증 (연습문제)

![[images/04-integral/thm56-1-1.png|400]]

$r=2$인 구에서 $x=-2$부터 $x=1$까지 잘린 왼쪽 부분의 부피를 구하여라.

> [!summary]- 풀이 (두 가지 방법)
>
> **(1) 구의 일부 공식 활용**
>
> $h = 1-(-2) = 3$, $a = \sqrt{2^2 - 1^2} = \sqrt{3}$
>
> $$V = \frac{\pi}{2} \cdot 3\left(3 + \frac{1}{3} \cdot 9\right) = \frac{\pi}{2} \cdot 3 \cdot 6 = 9\pi$$
>
> **(2) 적분을 이용한 방법**
>
> 구의 방정식 $x^2 + y^2 = 4$에서 $y^2 = 4 - x^2$
>
> $$V = \pi\int_{-2}^{1}(4-x^2)\,dx = \pi\left[4x - \frac{x^3}{3}\right]_{-2}^{1}$$
>
> $$= \pi\left[\left(4 - \frac{1}{3}\right) - \left(-8 + \frac{8}{3}\right)\right] = \pi\left(12 - 3\right) = 9\pi \quad \checkmark$$

---

## 2. 예제

### 예제 412

![[images/04-integral/exer412.png]]

그림과 같이 윗면의 반지름의 길이가 5, 아랫면의 반지름의 길이가 3, 높이가 4인 원뿔대 모양의 그릇이 있다. 이 그릇에 물을 가득 채울 때, 다음 중 담긴 물의 양을 나타낸 식으로 옳은 것은? (단, 그릇의 두께는 무시한다.)

① $\pi\displaystyle\int_0^4\!\left(3+\frac{x}{4}\right)^2dx$ ② $\pi\displaystyle\int_0^4\!\left(3+\frac{x}{3}\right)^2dx$ ③ $\pi\displaystyle\int_0^4\!\left(3+\frac{x}{2}\right)^2dx$
④ $\pi\displaystyle\int_0^4\!(3+x)^2dx$ ⑤ $\pi\displaystyle\int_0^4\!(3x)^2dx$

> [!summary]- 풀이
>
> 아랫면(높이 $x=0$)에서 반지름 $= 3$, 윗면(높이 $x=4$)에서 반지름 $= 5$
>
> 높이 $x$에서의 반지름: 선형 보간
>
> $$r(x) = 3 + \frac{5-3}{4} \cdot x = 3 + \frac{x}{2}$$
>
> $$V = \pi\int_0^4 r(x)^2\,dx = \pi\int_0^4\left(3+\frac{x}{2}\right)^2dx$$
>
> **정답: ③ $\pi\displaystyle\int_0^4\!\left(3+\dfrac{x}{2}\right)^2dx$**

---

### 예제 413

![[images/04-integral/exer413.png|400]]

좌표평면에서 두 곡선 $y = x^2$, $y^2 = x$로 둘러싸인 부분을 $x$축의 둘레로 회전시켜 생기는 회전체의 부피는?

① $\dfrac{3}{5}\pi$ ② $\dfrac{3}{7}\pi$ ③ $\dfrac{3}{8}\pi$ ④ $\dfrac{1}{3}\pi$ **⑤ $\dfrac{3}{10}\pi$**

> [!summary]- 풀이
>
> 두 곡선의 교점: $(0,0)$, $(1,1)$
>
> 구간 $[0,1]$에서 $y_2 = \sqrt{x} \geq y_1 = x^2$ (바깥쪽이 $\sqrt{x}$)
>
> 와셔법 적용:
>
> $$V_x = \pi\int_0^1\left[(y_2)^2 - (y_1)^2\right]dx = \pi\int_0^1\left[(\sqrt{x})^2 - (x^2)^2\right]dx$$
>
> $$= \pi\int_0^1(x - x^4)\,dx = \pi\left[\frac{x^2}{2} - \frac{x^5}{5}\right]_0^1$$
>
> $$= \pi\left(\frac{1}{2} - \frac{1}{5}\right) = \pi \cdot \frac{3}{10} = \frac{3}{10}\pi$$
>
> **정답: ⑤ $\dfrac{3}{10}\pi$**

---

### 예제 414

![[images/04-integral/exer414.png]]

좌표평면 위에 그림과 같이 $\overline{BD} = 2$인 정사각형 모양의 철판 ABCD가 있다. 이 철판을 $y$축 둘레로 회전시켜서 생기는 입체의 부피가 $12\pi$일 때, $\overline{OB}$의 길이는? (단, 점 B와 D는 $x$축 위에 있고, 철판의 부피는 무시한다.)

① $\dfrac{3}{2}$ ② $2$ ③ $\dfrac{5}{2}$ ④ $3$ ⑤ $4$

> [!summary]- 풀이
>
> **파푸스(Pappus) 정리** 활용:
>
> 도형을 축 둘레로 회전시킨 입체의 부피 = (도형의 넓이) × (도형의 무게중심이 이동한 거리)
>
> $$V = S \times 2\pi \bar{x}$$
>
> $\overline{BD} = 2$인 정사각형이므로 한 변의 길이 $= \sqrt{2}$ (대각선이 2이므로)
>
> 정사각형의 넓이 $S = (\sqrt{2})^2 = 2$
>
> 무게중심의 $x$좌표 $= \overline{OB} + 1$ (B에서 1만큼 안쪽)
>
> $$V = 2 \times 2\pi(\overline{OB}+1) = 4\pi(\overline{OB}+1) = 12\pi$$
>
> $$\overline{OB}+1 = 3 \implies \overline{OB} = 2$$
>
> **정답: ② $2$**

---

### 예제 415

반지름의 길이가 $5\,\text{cm}$인 반구 모양의 그릇에 매초 수면의 높이가 $1\,\text{cm}$씩 증가하도록 물이 흘러 들어가고 있다. 수면의 높이가 $3\,\text{cm}$인 순간에 부피의 증가 속도는? (단, 단위는 $\text{cm}^3$)

① $20\pi$ **② $21\pi$** ③ $22\pi$ ④ $23\pi$ ⑤ $24\pi$

> [!summary]- 풀이
>
> ![[images/04-integral/exer415.png]]
>
> 수면 높이 $t$일 때, 구의 일부 공식 적용:
>
> - 구 반지름: $R = 5$, 높이: $h = t$
> - 단면 반지름: $a^2 = 5^2 - (5-t)^2 = 10t - t^2$
>
> $$V = \frac{\pi}{2}t\left(10t - t^2 + \frac{1}{3}t^2\right) = \frac{\pi}{2}\left(10t^2 - \frac{2}{3}t^3\right)$$
>
> 시간에 대해 미분 ($\dfrac{dt}{d(\text{time})} = 1\,\text{cm/s}$이므로 $\dfrac{dV}{dt}$가 바로 속도):
>
> $$\frac{dV}{dt} = \frac{\pi}{2}(20t - 2t^2)$$
>
> $t = 3$에서:
>
> $$\frac{dV}{dt}\bigg|_{t=3} = \frac{\pi}{2}(60 - 18) = \frac{42\pi}{2} = 21\pi$$
>
> **정답: ② $21\pi$**

---

### 예제 416

![[images/04-integral/exer416.png]]

오른쪽 그림과 같이 반지름의 길이가 $30\,\text{cm}$인 반구 모양의 그릇에 물을 가득 채우고 여기에 쇠공을 조심스럽게 넣었더니 물의 절반이 넘쳐흘렀다. 이 때, 쇠공의 반지름의 길이는?

① $18\,\text{cm}$ ② $20\,\text{cm}$ ③ $21\,\text{cm}$ ④ $22\,\text{cm}$ ⑤ $24\,\text{cm}$

> [!summary]- 풀이
>
> ![[images/04-integral/exer416-1.png]]
>
> **핵심 관찰**: 쇠공을 넣으면 그릇 안에 잠긴 쇠공의 부피만큼 물이 넘친다.
> 물이 절반 넘쳤으므로:
>
> $$V_{\text{잠긴 쇠공}} = \frac{1}{2} V_{\text{반구}} = \frac{1}{2} \cdot \frac{2}{3}\pi \cdot 30^3 = \frac{1}{3}\pi \cdot 30^3 = 9000\pi$$
>
> 쇠공의 반지름을 $x$라 하면, 쇠공이 반구 그릇에 들어간 부분(구의 일부)의 높이:
>
> $$h = 30, \quad a^2 = x^2 - (x-30)^2 = 60x - 900$$
>
> 구의 일부 공식:
>
> $$V_{\text{잠긴}} = \frac{\pi}{2} \cdot 30\left(60x - 900 + \frac{1}{3} \cdot 30^2\right) = 9000\pi$$
>
> $$15\pi(60x - 900 + 300) = 9000\pi$$
>
> $$15(60x - 600) = 9000$$
>
> $$60x - 600 = 600 \implies 60x = 1200 \implies x = 20$$
>
> **정답: ② $20\,\text{cm}$**

---

### 예제 417

![[images/04-integral/exer417.png]]

오른쪽 그림과 같이 직원뿔 모양의 컵에 반지름의 길이가 $1$인 구를 넣었더니 컵에 접하여 원뿔의 꼭지점에서 구면까지의 최단 거리가 $1$이 되었다. 이 때, 구면 아래 부분의 컵의 부피는?

> [!summary]- 풀이
>
> ![[images/04-integral/exer417-1.png]]
>
> 구의 반지름 $= 1$, 꼭지점에서 구면까지의 최단 거리 $= 1$
>
> 꼭지점에서 구의 중심까지 거리 $= 1 + 1 = 2$
>
> 구가 원뿔 옆면에 접하므로, 원뿔의 반각을 $\theta$라 하면:
>
> $$\sin\theta = \frac{1}{2} \implies \theta = 30°$$
>
> 원뿔의 반각이 $30°$이므로, 높이 $h$에서의 반지름 $r = h\tan 30° = \dfrac{h}{\sqrt{3}}$
>
> 구의 중심 높이 $= 2$ (꼭지점 기준), 구가 닿는 높이(구의 아랫부분까지):
> $= 2 - 1 = 1$ → $h_{\text{구 아래}} = \dfrac{3}{2}$, 단면 반지름 $= \dfrac{\sqrt{3}}{2}$
>
> **구면 아래 컵 부피** = (원뿔 부피) - (구의 일부 부피):
>
> $$V_{\text{원뿔}} = \frac{1}{3}\pi\left(\frac{\sqrt{3}}{2}\right)^2 \cdot \frac{3}{2} = \frac{1}{3}\pi \cdot \frac{3}{4} \cdot \frac{3}{2} = \frac{3}{8}\pi$$
>
> 구의 일부: $h = \dfrac{1}{2}$, $a = \dfrac{\sqrt{3}}{2}$
>
> $$V_{\text{구관}} = \frac{\pi}{2} \cdot \frac{1}{2}\left(\frac{3}{4} + \frac{1}{3} \cdot \frac{1}{4}\right) = \frac{\pi}{4} \cdot \frac{10}{12} = \frac{5\pi}{24}$$
>
> $$V = \frac{3}{8}\pi - \frac{5}{24}\pi = \frac{9}{24}\pi - \frac{5}{24}\pi = \frac{4}{24}\pi = \boxed{\frac{\pi}{6}}$$

---

### 예제 418

![[images/04-integral/exer418.png]]

그림과 같이 한 변의 길이가 $1$인 정육면체를 직선 L에 대하여 회전했을 때 만들어지는 부피는?

> [!summary]- 풀이
>
> ![[images/04-integral/exer418-1.png]]
>
> 직선 L은 정육면체의 한 모서리를 지나는 축이다. 회전체의 단면은 최대 반경이 $1+x^2$인 원이다.
>
> ⚠️ **주의**: 회전체 단면적을 $\pi(1+x^2)$으로 놓고 $[0, \sqrt{2}]$까지 적분하면 **잘못된** 식이다.
>
> 이유: 회전체의 단면은 $x$가 커질수록 항상 증가하지 않는다. 전체 회전체를 표현하려면 **대칭성**을 이용해 절반 구간 $\left[0, \dfrac{\sqrt{2}}{2}\right]$까지만 적분한 뒤 2배 해야 한다.
>
> **올바른 식**:
>
> $$V = 2\int_0^{\frac{\sqrt{2}}{2}}\pi(1+x^2)\,dx = 2\left[\pi x + \frac{\pi}{3}x^3\right]_0^{\frac{\sqrt{2}}{2}}$$
>
> $$= 2\left(\frac{\sqrt{2}}{2}\pi + \frac{\pi}{3} \cdot \frac{2\sqrt{2}}{8}\right) = 2\pi\left(\frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{12}\right)$$
>
> $$= 2\pi \cdot \frac{7\sqrt{2}}{12} = \frac{7\sqrt{2}}{6}\pi$$

---

## 관련 주제

- [[60-volume-integral-1|부피와 적분(1)]]
- [[62-transcendental-volume|초월함수의 부피와 적분]]
- [[40-velocity-acceleration-1|속도, 가속도와 미분(1)]]

---

**학습 포인트:**
1. **구의 일부 공식** $V = \dfrac{\pi}{2}h\!\left(a^2 + \dfrac{1}{3}h^2\right)$: 반구 그릇 문제에서 적분보다 빠르다.
2. **파푸스 정리**: $V = S \times 2\pi\bar{x}$ — 도형의 넓이 × 무게중심의 회전 반지름 × $2\pi$
3. **와셔법**: 두 곡선 사이 회전체는 $V = \pi\int(r_{\text{외}}^2 - r_{\text{내}}^2)\,dx$
4. **회전체 부피 미분**: $\dfrac{dV}{dh} = S(h)$ (해당 높이의 단면적) — 변화율 문제의 핵심
5. **적분 구간 설정 주의**: 회전체가 대칭일 때 절반 구간 × 2를 사용해야 한다.
