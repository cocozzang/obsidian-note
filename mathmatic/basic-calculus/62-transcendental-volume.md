---
id: b3a7f291-e604-4d2c-a18e-7c9d52f0e384
aliases:
  - 초월함수의 부피와 적분
  - 초월함수 회전체
  - 삼각함수 부피
  - 로그함수 부피
tags:
  - 부피와적분
  - 초월함수
  - 회전체
  - 삼각함수적분
  - 로그함수적분
  - 단면적분
  - 부분적분
pages: 195-200
subject: 대학기초수학
title: 초월함수의 부피와 적분
topics:
  - 삼각함수·로그함수 회전체 부피
  - x축·y축 둘레 회전 구분
  - 부분적분을 이용한 부피 계산
  - 단면이 특수도형(정삼각형·정사각형)인 입체
  - 연속된 단면 적분
---

# 초월함수의 부피와 적분

이번 강의는 **삼각함수와 로그함수**가 포함된 영역의 회전체 부피를 다룬다. 이전 강의에서 배운 $V = \pi\int f(x)^2\,dx$ 공식에 **배각공식**, **부분적분** 등을 결합하여 계산한다. 또한 회전체가 아닌 **단면이 특수한 도형(정삼각형, 정사각형)인 입체**의 부피도 중요하게 다룬다.

---

## 1. 핵심 공식 정리

### 회전체 부피 기본 공식

**x축 둘레 회전** (y를 x의 함수로 표현):

$$V = \pi \int_a^b [f(x)]^2 \, dx$$

**y축 둘레 회전** (x를 y의 함수로 표현):

$$V = \pi \int_c^d [g(y)]^2 \, dy$$

### 단면이 특수도형인 입체

**단면이 정삼각형** (한 변의 길이 $= \ell$):

$$S(x) = \frac{\sqrt{3}}{4}\ell^2, \quad V = \int_a^b \frac{\sqrt{3}}{4}[f(x)]^2 \, dx$$

**단면이 정사각형** (한 변의 길이 $= \ell$):

$$S(x) = \ell^2, \quad V = \int_a^b [f(x)]^2 \, dx$$

> [!tip] 단면 적분의 핵심
> 회전체가 아닌 경우, 단면의 **한 변 = 밑면에서의 함수값** 임을 파악하는 것이 핵심이다.
> 단면이 정사각형이면 $\pi$가 붙지 않는다는 점을 주의!

---

## 2. 예제

### 예제 419

![[images/04-integral/exer419.png|300]]

오른쪽 그림은 함수 $y = x^2$과 $x = 1$, $y = 0$으로 둘러싸인 부분에 구간 $[0,\ 1]$을 $5$등분하여 직사각형을 내접시킨 것이다. 어두운 부분을 $x$축 둘레로 회전시켜서 생긴 회전체의 부피는?

① $\dfrac{213}{5^5}\pi$ $\quad$ ② $\dfrac{237}{5^5}\pi$ $\quad$ ③ $\dfrac{256}{5^5}\pi$ $\quad$ ④ $\dfrac{271}{5^5}\pi$ $\quad$ ⑤ $\dfrac{354}{5^5}\pi$

> [!summary]- 풀이
>
> **어두운 부분 = 곡선 $y=x^2$의 회전체 − 4개의 내접 직사각형 회전체**
>
> 5등분 구간에서 내접 직사각형의 오른쪽 끝점 높이 사용:
> $x = \dfrac{1}{5},\ \dfrac{2}{5},\ \dfrac{3}{5},\ \dfrac{4}{5}$에서의 $y = x^2$ 값
>
> $$V = \pi\int_{0}^{1}y^{2}\,dx - \frac{1}{5}\pi\left[\left(\frac{1}{5}\right)^{4}+\left(\frac{2}{5}\right)^{4}+\left(\frac{3}{5}\right)^{4}+\left(\frac{4}{5}\right)^{4}\right]$$
>
> $$= \pi\int_{0}^{1}x^{4}\,dx - \frac{\pi}{5^{5}}\left(1^{4}+2^{4}+3^{4}+4^{4}\right)$$
>
> $$= \pi\left[\frac{1}{5}x^{5}\right]_{0}^{1} - \frac{\pi}{5^{5}}(1+16+81+256)$$
>
> $$= \frac{\pi}{5} - \frac{354}{5^{5}}\pi = \frac{625-354}{5^{5}}\pi$$
>
> $$= \boxed{\frac{271}{5^{5}}\pi}$$
>
> **정답: ④**

---

### 예제 420

곡선 $y = \dfrac{1}{2}\ln x$와 $x$축, $y$축 및 직선 $y = \ln 2$로 둘러싸인 영역을 $y$축의 둘레로 회전시켜 생기는 회전체의 부피를 $V$라 할 때, $\dfrac{V}{\pi}$의 값을 소수점 아래 둘째 자리까지 구하시오.

![[images/04-integral/exer420.png|400]]

> [!summary]- 풀이
>
> **y축 둘레 회전** → x를 y의 함수로 변환
>
> $y = \dfrac{1}{2}\ln x$ $\Rightarrow$ $2y = \ln x$ $\Rightarrow$ $x = e^{2y}$
>
> y의 범위: $y=0$ (x축)부터 $y = \ln 2$까지
>
> $$V = \pi\int_{0}^{\ln 2} x^{2}\,dy = \pi\int_{0}^{\ln 2} e^{4y}\,dy$$
>
> $$= \pi\left[\frac{1}{4}e^{4y}\right]_{0}^{\ln 2} = \frac{\pi}{4}\left(e^{4\ln 2} - e^{0}\right)$$
>
> $$= \frac{\pi}{4}(2^{4}-1) = \frac{15}{4}\pi$$
>
> $$\boxed{\frac{V}{\pi} = \frac{15}{4} = 3.75}$$

---

### 예제 421

곡선 $y = 5\sqrt{\ln x}$와 $x$축 및 직선 $x = e$로 둘러싸인 부분을 $x$축 둘레로 회전하여 생기는 회전체의 부피를 $V$라 할 때, $\dfrac{V}{\pi}$의 값을 구하시오.

> [!summary]- 풀이
>
> **x축 둘레 회전**, $x$ 범위: $y=0$이 되는 점은 $\ln x = 0$ $\Rightarrow$ $x=1$부터 $x=e$까지
>
> $$V = \pi\int_{1}^{e}y^{2}\,dx = \pi\int_{1}^{e}25\ln x\,dx = 25\pi\int_{1}^{e}\ln x\,dx$$
>
> **$\int \ln x\,dx$ 계산** (부분적분):
>
> $$\int \ln x\,dx = x\ln x - x + C$$
>
> $$V = 25\pi\left[x\ln x - x\right]_{1}^{e} = 25\pi\left[(e-e)-(0-1)\right] = 25\pi \cdot 1 = 25\pi$$
>
> $$\boxed{\frac{V}{\pi} = 25}$$

---

### 예제 422

![[images/04-integral/exer422.png]]

곡선 $x = \sin y\ \left(0 \leq y \leq \dfrac{\pi}{2}\right)$를 $y$축의 둘레로 회전시켜 생긴 그릇에 물을 매초 $a$만큼씩 넣는다. 수면의 높이가 $\dfrac{\pi}{4}$가 되는 순간, 수면의 높이의 순간변화율은? (단, 새어나가는 물은 없다.)

① $\dfrac{a}{2\pi}$ $\quad$ ② $\dfrac{a}{\pi}$ $\quad$ ③ $\dfrac{2a}{\pi}$ $\quad$ ④ $\dfrac{3a}{2\pi}$ $\quad$ ⑤ $\dfrac{3a}{\pi}$

> [!summary]- 풀이
>
> **조건**: $\dfrac{dV}{dt} = a$ (부피의 시간 변화율)
>
> 수면 높이 $h$일 때 담긴 물의 부피 ($y$축 둘레 회전체):
>
> $$V = \pi\int_{0}^{h}x^{2}\,dy = \pi\int_{0}^{h}\sin^{2}y\,dy$$
>
> 배각공식 $\sin^2 y = \dfrac{1-\cos 2y}{2}$ 적용:
>
> $$V = \frac{\pi}{2}\int_{0}^{h}(1-\cos 2y)\,dy = \frac{\pi}{2}\left[y - \frac{1}{2}\sin 2y\right]_{0}^{h}$$
>
> $$V = \frac{\pi}{2}\left(h - \frac{1}{2}\sin 2h\right)$$
>
> 양변을 $t$로 미분 (연쇄법칙):
>
> $$\frac{dV}{dt} = \frac{\pi}{2}\left(1 - \cos 2h\right) \cdot \frac{dh}{dt} = a$$
>
> $h = \dfrac{\pi}{4}$를 대입:
>
> $$\frac{\pi}{2}\left(1 - \cos\frac{\pi}{2}\right)\cdot\frac{dh}{dt} = a$$
>
> $$\frac{\pi}{2}(1-0)\cdot\frac{dh}{dt} = a$$
>
> $$\boxed{\frac{dh}{dt} = \frac{2a}{\pi}}$$
>
> **정답: ③**

---

### 예제 423

곡선 $y = \cos 2x$와 $x$축, $y$축, $x = \dfrac{\pi}{2}$으로 둘러싸인 부분을 $x$축의 둘레로 회전시켜 생기는 회전체의 부피는? $\left(\text{단},\ 0 \leq x \leq \dfrac{\pi}{2}\right)$

① $\dfrac{\pi^2}{4}$ $\quad$ ② $\dfrac{\pi^2}{2}$ $\quad$ ③ $\dfrac{3}{4}\pi^2$ $\quad$ ④ $\pi^2$ $\quad$ ⑤ $2\pi^2$

![[images/04-integral/exer423.png|400]]

> [!summary]- 풀이
>
> $\cos 2x$는 $x = \dfrac{\pi}{4}$에서 $0$을 지나고 이후 음수가 된다.
>
> $y^2 = \cos^2 2x$이므로 부호에 관계없이 $y^2$는 동일하다 → 적분 구간을 나눌 필요 없음
>
> $$V = \pi\int_{0}^{\frac{\pi}{2}}\cos^{2}2x\,dx$$
>
> 배각공식 $\cos^2 2x = \dfrac{1+\cos 4x}{2}$ 적용:
>
> $$= \frac{\pi}{2}\int_{0}^{\frac{\pi}{2}}(1+\cos 4x)\,dx = \frac{\pi}{2}\left[x + \frac{1}{4}\sin 4x\right]_{0}^{\frac{\pi}{2}}$$
>
> $$= \frac{\pi}{2}\left(\frac{\pi}{2} + 0 - 0\right) = \boxed{\frac{\pi^{2}}{4}}$$
>
> **정답: ①**

---

### 예제 424

타원 $4x^2 + y^2 = 4$를 $x$축의 둘레로 회전시켜 생기는 회전체의 부피와 $y$축의 둘레로 회전시켜 생기는 회전체의 부피의 합은?

① $\dfrac{8}{3}\pi$ $\quad$ ② $\dfrac{16}{3}\pi$ $\quad$ ③ $8\pi$ $\quad$ ④ $\dfrac{32}{3}\pi$ $\quad$ ⑤ $\dfrac{40}{3}\pi$

![[images/04-integral/exer424.png|400]]

> [!summary]- 풀이
>
> **타원 방정식 정리**:
>
> $$4x^2 + y^2 = 4 \implies x^2 = \frac{4-y^2}{4},\ y^2 = 4(1-x^2)$$
>
> x축 범위: $-1 \leq x \leq 1$, y축 범위: $-2 \leq y \leq 2$
>
> **y축 둘레 회전 부피** (x를 y의 함수):
>
> $$V_y = \pi\int_{-2}^{2}x^{2}\,dy = \frac{\pi}{4}\int_{-2}^{2}(4-y^{2})\,dy = \frac{\pi}{2}\int_{0}^{2}(4-y^{2})\,dy$$
>
> $$= \frac{\pi}{2}\left[4y - \frac{y^{3}}{3}\right]_{0}^{2} = \frac{\pi}{2}\left(8 - \frac{8}{3}\right) = \frac{\pi}{2} \cdot \frac{16}{3} = \frac{8\pi}{3}$$
>
> **x축 둘레 회전 부피** (y를 x의 함수):
>
> $$V_x = \pi\int_{-1}^{1}y^{2}\,dx = 4\pi\int_{-1}^{1}(1-x^{2})\,dx = 8\pi\int_{0}^{1}(1-x^{2})\,dx$$
>
> $$= 8\pi\left[x - \frac{x^{3}}{3}\right]_{0}^{1} = 8\pi\left(1 - \frac{1}{3}\right) = 8\pi \cdot \frac{2}{3} = \frac{16\pi}{3}$$
>
> **합계**:
>
> $$V_y + V_x = \frac{8}{3}\pi + \frac{16}{3}\pi = \frac{24}{3}\pi = \boxed{8\pi}$$
>
> **정답: ③**

---

### 예제 425

곡선 $y = \tan x$와 $x$축 및 직선 $x = \dfrac{\pi}{3}$로 둘러싸인 부분을 $x$축 둘레로 회전시켜 생기는 회전체의 부피는?

① $\dfrac{\pi^2}{3}$ $\quad$ ② $\sqrt{2}\,\pi + \dfrac{\pi^2}{3}$ $\quad$ ③ $\sqrt{2}\,\pi - \dfrac{\pi^2}{3}$ $\quad$ ④ $\sqrt{3}\,\pi + \dfrac{\pi^2}{3}$ $\quad$ ⑤ $\sqrt{3}\,\pi - \dfrac{\pi^2}{3}$

![[images/04-integral/exer425.png|300]]

> [!summary]- 풀이
>
> $$V = \pi\int_{0}^{\frac{\pi}{3}}\tan^{2}x\,dx$$
>
> 항등식 $\tan^2 x = \sec^2 x - 1$ 적용:
>
> $$= \pi\int_{0}^{\frac{\pi}{3}}(\sec^{2}x - 1)\,dx = \pi\left[\tan x - x\right]_{0}^{\frac{\pi}{3}}$$
>
> $$= \pi\left(\tan\frac{\pi}{3} - \frac{\pi}{3} - 0\right) = \pi\left(\sqrt{3} - \frac{\pi}{3}\right)$$
>
> $$= \boxed{\sqrt{3}\,\pi - \frac{\pi^{2}}{3}}$$
>
> **정답: ⑤**

---

### 예제 426

곡선 $y = \ln x$와 $x$축 및 직선 $x = e$로 둘러싸인 부분을 $x$축의 둘레로 회전시켜 생기는 회전체의 부피는?

① $(e-1)\pi$ $\quad$ ② $(e-2)\pi$ $\quad$ ③ $(e-3)\pi$ $\quad$ ④ $(e-4)\pi$ $\quad$ ⑤ $(e-5)\pi$

> [!summary]- 풀이
>
> $y = \ln x$와 $x$축의 교점: $x = 1$ → 범위 $[1, e]$
>
> $$V = \pi\int_{1}^{e}(\ln x)^{2}\,dx$$
>
> **$\int(\ln x)^2\,dx$ 부분적분** (두 번 적용):
>
> $$\int(\ln x)^{2}\,dx = x(\ln x)^{2} - 2\int\ln x\,dx = x(\ln x)^{2} - 2(x\ln x - x) + C$$
>
> $$= x(\ln x)^{2} - 2x\ln x + 2x + C$$
>
> $$V = \pi\left[x(\ln x)^{2} - 2x\ln x + 2x\right]_{1}^{e}$$
>
> $x=e$: $\quad e(1)^{2} - 2e(1) + 2e = e - 2e + 2e = e$
>
> $x=1$: $\quad 1(0)^{2} - 2(1)(0) + 2(1) = 2$
>
> $$V = \pi(e - 2) = \boxed{(e-2)\pi}$$
>
> **정답: ②**

---

### 예제 427

어떤 입체의 밑면은 곡선 $y = \ln x$와 $x$축 및 직선 $x = e$로 둘러싸인 평면이고, $x$축에 수직인 평면으로 이 입체를 자른 단면은 한 변이 밑면에 있는 **정삼각형**이다. 이 입체의 부피를 구하여라.

① $\dfrac{\sqrt{3}}{4}(e+2)$ $\quad$ ② $\dfrac{\sqrt{3}}{4}(e+1)$ $\quad$ ③ $\dfrac{\sqrt{3}}{4}e$ $\quad$ ④ $\dfrac{\sqrt{3}}{4}(e-1)$ $\quad$ ⑤ $\dfrac{\sqrt{3}}{4}(e-2)$

![[images/04-integral/exer427.png|300]]

> [!summary]- 풀이
>
> 위치 $x$에서 단면의 한 변의 길이 $= y = \ln x$
>
> 정삼각형의 넓이 (한 변 $\ell$):
>
> $$S(x) = \frac{\sqrt{3}}{4}(\ln x)^{2}$$
>
> **예제 426 결과 활용**: $\displaystyle\int_{1}^{e}(\ln x)^{2}\,dx = e - 2$
>
> $$V = \int_{1}^{e}\frac{\sqrt{3}}{4}(\ln x)^{2}\,dx = \frac{\sqrt{3}}{4}\int_{1}^{e}(\ln x)^{2}\,dx = \frac{\sqrt{3}}{4}(e-2)$$
>
> $$\boxed{V = \frac{\sqrt{3}}{4}(e-2)}$$
>
> **정답: ⑤**

---

### 예제 428

좌표평면 위에 두 곡선 $y = \sin x$, $y = \cos x\ \left(\dfrac{\pi}{4} \leq x \leq \dfrac{5\pi}{4}\right)$으로 둘러싸인 도형을 밑면으로 하고, $x$축에 수직인 평면으로 자른 단면이 **정사각형**으로 이루어진 입체의 부피는?

① $\dfrac{\pi}{4}$ $\quad$ ② $\dfrac{\pi}{2}$ $\quad$ ③ $\pi$ $\quad$ ④ $2\pi$ $\quad$ ⑤ $4\pi$

![[images/04-integral/exer428.png|400]]

> [!summary]- 풀이
>
> 위치 $x$에서 정사각형의 한 변의 길이 $= \sin x - \cos x$
>
> 정사각형 단면의 넓이 $= (\sin x - \cos x)^{2}$
>
> $$V = \int_{\frac{\pi}{4}}^{\frac{5\pi}{4}}(\sin x - \cos x)^{2}\,dx$$
>
> $(\sin x - \cos x)^{2} = \sin^{2}x - 2\sin x\cos x + \cos^{2}x = 1 - \sin 2x$
>
> $$= \int_{\frac{\pi}{4}}^{\frac{5\pi}{4}}(1 - \sin 2x)\,dx = \left[x + \frac{1}{2}\cos 2x\right]_{\frac{\pi}{4}}^{\frac{5\pi}{4}}$$
>
> $x = \dfrac{5\pi}{4}$: $\quad \dfrac{5\pi}{4} + \dfrac{1}{2}\cos\dfrac{5\pi}{2} = \dfrac{5\pi}{4} + 0$
>
> $x = \dfrac{\pi}{4}$: $\quad \dfrac{\pi}{4} + \dfrac{1}{2}\cos\dfrac{\pi}{2} = \dfrac{\pi}{4} + 0$
>
> $$V = \frac{5\pi}{4} - \frac{\pi}{4} = \boxed{\pi}$$
>
> **정답: ③**

---

### 예제 429

![[images/04-integral/exer429.png]]

좌표공간에 다음 네 점을 꼭짓점으로 하는 직사각형 PQRS가 있다.

$$P(x,\ 0,\ 0),\quad Q(x,\ \sin x,\ 0),\quad R(x,\ \sin x,\ \cos^{2}x),\quad S(x,\ 0,\ \cos^{2}x)$$

직사각형이 네 선분 $\overline{PQ}$, $\overline{QR}$, $\overline{RS}$, $\overline{SP}$가 만들어내는 곡면으로 둘러싸인 입체의 부피는? $\left(\text{단},\ 0 \leq x \leq \dfrac{\pi}{2}\right)$

① $2$ $\quad$ ② $\dfrac{3}{2}$ $\quad$ ③ $1$ $\quad$ ④ $\dfrac{1}{2}$ $\quad$ ⑤ $\dfrac{1}{3}$


> [!summary]- 풀이
>
> **핵심**: 위치 $x$에서의 직사각형 단면의 넓이를 구한다.
>
> 직사각형의 두 변의 길이:
> - $\overline{PQ}$ 방향: $y$성분의 차이 $= \sin x - 0 = \sin x$
> - $\overline{PS}$ 방향: $z$성분의 차이 $= \cos^{2}x - 0 = \cos^{2}x$
>
> 단면 넓이:
>
> $$S(x) = \sin x \cdot \cos^{2}x$$
>
> 부피:
>
> $$V = \int_{0}^{\frac{\pi}{2}}\sin x\cos^{2}x\,dx$$
>
> 치환: $t = \cos x$, $dt = -\sin x\,dx$
>
> $x=0$일 때 $t=1$, $x=\dfrac{\pi}{2}$일 때 $t=0$
>
> $$V = \int_{1}^{0}t^{2}(-dt) = \int_{0}^{1}t^{2}\,dt = \left[\frac{t^{3}}{3}\right]_{0}^{1} = \boxed{\frac{1}{3}}$$
>
![[images/04-integral/exer429-1.png|600]]
> **정답: ⑤**

---

## 관련 주제

- [[61-volume-integral-2|부피와 적분(2)]]
- [[44-integration-substitution-1|치환적분(1)]]
- [[45-integration-by-parts|부분적분]]
- [[63-arc-length-1|속도와 거리 및 곡선의 길이(1)]]

---

**학습 포인트:**
1. **삼각함수 회전체**: $\cos^2$, $\sin^2$ 적분 시 반드시 배각공식($\cos^2\theta = \dfrac{1+\cos 2\theta}{2}$)으로 변환
2. **로그함수 회전체**: $\int(\ln x)^2\,dx$는 부분적분을 **두 번** 적용 → $x(\ln x)^2 - 2x\ln x + 2x$
3. **$\tan^2$ 적분**: $\tan^2 x = \sec^2 x - 1$로 바꾼 뒤 적분
4. **단면 적분 (비회전체)**: 단면이 정삼각형 → $\dfrac{\sqrt{3}}{4}\ell^2$, 정사각형 → $\ell^2$ ($\pi$ 없음!)
5. **연속된 단면 (3D 입체)**: 각 $x$에서의 단면 넓이 $= $ (두 변의 곱)으로 설정 후 적분
6. **부피 변화율**: $\dfrac{dV}{dt} = S(h) \cdot \dfrac{dh}{dt}$ — 단면적 × 높이 변화율
