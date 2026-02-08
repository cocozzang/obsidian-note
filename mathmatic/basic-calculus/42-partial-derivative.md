---
id: 9a6e2d4f-5b7c-4e3a-8d1f-7c9b3a6e4f2d
aliases:
  - 이변수 함수와 편도함수
  - 편미분
  - 이변수 함수의 미분
  - 다변수 미적분 입문
tags:
  - 이변수함수
  - 편도함수
  - 편미분
  - 연쇄법칙
  - 다변수미적분
  - 관련변화율
  - 생산함수
pages: 125-128
subject: 대학기초수학
title: 이변수 함수와 편도함수
topics:
  - 편도함수의 정의
  - 편미분 계산
  - 이변수 함수의 연쇄법칙
  - 관련 변화율 (2변수)
  - 생산함수 응용
---

# 이변수 함수와 편도함수

## Def 4: 이변수 함수에서의 편도함수

이변수 함수 $z = f(x, y)$에 대하여:

### (1) $x$에 관한 $f$의 편도함수

$$\frac{\partial f}{\partial x} = f_x(x, y) = \lim_{\Delta x \to 0} \frac{f(x + \Delta x, y) - f(x, y)}{\Delta x}$$

**의미**: $y$를 상수로 보고 $x$에 관해 미분

### (2) $y$에 관한 $f$의 편도함수

$$\frac{\partial f}{\partial y} = f_y(x, y) = \lim_{\Delta y \to 0} \frac{f(x, y + \Delta y) - f(x, y)}{\Delta y}$$

**의미**: $x$를 상수로 보고 $y$에 관해 미분

---

## 편도함수 계산 방법

$z = f(x, y)$의 편도함수를 구하는 방법:

① $f_x$ → $y$를 상수로 보고 $x$에 관해 미분
② $f_y$ → $x$를 상수로 보고 $y$에 관해 미분

---

## 예제

### 예제 267

$f(x, y) = x^3 + x^2y^3 - 2y^2$일 때 $f_x(1, 1)$과 $f_y(1, 1)$을 구하여라.

> [!summary]- 풀이
> **Step 1**: $x$에 관한 편도함수 ($y$를 상수로 취급)
>
> $$f_x(x, y) = \frac{\partial f}{\partial x} = 3x^2 + 2xy^3$$
>
> $(1, 1)$에서:
>
> $$f_x(1, 1) = 3(1)^2 + 2(1)(1)^3 = 3 + 2 = 5$$
>
> **Step 2**: $y$에 관한 편도함수 ($x$를 상수로 취급)
>
> $$f_y(x, y) = \frac{\partial f}{\partial y} = 3x^2y^2 - 4y$$
>
> $(1, 1)$에서:
>
> $$f_y(1, 1) = 3(1)^2(1)^2 - 4(1) = 3 - 4 = -1$$
>
> $$\therefore f_x(1, 1) = 5, \quad f_y(1, 1) = -1$$

---

### 예제 268

$f(x, y) = \sin\left(\frac{x}{1+y}\right)$일 때 $\frac{\partial f}{\partial x}$와 $\frac{\partial f}{\partial y}$를 구하여라.

> [!summary]- 풀이
> **Step 1**: $x$에 관한 편도함수
>
> $\frac{x}{1+y}$를 $x$로 미분 (연쇄법칙):
>
> $$\frac{\partial f}{\partial x} = \cos\left(\frac{x}{1+y}\right) \cdot \frac{1}{1+y}$$
>
> $$= \frac{1}{1+y}\cos\left(\frac{x}{1+y}\right)$$
>
> **Step 2**: $y$에 관한 편도함수
>
> $\frac{x}{1+y}$를 $y$로 미분 (연쇄법칙):
>
> $$\frac{\partial}{\partial y}\left(\frac{x}{1+y}\right) = x \cdot \frac{-1}{(1+y)^2} = \frac{-x}{(1+y)^2}$$
>
> $$\frac{\partial f}{\partial y} = \cos\left(\frac{x}{1+y}\right) \cdot \frac{-x}{(1+y)^2}$$
>
> $$= \frac{-x}{(1+y)^2}\cos\left(\frac{x}{1+y}\right)$$

---

### 예제 269

함수 $f(x, y) = \ln(3x^5 + 2y^3) + e^{2x}$의 $f_x$와 $f_y$를 구하여라.

> [!summary]- 풀이
> **Step 1**: $x$에 관한 편도함수
>
> $$f_x = \frac{\partial}{\partial x}\left[\ln(3x^5 + 2y^3)\right] + \frac{\partial}{\partial x}(e^{2x})$$
>
> $$= \frac{15x^4}{3x^5 + 2y^3} + 2e^{2x}$$
>
> **Step 2**: $y$에 관한 편도함수
>
> $$f_y = \frac{\partial}{\partial y}\left[\ln(3x^5 + 2y^3)\right] + \frac{\partial}{\partial y}(e^{2x})$$
>
> $$= \frac{6y^2}{3x^5 + 2y^3} + 0$$
>
> $$= \frac{6y^2}{3x^5 + 2y^3}$$

---

### 예제 270

$z = e^{xy}\cos x \sin y$의 편도함수 $\frac{\partial z}{\partial x}$와 $\frac{\partial z}{\partial y}$를 구하여라.

> [!summary]- 풀이
> **Step 1**: $x$에 관한 편도함수 (곱의 미분법)
>
> $$z = e^{xy} \cdot \cos x \cdot \sin y$$
>
> $\sin y$를 상수로 취급:
>
> $$\frac{\partial z}{\partial x} = \sin y \cdot \frac{\partial}{\partial x}(e^{xy} \cos x)$$
>
> 곱의 미분법:
>
> $$= \sin y \cdot \left[ye^{xy} \cdot \cos x + e^{xy} \cdot (-\sin x)\right]$$
>
> $$= \sin y \cdot e^{xy}(y\cos x - \sin x)$$
>
> **Step 2**: $y$에 관한 편도함수
>
> $\cos x$를 상수로 취급:
>
> $$\frac{\partial z}{\partial y} = \cos x \cdot \frac{\partial}{\partial y}(e^{xy} \sin y)$$
>
> 곱의 미분법:
>
> $$= \cos x \cdot \left[xe^{xy} \cdot \sin y + e^{xy} \cdot \cos y\right]$$
>
> $$= \cos x \cdot e^{xy}(x\sin y + \cos y)$$

---

### 예제 271

$z = x\sin y + y\sec x$의 편도함수 $\frac{\partial z}{\partial x}$와 $\frac{\partial z}{\partial y}$를 구하여라.

> [!summary]- 풀이
> **Step 1**: $x$에 관한 편도함수
>
> $$\frac{\partial z}{\partial x} = \frac{\partial}{\partial x}(x\sin y) + \frac{\partial}{\partial x}(y\sec x)$$
>
> $$= \sin y + y \cdot \frac{\partial}{\partial x}(\sec x)$$
>
> $$\sec x$의 도함수\*\*:
>
> $$(\sec x)' = \left(\frac{1}{\cos x}\right)' = \frac{\sin x}{\cos^2 x} = \tan x \sec x$$
>
> 따라서:
>
> $$\frac{\partial z}{\partial x} = \sin y + y\tan x\sec x$$
>
> **Step 2**: $y$에 관한 편도함수
>
> $$\frac{\partial z}{\partial y} = \frac{\partial}{\partial y}(x\sin y) + \frac{\partial}{\partial y}(y\sec x)$$
>
> $$= x\cos y + \sec x$$

---

### 예제 272

$u = e^{x^2 + xy + z^2}$의 편도함수 $\frac{\partial u}{\partial x}$, $\frac{\partial u}{\partial y}$, $\frac{\partial u}{\partial z}$를 구하여라.

> [!summary]- 풀이
> **3변수 함수의 편미분**
>
> **Step 1**: $x$에 관한 편도함수 ($y, z$를 상수로 취급)
>
> $$\frac{\partial u}{\partial x} = e^{x^2 + xy + z^2} \cdot \frac{\partial}{\partial x}(x^2 + xy + z^2)$$
>
> $$= e^{x^2 + xy + z^2} \cdot (2x + y)$$
>
> $$= (2x + y)e^{x^2 + xy + z^2}$$
>
> **Step 2**: $y$에 관한 편도함수 ($x, z$를 상수로 취급)
>
> $$\frac{\partial u}{\partial y} = e^{x^2 + xy + z^2} \cdot \frac{\partial}{\partial y}(x^2 + xy + z^2)$$
>
> $$= e^{x^2 + xy + z^2} \cdot x$$
>
> $$= xe^{x^2 + xy + z^2}$$
>
> **Step 3**: $z$에 관한 편도함수 ($x, y$를 상수로 취급)
>
> $$\frac{\partial u}{\partial z} = e^{x^2 + xy + z^2} \cdot \frac{\partial}{\partial z}(x^2 + xy + z^2)$$
>
> $$= e^{x^2 + xy + z^2} \cdot 2z$$
>
> $$= 2ze^{x^2 + xy + z^2}$$

---

## Thm 42: 이변수 함수에 대한 연쇄법칙

이변수 함수 $u = f(x, y)$는 연속인 제 1계 편도함수 $f_x(x, y)$와 $f_y(x, y)$를 가지며 $x = g(t)$와 $y = h(t)$는 $t$에 관해 미분가능한 함수일 때 $u$는 $t$에 관한 미분가능한 함수이고 그 도함수는:

$$\frac{du}{dt} = \frac{\partial u}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial u}{\partial y} \cdot \frac{dy}{dt}$$

**⇒ 자세한 증명은 대학미적분학 강의에서 한다.**

---

### 예제 273

$u = x^2 + xe^y$, $x = \sin t$, $y = \ln t$일 때 $t$에 관한 $u$의 전도함수 $\frac{du}{dt}$를 구하여라.

> [!summary]- 풀이
> **Step 1**: 연쇄법칙 적용
>
> $$\frac{du}{dt} = \frac{\partial u}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial u}{\partial y} \cdot \frac{dy}{dt}$$
>
> **Step 2**: 각 편도함수와 도함수 계산
>
> $$\frac{\partial u}{\partial x} = 2x + e^y$$
>
> $$\frac{dx}{dt} = \cos t$$
>
> $$\frac{\partial u}{\partial y} = xe^y$$
>
> $$\frac{dy}{dt} = \frac{1}{t}$$
>
> **Step 3**: 대입
>
> $$\frac{du}{dt} = (2x + e^y)\cos t + xe^y \cdot \frac{1}{t}$$
>
> $x = \sin t$, $y = \ln t$를 대입하면:
>
> $$\frac{du}{dt} = (2\sin t + e^{\ln t})\cos t + \sin t \cdot e^{\ln t} \cdot \frac{1}{t}$$
>
> $$= (2\sin t + t)\cos t + \sin t \cdot t \cdot \frac{1}{t}$$
>
> $$= (2\sin t + t)\cos t + \sin t$$

---

### 예제 274

원기둥의 높이는 매초 4cm의 속도로 감소하고 밑면의 반지름은 매초 1cm의 속도로 증가할 때 높이가 50cm이고 반지름이 20cm인 순간에 부피의 변화속도를 구하여라.

> [!summary]- 풀이
> **Step 1**: 함수 정의
>
> 원기둥의 부피:
>
> $$V = f(r, h) = \pi r^2 h$$
>
> **Step 2**: 주어진 조건
>
> $$\frac{dr}{dt} = 1 \text{ cm/초} \quad (\text{반지름 증가})$$
>
> $$\frac{dh}{dt} = -4 \text{ cm/초} \quad (\text{높이 감소})$$
>
> **Step 3**: 연쇄법칙 적용
>
> $$\frac{dV}{dt} = \frac{\partial V}{\partial r} \cdot \frac{dr}{dt} + \frac{\partial V}{\partial h} \cdot \frac{dh}{dt}$$
>
> **Step 4**: 편도함수 계산
>
> $$\frac{\partial V}{\partial r} = 2\pi rh$$
>
> $$\frac{\partial V}{\partial h} = \pi r^2$$
>
> **Step 5**: 대입
>
> $$\frac{dV}{dt} = 2\pi rh \cdot 1 + \pi r^2 \cdot (-4)$$
>
> $$= 2\pi rh - 4\pi r^2$$
>
> $$= 2\pi r(h - 2r)$$
>
> **Step 6**: $h = 50$, $r = 20$일 때
>
> $$\frac{dV}{dt} = 2\pi \cdot 20 \cdot (50 - 2 \cdot 20)$$
>
> $$= 40\pi(50 - 40)$$
>
> $$= 40\pi \cdot 10$$
>
> $$= 400\pi \text{ cm}^3/\text{초}$$

---

### 예제 275

생산함수 $P$는 노동 $L$과 자본 $C$와 관계가 있으며 다음과 같은 공식을 만족한다고 하자.

$$P = 3.5L^{6/5}C^{1/2}$$

$L = 12$이고 $C = 4$일 때 노동의 변화율은 2.5이며 자본의 변화율은 0.5이다. 생산의 증가율을 구하면? (단, $12^{1/5} = 1.643$으로 계산한다.)

① 약 11.7 ② 약 22.2 ③ 약 31.1 ④ 약 43.1

> [!summary]- 풀이
> **Step 1**: 주어진 조건
>
> $$\frac{dL}{dt} = 2.5, \quad \frac{dC}{dt} = 0.5$$
>
> $L = 12$, $C = 4$일 때의 $\frac{dP}{dt}$를 구한다.
>
> **Step 2**: 연쇄법칙
>
> $$\frac{dP}{dt} = \frac{\partial P}{\partial L} \cdot \frac{dL}{dt} + \frac{\partial P}{\partial C} \cdot \frac{dC}{dt}$$
>
> **Step 3**: 편도함수 계산
>
> $$\frac{\partial P}{\partial L} = 3.5 \cdot \frac{6}{5}L^{1/5}C^{1/2}$$
>
> $$= \frac{21}{5}L^{1/5}C^{1/2}$$
>
> $$\frac{\partial P}{\partial C} = 3.5 \cdot \frac{1}{2}L^{6/5}C^{-1/2}$$
>
> $$= \frac{7}{4}L^{6/5}C^{-1/2}$$
>
> **Step 4**: $L = 12$, $C = 4$에서 계산
>
> $$\frac{\partial P}{\partial L}\bigg|_{L=12, C=4} = \frac{21}{5} \cdot 12^{1/5} \cdot 4^{1/2}$$
>
> $$= \frac{21}{5} \cdot 12^{1/5} \cdot 2$$
>
> $$= \frac{42}{5} \cdot 12^{1/5}$$
>
> $$\frac{\partial P}{\partial C}\bigg|_{L=12, C=4} = \frac{7}{4} \cdot 12^{6/5} \cdot 4^{-1/2}$$
>
> $$= \frac{7}{4} \cdot 12^{6/5} \cdot \frac{1}{2}$$
>
> $$= \frac{7}{8} \cdot 12 \cdot 12^{1/5}$$
>
> $$= \frac{21}{2} \cdot 12^{1/5}$$
>
> **Step 5**: 전체 변화율
>
> $$\frac{dP}{dt} = \frac{42}{5} \cdot 12^{1/5} \cdot 2.5 + \frac{21}{2} \cdot 12^{1/5} \cdot 0.5$$
>
> $$= 21 \cdot 12^{1/5} + \frac{21}{4} \cdot 12^{1/5}$$
>
> $$= 21 \cdot 12^{1/5}\left(1 + \frac{1}{4}\right)$$
>
> $$= 21 \cdot 12^{1/5} \cdot \frac{5}{4}$$
>
> $$= \frac{105}{4} \cdot 12^{1/5}$$
>
> **Step 6**: $12^{1/5} = 1.643$ 대입
>
> $$\frac{dP}{dt} = \frac{105}{4} \cdot 1.643$$
>
> $$= 26.25 \cdot 1.643$$
>
> $$\approx 43.13$$
>
> $$\therefore \text{답: ④ 약 43.1}$$

---

## 연습문제

각 예제를 통해 다음 내용을 복습하시오:

1. 이변수 함수의 편도함수 계산
2. 삼각함수·지수함수·로그함수의 편미분
3. 곱의 미분법을 이용한 편미분
4. 3변수 함수의 편미분
5. 이변수 함수의 연쇄법칙
6. 관련 변화율 (원기둥 부피)
7. 경제학 응용 (생산함수)

---

## 관련 주제

- [[40-velocity-acceleration-1|속도, 가속도와 미분(1)]]
- [[41-velocity-acceleration-2|속도, 가속도와 미분(2)]]
- [[22-transcendental-derivative-1|초월함수의 도함수(1)]]
- [[20-derivative-applications|도함수의 활용]]

---

**학습 포인트:**

1. **편도함수**: 다른 변수를 상수로 보고 한 변수에 대해서만 미분
2. **기호**: $\frac{\partial f}{\partial x}$, $f_x$, $\frac{\partial z}{\partial x}$ 모두 같은 의미
3. **연쇄법칙**: $\frac{du}{dt} = \frac{\partial u}{\partial x}\frac{dx}{dt} + \frac{\partial u}{\partial y}\frac{dy}{dt}$
4. **계산 주의**: 어느 변수로 미분하는지 명확히 파악
5. **실용**: 관련 변화율, 경제학의 생산함수 분석에 활용
6. **3변수 이상**: 같은 원리로 확장 가능
7. **대학 수준 예비**: 이 내용은 대학 미적분학의 기초
