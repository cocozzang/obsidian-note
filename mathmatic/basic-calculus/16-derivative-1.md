---
id: 7a3f8b2c-4d5e-4f1a-9c8d-2e6f7a9b1c3d
aliases:
  - 변화율과 도함수(1)
  - 미분의 정의
  - 평균변화율
  - 순간변화율
  - 도함수
tags:
  - 미분법
  - 변화율
  - 평균변화율
  - 순간변화율
  - 도함수
  - 미분공식
  - 접선의기울기
pages: 46-47
subject: 대학기초수학
title: 변화율과 도함수(1) - 미분의 정의
topics:
  - 평균변화율과 순간변화율
  - 도함수의 정의
  - 기본 미분공식
  - 미분공식 유도
---

# 변화율과 도함수(1)

## 1. 변화율의 개념

### Def (2): 변화율

함수 $y=f(x)$의 변화율은 함수값의 변화량과 독립변수의 변화량 사이의 비율을 나타낸다.

#### (1) 평균변화율

구간 $[a, b]$에서 $y=f(x)$의 **평균변화율**은 $\frac{y의 \; 증분}{x의 \; 증분} = \frac{\Delta y}{\Delta x}$를 말한다.

$$\frac{\Delta y}{\Delta x} = \frac{f(b)-f(a)}{b-a} = \frac{f(a+\Delta x)-f(a)}{\Delta x}$$

이다.

**기하학적 의미**: 두 점 P와 Q를 지나는 직선의 기울기를 말한다.

**물리적 의미**: 평균속도를 말한다.

#### (2) 순간변화율

평균변화율의 극한값 즉, $\lim_{b \to a} \frac{f(b)-f(a)}{b-a} = \lim_{\Delta x \to 0} \frac{f(a+\Delta x)-f(a)}{\Delta x}$를

**순간 변화율**이라 하고 $f'(a)$로 표시한다.

**기하학적 의미**: 점 $P(a, f(a))$에서 $y=f(x)$에 접하는 접선의 기울기를 말한다.

**물리적 의미**: 순간속도를 말한다.

**요약**:
- (1) 평균변화율 $\Rightarrow$ 구간 $[a, b]$에서 곡선 $y=f(x)$의 기울기는 정도의 평균값을 말한다.
- (2) 순간변화율 $\Rightarrow$ 평균변화율의 극한값을 말한다.

---

## 2. 도함수의 정의

### Thm (19): 도함수

미분계수의 일반화 즉, 모든 $x$에 대한 미분계수 $f'(x)$를 함수 $f(x)$의 **도함수**라 하고 $f'(x)$, $y'$, $\frac{dy}{dx}$, $\frac{d}{dx}f(x)$ 등으로 표시한다.

$$f'(x) = \lim_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x} = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}$$

이다.

**도함수 표기법**:
- $f'(x)$ : 라그랑주 표기법
- $y'$ : 간단한 표기법
- $\frac{dy}{dx}$ : 라이프니츠 표기법
- $\frac{d}{dx}f(x)$ : 연산자 표기법

**순간변화율의 두 가지 표현**:

$$\lim_{b \to a} \frac{f(b)-f(a)}{b-a} = \lim_{\Delta x \to 0} \frac{f(a+\Delta x)-f(a)}{\Delta x} = f'(a)$$

$$\lim_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x} = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = f'(x)$$

---

## 3. 기본 미분공식

### (1) 미분법의 공식

다음은 미분법의 기본 공식들이다:

① $y=c \to y'=0$

② $y=x^n \to y'=nx^{n-1}$

③ $y=f(x)g(x) \to y'=f'(x)g(x)+f(x)g'(x)$

④ $y=\{f(x)\}^n \to y'=n\{f(x)\}^{n-1} \cdot f'(x)$

---

### 예제 1: $f(x)=x^2$의 미분

$f(x)=x^2$일 때, $f'(x)=2x$임을 유도하시오.

> [!summary]- 풀이
> 도함수의 정의를 이용한다.
> 
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{(x+h)^2-x^2}{h}$$
> 
> 분자를 전개하면:
> 
> $$= \lim_{h \to 0} \frac{x^2+2xh+h^2-x^2}{h} = \lim_{h \to 0} \frac{2xh+h^2}{h}$$
> 
> $h$로 약분하면:
> 
> $$= \lim_{h \to 0} \left(2x + h\right) = 2x$$
> 
> $$\therefore f(x)=x^2 \;,\; f'(x)=2x$$

### 예제 2: $f(x)=\sin x$의 미분

$f(x)=\sin x$일 때, $f'(x)=\cos x$임을 유도하시오.

> [!summary]- 풀이
> 도함수의 정의를 이용한다.
> 
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{\sin(x+h)-\sin x}{h}$$
> 
> 삼각함수의 합차공식 $\sin A - \sin B = 2\cos\left(\frac{A+B}{2}\right)\sin\left(\frac{A-B}{2}\right)$를 적용하면:
> 
> $$= \lim_{h \to 0} \frac{2\cos\left(\frac{x+h+x}{2}\right)\sin\left(\frac{h}{2}\right)}{h}$$
> 
> 정리하면:
> 
> $$= \lim_{h \to 0} \frac{2}{h} \cdot \cos\left(\frac{2x}{2}+\frac{h}{2}\right) \cdot \sin\left(\frac{h}{2}\right)$$
> 
> $$= \lim_{h \to 0} \cos\left(x+\frac{h}{2}\right) \cdot \frac{\sin\left(\frac{h}{2}\right)}{\frac{h}{2}}$$
> 
> $\lim_{t \to 0} \frac{\sin t}{t} = 1$을 이용하면:
> 
> $$= \cos x \cdot 1 = \cos x$$
> 
> $$\therefore f(x)=\sin x \;,\; f'(x)=\cos x$$

---

## 5. 미분공식 유도

### 공식 ①: $y=c \to y'=0$

상수함수의 미분은 0이다.

> [!summary]- 유도
> $f(x)=c$일 때:
> 
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{c-c}{h} = \lim_{h \to 0} \frac{0}{h} = 0$$
> 
> **설명**: $c-c$는 0이고, $\frac{0}{h}=0$이므로 극한값도 0이다.

### 공식 ②: $y=x^n \to y'=nx^{n-1}$

거듭제곱 함수의 미분공식이다.

> [!summary]- 유도
> **일반화된 합차공식**:
> 
> $$a^n - b^n = (a-b)(a^{n-1} + a^{n-2} \cdot b + a^{n-3} \cdot b^2 + \cdots + b^{n-1})$$
> 
> 예시:
> - $a^2-b^2 = (a-b)(a+b)$
> - $a^3-b^3 = (a-b)(a^2+ab+b^2)$
> 
> 도함수의 정의를 적용하면:
> 
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{(x+h)^n - x^n}{h}$$
> 
> 합차공식을 이용하면:
> 
> $$= \lim_{h \to 0} \frac{h\left[(x+h)^{n-1} + (x+h)^{n-2} \cdot x + (x+h)^{n-3} \cdot x^2 + \cdots + x^{n-1}\right]}{h}$$
> 
> $h$로 약분하면:
> 
> $$= \lim_{h \to 0} \left[(x+h)^{n-1} + (x+h)^{n-2} \cdot x + (x+h)^{n-3} \cdot x^2 + \cdots + x^{n-1}\right]$$
> 
> $h \to 0$을 대입하면:
> 
> $$= (x+0)^{n-1} + (x+0)^{n-2} \cdot x + (x+0)^{n-3} \cdot x^2 + \cdots + x^{n-1}$$
> 
> $$= x^{n-1} + x^{n-2} \cdot x + x^{n-3} \cdot x^2 + \cdots + x^{n-1}$$
> 
> $$= x^{n-1} + x^{n-1} + x^{n-1} + \cdots + x^{n-1} \quad (n\text{개 항})$$
> 
> $$= nx^{n-1}$$
> 
> $$\therefore f(x)=x^n \;,\; f'(x)=nx^{n-1}$$

### 공식 ③: $y=f(x)g(x) \to y'=f'(x)g(x)+f(x)g'(x)$

두 함수의 곱의 미분공식이다.

> [!summary]- 유도
> $F(x) = f(x)g(x)$로 놓으면:
> 
> $$F'(x) = \lim_{h \to 0} \frac{F(x+h)-F(x)}{h} = \lim_{h \to 0} \frac{f(x+h) \cdot g(x+h) - f(x) \cdot g(x)}{h}$$
> 
> 분자를 변형하기 위해 $f(x)g(x+h)$를 빼고 더한다:
> 
> $$= \lim_{h \to 0} \frac{f(x+h) \cdot g(x+h) - f(x)g(x+h) + f(x)g(x+h) - f(x) \cdot g(x)}{h}$$
> 
> 두 항으로 분리하면:
> 
> $$= \lim_{h \to 0} \frac{f(x+h) \cdot g(x+h) - f(x)g(x+h)}{h} + \lim_{h \to 0} \frac{f(x)g(x+h) - f(x) \cdot g(x)}{h}$$
> 
> 공통인수를 묶으면:
> 
> $$= \lim_{h \to 0} \frac{[f(x+h)-f(x)] \cdot g(x+h)}{h} + \lim_{h \to 0} \frac{f(x) \cdot [g(x+h)-g(x)]}{h}$$
> 
> 극한을 분리하면:
> 
> $$= \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} \cdot \lim_{h \to 0} g(x+h) + f(x) \cdot \lim_{h \to 0} \frac{g(x+h)-g(x)}{h}$$
> 
> $g(x)$가 연속이므로 $\lim_{h \to 0} g(x+h) = g(x)$이다:
> 
> $$= f'(x) \cdot g(x) + f(x) \cdot g'(x)$$
> 
> $$\therefore [f(x)g(x)]' = f'(x)g(x) + f(x)g'(x)$$

### 공식 ④: $y=\{f(x)\}^n \to y'=n\{f(x)\}^{n-1} \cdot f'(x)$

합성함수의 미분공식 (연쇄법칙)이다.

> [!summary]- 유도
> $F(x) = \{f(x)\}^n$로 놓으면:
> 
> $$F'(x) = \lim_{h \to 0} \frac{F(x+h)-F(x)}{h} = \lim_{h \to 0} \frac{\{f(x+h)\}^n - \{f(x)\}^n}{h}$$
> 
> 합차공식 $a^n - b^n = (a-b)(a^{n-1} + a^{n-2}b + \cdots + b^{n-1})$를 적용하면:
> 
> $$= \lim_{h \to 0} \frac{\{f(x+h)-f(x)\} \cdot \left[\{f(x+h)\}^{n-1} + \{f(x+h)\}^{n-2} \cdot f(x) + \cdots + \{f(x)\}^{n-1}\right]}{h}$$
> 
> 극한을 분리하면:
> 
> $$= \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} \cdot \lim_{h \to 0} \left[\{f(x+h)\}^{n-1} + \{f(x+h)\}^{n-2} \cdot f(x) + \cdots + \{f(x)\}^{n-1}\right]$$
> 
> $h \to 0$일 때, $f(x+h) \to f(x)$ (연속성)이므로:
> 
> $$= f'(x) \cdot \left[\{f(x)\}^{n-1} + \{f(x)\}^{n-2} \cdot f(x) + \cdots + \{f(x)\}^{n-1}\right]$$
> 
> 대괄호 안은 $\{f(x)\}^{n-1}$이 $n$개 있으므로:
> 
> $$= f'(x) \cdot n\{f(x)\}^{n-1}$$
> 
> $$\therefore [\{f(x)\}^n]' = n\{f(x)\}^{n-1} \cdot f'(x)$$

---

## 6. 연습문제

1. 평균변화율과 순간변화율의 기하학적 의미를 설명하시오.
2. 도함수의 정의를 이용하여 $f(x)=x^3$의 도함수를 구하시오.
3. 곱의 미분법을 이용하여 $(x^2 \cdot \sin x)'$를 계산하시오.

(각 예제를 통해 학습한 내용을 복습하고, 미분의 정의와 기본 공식의 유도과정을 숙지하시오.)

---

## 7. 관련 주제

- [[15-transcendental-limit-3|초월함수의 극한(3)]]
- [[17-derivative-2|변화율과 도함수(2)]]
- [[01-function-limit-1|함수의 극한(1)]]

---

**학습 포인트:**
1. 평균변화율은 할선의 기울기, 순간변화율은 접선의 기울기를 의미한다.
2. 도함수는 순간변화율을 일반화한 개념이다.
3. 기본 미분공식 4개를 유도과정과 함께 이해해야 한다.
4. 합차공식을 활용한 거듭제곱 미분의 유도가 핵심이다.
5. 곱의 미분과 합성함수의 미분은 각각 독립적인 공식으로 기억한다.
