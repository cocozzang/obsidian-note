---
id: a7b2c4d6-e8f0-4a2b-9c1d-3e5f7a8b9c0d
aliases:
  - 여러가지 함수의 미분법(2)
  - 이계도함수
  - 매개변수 이계도함수
  - 합성함수 미분 응용
tags:
  - 이계도함수
  - 매개변수미분법
  - 합성함수미분법
  - 로그미분법
  - 몫의미분법
pages: 72-73
subject: 대학기초수학
title: 여러가지 함수의 미분법(2) - 이계도함수, 매개변수·합성함수·로그 미분법 응용
topics:
  - 매개변수 함수의 이계도함수
  - 로그 미분법 응용
  - 합성함수 미분법 응용
  - 몫의 미분법 응용
---

# 여러가지 함수의 미분법(2)

이 강의에서는 25강에서 배운 미분법들(매개변수 미분법, 합성함수 미분법, 로그 미분법, 몫의 미분법)을 다양한 예제에 응용한다.

---

## 1. 매개변수 함수의 이계도함수

매개변수로 표현된 함수 $x = f(t)$, $y = g(t)$의 이계도함수는 다음과 같이 구한다:

$$\frac{dy}{dx} = \frac{g'(t)}{f'(t)}$$

$$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{d}{dt}\left(\frac{dy}{dx}\right) \cdot \frac{dt}{dx} = \frac{d}{dt}\left(\frac{dy}{dx}\right) \cdot \frac{1}{\frac{dx}{dt}}$$

---

## 2. 예제

### 예제 147

$$\begin{cases} x = e^t + e^{-t} \\ y = e^t - e^{-t} \end{cases}$$

일 때 $\frac{d^2y}{dx^2}$을 구하여라.

> [!summary]- 풀이
> **1단계: 일계도함수 구하기**
> 
> $$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{e^t + e^{-t}}{e^t - e^{-t}} = \frac{x}{y}$$
> 
> **2단계: 이계도함수 구하기**
> 
> $\frac{dy}{dx} = \frac{x}{y}$를 $x$에 대해 한 번 더 미분한다. (몫의 미분법 적용)
> 
> $$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{x}{y}\right) = \frac{1 \cdot y - x \cdot y'}{y^2}$$
> 
> 여기서 $y' = \frac{dy}{dx} = \frac{x}{y}$이므로
> 
> $$= \frac{y - x \cdot \frac{x}{y}}{y^2} = \frac{y - \frac{x^2}{y}}{y^2} = \frac{\frac{y^2 - x^2}{y}}{y^2} = \frac{y^2 - x^2}{y^3}$$
> 
> $$\therefore \frac{d^2y}{dx^2} = \frac{y^2 - x^2}{y^3}$$

---

### 예제 148

함수 $f(x) = x^{\sin x}$ $(x > 0)$에 대하여

$$\lim_{h \to 0} \frac{f\left(\frac{\pi}{2} + 2h\right) - f\left(\frac{\pi}{2}\right)}{h}$$

의 값을 구하여라.

> [!summary]- 풀이
> **1단계: 극한식을 미분계수 형태로 변환**
> 
> $$\lim_{h \to 0} \frac{f\left(\frac{\pi}{2} + 2h\right) - f\left(\frac{\pi}{2}\right)}{h} = \lim_{h \to 0} \frac{f\left(\frac{\pi}{2} + 2h\right) - f\left(\frac{\pi}{2}\right)}{2h} \cdot 2 = 2f'\left(\frac{\pi}{2}\right)$$
> 
> **2단계: 로그 미분법으로 $f'(x)$ 구하기**
> 
> $f(x) = x^{\sin x}$의 양변에 자연로그를 취하면
> 
> $$\ln f(x) = \sin x \cdot \ln x$$
> 
> 양변을 $x$에 대해 미분하면
> 
> $$\frac{f'(x)}{f(x)} = \cos x \cdot \ln x + \sin x \cdot \frac{1}{x}$$
> 
> $$f'(x) = f(x) \cdot \left(\cos x \cdot \ln x + \frac{\sin x}{x}\right)$$
> 
> **3단계: $x = \frac{\pi}{2}$ 대입**
> 
> $$f\left(\frac{\pi}{2}\right) = \left(\frac{\pi}{2}\right)^{\sin\frac{\pi}{2}} = \left(\frac{\pi}{2}\right)^1 = \frac{\pi}{2}$$
> 
> $$f'\left(\frac{\pi}{2}\right) = \frac{\pi}{2} \cdot \left(\cos\frac{\pi}{2} \cdot \ln\frac{\pi}{2} + \frac{\sin\frac{\pi}{2}}{\frac{\pi}{2}}\right) = \frac{\pi}{2} \cdot \left(0 + \frac{1}{\frac{\pi}{2}}\right) = \frac{\pi}{2} \cdot \frac{2}{\pi} = 1$$
> 
> $$\therefore 2f'\left(\frac{\pi}{2}\right) = 2 \times 1 = 2$$

---

### 예제 149

함수 $f(x) = e^{3x} + \cos x$와 실수 전체에서 미분가능한 두 함수 $g(x)$, $h(x)$가 있다. 합성함수 $P(x) = (h \circ g \circ f)(x)$에 대해 $P'(0) = 12$일 때 $(h \circ g)'(2)$의 값을 구하여라.

> [!summary]- 풀이
> **1단계: 합성함수의 미분 (연쇄법칙)**
> 
> $$P'(x) = h'(g(f(x))) \cdot g'(f(x)) \cdot f'(x)$$
> 
> **2단계: $f(0)$, $f'(0)$ 계산**
> 
> $$f(x) = e^{3x} + \cos x$$
> 
> $$f(0) = e^0 + \cos 0 = 1 + 1 = 2$$
> 
> $$f'(x) = 3e^{3x} - \sin x$$
> 
> $$f'(0) = 3e^0 - \sin 0 = 3 - 0 = 3$$
> 
> **3단계: $P'(0) = 12$ 조건 적용**
> 
> $$P'(0) = h'(g(f(0))) \cdot g'(f(0)) \cdot f'(0)$$
> 
> $$= h'(g(2)) \cdot g'(2) \cdot 3 = 12$$
> 
> $$\therefore h'(g(2)) \cdot g'(2) = 4$$
> 
> **4단계: $(h \circ g)'(2)$ 계산**
> 
> 합성함수의 미분법에 의해
> 
> $$(h \circ g)'(2) = h'(g(2)) \cdot g'(2) = 4$$

---

### 예제 150

곡선 $x = \theta - \sin\theta$, $y = 1 - \cos\theta$에 대하여 기울기가 1인 접선의 $y$절편을 구하여라. (단, $0 < \theta < \pi$)

> [!summary]- 풀이
> **1단계: $\frac{dy}{dx}$ 구하기**
> 
> $$\frac{dy}{dx} = \frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}} = \frac{\sin\theta}{1 - \cos\theta}$$
> 
> **2단계: 기울기가 1인 점 찾기**
> 
> $$\frac{\sin\theta}{1 - \cos\theta} = 1$$
> 
> $$\sin\theta = 1 - \cos\theta$$
> 
> $$\sin\theta + \cos\theta = 1$$
> 
> 삼각함수의 합성: $\sqrt{2}\sin\left(\theta + \frac{\pi}{4}\right) = 1$
> 
> $$\sin\left(\theta + \frac{\pi}{4}\right) = \frac{1}{\sqrt{2}}$$
> 
> $$\theta + \frac{\pi}{4} = \frac{\pi}{4} \text{ 또는 } \frac{3\pi}{4}$$
> 
> $$\theta = 0 \text{ 또는 } \frac{\pi}{2}$$
> 
> 조건 $0 < \theta < \pi$에서 $\theta = \frac{\pi}{2}$
> 
> **3단계: 접점 좌표 계산**
> 
> $$x = \frac{\pi}{2} - \sin\frac{\pi}{2} = \frac{\pi}{2} - 1$$
> 
> $$y = 1 - \cos\frac{\pi}{2} = 1 - 0 = 1$$
> 
> 접점: $\left(\frac{\pi}{2} - 1, 1\right)$
> 
> **4단계: 접선의 방정식과 $y$절편**
> 
> 기울기 1, 점 $\left(\frac{\pi}{2} - 1, 1\right)$을 지나는 직선:
> 
> $$y - 1 = 1 \cdot \left(x - \frac{\pi}{2} + 1\right)$$
> 
> $$y = x - \frac{\pi}{2} + 2$$
> 
> $$\therefore y\text{절편} = 2 - \frac{\pi}{2}$$

---

### 예제 151

$x = \cos^3\theta$, $y = \sin^3\theta$일 때 $\left[\frac{d^2y}{dx^2}\right]_{\theta = \frac{\pi}{4}}$의 값을 구하여라.

> [!summary]- 풀이
> **1단계: 일계도함수 구하기**
> 
> $$\frac{dx}{d\theta} = 3\cos^2\theta \cdot (-\sin\theta) = -3\cos^2\theta\sin\theta$$
> 
> $$\frac{dy}{d\theta} = 3\sin^2\theta \cdot \cos\theta$$
> 
> $$\frac{dy}{dx} = \frac{\frac{dy}{d\theta}}{\frac{dx}{d\theta}} = \frac{3\sin^2\theta\cos\theta}{-3\cos^2\theta\sin\theta} = -\frac{\sin\theta}{\cos\theta} = -\tan\theta$$
> 
> **2단계: 이계도함수 구하기**
> 
> $$\frac{d^2y}{dx^2} = \frac{d}{dx}(-\tan\theta) = \frac{d}{d\theta}(-\tan\theta) \cdot \frac{d\theta}{dx}$$
> 
> $\frac{d\theta}{dx} = \frac{1}{\frac{dx}{d\theta}} = \frac{1}{-3\cos^2\theta\sin\theta}$이므로
> 
> $$\frac{d^2y}{dx^2} = (-\sec^2\theta) \cdot \frac{1}{-3\cos^2\theta\sin\theta} = \frac{\sec^2\theta}{3\cos^2\theta\sin\theta}$$
> 
> **3단계: $\theta = \frac{\pi}{4}$ 대입**
> 
> $$\sec^2\frac{\pi}{4} = (\sqrt{2})^2 = 2$$
> 
> $$\cos^2\frac{\pi}{4} = \left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{2}$$
> 
> $$\sin\frac{\pi}{4} = \frac{1}{\sqrt{2}}$$
> 
> $$\left[\frac{d^2y}{dx^2}\right]_{\theta = \frac{\pi}{4}} = \frac{2}{3 \cdot \frac{1}{2} \cdot \frac{1}{\sqrt{2}}} = \frac{2}{\frac{3}{2\sqrt{2}}} = 2 \cdot \frac{2\sqrt{2}}{3} = \frac{4\sqrt{2}}{3}$$

---

### 예제 152

함수 $f(x) = \frac{(x-1)^3}{x^3 + x^2}$일 때 $f'(2)$의 값을 구하여라.

> [!summary]- 풀이
> **몫의 미분법 적용**
> 
> $f(x) = \frac{(x-1)^3}{x^3 + x^2}$에서
> 
> 분자: $(x-1)^3$, 분자의 미분: $3(x-1)^2$
> 
> 분모: $x^3 + x^2 = x^2(x+1)$, 분모의 미분: $3x^2 + 2x$
> 
> $$f'(x) = \frac{3(x-1)^2 \cdot (x^3 + x^2) - (x-1)^3 \cdot (3x^2 + 2x)}{(x^3 + x^2)^2}$$
> 
> **$x = 2$ 대입하여 계산**
> 
> - $(x-1)^2 = 1$, $(x-1)^3 = 1$
> - $x^3 + x^2 = 8 + 4 = 12$
> - $3x^2 + 2x = 12 + 4 = 16$
> 
> $$f'(2) = \frac{3 \cdot 1 \cdot 12 - 1 \cdot 16}{12^2} = \frac{36 - 16}{144} = \frac{20}{144} = \frac{5}{36}$$

---

### 예제 153

함수 $f(x) = \frac{x^6(x-1)^5(x-2)^4}{(x-3)^3(x-4)^2}$일 때, $\lim_{x \to 6} \frac{f'(x)}{f(x)}$의 값을 구하여라.

> [!summary]- 풀이
> **로그 미분법 적용**
> 
> 양변에 절댓값 자연로그를 취하면
> 
> $$\ln|f(x)| = 6\ln|x| + 5\ln|x-1| + 4\ln|x-2| - 3\ln|x-3| - 2\ln|x-4|$$
> 
> 양변을 $x$에 대해 미분하면
> 
> $$\frac{f'(x)}{f(x)} = \frac{6}{x} + \frac{5}{x-1} + \frac{4}{x-2} - \frac{3}{x-3} - \frac{2}{x-4}$$
> 
> **$x = 6$ 대입**
> 
> $$\lim_{x \to 6} \frac{f'(x)}{f(x)} = \frac{6}{6} + \frac{5}{5} + \frac{4}{4} - \frac{3}{3} - \frac{2}{2}$$
> 
> $$= 1 + 1 + 1 - 1 - 1 = 1$$

---

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 매개변수 함수의 이계도함수, 합성함수의 연쇄법칙, 로그 미분법의 응용 방법을 숙지하시오.)

---

## 관련 주제

- [[25-differentiation-methods-1|여러가지 함수의 미분법(1)]]
- [[27-differentiation-methods-3|여러가지 함수의 미분법(3)]]

---

**학습 포인트:**
1. **매개변수 함수의 이계도함수**: $\frac{d^2y}{dx^2} = \frac{d}{dt}\left(\frac{dy}{dx}\right) \cdot \frac{1}{\frac{dx}{dt}}$
2. **극한과 미분계수 관계**: $\lim_{h \to 0} \frac{f(a+kh) - f(a)}{h} = kf'(a)$
3. **삼중 합성함수의 미분**: $(h \circ g \circ f)'(x) = h'(g(f(x))) \cdot g'(f(x)) \cdot f'(x)$
4. **로그 미분법의 활용**: 복잡한 곱·몫의 분수식은 로그를 취하면 $\frac{f'(x)}{f(x)}$ 형태로 간단하게 계산 가능
