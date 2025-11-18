---
id: abc31732-234b-4128-8723-450376412c02
aliases:
  - 집합
  - 명제
tags:
  - 집합
  - 명제
lecture: 큐스터디 썡기초수학
title: 1강 집합,명제
topics:
  - 집합의 정의와 표시
  - 부분집합과 집합의 개수
  - 집합의 연산 (합집합, 교집합, 차집합, 여집합)
  - 집합의 연산법칙 (교환, 결합, 분배, 흡수, 드모르간)
  - 원소의 개수
---

# 1. 집합

## 01 부분집합

### 1. 집합과 원소

#### (1) 집합(Set)

어떤 기준에 의하여 그 대상이 분명한 것들의 모임

#### (2) 원소(Element)

집합을 이루는 낱낱의 것

**예제**: 집합 $A = \{0, 1, 2\}$에 대하여 다음 중 옳지 않은 것은?

- ① $0 \in A$ ✓
- ② $\varnothing \subset A$ ✓
- ③ $\{0, 1\} \subset A$ ✓
- ④ $\{-1, 0\} \not\subset A$ ✓
- ⑤ $\{0\} \in A$ ✗ (원소와 부분집합 구분)

---

### 2. 집합의 표시

#### (1) 원소나열법

$$A = \{2, 4, 6, 8, \cdots\}$$

#### (2) 조건제시법

$$A = \{x \mid x\text{는 2의 배수}\}$$

---

### 3. 부분집합

#### (1) 부분집합의 정의

$$A \subset B \Longleftrightarrow x \in A \text{이면 } x \in B$$

**관계**:

- $A \subset B$ 이고 $A \neq B$ → 진부분집합
- $A \subset B$ 이고 $B \subset A$ → $A = B$ (상등)

#### (2) 부분집합의 성질

- $A \subset A$
- $\varnothing \subset A$
- $A \subset B$이고 $B \subset C$이면 $A \subset C$

#### (3) 부분집합의 개수

$A$의 원소가 $n$개이면 $A$의 부분집합의 개수는 **$2^n$개**

**예제**: $A = \{1, 2, 3\}$에 대하여 부분집합의 개수는?

- 전체 부분집합: $2^3 = 8$개

**연습문제**:

1. 1을 꼭 포함하는 부분집합의 개수는?
   - 답: $2^2 = 4$개 (나머지 2개 원소를 선택)

2. 2를 포함하지 않는 부분집합의 개수는?
   - 답: $2^2 = 4$개

3. 적어도 홀수를 하나 이상 가지는 부분집합의 개수는?
   - 답: $2^3 - 2^1 = 6$개 (전체 - 짝수만 포함)

---

## 02 집합의 연산법칙

### 1. 연산법칙 I

#### 기본 연산

① **합집합**: $A \cup B = \{x \mid x \in A \text{ or } x \in B\}$

② **교집합**: $A \cap B = \{x \mid x \in A \text{ and } x \in B\}$

③ **서로소**: $A \cap B = \varnothing$

④ **차집합**:

- $A - B = \{x \mid x \in A \text{ and } x \notin B\} = A \cap B^c$
- $B - A = \{x \mid x \in B \text{ and } x \notin A\} = B \cap A^c$

⑤ **여집합**: $A^c = \{x \mid x \in U \text{ 이고 } x \notin A\}$

#### 당연한 성질

- $A \cup \varnothing = A$
- $A \cap \varnothing = \varnothing$
- $A \cap A^c = \varnothing$
- $A \cup A^c = U$
- $(A^c)^c = A$
- $\varnothing^c = U$
- $U^c = \varnothing$

#### 중요한 관계

- $A \subset B$ $\Rightarrow$ $A \cup B = B$
- $A \subset B$ $\Rightarrow$ $A \cap B = A$
- $A \subset B$ $\Rightarrow$ $A - B = \varnothing$
- $A \subset B$ $\Rightarrow$ $B^c \subset A^c$
- $A \cup B = \varnothing$ $\Rightarrow$ $A = B = \varnothing$

---

### 2. 연산법칙 II

#### ① 교환법칙

- $A \cup B = B \cup A$
- $A \cap B = B \cap A$

#### ② 결합법칙

- $(A \cup B) \cup C = A \cup (B \cup C)$
- $(A \cap B) \cap C = A \cap (B \cap C)$

#### ③ 분배법칙

- $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
- $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$

**예제**: $(A \cap B) \cup (A \cap C) = A \cap (B \cup C)$ 증명

#### ④ 흡수법칙

- $A \cup (A \cap B) = A$
- $A \cap (A \cup B) = A$

#### ⑤ 드 모르간 법칙

- $(A \cap B)^c = A^c \cup B^c$
- $(A \cup B)^c = A^c \cap B^c$

---

### 3. 원소의 개수

#### 기본 공식

① $n(A \cup B) = n(A) + n(B) - n(A \cap B)$

② $n(A \cap B) = n(A) + n(B) - n(A \cup B)$

③ $n(A \cup B \cup C) = n(A) + n(B) + n(C)$
$- n(A \cap B) - n(B \cap C) - n(C \cap A)$
$+ n(A \cap B \cap C)$

④ $n(A - B) = n(A) - n(A \cap B) = n(A \cup B) - n(B)$

**주의**: $n(A - B) \neq n(A) - n(B)$

---

## 연습문제

### 문제 1

전체집합 $U = \{x \mid x\text{는 10이하의 자연수}\}$,
$P = \{x \mid x\text{는 4의 약수}\}$,
$Q = \{x \mid 2x - 17 \leq 0\}$
일 때 $P \subset X \subset Q$를 만족시키는 집합 $X$의 개수는?

**풀이**:

- $P = \{1, 2, 4\}$
- $Q = \{x \mid x \leq 8.5\} \cap U = \{1, 2, 3, 4, 5, 6, 7, 8\}$
- $Q - P = \{3, 5, 6, 7, 8\}$ (5개)
- $X$의 개수 = $2^5 = 32$개

---

### 문제 2

$n(U) = 40$, 야구를 좋아하는 학생의 수는 25명, 축구를 좋아하는 학생의 수는 20명이다. 아무것도 좋아하지 않는 학생의 수는 3명이다. 야구만 좋아하는 학생의 수를 구하여라.

**풀이**:

- $n(A) = 25$ (야구)
- $n(B) = 20$ (축구)
- $n((A \cup B)^c) = 3$
- $n(A \cup B) = 40 - 3 = 37$
- $n(A \cap B) = 25 + 20 - 37 = 8$
- 야구만 좋아하는 학생 = $n(A - B) = 25 - 8 = 17$명

---
