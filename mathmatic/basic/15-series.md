---
id: f6a7b8c9-d0e1-2f3a-4b5c-6d7e8f9a0b1c
aliases:
  - 무한급수
  - 급수
  - 부분합
tags:
  - 급수
  - 무한급수
  - 수렴
  - 발산
  - 무한등비급수
lecture: 큐스터디 썡기초수학
title: 15강 무한급수
topics:
  - 무한급수의 정의
  - 수렴과 발산
  - 무한급수의 수렴 조건
  - 무한등비급수
  - 무한급수의 성질
---

# 15. 수열의 극한과 무한급수 (계속)

## 02 무한급수

### (1) 정의

#### ① 무한급수

무한수열 $\{a_n\}$의 각 항을 더한 식:

$$a_1 + a_2 + a_3 + \cdots + a_n + \cdots$$

를 **무한급수**라고 하고 기호로 $\sum_{n=1}^{\infty} a_n$이라고 씁니다.

---

#### ② 부분합

무한급수 $\sum_{n=1}^{\infty} a_n$에서 첫째항부터 제$n$항까지의 합:

$$S_n = a_1 + a_2 + \cdots + a_n = \sum_{k=1}^{n} a_k$$

를 **제$n$항까지의 부분합** 또는 **$n$번째 부분합**이라고 합니다.

---

### (2) 무한급수의 수렴과 발산

무한급수 $\sum_{n=1}^{\infty} a_n$의 $n$번째 부분합을 $S_n = \sum_{k=1}^{n} a_k$라 할 때:

#### ① 무한급수의 합 (수렴)

수열 $\{S_n\}$이 일정한 값 $S$에 수렴하면:

$$\lim_{n \to \infty} S_n = S$$

무한급수 $\sum_{n=1}^{\infty} a_n$은 $S$에 **수렴**한다고 하고:

$$\sum_{n=1}^{\infty} a_n = S$$

---

#### ② 발산

$\{S_n\}$이 발산하면 $\sum_{n=1}^{\infty} a_n$도 **발산**한다

---

### 📝 예제 1

무한급수 $\sum_{n=1}^{\infty} \frac{1}{2^n}$의 수렴, 발산을 조사하고, 수렴하면 그 합을 구하여라.

**풀이**:

부분합:
$$S_n = \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \cdots + \frac{1}{2^n}$$

이는 첫째항 $\frac{1}{2}$, 공비 $\frac{1}{2}$인 등비수열의 합:

$$S_n = \frac{\frac{1}{2}(1 - (\frac{1}{2})^n)}{1 - \frac{1}{2}} = \frac{\frac{1}{2}(1 - \frac{1}{2^n})}{\frac{1}{2}} = 1 - \frac{1}{2^n}$$

$$\lim_{n \to \infty} S_n = \lim_{n \to \infty} \left(1 - \frac{1}{2^n}\right) = 1 - 0 = 1$$

따라서 **수렴**하고, 그 합은 **1**

---

### 📝 예제 2

무한급수 $\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$의 합을 구하여라.

**풀이**:

부분분수 분해:
$$\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}$$

부분합:
$$S_n = \sum_{k=1}^{n} \frac{1}{k(k+1)} = \sum_{k=1}^{n} \left(\frac{1}{k} - \frac{1}{k+1}\right)$$

$$= \left(1 - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \cdots + \left(\frac{1}{n} - \frac{1}{n+1}\right)$$

$$= 1 - \frac{1}{n+1} = \frac{n}{n+1}$$

$$\lim_{n \to \infty} S_n = \lim_{n \to \infty} \frac{n}{n+1} = 1$$

따라서 $\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = 1$

---

### (3) 무한급수의 수렴 조건

무한급수 $\sum_{n=1}^{\infty} a_n$이 수렴하면:

$$\lim_{n \to \infty} a_n = 0$$

**역은 성립하지 않음!**

즉, $\lim_{n \to \infty} a_n = 0$이어도 급수가 발산할 수 있음

---

### 중요한 판정법

#### ① $\lim_{n \to \infty} a_n \neq 0$이면

→ 급수는 **무조건 발산**

#### ② $\lim_{n \to \infty} a_n = 0$이면

→ 급수가 수렴할 **가능성 있음** (더 조사 필요)

---

### 📝 예제 3

다음 무한급수의 수렴, 발산을 판정하여라.

(1) $\sum_{n=1}^{\infty} \frac{n}{n+1}$

(2) $\sum_{n=1}^{\infty} \frac{1}{n^2}$

**풀이**:

(1) $\lim_{n \to \infty} \frac{n}{n+1} = 1 \neq 0$

→ **발산**

(2) $\lim_{n \to \infty} \frac{1}{n^2} = 0$

→ 수렴 가능성 있음 (실제로 수렴함, 나중에 증명)

---

### 📝 예제 4

두 수열 $\{a_n\}$, $\{b_n\}$에 대하여 무한급수:

$$\sum_{n=1}^{\infty} (3a_n + 2b_n), \quad \sum_{n=1}^{\infty} a_n$$

이 모두 수렴할 때, 다음 중 항상 수렴하는 것은?

① $\sum_{n=1}^{\infty} b_n$
② $\sum_{n=1}^{\infty} a_n b_n$
③ $\sum_{n=1}^{\infty} (a_n - b_n)$

**풀이**:

$\sum (3a_n + 2b_n) = 3\sum a_n + 2\sum b_n$이 수렴하고,
$\sum a_n$이 수렴하므로:

$$2\sum b_n = \sum (3a_n + 2b_n) - 3\sum a_n$$

우변이 수렴하므로 $\sum b_n$도 수렴

따라서 ① 항상 수렴 ✓

③도 $\sum a_n - \sum b_n$이므로 수렴 ✓

---

## (4) 무한등비급수

### ① 정의

첫째항이 $a$, 공비가 $r$인 등비수열:

$$a, ar, ar^2, ar^3, \cdots$$

의 무한급수:

$$\sum_{n=1}^{\infty} ar^{n-1} = a + ar + ar^2 + \cdots$$

를 **무한등비급수**라고 합니다.

---

### ② 무한등비급수의 수렴 조건과 합

공비 $r$에 따라:

#### **$|r| < 1$일 때**: 수렴

$$\sum_{n=1}^{\infty} ar^{n-1} = \frac{a}{1-r}$$

**유도**:

부분합 $S_n = \frac{a(1-r^n)}{1-r}$

$$\lim_{n \to \infty} S_n = \lim_{n \to \infty} \frac{a(1-r^n)}{1-r} = \frac{a(1-0)}{1-r} = \frac{a}{1-r}$$

($|r| < 1$이므로 $r^n \to 0$)

---

#### **$|r| \geq 1$일 때**: 발산

- $r = 1$: $a + a + a + \cdots$ → 발산
- $r = -1$: $a - a + a - a + \cdots$ → 진동
- $|r| > 1$: 항이 무한대로 → 발산

---

### 무한등비급수 정리표

| 공비 $r$ | 수렴/발산 | 합 |
|---------|----------|-----|
| $\|r\| < 1$ | 수렴 | $\frac{a}{1-r}$ |
| $\|r\| \geq 1$ | 발산 | - |

---

### 📝 예제 5

다음 무한등비급수의 수렴, 발산을 조사하고, 수렴하면 그 합을 구하여라.

(1) $\sum_{n=1}^{\infty} 3 \cdot \left(\frac{1}{2}\right)^{n-1}$

(2) $\sum_{n=1}^{\infty} 2 \cdot (-3)^{n-1}$

(3) $1 - \frac{1}{3} + \frac{1}{9} - \frac{1}{27} + \cdots$

**풀이**:

(1) $a = 3$, $r = \frac{1}{2}$

$|r| = \frac{1}{2} < 1$ → 수렴

$$\sum = \frac{3}{1 - \frac{1}{2}} = \frac{3}{\frac{1}{2}} = 6$$

(2) $a = 2$, $r = -3$

$|r| = 3 > 1$ → **발산**

(3) $a = 1$, $r = -\frac{1}{3}$

$|r| = \frac{1}{3} < 1$ → 수렴

$$\sum = \frac{1}{1 - (-\frac{1}{3})} = \frac{1}{1 + \frac{1}{3}} = \frac{1}{\frac{4}{3}} = \frac{3}{4}$$

---

### 📝 예제 6

$$\sum_{n=1}^{\infty} \frac{2^n + 3^n}{6^n}$$

의 값을 구하여라.

**풀이**:

$$\sum_{n=1}^{\infty} \frac{2^n + 3^n}{6^n} = \sum_{n=1}^{\infty} \left(\frac{2^n}{6^n} + \frac{3^n}{6^n}\right)$$

$$= \sum_{n=1}^{\infty} \left(\frac{1}{3}\right)^n + \sum_{n=1}^{\infty} \left(\frac{1}{2}\right)^n$$

첫 번째 급수: $a = \frac{1}{3}$, $r = \frac{1}{3}$

$$\sum_{n=1}^{\infty} \left(\frac{1}{3}\right)^n = \frac{\frac{1}{3}}{1 - \frac{1}{3}} = \frac{\frac{1}{3}}{\frac{2}{3}} = \frac{1}{2}$$

두 번째 급수: $a = \frac{1}{2}$, $r = \frac{1}{2}$

$$\sum_{n=1}^{\infty} \left(\frac{1}{2}\right)^n = \frac{\frac{1}{2}}{1 - \frac{1}{2}} = \frac{\frac{1}{2}}{\frac{1}{2}} = 1$$

따라서:
$$\sum = \frac{1}{2} + 1 = \frac{3}{2}$$

---

### 📝 예제 7

$$0.\dot{3}\dot{6} = 0.363636\cdots$$

을 분수로 나타내어라.

**풀이**:

$$0.363636\cdots = 0.36 + 0.0036 + 0.000036 + \cdots$$

$$= \frac{36}{100} + \frac{36}{10000} + \frac{36}{1000000} + \cdots$$

$$= \frac{36}{100}\left(1 + \frac{1}{100} + \frac{1}{10000} + \cdots\right)$$

무한등비급수: $a = 1$, $r = \frac{1}{100}$

$$= \frac{36}{100} \times \frac{1}{1 - \frac{1}{100}} = \frac{36}{100} \times \frac{100}{99} = \frac{36}{99} = \frac{4}{11}$$

---

## (5) 무한급수의 성질

무한급수 $\sum_{n=1}^{\infty} a_n = A$, $\sum_{n=1}^{\infty} b_n = B$일 때:

#### ① 상수배

$$\sum_{n=1}^{\infty} ca_n = c\sum_{n=1}^{\infty} a_n = cA$$

(단, $c$는 상수)

---

#### ② 합과 차

$$\sum_{n=1}^{\infty} (a_n \pm b_n) = \sum_{n=1}^{\infty} a_n \pm \sum_{n=1}^{\infty} b_n = A \pm B$$

---

### 주의사항

$$\sum_{n=1}^{\infty} a_n \times \sum_{n=1}^{\infty} b_n \neq \sum_{n=1}^{\infty} a_n b_n$$

$$\frac{\sum_{n=1}^{\infty} a_n}{\sum_{n=1}^{\infty} b_n} \neq \sum_{n=1}^{\infty} \frac{a_n}{b_n}$$

---

### 📝 예제 8

무한급수 $\sum_{n=1}^{\infty} \frac{2^n}{3^n}$과 $\sum_{n=1}^{\infty} \frac{1}{2^n}$이 수렴할 때:

$$\sum_{n=1}^{\infty} \frac{2^n + 3}{3^n \cdot 2^n}$$

을 구하여라.

**풀이**:

$$\sum_{n=1}^{\infty} \frac{2^n + 3}{3^n \cdot 2^n} = \sum_{n=1}^{\infty} \left(\frac{2^n}{3^n \cdot 2^n} + \frac{3}{3^n \cdot 2^n}\right)$$

$$= \sum_{n=1}^{\infty} \frac{1}{3^n} + 3\sum_{n=1}^{\infty} \frac{1}{6^n}$$

첫 번째: $\frac{\frac{1}{3}}{1-\frac{1}{3}} = \frac{1}{2}$

두 번째: $\frac{\frac{1}{6}}{1-\frac{1}{6}} = \frac{1}{5}$

$$= \frac{1}{2} + 3 \times \frac{1}{5} = \frac{1}{2} + \frac{3}{5} = \frac{5 + 6}{10} = \frac{11}{10}$$

---

### 📝 예제 9

첫째항이 $a$이고 공비가 $r$ ($|r| < 1$)인 무한등비수열에서:

$$\sum_{n=1}^{\infty} a_n = 3, \quad \sum_{n=1}^{\infty} a_n^2 = \frac{9}{2}$$

일 때, $a$와 $r$의 값을 구하여라.

**풀이**:

$$\sum_{n=1}^{\infty} ar^{n-1} = \frac{a}{1-r} = 3 \cdots ①$$

$$\sum_{n=1}^{\infty} (ar^{n-1})^2 = \sum_{n=1}^{\infty} a^2r^{2(n-1)} = \frac{a^2}{1-r^2} = \frac{9}{2} \cdots ②$$

②÷①:
$$\frac{a^2}{1-r^2} \div \frac{a}{1-r} = \frac{9}{2} \div 3$$

$$\frac{a^2}{1-r^2} \times \frac{1-r}{a} = \frac{3}{2}$$

$$\frac{a}{(1-r)(1+r)} \times (1-r) = \frac{3}{2}$$

$$\frac{a}{1+r} = \frac{3}{2}$$

$$a = \frac{3(1+r)}{2} \cdots ③$$

③을 ①에 대입:
$$\frac{\frac{3(1+r)}{2}}{1-r} = 3$$

$$\frac{3(1+r)}{2(1-r)} = 3$$

$$\frac{1+r}{1-r} = 2$$

$$1+r = 2(1-r)$$

$$1+r = 2 - 2r$$

$$3r = 1$$

$$r = \frac{1}{3}$$

③에 대입:
$$a = \frac{3(1 + \frac{1}{3})}{2} = \frac{3 \times \frac{4}{3}}{2} = 2$$

따라서 $a = 2$, $r = \frac{1}{3}$

---

## 🔑 핵심 정리

### 무한급수의 정의

$$\sum_{n=1}^{\infty} a_n = \lim_{n \to \infty} S_n$$

여기서 $S_n = \sum_{k=1}^{n} a_k$ (부분합)

### 수렴 조건

급수가 수렴하면:
$$\lim_{n \to \infty} a_n = 0$$

역은 성립 안 함!

### 무한등비급수

$$\sum_{n=1}^{\infty} ar^{n-1} = \begin{cases}
\frac{a}{1-r} & (|r| < 1) \\
\text{발산} & (|r| \geq 1)
\end{cases}$$

### 급수의 성질

- $\sum ca_n = c\sum a_n$
- $\sum (a_n \pm b_n) = \sum a_n \pm \sum b_n$

---

## 📚 연습문제

### 문제 1

다음 무한급수의 수렴, 발산을 조사하고, 수렴하면 그 합을 구하여라.

(1) $\sum_{n=1}^{\infty} \frac{3}{2^n}$

(2) $\sum_{n=1}^{\infty} \frac{(-1)^n}{3^n}$

---

### 문제 2

$$\sum_{n=1}^{\infty} \frac{1}{n(n+2)}$$

의 값을 구하여라.

---

### 문제 3

무한급수 $\sum_{n=1}^{\infty} a_n$이 수렴하고 $\lim_{n \to \infty} a_n = 0$일 때, 다음 중 항상 수렴하는 것은?

① $\sum_{n=1}^{\infty} 2a_n$
② $\sum_{n=1}^{\infty} a_n^2$
③ $\sum_{n=1}^{\infty} (a_n + 1)$

---

### 문제 4

$$0.\dot{2}\dot{7} = 0.272727\cdots$$

을 분수로 나타내어라.

---

### 문제 5

첫째항이 2이고 공비가 $r$인 등비수열에서:

$$\sum_{n=1}^{\infty} a_n = 6$$

일 때, $r$의 값과 $\sum_{n=1}^{\infty} a_n^2$의 값을 구하여라.

---

## 🔗 관련 링크

- [[14-limit|14강: 수열의 극한]] - 이전 주제
- [[16-exponent-log|16강: 지수와 로그]] - 다음 주제

---

*다음 챕터: [[16-exponent-log|16강 지수와 로그]]*
