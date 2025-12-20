---
id: 18-derivative-3
aliases:
  - 변화율과 도함수(3)
  - 미분계수를 이용한 극한 계산
  - 도함수의 극한 응용
tags:
  - 미분계수
  - 극한계산
  - 도함수응용
  - 우함수미분
  - 기함수미분
  - 미분불능
pages: 51-54
subject: 대학기초수학
title: 변화율과 도함수(3) - 미분계수를 이용한 극한 계산
topics:
  - 미분계수를 이용한 극한 계산
  - 우함수와 기함수의 미분
  - 미분계수 극한 공식
  - 미분불능점
---

# 변화율과 도함수(3)

## 1. 미분계수를 이용한 복잡한 극한 계산

### 예제 98: 다항함수의 극한 변형

**문제**: 다항함수 $f(x)$에 대하여 $f'(2)=3$일 때 $\lim_{x \to 2} \frac{x^3-8}{f(x)-f(2)}$를 구하여라.

> [!summary]- 풀이
> 분자를 인수분해하고 미분계수의 정의를 이용한다.
>
> $$\lim_{x \to 2} \frac{x^3-8}{f(x)-f(2)} = \lim_{x \to 2} \frac{(x-2)(x^2+2x+4)}{f(x)-f(2)} \cdot \frac{\frac{1}{x-2}}{\frac{1}{x-2}}$$
>
> $$= \lim_{x \to 2} \frac{x^2+2x+4}{\frac{f(x)-f(2)}{x-2}}$$
>
> 분모는 $f'(2)$로 수렴하므로:
>
> $$= \lim_{x \to 2} \frac{x^2+2x+4}{f'(2)} = \frac{4+4+4}{3} = \frac{12}{3} = 4$$

### 예제 99: 우함수와 기함수의 성질 활용

**문제**: 다항함수 $f(x)$에 대하여 $f(-x)=f(x)$, $f'(3)=6$, $f'(9)=-8$일 때, $\lim_{x \to -3} \frac{f(x^2)-f(9)}{f(x)-f(3)}$를 구하여라.

**참고**:

- $f(x)$가 우함수이면, $f(-x)=f(x)$
- $f'(x)$는 기함수가 된다: $f'(-x)=-f'(x)$

> [!summary]- 풀이
> 우함수의 성질을 이용하여 $f(3)=f(-3)$임을 알 수 있다.
>
> $$\lim_{x \to -3} \frac{f(x^2)-f(9)}{f(x)-f(3)} = \lim_{x \to -3} \frac{\frac{f(x^2)-f(9)}{x^2-9} \cdot (x^2-9)}{\frac{f(x)-f(-3)}{x-(-3)} \cdot (x+3)}$$
>
> 미분계수의 정의를 적용하면:
>
> $$= \lim_{x \to -3} \frac{f'(9) \cdot (x^2-9)}{f'(-3) \cdot (x+3)}$$
>
> $f'$는 기함수이므로 $f'(-3)=-f'(3)=-6$이고, $x^2-9=(x-3)(x+3)$를 이용하면:
>
> $$= \lim_{x \to -3} \frac{-8 \cdot (x-3)(x+3)}{-6 \cdot (x+3)} = \frac{-8 \cdot (-6)}{-6} = -8$$

### 예제 100: 제곱근 형태의 극한

**문제**: 다항함수 $f(x)$에 대하여 $f(2)=9$, $f'(2)=2$일 때, $\lim_{x \to 2} \frac{\sqrt{f(x)}-\sqrt{f(2)}}{\sqrt{x}-\sqrt{2}}$를 구하라.

> [!summary]- 풀이
> 분자와 분모를 유리화한다.
>
> $$\lim_{x \to 2} \frac{\sqrt{f(x)}-\sqrt{f(2)}}{\sqrt{x}-\sqrt{2}} = \lim_{x \to 2} \frac{f(x)-f(2)}{x-2} \cdot \frac{\sqrt{x}+\sqrt{2}}{\sqrt{f(x)}+\sqrt{f(2)}}$$
>
> 미분계수의 정의를 적용하면:
>
> $$= \lim_{x \to 2} f'(2) \cdot \frac{\sqrt{x}+\sqrt{2}}{\sqrt{f(x)}+\sqrt{f(2)}}$$
>
> $$= 2 \cdot \frac{2\sqrt{2}}{\sqrt{9}+\sqrt{9}} = 2 \cdot \frac{2\sqrt{2}}{6} = \frac{2\sqrt{2}}{3}$$

### 예제 101: 일반적인 극한 공식 증명

**문제**: $\lim_{x \to a} \frac{x^n f(a) - a^n f(x)}{x-a} = na^{n-1}f(a) - a^n f'(a)$임을 보여라.

> [!summary]- 풀이
> 극한을 두 부분으로 나눈다.
>
> $$\lim_{x \to a} \frac{x^n f(a) - a^n f(x)}{x-a} = \lim_{x \to a} \frac{x^n f(a)}{x-a} - \lim_{x \to a} \frac{a^n f(x)}{x-a}$$
>
> 각 항에 $f(a)$를 더하고 빼서 정리하면:
>
> $$= \lim_{x \to a} \frac{x^n f(a) - a^n f(a)}{x-a} - \lim_{x \to a} \frac{a^n f(x) - a^n f(a)}{x-a}$$
>
> $$= \lim_{x \to a} \frac{x^n - a^n}{x-a} \cdot f(a) - \lim_{x \to a} \frac{f(x) - f(a)}{x-a} \cdot a^n$$
>
> $x^n - a^n = (x-a)(x^{n-1} + ax^{n-2} + a^2 x^{n-3} + \cdots + a^{n-1})$이므로:
>
> $$= \lim_{x \to a} (x^{n-1} + ax^{n-2} + a^2 x^{n-3} + \cdots + a^{n-1}) \cdot f(a) - \lim_{x \to a} f'(a) \cdot a^n$$
>
> $$= na^{n-1} \cdot f(a) - f'(a) \cdot a^n$$

## 2. Thm 20: 미분계수를 이용한 극한 계산 공식

### 정리 20

**(1)** $\lim_{h \to 0} \frac{f(a+mh) - f(a+nh)}{h} = (m-n)f'(a)$

**(2)** $\lim_{n \to \infty} n\left\{f\left(a+\frac{k}{n}\right) - f(a)\right\} = k \cdot f'(a)$

### 공식 유도

**(1)의 유도 과정**:

$$\lim_{h \to 0} \frac{f(a+mh) - f(a+nh)}{h} = \lim_{h \to 0} \frac{f(a+mh) - f(a+nh)}{(a+mh) - (a+nh)} \times (m-n)$$

$$= (m-n) \cdot f'(a)$$

**(2)의 유도 과정**:

$$\lim_{n \to \infty} n\left\{f\left(a+\frac{k}{n}\right) - f(a)\right\} = \lim_{n \to \infty} n \cdot \frac{k}{n} \cdot \frac{f\left(a+\frac{k}{n}\right) - f(a)}{\frac{k}{n}}$$

$$= k \cdot f'(a)$$

## 3. 예제: 미분계수 극한 공식 활용

### 예제 102: 공식 (1) 적용

**문제**: 다항함수 $f(x)$에 대하여 $f'(1)=4$일 때, $\lim_{h \to 0} \frac{f(1-3h) - f(1+4h)}{h}$를 구하여라.

> [!summary]- 풀이
> 미분계수 극한 공식을 적용한다.
>
> $$\lim_{h \to 0} \frac{f(1-3h) - f(1+4h)}{h} = \lim_{h \to 0} \frac{f(1-3h) - f(1+4h)}{(1-3h) - (1+4h)} \cdot \frac{(1-3h) - (1+4h)}{h}$$
>
> $$= \lim_{h \to 0} f'(1) \cdot \frac{-7h}{h} = -7f'(1) = -7 \times 4 = -28$$

### 예제 103: 미지수 결정 문제

**문제**: 다항함수 $f(x)$에 대하여 $f'(3)=6$이고 $\lim_{h \to 0} \frac{f(3+ph) - f(3-qh)}{h} = 12$일 때, $p+q$의 값을 구하라.

> [!summary]- 풀이
> 공식 (1)을 적용하면:
>
> $$\lim_{h \to 0} \frac{f(3+ph) - f(3-qh)}{h} = \lim_{h \to 0} \frac{f(3+ph) - f(3-qh)}{(3+ph) - (3-qh)} \cdot \frac{(3+ph) - (3-qh)}{h}$$
>
> $$= \lim_{h \to 0} f'(3) \cdot \frac{(p+q)h}{h} = 12$$
>
> $$(p+q) \cdot 6 = 12$$
>
> $$p+q = 2$$

### 예제 104: 제곱항이 포함된 극한

**문제**: 다항함수 $f(x)$에 대하여 $f'(a)=4$일 때 $\lim_{h \to 0} \frac{f(a+2h) - f(a+h^2)}{h}$의 값을 구하여라.

> [!summary]- 풀이
> 분모를 $(a+2h) - (a+h^2) = 2h - h^2 = (2-h)h$로 표현한다.
>
> $$\lim_{h \to 0} \frac{f(a+2h) - f(a+h^2)}{h} = \lim_{h \to 0} \frac{f(a+2h) - f(a+h^2)}{(2-h)h} \cdot (2-h)$$
>
> $$= 2 \cdot f'(a) = 2 \times 4 = 8$$

### 예제 105: 공식 (2) 적용

**문제**: 다항함수 $f(x)$에 대하여 $\lim_{n \to \infty} n\left\{f\left(a+\frac{b}{n}\right) - f\left(a-\frac{b}{n}\right)\right\}$의 값을 구하여라 (단, $b \neq 0$).

> [!summary]- 풀이
> 극한을 변형하여 미분계수의 정의를 적용한다.
>
> $$\lim_{n \to \infty} n\left\{f\left(a+\frac{b}{n}\right) - f\left(a-\frac{b}{n}\right)\right\} = \lim_{n \to \infty} n \cdot \frac{f\left(a+\frac{b}{n}\right) - f\left(a-\frac{b}{n}\right)}{\frac{2b}{n}} \cdot \frac{2b}{n}$$
>
> $$= 2b \cdot f'(a)$$

### 예제 106: 접선의 기울기 활용

**문제**: 미분가능한 함수 $y=f(x)$의 그래프 위의 한 점 $P(2,1)$에서의 접선의 방정식이 $y=3x-5$일 때, $\lim_{n \to \infty} \frac{n}{2}\left\{f\left(2+\frac{1}{3n}\right) - f(2)\right\}$의 값을 구하여라.

> [!summary]- 풀이
> 접선의 기울기로부터 $f'(2)=3$임을 알 수 있다.
>
> $$\lim_{n \to \infty} \frac{n}{2}\left\{f\left(2+\frac{1}{3n}\right) - f(2)\right\} = \lim_{n \to \infty} \frac{n}{2} \cdot \frac{f\left(2+\frac{1}{3n}\right) - f(2)}{\frac{1}{3n}} \cdot \frac{1}{3n}$$
>
> $$= \frac{1}{6} \cdot f'(2) = \frac{1}{6} \times 3 = \frac{1}{2}$$

### 예제 107: 합성함수의 미분 (오류 분석 포함)

**문제**: 함수 $f(x)=(1+x)^{100}$일 때 $\lim_{n \to \infty} n\left\{f\left(1+\frac{1}{n}\right) - f(1)\right\}$의 값을 구하여라.

**⚠️ 흔한 오류**:

$f(1)=2^{100}$ (상수)이므로 $f'(1)=0$이라고 잘못 생각하는 경우

**오류 분석**: $f(1)$의 결과가 상수라고 해서 $f'(1)=0$은 아니다.

- $f(x)=2$처럼 함수 전체가 상수일 때만 $f'(x)=0$이다.
- $f(x)=(1+x)^{100}$은 $x$의 변화에 따라 기울기가 달라지므로, $f'(x)$를 먼저 구한 후 $f'(1)$을 계산해야 한다.

> [!summary]- 올바른 풀이
> 먼저 $f(x)$를 미분한다.
>
> $$f'(x) = 100(1+x)^{99}$$
>
> 따라서:
>
> $$f'(1) = 100 \cdot 2^{99}$$
>
> 공식을 적용하면:
>
> $$\lim_{n \to \infty} n\left\{f\left(1+\frac{1}{n}\right) - f(1)\right\} = \lim_{n \to \infty} n \cdot \frac{f\left(1+\frac{1}{n}\right) - f(1)}{\frac{1}{n}} \cdot \frac{1}{n}$$
>
> $$= \frac{n}{n} \cdot f'(1) = f'(1) = 100 \cdot 2^{99}$$

## 4. 미분불능점

### 예제 108: 절댓값 함수의 미분불능

**문제**: 함수 $f(x)=|x-2|$일 때, $\lim_{h \to 0} \frac{f(2+h) - f(2-h)}{2h}$를 구하여라.

> [!summary]- 풀이
> **미분불능점**: 좌미분계수와 우미분계수가 다른 지점, 또는 불연속 함수의 끊어진 부분을 미분불능점이라 정의하고, 해당 지점에 대한 순간기울기를 정의할 수 없기 >때문에 미분하지 않는다.
> $f(x)=|x-2|$는 점 $(2,0)$에서 V자 형태의 그래프를 가진다.
>
> ```
>    y
>   \|      /
>    \     /
>    |\   /
>    | \ /
> ---+--●---------- x
>    0  2
>
>
> ```
>
> - $x<2$일 때: $f'(x)=-1$
> - $x>2$일 때: $f'(x)=1$
> - $x=2$일 때: 좌미분계수와 우미분계수가 다르므로 **미분불능**
>   이 문제는 미분계수가 아닌 단순 극한 문제로 풀어야 한다.
>
> $$\lim_{h \to 0} \frac{f(2+h) - f(2-h)}{2h} = \lim_{h \to 0} \frac{|2+h-2| - |2-h-2|}{2h}$$
>
> $$= \lim_{h \to 0} \frac{|h| - |-h|}{2h} = \lim_{h \to 0} \frac{h - h}{2h} = 0$$
>
> **답**: $0$

**주의**: 이 극한값이 0이라고 해서 $f'(2)=0$은 아니다. $f(x)$는 $x=2$에서 미분불능이므로 $f'(2)$는 정의되지 않는다.

## 연습문제

(각 예제를 통해 학습한 내용을 복습하고, 미분계수를 이용한 극한 계산 기법을 숙지하시오.)

## 관련 주제

- [[17-derivative-2|변화율과 도함수(2)]]
- [[19-polynomial-equation|다항함수의 함수방정식]]

---

**학습 포인트:**

1. **미분계수를 이용한 극한 계산**: $\lim_{x \to a} \frac{f(x)-f(a)}{x-a} = f'(a)$ 형태로 변형하여 계산
2. **미분계수 극한 공식**:
   - $\lim_{h \to 0} \frac{f(a+mh)-f(a+nh)}{h} = (m-n)f'(a)$
   - $\lim_{n \to \infty} n\{f(a+\frac{k}{n})-f(a)\} = kf'(a)$
3. **우함수와 기함수의 미분**: 우함수 $f(x)$의 도함수 $f'(x)$는 기함수
4. **미분불능점**: 좌미분계수 ≠ 우미분계수인 점에서는 미분계수가 정의되지 않음
