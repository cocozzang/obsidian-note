---
id: f8a3d2e1-7b4c-4f9a-8e5d-1c2a3b4d5e6f
aliases:
  - 여러가지 함수의 미분법(1)
  - 몫의 미분법
  - 합성함수의 미분법
  - 매개변수 미분법
  - 음함수 미분법
  - 로그 미분법
tags:
  - 몫의미분법
  - 합성함수미분법
  - 매개변수미분법
  - 음함수미분법
  - 로그미분법
  - 연쇄법칙
pages: 70-71
subject: 대학기초수학
title: 여러가지 함수의 미분법(1) - 몫, 합성, 매개변수, 음함수, 로그 미분법
topics:
  - 몫의 미분법
  - 합성함수의 미분법 (연쇄법칙)
  - 매개변수 미분법
  - 음함수 미분법
  - 로그를 취하는 미분법
---

# 여러가지 함수의 미분법(1)

## 1. 몫의 미분법, 합성함수의 미분법

### Thm (26): 몫의 미분법, 합성함수의 미분법

#### (1) 몫의 미분법

미분가능한 두 함수 $f(x)$, $g(x)$에 대하여 $g(x) \neq 0$일 때

$$\left\{ \frac{f(x)}{g(x)} \right\}' = \frac{f'(x)g(x) - f(x)g'(x)}{\{g(x)\}^2}$$

> [!summary]- 유도 과정
> $F(x) = \frac{f(x)}{g(x)}$로 놓으면
> 
> $$\left\{ \frac{f(x)}{g(x)} \right\}' = F'(x) = \lim_{h \to 0} \frac{F(x+h) - F(x)}{h}$$
> 
> $$= \lim_{h \to 0} \frac{\frac{f(x+h)}{g(x+h)} - \frac{f(x)}{g(x)}}{h}$$
> 
> 분모분자에 $g(x) \cdot g(x+h)$를 곱해주면
> 
> $$= \lim_{h \to 0} \frac{f(x+h) \cdot g(x) - f(x) \cdot g(x+h)}{h} \cdot \frac{1}{g(x) \cdot g(x+h)}$$
> 
> 분자의 각 항에 $f(x)g(x)$를 더하고 빼주면
> 
> $$= \lim_{h \to 0} \left( \frac{f(x+h)g(x) - f(x)g(x)}{h} - \frac{f(x)g(x+h) - f(x)g(x)}{h} \right) \cdot \frac{1}{g(x) \cdot g(x+h)}$$
> 
> $$= \lim_{h \to 0} \left( \frac{f(x+h) - f(x)}{h} \cdot g(x) - \frac{g(x+h) - g(x)}{h} \cdot f(x) \right) \cdot \frac{1}{g(x) \cdot g(x+h)}$$
> 
> $$= \left( f'(x) \cdot g(x) - g'(x) \cdot f(x) \right) \cdot \frac{1}{\{g(x)\}^2}$$
> 
> $$\therefore \left\{ \frac{f(x)}{g(x)} \right\}' = \frac{f'(x)g(x) - f(x)g'(x)}{\{g(x)\}^2}$$

#### (2) 합성함수의 미분법 (연쇄법칙, Chain Rule)

$$\{f(g(x))\}' = f'(g(x)) \cdot g'(x)$$

> [!note]- 프라임(')의 의미
> 프라임은 함수의 **독립변수(가장 안쪽 변수)**에 대해 미분하라는 의미이다.
> 
> 함수 $f$의 독립변수는 $g(x)$이지만, 합성함수 $f \circ g$의 독립변수는 $x$이므로
> 
> $$\{f(g(x))\}' = \frac{df(g(x))}{dx}$$
> 
> 가 된다. (주의: $\frac{df(g(x))}{dg(x)}$가 아님)

> [!summary]- 유도 과정
> $$\{f(g(x))\}' = \frac{d}{dx}f(g(x))$$
> 
> $df(g(x))$를 도함수로 표현하기 위해 함수 $f$의 독립변수인 $g(x)$의 차가 필요하므로, 분모분자에 $dg(x)$를 곱해주면
> 
> $$= \frac{df(g(x))}{dg(x)} \cdot \frac{dg(x)}{dx}$$
> 
> $$= f'(g(x)) \cdot g'(x)$$
> 
> $$\therefore \{f(g(x))\}' = f'(g(x)) \cdot g'(x)$$

#### 연습문제

**① $\{\sin^2 x\}'$를 구하여라**

> [!summary]- 풀이
> $$\{\sin^2 x\}' = \{(\sin x)^2\}' = 2\sin x \cdot \cos x = \sin 2x$$

**② $\{\sec^3 x\}'$를 구하여라**

> [!summary]- 풀이
> $$\{\sec^3 x\}' = \{(\sec x)^3\}' = 3\sec^2 x \cdot (\sec x)' = 3\sec^2 x \cdot \sec x \tan x = 3\sec^3 x \tan x$$

---

## 2. 매개변수 미분법, 음함수 미분법

### Thm (27): 매개변수 미분법, 음함수 미분법

#### (1) 매개변수로 나타내어진 함수의 미분법

미분가능한 두 함수 $x = f(t)$, $y = g(t)$에 대하여

$$\frac{dy}{dx} = \frac{g'(t)}{f'(t)}$$

> [!summary]- 유도 과정
> $\frac{dy}{dx}$의 분모분자에 $dt$를 나눠주면
> 
> $$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{g'(t)}{f'(t)}$$

**예) $x = \sin\theta$, $y = \cos\theta$일 때, $x^2 + y^2 = 1$의 $\frac{dy}{dx}$를 구하여라**

> [!summary]- 풀이
> $$\frac{dy}{dx} = \frac{(\cos\theta)'}{(\sin\theta)'} = \frac{-\sin\theta}{\cos\theta} = -\tan\theta$$

#### (2) 음함수의 미분법

$$\frac{d}{dx}(y^n) = ny^{n-1}\frac{dy}{dx} = ny^{n-1}y'$$

> [!summary]- 유도 과정
> $$\frac{d}{dx}(y^n) = \frac{d}{dy}(y^n) \cdot \frac{dy}{dx} = ny^{n-1} \cdot y'$$

> [!note]- 양함수, 음함수, 다가함수
> **양함수(explicit function)**: 종속변수와 독립변수가 분리된 함수
> $$y = f(x)$$
> 
> **음함수(implicit function)**: 종속변수가 독립변수와 분리되지 않은 관계식
> $$F(x, y) = 0$$
> 
> 예를 들어 원의 방정식 $x^2 + y^2 = 1$은 음함수이며, $F(x, y) = x^2 + y^2 - 1 = 0$으로 표현할 수 있다.
> 
> 이 음함수를 양함수로 표현하면 $y = \pm\sqrt{1-x^2}$가 되어 하나의 $x$에 두 개의 $y$가 대응하므로 함수의 정의에 어긋난다. 따라서 두 개의 양함수로 분리해야 한다:
> - $y = \sqrt{1-x^2}$ (상반원)
> - $y = -\sqrt{1-x^2}$ (하반원)
> 
> **다가함수(multivalued function)**: 이처럼 하나의 독립변수에 여러 종속변수가 대응하는 음함수

**예) 음함수 $2x^2 + y^2 = 4$의 도함수를 구하여라**

> [!summary]- 풀이
> 양변을 $x$에 관해 미분하면
> 
> $$\frac{d(2x^2)}{dx} + \frac{d(y^2)}{dx} = \frac{d(4)}{dx}$$
> 
> $$4x + 2y \cdot y' = 0$$
> 
> $$y' = -\frac{2x}{y}$$
> 
> 점 $(1, \sqrt{2})$에서의 접선의 기울기는
> 
> $$y'(1, \sqrt{2}) = -\frac{2 \cdot 1}{\sqrt{2}} = -\sqrt{2}$$

**예) $x \cdot \tan x + y^2 = 4$의 $\frac{dy}{dx}$를 구하여라**

> [!summary]- 풀이
> 양변을 $x$에 관해 미분하면
> 
> $$\frac{d(x \cdot \tan x)}{dx} + \frac{d(y^2)}{dx} = 0$$
> 
> $$\tan x + x \cdot \sec^2 x + 2y \cdot y' = 0$$
> 
> $$y' = -\frac{\tan x + x\sec^2 x}{2y}$$

---

## 3. 로그를 취하는 미분법

### Thm (28): 로그를 취하는 미분법

밑과 지수 둘 모두에 독립변수가 있거나, 몫의 미분으로 미분하기 복잡한 분수식을 미분할 때 **양변에 자연로그를 취하고 미분**한다.

**(1)** $y = x^x$ $\implies$ $y' = x^x(\ln x + 1)$

**(2)** $y = x^{\ln x}$ $\implies$ $y' = x^{\ln x} \cdot \frac{2\ln x}{x}$

> [!summary]- (1) $y = x^x$의 유도 과정
> 양변에 자연로그를 취하면
> 
> $$\ln y = \ln x^x = x \ln x$$
> 
> 양변을 $x$에 관해 미분하면
> 
> $$\frac{1}{y} \cdot y' = \ln x + x \cdot \frac{1}{x} = \ln x + 1$$
> 
> $$y' = y(\ln x + 1) = x^x(\ln x + 1)$$

> [!summary]- (2) $y = x^{\ln x}$의 유도 과정
> 양변에 자연로그를 취하면
> 
> $$\ln y = \ln x^{\ln x} = \ln x \cdot \ln x = (\ln x)^2$$
> 
> 양변을 $x$에 관해 미분하면
> 
> $$\frac{1}{y} \cdot y' = 2\ln x \cdot \frac{1}{x}$$
> 
> $$y' = y \cdot \frac{2\ln x}{x} = x^{\ln x} \cdot \frac{2\ln x}{x}$$

> [!note]- 절댓값 로그의 미분
> $$\{\ln |f(x)|\}' = \frac{f'(x)}{f(x)}$$
> 
> **유도**: $f(x) > 0$일 때 $\{\ln |f(x)|\}' = \frac{f'(x)}{f(x)}$
> 
> $f(x) < 0$일 때 $\{\ln |f(x)|\}' = \{\ln(-f(x))\}' = \frac{-f'(x)}{-f(x)} = \frac{f'(x)}{f(x)}$
> 
> 따라서 $\{\ln |f(x)|\}' = \{\ln f(x)\}'$

---

## 4. 예제

### 예제 144

곡선 $\sec^2(xy) = 2x$ 위의 점 $\left(1, \frac{\pi}{4}\right)$에서의 접선의 기울기를 구하여라.

> [!summary]- 풀이
> $\{\sec(xy)\}^2 = 2x$의 양변을 $x$로 미분하면
> 
> $$2\sec(xy) \cdot \{\sec(xy)\}' = 2$$
> 
> $$2\sec(xy) \cdot \sec(xy)\tan(xy) \cdot (xy)' = 2$$
> 
> $(xy)' = y + xy'$ (곱의 미분)이므로
> 
> $$2\sec(xy) \cdot \sec(xy) \cdot \tan(xy) \cdot (y + xy') = 2$$
> 
> $x = 1$, $y = \frac{\pi}{4}$ 대입:
> 
> $$2\sec\frac{\pi}{4} \cdot \sec\frac{\pi}{4} \cdot \tan\frac{\pi}{4} \cdot \left(\frac{\pi}{4} + y'\right) = 2$$
> 
> $$2 \cdot \sqrt{2} \cdot \sqrt{2} \cdot 1 \cdot \left(\frac{\pi}{4} + y'\right) = 2$$
> 
> $$4\left(\frac{\pi}{4} + y'\right) = 2$$
> 
> $$\pi + 4y' = 2$$
> 
> $$y' = \frac{2 - \pi}{4} = \frac{1}{2} - \frac{\pi}{4}$$

### 예제 145

음함수 $x + y\cos x = 1$에 대하여 $x = \pi$에서의 접선의 기울기를 구하여라.

> [!summary]- 풀이
> 양변을 $x$로 미분하면
> 
> $$1 + (y'\cos x + y \cdot (-\sin x)) = 0$$
> 
> $$1 + y'\cos x - y\sin x = 0$$
> 
> $x = \pi$일 때, 원래 식에서 $\pi + y\cos\pi = 1$이므로 $y(-1) = 1 - \pi$, 즉 $y = \pi - 1$
> 
> $x = \pi$ 대입: $\cos\pi = -1$, $\sin\pi = 0$
> 
> $$1 + y'(-1) - y \cdot 0 = 0$$
> 
> $$1 - y' = 0$$
> 
> $$y' = 1$$

### 예제 146

$f(x) = \left(\frac{1}{x}\right)^{\ln x}$일 때 $f'(e)$의 값을 구하여라.

> [!summary]- 풀이
> 양변에 자연로그를 취하면
> 
> $$\ln f(x) = \ln\left(\frac{1}{x}\right)^{\ln x} = \ln x \cdot \ln\left(\frac{1}{x}\right) = \ln x \cdot \ln x^{-1} = -(\ln x)^2$$
> 
> 양변을 $x$에 관해 미분하면
> 
> $$\frac{f'(x)}{f(x)} = -2\ln x \cdot \frac{1}{x}$$
> 
> $$f'(x) = f(x) \cdot \left(-\frac{2\ln x}{x}\right) = \left(\frac{1}{x}\right)^{\ln x} \cdot \left(-\frac{2\ln x}{x}\right)$$
> 
> $x = e$ 대입: $\ln e = 1$
> 
> $$f'(e) = \left(\frac{1}{e}\right)^1 \cdot \left(-\frac{2 \cdot 1}{e}\right) = \frac{1}{e} \cdot \left(-\frac{2}{e}\right) = -\frac{2}{e^2}$$

---

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 몫의 미분법, 합성함수의 미분법, 매개변수 미분법, 음함수 미분법, 로그 미분법의 적용 방법을 숙지하시오.)

---

## 관련 주제

- [[24-transcendental-continuity|초월함수의 연속과 미분가능성]]
- [[26-differentiation-methods-2|여러가지 함수의 미분법(2)]]

---

**학습 포인트:**
1. **몫의 미분법**: $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$ (분자: 미분 순서 주의)
2. **합성함수의 미분법**: 바깥 함수 먼저 미분 → 안쪽 함수 미분 (연쇄법칙)
3. **매개변수 미분법**: $\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$
4. **음함수 미분법**: $y$를 $x$의 함수로 보고 양변을 $x$로 미분, $\frac{d}{dx}(y^n) = ny^{n-1}y'$
5. **로그 미분법**: 밑과 지수에 모두 변수가 있을 때, 양변에 $\ln$을 취한 후 미분
