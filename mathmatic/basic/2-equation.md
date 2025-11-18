---
id: 6fe05559-4deb-4d4f-89de-bdcdae28d856
aliases:
  - 방정식
  - 부등식
  - 곱셈공식
tags:
  - 집합
  - 명제
lecture: 큐스터디 썡기초수학
title: 2강 방정식, 부등식
topics:
  - 곱셈공식과 변형
  - 인수분해 공식
  - 일차방정식
  - 이차방정식 (근의 공식, 판별식, 근과 계수의 관계)
  - 삼차, 사차 방정식
  - 일차부등식
  - 이차부등식
  - 절댓값을 포함한 방정식과 부등식
---

## 부록 1: 곱셈공식

### 기본 공식

(1) $(a+b)^2 = a^2 + 2ab + b^2$, $(a-b)^2 = a^2 - 2ab + b^2$

(2) $(a+b)(a-b) = a^2 - b^2$

(3) $(x+a)(x+b) = x^2 + (a+b)x + ab$

(4) $(ax+b)(cx+d) = acx^2 + (ad+bc)x + bd$

(5) $(x+a)(x+b)(x+c) = x^3 + (a+b+c)x^2 + (ab+bc+ca)x + abc$
$(x-a)(x-b)(x-c) = x^3 - (a+b+c)x^2 + (ab+bc+ca)x - abc$

(6) $(a+b+c)^2 = a^2 + b^2 + c^2 + 2(ab+bc+ca)$
$a^2 + b^2 + c^2 = (a+b+c)^2 - 2(ab+bc+ca)$

(7) $(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3$
$(a-b)^3 = a^3 - 3a^2b + 3ab^2 - b^3$

(8) $a^3 + b^3 = (a+b)^3 - 3ab(a+b)$
$a^3 - b^3 = (a-b)^3 + 3ab(a-b)$

(9) $a^3 + b^3 + c^3 - 3abc = (a+b+c)(a^2+b^2+c^2-ab-bc-ca)$
$= \frac{1}{2}(a+b+c)\{(a-b)^2 + (b-c)^2 + (c-a)^2\}$

(10) $(a^2+ab+b^2)(a^2-ab+b^2) = a^4 + a^2b^2 + b^4$

(11) $(a+b)(b+c)(c+a) = (a+b+c)(ab+bc+ca) - abc$

---

## 부록 2: 곱셈공식의 변형

(1) $a^2 + b^2 = (a+b)^2 - 2ab = (a-b)^2 + 2ab$

(2) $x^2 + \frac{1}{x^2} = \left(x + \frac{1}{x}\right)^2 - 2$

(3) $a^3 + b^3 = (a+b)^3 - 3ab(a+b)$, $a^3 - b^3 = (a-b)^3 + 3ab(a-b)$

(4) $x^3 + \frac{1}{x^3} = \left(x + \frac{1}{x}\right)^3 - 3\left(x + \frac{1}{x}\right)$

(5) $(x-y)^2 = (x+y)^2 - 4xy$

(6) $\left(x - \frac{1}{x}\right)^2 = \left(x + \frac{1}{x}\right)^2 - 4$

(7) $x^5 + y^5 = (x^2+y^2)(x^3+y^3) - x^2y^2(x+y)$

(8) $x^7 + y^7 = (x^3+y^3)(x^4+y^4) - x^3y^3(x+y)$

(9) $a^2 + b^2 + c^2 = (a+b+c)^2 - 2(ab+bc+ca)$

(10) $a^2 + b^2 + c^2 - ab - bc - ca = \frac{1}{2}\{(a-b)^2 + (b-c)^2 + (c-a)^2\}$

(11) $a^3 + b^3 + c^3 - 3abc = (a+b+c)(a^2+b^2+c^2-ab-bc-ca)$
$\Rightarrow a+b+c=0$ or $a=b=c$

**증명**:
$a^3 + b^3 + c^3 - 3abc = (a+b+c)(a^2+b^2+c^2-ab-bc-ca)$
$= \frac{1}{2}(a+b+c)\{(a-b)^2 + (b-c)^2 + (c-a)^2\} = 0$ 이 되어
$a+b+c=0$ 또는 $a=b=c$가 된다.

---

## 부록 3: 인수분해 공식

① $ma \pm mb = m(a \pm b)$

② $a^2 \pm 2ab + b^2 = (a \pm b)^2$

③ $a^2 - b^2 = (a+b)(a-b)$

④ $x^2 \pm (a+b)x + ab = (x \pm a)(x \pm b)$

⑤ $acx^2 \pm (ad+bc)x \pm bd = (ax \pm b)(cx \pm d)$

⑥ $a^2 + b^2 + c^2 + 2ab + 2bc + 2ca = (a+b+c)^2$

⑦ $a^4 + a^2b^2 + b^4 = (a^2+ab+b^2)(a^2-ab+b^2)$

⑧ $a^3 + 3a^2b + 3ab^2 + b^3 = (a+b)^3$
$a^3 - 3a^2b + 3ab^2 - b^3 = (a-b)^3$

⑨ $a^3 + b^3 = (a+b)(a^2-ab+b^2)$
$a^3 - b^3 = (a-b)(a^2+ab+b^2)$

**중요**:

- $x^3 + 1 = (x+1)(x^2-x+1)$
- $x^3 - 1 = (x-1)(x^2+x+1)$

⑩ $a^3 + b^3 + c^3 - 3abc = (a+b+c)(a^2+b^2+c^2-ab-bc-ca)$
$x^3 + (a+b+c)x^2 + (ab+bc+ca)x + abc = (x+a)(x+b)(x+c)$
$x^3 - (a+b+c)x^2 + (ab+bc+ca)x - abc = (x-a)(x-b)(x-c)$

⑫ $(a+b+c)(ab+bc+ca) - abc = (a+b)(b+c)(c+a)$

**증명**:
$(a+b+c)(ab+bc+ca) - abc$
$= a^2b + abc + ca^2 + ab^2 + b^2c + abc + bc^2 + c^2a - abc$
$= (b+c)a^2 + (b^2+2bc+c^2)a + bc(b+c)$
$= (b+c)\{a^2 + (b+c)a + bc\}$
$= (b+c)(a+b)(a+c)$
$= (a+b)(b+c)(c+a)$

---

## 3. 방정식

### 01 일차방정식

#### (1) 기본 형태

$ax = b$를 풀어라.

#### (2) 절댓값 기호를 포함한 일차방정식

$\sqrt{a^2} = |a| = \begin{cases}
a, & a \geq 0 \\
-a, & a < 0
\end{cases}$

**예제**: $|x| + |x-1| = 3$을 풀어라.

---

### 02 이차방정식

#### (1) $ax^2 + bx + c = 0$ $(a \neq 0)$의 풀이

① **인수분해를 이용한 풀이**:
$x^2 - 5x + 6 = 0 \Rightarrow (x-2)(x-3) = 0$
$\therefore x = 2 \text{ 또는 } x = 3$

② **완전제곱식을 이용한 풀이**:

$ax^2 + bx + c = 0 \to a\left(x + \frac{b}{2a}\right)^2 = \frac{b^2-4ac}{4a}$
$\to \left(x + \frac{b}{2a}\right)^2 = \frac{b^2-4ac}{4a^2}$
$\to x + \frac{b}{2a} = \pm\sqrt{\frac{b^2-4ac}{4a^2}}$

$\therefore x = -\frac{b}{2a} \pm \frac{\sqrt{b^2-4ac}}{2a}$

③ **근의 공식을 이용한 풀이**:
$x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$

**짝수공식**: $ax^2 + 2b'x + c = 0$의 해
$x = \frac{-b' \pm \sqrt{b'^2-ac}}{a}$

**근의 공식 유도과정**:

$ax^2 + bx + c = 0 \to x^2 + \frac{b}{a}x + \frac{c}{a} = 0$
$\to x^2 + \frac{b}{a}x = -\frac{c}{a}$
$\to x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 = -\frac{c}{a} + \left(\frac{b}{2a}\right)^2$
$\to \left(x + \frac{b}{2a}\right)^2 = \frac{b^2-4ac}{4a^2}$
$\to x + \frac{b}{2a} = \pm\frac{\sqrt{b^2-4ac}}{2a}$
$\therefore x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$

#### (2) 판별식 $D = b^2 - 4ac$ (또는 $D' = b'^2 - ac$)

① $D > 0$ : 서로 다른 두 실근
② $D = 0$ : 중근
③ $D < 0$ : 허근

#### (3) 근과 계수와의 관계

$ax^2 + bx + c = 0$ $(a \neq 0)$의 두 근을 $\alpha, \beta$라 하면

$\alpha = \frac{-b + \sqrt{b^2-4ac}}{2a}, \quad \beta = \frac{-b - \sqrt{b^2-4ac}}{2a}$

에 대하여

$\alpha + \beta = -\frac{b}{a}, \quad \alpha\beta = \frac{c}{a}$

#### (4) 이차방정식의 작성

두 근이 $\alpha, \beta$인 이차방정식은:
$x^2 - (\alpha+\beta)x + \alpha\beta = 0$
$\Rightarrow a\{x^2 - (\alpha+\beta)x + \alpha\beta\} = 0$

**예제 1**: 이차방정식 $x^2 - 4x + 2 = 0$의 두 근을 $\alpha, \beta$라 할 때 $\alpha^2 + \beta^2$의 값은?

**풀이**:
근과 계수의 관계에서 $\alpha + \beta = 4$, $\alpha\beta = 2$
$\alpha^2 + \beta^2 = (\alpha+\beta)^2 - 2\alpha\beta = 4^2 - 2(2) = 16 - 4 = 12$

**예제 2**: $x^2 + 2x + 3 = 0$의 두 근을 $\alpha, \beta$라 할 때 $\alpha^2, \beta^2$을 두 근으로 하는 이차방정식은?

**풀이**:
$\alpha + \beta = -2$, $\alpha\beta = 3$
$\alpha^2 + \beta^2 = (\alpha+\beta)^2 - 2\alpha\beta = 4 - 6 = -2$
$\alpha^2\beta^2 = (\alpha\beta)^2 = 9$
$\therefore x^2 - (-2)x + 9 = 0 \Rightarrow x^2 + 2x + 9 = 0$

---

### 03 삼, 사차 방정식

**예제 1**: $x^3 - 2x^2 - x + 2 = 0$의 해를 구하라.

**풀이**: 인수분해를 이용
$x^3 - 2x^2 - x + 2 = x^2(x-2) - (x-2)$
$= (x-2)(x^2-1) = (x-2)(x-1)(x+1) = 0$
$\therefore x = -1, 1, 2$

**예제 2**: $x^4 - 5x^3 + 6x^2 + 2x - 4 = 0$의 해를 구하라.

**풀이**:
인수정리를 이용하거나 인수분해 시도
$x = 1$을 대입: $1 - 5 + 6 + 2 - 4 = 0$ (해!)
$x = 2$를 대입: $16 - 40 + 24 + 4 - 4 = 0$ (해!)

$(x-1)(x-2)$로 나누면:
$x^4 - 5x^3 + 6x^2 + 2x - 4 = (x-1)(x-2)(x^2-2x+2)$

$x^2-2x+2 = 0$의 해: $x = \frac{2 \pm \sqrt{4-8}}{2} = \frac{2 \pm 2i}{2} = 1 \pm i$

$\therefore x = 1, 2, 1+i, 1-i$

---

## 4. 부등식

### 기본성질

① $a > b, b > c \to a > c$

② $a > b \to a + c > b + c$, $a - c > b - c$

③ $a > b$일 때

- $c > 0$이면 $ac > bc$, $\frac{a}{c} > \frac{b}{c}$
- $c < 0$이면 $ac < bc$, $\frac{a}{c} < \frac{b}{c}$

---

### 01 일차부등식

#### (1) 기본 형태

$ax > b$를 풀어라.

**예제**: $3x - 5 > 2x + 1$
$3x - 2x > 1 + 5$
$x > 6$

#### (2) 절댓값 기호를 포함한 부등식

① $|x| < a \to -a < x < a$

② $|x| \geq b \to x \geq b$ 또는 $x \leq -b$

③ $a \leq |x| < b \to a < x < b$ 또는 $-b < x < -a$

---

### 02 이차부등식

이차부등식 $ax^2 + bx + c = 0$ $(a > 0)$의 서로 다른 두 실근을 $\alpha, \beta$ $(\alpha < \beta)$라 하면

① $ax^2 + bx + c > 0 \Leftrightarrow a(x-\alpha)(x-\beta) > 0 \Rightarrow x > \beta$(큰 근), $x < \alpha$(작은 근)

**"$x$는 큰 것보다 크고, 작은 것보다 작다."**

② $ax^2 + bx + c < 0 \Leftrightarrow a(x-\alpha)(x-\beta) < 0 \Rightarrow \alpha < x < \beta$

**"$x$는 두 근 사이"**

③ $ax^2 + bx + c \geq 0 \Leftrightarrow a(x-\alpha)(x-\beta) \geq 0 \Rightarrow x \geq \beta$(큰 근), $x \leq \alpha$(작은 근)

**"$x$는 큰 것보다 크거나 같고, 작은 것보다 작거나 같다."**

④ $ax^2 + bx + c \leq 0 \Leftrightarrow a(x-\alpha)(x-\beta) \leq 0 \Rightarrow \alpha \leq x \leq \beta$

**"$x$는 두 근 사이"**

---

**예제 1**: $x$에 대한 부등식 $2x - a < bx + 3$의 해가 존재하지 않을 때 $a+b$의 최댓값은?

**풀이**:
$2x - a < bx + 3$
$(2-b)x < a + 3$

해가 존재하지 않으려면:

- $2 - b = 0$이고 $a + 3 \leq 0$
- 즉, $b = 2$이고 $a \leq -3$

$a+b$의 최댓값: $-3 + 2 = -1$

---

**예제 2**: $x^2 - 2x - 15 < 0$을 풀어라.

**풀이**:
$x^2 - 2x - 15 = (x-5)(x+3) < 0$

두 근: $x = -3, 5$

$\therefore -3 < x < 5$

---

**예제 3**: $|x-1| + |x+2| < 5$를 풀어라.

**풀이**: 절댓값 기호를 경우를 나누어 풀기

① $x < -2$일 때:
$-(x-1) - (x+2) < 5$
$-x+1-x-2 < 5$
$-2x < 6$
$x > -3$
$\therefore -3 < x < -2$

② $-2 \leq x < 1$일 때:
$-(x-1) + (x+2) < 5$
$-x+1+x+2 < 5$
$3 < 5$ (항상 참)
$\therefore -2 \leq x < 1$

③ $x \geq 1$일 때:
$(x-1) + (x+2) < 5$
$2x+1 < 5$
$x < 2$
$\therefore 1 \leq x < 2$

**최종 답**: $-3 < x < 2$

---

**예제 4**: 이차부등식 $x^2 + px + q < 0$의 해가 $-1 < x < 3$일 때, 이차부등식 $x^2 + (p-1)x + (q-1) < 0$의 해가 $\alpha < x < \beta$라고 한다. $\alpha + \beta$를 구하면?

**풀이**:
주어진 조건에서:
$x^2 + px + q = (x+1)(x-3) = x^2 - 2x - 3$

따라서 $p = -2, q = -3$

새로운 부등식:
$x^2 + (-2-1)x + (-3-1) < 0$
$x^2 - 3x - 4 < 0$
$(x-4)(x+1) < 0$

$\therefore -1 < x < 4$

$\alpha = -1, \beta = 4$

$\alpha + \beta = -1 + 4 = 3$

---

## 정리

### 방정식 풀이 전략

1. **일차방정식**: 양변을 정리하여 $x$를 분리
2. **이차방정식**:
   - 인수분해 가능 → 인수분해
   - 인수분해 불가능 → 근의 공식
3. **고차방정식**: 인수정리, 인수분해 활용

### 부등식 풀이 전략

1. **일차부등식**: 일차방정식과 유사하게 풀되, 음수로 나눌 때 부등호 방향 바뀜 주의
2. **이차부등식**:
   - 인수분해하여 두 근 구하기
   - 두 근 사이인지, 두 근 밖인지 판단
3. **절댓값 부등식**: 경우를 나누어 풀기
