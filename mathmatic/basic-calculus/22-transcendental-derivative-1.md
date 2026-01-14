---
id: f8a3c2d1-7e4b-4f9a-b5c8-6d2e1a9f0b3c
aliases:
  - 초월함수의 도함수(1)
  - 삼각함수의 도함수
  - 지수로그함수의 도함수
tags:
  - 초월함수
  - 도함수
  - 삼각함수미분
  - 지수함수미분
  - 로그함수미분
pages: 63
subject: 대학기초수학
title: 초월함수의 도함수(1) - 삼각함수와 지수·로그함수의 도함수
topics:
  - 삼각함수의 도함수 공식
  - 지수함수의 도함수 공식
  - 로그함수의 도함수 공식
  - 도함수 유도 과정
---

# 초월함수의 도함수(1)

## 1. 삼각함수의 도함수

### Thm (24): 삼각함수의 도함수

|   함수   |      도함수      |
| :------: | :--------------: |
| $\sin x$ |     $\cos x$     |
| $\cos x$ |    $-\sin x$     |
| $\tan x$ |    $\sec^2 x$    |
| $\cot x$ |   $-\csc^2 x$    |
| $\sec x$ | $\sec x \tan x$  |
| $\csc x$ | $-\csc x \cot x$ |

### 삼각함수 도함수의 유도

#### ① $(\sin x)' = \cos x$

> [!summary]- 유도 과정
> $f(x) = \sin x$로 놓으면
>
> $$(\sin x)' = \lim_{h \to 0} \frac{\sin(x+h) - \sin x}{h}$$
>
> [[11-advanced-trigonometry-4#합차를 곱으로 변환하는 공식|합차를 곱으로 변환하는 공식]]을 적용하면
>
> $$= \lim_{h \to 0} \frac{2\cos\left(x + \frac{h}{2}\right) \sin\left(\frac{h}{2}\right)}{h}$$
>
> 분모를 $\frac{h}{2}$로 맞추면
>
> $$= \lim_{h \to 0} \frac{\cos\left(x + \frac{h}{2}\right) \cdot \sin\left(\frac{h}{2}\right)}{\frac{h}{2}}$$
>
> $\lim_{t \to 0} \frac{\sin t}{t} = 1$을 적용하면
>
> $$= \lim_{h \to 0} \cos\left(x + \frac{h}{2}\right) = \cos x$$
>
> $$\therefore (\sin x)' = \cos x$$

#### ② $(\cos x)' = -\sin x$

> [!summary]- 유도 과정
> $f(x) = \cos x$로 놓으면
>
> $$(\cos x)' = \lim_{h \to 0} \frac{\cos(x+h) - \cos x}{h}$$
>
> 합차를 곱으로 변환하는 공식을 적용하면
>
> $$= \lim_{h \to 0} \frac{-2\sin\left(x + \frac{h}{2}\right) \sin\left(\frac{h}{2}\right)}{h}$$
>
> $$= \lim_{h \to 0} -\sin\left(x + \frac{h}{2}\right) \cdot \frac{\sin\left(\frac{h}{2}\right)}{\frac{h}{2}}$$
>
> $$= -\sin x \cdot 1 = -\sin x$$
>
> $$\therefore (\cos x)' = -\sin x$$

#### ③ $(\tan x)' = \sec^2 x$

> [!summary]- 유도 과정
> 몫의 미분법: $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$
>
> $$(\tan x)' = \left(\frac{\sin x}{\cos x}\right)' = \frac{(\sin x)' \cos x - \sin x (\cos x)'}{\cos^2 x}$$
>
> $$= \frac{\cos x \cdot \cos x - \sin x \cdot (-\sin x)}{\cos^2 x}$$
>
> $$= \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x$$
>
> $$\therefore (\tan x)' = \sec^2 x$$

#### ④ $(\cot x)' = -\csc^2 x$

> [!summary]- 유도 과정
> $$(\cot x)' = \left(\frac{\cos x}{\sin x}\right)' = \frac{(-\sin x) \sin x - \cos x \cdot \cos x}{\sin^2 x}$$
>
> $$= \frac{-\sin^2 x - \cos^2 x}{\sin^2 x} = \frac{-1}{\sin^2 x} = -\csc^2 x$$
>
> $$\therefore (\cot x)' = -\csc^2 x$$

#### ⑤ $(\sec x)' = \sec x \tan x$

> [!summary]- 유도 과정
> $$(\sec x)' = \left(\frac{1}{\cos x}\right)' = \frac{0 \cdot \cos x - 1 \cdot (-\sin x)}{\cos^2 x}$$
>
> $$= \frac{\sin x}{\cos^2 x} = \frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} = \sec x \tan x$$
>
> $$\therefore (\sec x)' = \sec x \tan x$$

#### ⑥ $(\csc x)' = -\csc x \cot x$

> [!summary]- 유도 과정
> $$(\csc x)' = \left(\frac{1}{\sin x}\right)' = \frac{0 \cdot \sin x - 1 \cdot \cos x}{\sin^2 x}$$
>
> $$= \frac{-\cos x}{\sin^2 x} = \frac{-1}{\sin x} \cdot \frac{\cos x}{\sin x} = -\csc x \cot x$$
>
> $$\therefore (\csc x)' = -\csc x \cot x$$

---

## 2. 지수·로그함수의 도함수

### Thm (25): 지수·로그함수의 도함수

|     함수     |              도함수              |
| :--------: | :---------------------------: |
|   $e^x$    |             $e^x$             |
|   $a^x$    |          $a^x \ln a$          |
|  $\ln x$   | $\frac{1}{x}$, $\frac{x'}{x}$ |
| $\log_a x$ |      $\frac{1}{x \ln a}$      |

### 지수함수 도함수의 유도

#### ① $(e^x)' = e^x$, $(a^x)' = a^x \ln a$

> [!summary]- 유도 과정
> $f(x) = a^x$로 놓으면
>
> $$(a^x)' = \lim_{h \to 0} \frac{a^{x+h} - a^x}{h} = \lim_{h \to 0} \frac{a^x(a^h - 1)}{h}$$
>
> $$= a^x \cdot \lim_{h \to 0} \frac{a^h - 1}{h}$$
>
> [[13-transcendental-limit-1#(3) 극한값 e의 정리|극한값 e의 정리]]에서 $\lim_{h \to 0} \frac{a^h - 1}{h} = \ln a$이므로
>
> $$= a^x \cdot \ln a$$
>
> $$\therefore (a^x)' = a^x \ln a$$
>
> 특히 $a = e$일 때, $\ln e = 1$이므로
>
> $$(e^x)' = e^x$$

**예제**: $(3^{2x})'$를 구하시오.

> [!summary]- 풀이
> 합성함수의 미분법을 적용하면
>
> $$(3^{2x})' = 3^{2x} \cdot \ln 3 \cdot (2x)' = 2 \cdot 3^{2x} \cdot \ln 3$$

### 로그함수 도함수의 유도

#### ② $(\ln x)' = \frac{1}{x}$, $(\log_a x)' = \frac{1}{x \ln a}$

> [!summary]- 유도 과정
> $f(x) = \log_a x$로 놓으면
>
> $$(\log_a x)' = \lim_{h \to 0} \frac{\log_a(x+h) - \log_a x}{h}$$
>
> $$= \lim_{h \to 0} \frac{1}{h} \log_a\left(\frac{x+h}{x}\right) = \lim_{h \to 0} \frac{1}{h} \log_a\left(1 + \frac{h}{x}\right)$$
> 
> $$=\lim_{ h \to 0 } \log_{a}\left( 1+\frac{h}{x} \right)^{\frac{1}{h}}=\lim_{ h \to 0 } \log_{a}\left( 1+\frac{h}{x} \right)^{\frac{x}{h}\cdot\frac{1}{x} }$$
>
> $$= \log_{a}e^{\frac{1}{x}}=\frac{1}{x}\cdot \frac{1}{\ln a}=\frac{1}{x\cdot \ln a}$$
>
> $$\therefore (\log_a x)' = \frac{1}{x \ln a}$$
>
> 특히 $a = e$일 때, $\ln e = 1$이므로
>
> $$(\ln x)' = \frac{1}{x}$$

**예제**: $(\log_2 3x^3)'$를 구하시오.

> [!summary]- 풀이
> 합성함수의 미분법을 적용하면
>
> $$(\log_2 3x^3)' = \frac{1}{3x^3 \cdot \ln 2} \cdot (3x^3)'$$
>
> $$= \frac{1}{3x^3 \cdot \ln 2} \cdot 9x^2 = \frac{9x^2}{3x^3 \cdot \ln 2}$$
>
> $$= \frac{3}{x \cdot \ln 2}$$

---

## 3. 공식 암기 팁

### 삼각함수 도함수 암기법

```
        sin → cos (양)
        ↑         ↓
      -cos ← -sin (음)
```

- $\sin$을 미분하면 $\cos$ (부호 유지)
- $\cos$를 미분하면 $-\sin$ (부호 변환)
- **co-** 가 붙은 함수($\cos$, $\cot$, $\csc$)의 도함수는 **음수**

### 지수·로그함수 암기법

- $e^x$는 미분해도 자기 자신
- $a^x$는 미분하면 $\ln a$가 곱해짐
- $\ln x$의 도함수는 $\frac{1}{x}$
- $\log_a x$의 도함수는 $\frac{1}{x}$에 $\frac{1}{\ln a}$가 곱해짐

---

## 연습문제
$(\sin x)'$
$(\cos x)'$
$(\tan x)'$
$(\cot x)'$
$(\sec x)'$
$(\csc x)'$
$(e^{x})'$
$(a^{x})'$
$(\ln x)'$
$(\log_{a}x)'$


다음 함수의 도함수를 구하시오.

(1) $y = \sin 2x$

(2) $y = e^{3x}$

(3) $y = \ln(x^2 + 1)$

(4) $y = \tan x + \sec x$

---

## 관련 주제

- [[21-differentiability|21강: 미분가능성]]
- [[23-transcendental-derivative-2|23강: 초월함수의 도함수(2)]]
- [[11-advanced-trigonometry-4|11강: 심화삼각함수(4) - 기타공식]]
- [[13-transcendental-limit-1|13강: 초월함수의 극한(1)]]

---

**학습 포인트:**

1. 삼각함수 6개의 도함수 공식을 정확히 암기할 것
2. 지수·로그함수의 도함수에서 밑이 $e$인 경우와 일반적인 경우를 구분할 것
3. 도함수 유도 과정에서 극한의 정의와 기본 극한 공식의 활용법을 이해할 것
4. co-함수($\cos$, $\cot$, $\csc$)의 도함수는 음의 부호를 가진다는 규칙 기억할 것
