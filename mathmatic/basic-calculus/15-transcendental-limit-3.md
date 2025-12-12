---
id: 15-transcendental-limit-3
aliases:
  - 초월함수의 극한(3)
  - 초월함수 극한 문제풀이
  - 미정계수 극한 문제
tags:
  - 초월함수
  - 극한문제풀이
  - 삼각함수의극한
  - 지수함수의극한
  - 미정계수
  - 연속성
  - 극한과연속
pages: 43-45
subject: 대학기초수학
title: 초월함수의 극한(3) - 종합 문제풀이
topics:
  - 초월함수 극한 응용
  - 미정계수 문제
  - 연속성과 극한
  - 극한의 치환
---

# 초월함수의 극한(3) - 종합 문제풀이

## 1. 개요

이 강의는 **Thm 18 (초월함수의 기본극한)**을 활용한 종합 문제풀이입니다. 개념 설명 없이 예제 문제만으로 구성되어 있으며, 다양한 유형의 극한 문제를 다룹니다.

### 복습: Thm 18 핵심 공식

**삼각함수의 극한:**
$$\lim_{x \to 0} \frac{\sin x}{x} = 1, \quad \lim_{x \to 0} \frac{\tan x}{x} = 1$$

**반각공식을 이용한 극한:**
$$\lim_{x \to 0} \frac{1-\cos x}{x^2} = \frac{1}{2}$$

**지수·로그 함수의 극한:**
$$\lim_{x \to 0} \frac{a^x - 1}{x} = \ln a, \quad \lim_{x \to 0} \frac{\ln(x+1)}{x} = 1$$

---

## 2. 예제 문제

### 예제 80

$$\lim_{x \to 0} \frac{1-\cos x}{ax\sin x + b} = \frac{1}{2}$$

일 때, $a+b$의 값을 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to 0$일 때 분모 $\to 0$이어야 하므로, 먼저 $b=0$임을 확인한다.
>
> $x \to 0$일 때 분자 $\to 0$이므로, 극한값이 존재하려면 분모도 $\to 0$이어야 한다.
>
> $$\lim_{x \to 0}(ax\sin x + b) = 0 + b = 0 \quad \therefore b = 0$$
>
> 이제 $b=0$을 대입하여 극한값을 계산:
>
> $$\lim_{x \to 0} \frac{1-\cos x}{ax\sin x} = \frac{1}{2}$$
>
> 반각공식 $1-\cos x = 2\sin^2 \frac{x}{2}$를 이용:
>
> $$\lim_{x \to 0} \frac{2\sin^2 \frac{x}{2}}{ax\sin x} = \lim_{x \to 0} \frac{2\sin^2 \frac{x}{2}}{ax \cdot 2\sin\frac{x}{2}\cos\frac{x}{2}}$$
>
> $$= \lim_{x \to 0} \frac{\sin\frac{x}{2}}{ax\cos\frac{x}{2}} = \lim_{x \to 0} \frac{1}{a} \cdot \frac{\sin\frac{x}{2}}{\frac{x}{2}} \cdot \frac{1}{2\cos\frac{x}{2}}$$
>
> $$= \frac{1}{a} \cdot 1 \cdot \frac{1}{2} = \frac{1}{2a}$$
>
> 주어진 조건에서:
>
> $$\frac{1}{2a} = \frac{1}{2} \quad \therefore a = 1$$
>
> $$\boxed{a + b = 1 + 0 = 1}$$

---

### 예제 81

$$\lim_{x \to a} \frac{5^x - 1}{3\sin(x-a)} = b\ln 5$$

일 때, $a+b$의 값을 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to a$일 때 분모 $\to 0$이므로, 분자도 $\to 0$이어야 한다.
>
> 따라서 $\lim_{x \to a}(5^x - 1) = 5^a - 1 = 0$에서 $5^a = 1$
>
> $$\therefore a = 0$$
>
> 이제 $a=0$을 대입하여 극한값 계산:
>
> $$\lim_{x \to 0} \frac{5^x - 1}{3\sin x}$$
>
> 분자와 분모를 각각 $x$로 나누어 정리:
>
> $$= \lim_{x \to 0} \frac{\frac{5^x-1}{x}}{3 \cdot \frac{\sin x}{x}} = \frac{\ln 5}{3 \cdot 1} = \frac{\ln 5}{3}$$
>
> 주어진 조건에서:
>
> $$\frac{\ln 5}{3} = b\ln 5 \quad \therefore b = \frac{1}{3}$$
>
> $$\boxed{a + b = 0 + \frac{1}{3} = \frac{1}{3}}$$

---

### 예제 82

$$\lim_{x \to 0} \frac{\sin^2 x}{a - b\cos x} = 3$$

일 때, $a^2 + b^2$의 값을 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to 0$일 때 분자 $\to 0$이므로, 분모도 $\to 0$이어야 한다.
>
> $$\lim_{x \to 0}(a - b\cos x) = a - b = 0 \quad \therefore b = a$$
>
> 이제 $b=a$를 대입:
>
> $$\lim_{x \to 0} \frac{\sin^2 x}{a - a\cos x} = \lim_{x \to 0} \frac{\sin^2 x}{a(1-\cos x)}$$
>
> 반각공식 $1-\cos x = 2\sin^2 \frac{x}{2}$를 이용:
>
> $$= \lim_{x \to 0} \frac{\sin^2 x}{a \cdot 2\sin^2 \frac{x}{2}}$$
>
> $$\lim_{x \to 0}\frac{x^2}{a \cdot 2 \cdot \frac{x^2}{4}}=\lim_{x \to 0}\frac{1}{a \cdot 2 \cdot \frac{1}{4}}$$
> $$= \frac{1}{\frac{a}{2}}= \frac{2}{a}$$
>
> 주어진 조건에서:
>
> $$\frac{2}{a} = 3 \quad \therefore a = \frac{2}{3}$$
>
> $b = a = \frac{2}{3}$이므로:
>
> $$\boxed{a^2 + b^2 = \left(\frac{2}{3}\right)^2 + \left(\frac{2}{3}\right)^2 = \frac{4}{9} + \frac{4}{9} = \frac{8}{9}}$$

---

### 예제 83

$$\lim_{x \to \frac{\pi}{2}} \frac{\cos x}{\frac{\pi}{2} - x}$$

를 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to \frac{\pi}{2}$이므로 Thm 18을 직접 적용할 수 없다. 치환을 통해 $\theta \to 0$ 형태로 변환한다.
>
> $x - \frac{\pi}{2} = \theta$로 치환하면, $x = \frac{\pi}{2} + \theta$
>
> $x \to \frac{\pi}{2}$일 때, $\theta \to 0$
>
> $$\lim_{\theta \to 0} \frac{\cos\left(\frac{\pi}{2} + \theta\right)}{-\theta}$$
>
> 삼각함수 공식: $\cos\left(\frac{\pi}{2} + \theta\right) = -\sin\theta$
>
> $$= \lim_{\theta \to 0} \frac{-\sin\theta}{-\theta} = \lim_{\theta \to 0} \frac{\sin\theta}{\theta} = \boxed{1}$$

---

### 예제 84

$$\lim_{x \to -\frac{\pi}{6}} \frac{\sqrt{3}\sin x + \cos x}{6x + \pi}$$

를 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to -\frac{\pi}{6}$이므로 치환을 이용한다.
>
> $x + \frac{\pi}{6} = \theta$로 치환하면, $x = \theta - \frac{\pi}{6}$
>
> $x \to -\frac{\pi}{6}$일 때, $\theta \to 0$
>
> **분자 변형**:
>
> $\sqrt{3}\sin x + \cos x$를 삼각함수 합성 공식으로 변환:
> $\because \tan\alpha = \frac{1}{\sqrt3}   \therefore \alpha=\frac{\pi}{6}$
>
> $$\sqrt{3}\sin x + \cos x = 2\sin\left(x + \frac{\pi}{6}\right)=2\sin\theta$$
>
> **분모**:
> $$6x+\pi = 6(\theta-\frac{\pi}{6})+\pi=6\theta$$
>
> 준식 :
> $$\frac{2\sin\theta}{6\theta}=\frac{2}{6}=\frac{1}{3}$$

---

### 예제 85

$$\lim_{x \to 1} \frac{a\sin(x-1)}{x^3 + b} = 4$$

일 때, $a+b$를 구하여라.

    > [!summary]- 풀이

> **핵심**: $x \to 1$일 때 분자 $\to 0$이므로, 분모도 $\to 0$이어야 한다.
>
> $$\lim_{x \to 1}(x^3 + b) = 1 + b = 0 \quad \therefore b = -1$$
>
> 이제 $b=-1$을 대입:
>
> $$\lim_{x \to 1} \frac{a\sin(x-1)}{x^3 - 1}$$
>
> 분모를 인수분해: $x^3 - 1 = (x-1)(x^2 + x + 1)$
>
> $$= \lim_{x \to 1} \frac{a\sin(x-1)}{(x-1)(x^2+x+1)} = \lim_{x\to1}\frac{a}{x^2+x+1}=4$$
>
> $$\frac{a}{3}=4 \;,\; a=12$$
>
> $$\boxed{a + b = 12 + (-1) = 11}$$

---

### 예제 86

$$\lim_{x \to \infty} \frac{5x+1}{2}\tan\frac{2}{x-3}$$

의 값을 구하여라.

> [!summary]- 풀이
> **핵심**: $x \to \infty$이므로 치환을 통해 $\theta \to 0$ 형태로 변환한다.
>
> $\frac{2}{x-3} = \theta$로 치환하면, $x =3 + \frac{2}{\theta}$
>
> 준식:
> $$\lim_{\theta \to 0} \frac{5(3 + \frac{2}{\theta})+1}{2} \cdot \tan\theta$$
>
> $$= \lim_{\theta \to 0} \frac{16\theta + 10}{2\theta} \cdot \theta = 8\theta + 5= 5$$

---

### 예제 87

함수 $f(x) = \begin{cases} \frac{\sin 2(x-1)}{x-1} & (x \neq 1) \\ k & (x=1) \end{cases}$가 $x=1$에서 연속일 때, 상수 $k$를 구하여라.

> [!summary]- 풀이
> **핵심**: $f(x)$가 $x=1$에서 연속이려면 $\lim_{x \to 1}f(x) = f(1) = k$이어야 한다.
>
> $$k = \lim_{x \to 1} \frac{\sin 2(x-1)}{x-1}$$
>
> $x-1 = \theta$로 치환하면, $x \to 1$일 때 $\theta \to 0$:
>
> $$k = \lim_{\theta \to 0} \frac{\sin 2\theta}{\theta}$$
>
> $$= \lim_{\theta \to 0} \frac{\sin 2\theta}{2\theta} \cdot 2 = 1 \cdot 2 = \boxed{2}$$

---

### 예제 88

함수 $f(x) = \begin{cases} \frac{1-\cos x}{\sin^2 kx} & (x \neq 0) \\ 3 & (x=0) \end{cases}$가 $x=0$에서 연속일 때, 상수 $k^2$를 구하여라.

> [!summary]- 풀이
> **핵심**: $f(x)$가 $x=0$에서 연속이려면 $\lim_{x \to 0}f(x) = f(0) = 3$이어야 한다.
>
> $$3 = \lim_{x \to 0} \frac{1-\cos x}{\sin^2 kx}$$
>
> 반각공식 $1-\cos x = 2\sin^2 \frac{x}{2}$를 이용:
>
> $$= \lim_{x \to 0} \frac{2\sin^2 \frac{x}{2}}{\sin^2 kx}$$
>
> $$= \lim_{x \to 0} 2 \cdot \left(\frac{\sin\frac{x}{2}}{\frac{x}{2}}\right)^2 \cdot \frac{\left(\frac{x}{2}\right)^2}{\sin^2 kx}$$
>
> $$= 2 \cdot 1^2 \cdot \lim_{x \to 0} \frac{\frac{x^2}{4}}{\sin^2 kx}$$
>
> $$= \frac{1}{2} \cdot \lim_{x \to 0} \frac{x^2}{\sin^2 kx}$$
>
> $$= \frac{1}{2} \cdot \lim_{x \to 0} \frac{1}{\left(\frac{\sin kx}{kx}\right)^2} \cdot \frac{1}{k^2}$$
>
> $$= \frac{1}{2} \cdot \frac{1}{1^2} \cdot \frac{1}{k^2} = \frac{1}{2k^2}$$
>
> 주어진 조건에서:
>
> $$\frac{1}{2k^2} = 3 \quad \therefore k^2 = \frac{1}{6}$$
>
> $$\boxed{k^2 = \frac{1}{6}}$$

---

## 3. 연습문제

각 예제를 통해 다음 내용을 복습하시오:

1. **미정계수 결정 방법**: 극한값이 존재하려면 분자와 분모가 동시에 0으로 수렴해야 한다.
2. **치환의 활용**: $x \to a$ ($a \neq 0$)인 경우, $x-a = \theta$로 치환하여 $\theta \to 0$ 형태로 변환
3. **연속성 조건**: $\lim_{x \to a}f(x) = f(a)$
4. **반각공식 활용**: $1-\cos x = 2\sin^2 \frac{x}{2}$
5. **삼각함수 합성**: $a\sin x + b\cos x = \sqrt{a^2+b^2}\sin(x+\alpha)$ (단, $\tan\alpha = \frac{b}{a}$)

---

## 4. 관련 주제

- [[13-transcendental-limit-1|초월함수의 극한(1) - 기본극한값]]
- [[14-transcendental-limit-2|초월함수의 극한(2)]]
- [[16-derivative-intro-1|변화율과 도함수(1)]]

---

**학습 포인트:**

1. **미정계수 문제**: 극한값이 존재하는 조건을 이용하여 미지수를 결정
2. **치환의 중요성**: $x \to a$ 형태를 $\theta \to 0$ 형태로 변환하여 Thm 18 적용
3. **연속성과 극한**: 함수가 한 점에서 연속이기 위한 조건
4. **복합적 공식 활용**: 반각공식, 배각공식, 삼각함수 합성 등을 적절히 활용
5. **단계별 계산**: 복잡한 극한 문제는 단계를 나누어 차근차근 계산
