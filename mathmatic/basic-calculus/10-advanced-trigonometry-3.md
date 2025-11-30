---
id: 3f4e5a6b-7c8d-9e0f-1a2b-3c4d5e6f7a8b
aliases:
  - 심화삼각함수(3)
  - 배각공식 문제풀이
  - 반각공식 응용
  - 삼각함수와 이차방정식
tags:
  - 삼각함수
  - 배각공식
  - 반각공식
  - 이차방정식
  - 근과계수의관계
  - 삼각함수의최댓값
pages: 27-29
subject: 대학기초수학
title: 심화삼각함수(3) - 배각공식과 반각공식의 응용
topics:
  - 배각공식의 활용
  - 반각공식의 활용
  - 삼각함수와 이차방정식
  - 삼각함수의 최댓값 문제
  - 근과 계수의 관계
---

# 제2장 초월함수의 극한

## 심화삼각함수(3) - 배각공식과 반각공식의 응용

### 배각공식 복습

#### 사인 배각공식

$$\sin 2\theta = 2\sin\theta \cos\theta$$

#### 코사인 배각공식

$$\cos 2\theta = \cos^2\theta - \sin^2\theta$$
$$= 2\cos^2\theta - 1$$
$$= 1 - 2\sin^2\theta$$

#### 탄젠트 배각공식

$$\tan 2\theta = \frac{2\tan\theta}{1 - \tan^2\theta}$$

### 반각공식

코사인 배각공식으로부터 반각공식을 유도할 수 있다.

#### 사인 반각공식

$$\cos 2\theta = 1 - 2\sin^2\theta$$에서
$$2\sin^2\theta = 1 - \cos 2\theta$$
$$\sin^2\theta = \frac{1 - \cos 2\theta}{2}$$

$\theta$를 $\frac{\theta}{2}$로 치환하면:
$$\sin^2\frac{\theta}{2} = \frac{1 - \cos\theta}{2}$$

#### 코사인 반각공식

$$\cos 2\theta = 2\cos^2\theta - 1$$에서
$$2\cos^2\theta = 1 + \cos 2\theta$$
$$\cos^2\theta = \frac{1 + \cos 2\theta}{2}$$

$\theta$를 $\frac{\theta}{2}$로 치환하면:
$$\cos^2\frac{\theta}{2} = \frac{1 + \cos\theta}{2}$$

#### 탄젠트 반각공식

$$\tan^2\frac{\theta}{2} = \frac{\sin^2\frac{\theta}{2}}{\cos^2\frac{\theta}{2}} = \frac{\frac{1-\cos\theta}{2}}{\frac{1+\cos\theta}{2}} = \frac{1-\cos\theta}{1+\cos\theta}$$

---

## 1. 삼각함수와 이차방정식

삼각함수 문제에서 이차방정식의 개념이 자주 등장한다. 특히 **근과 계수의 관계**는 매우 중요한 도구이다.

### 이차방정식의 기본 개념

#### Def: 이차방정식

이차방정식은 다음과 같은 형태의 방정식이다:
$$ax^2 + bx + c = 0 \quad (a \neq 0)$$

#### 근의 공식

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

#### 판별식 (Discriminant)

$$D = b^2 - 4ac$$

- $D > 0$: 서로 다른 두 실근
- $D = 0$: 중근 (같은 실근 2개)
- $D < 0$: 서로 다른 두 허근 (복소수근)

### 근과 계수의 관계 (Vieta's Formulas)

이차방정식 $ax^2 + bx + c = 0$의 두 근을 $\alpha$, $\beta$라 하면:

#### (1) 근의 합

$$\alpha + \beta = -\frac{b}{a}$$

#### (2) 근의 곱

$$\alpha \cdot \beta = \frac{c}{a}$$

### 응용: 근으로부터 이차방정식 만들기

두 수 $p$, $q$를 근으로 하는 이차방정식은:
$$x^2 - (p+q)x + pq = 0$$

이는 근과 계수의 관계를 역으로 적용한 것이다:

- 근의 합 = $p + q$ → 계수: $-(p+q)$
- 근의 곱 = $pq$ → 계수: $pq$

### 특별한 경우: 서로소인 자연수

문제에서 "$a, b$는 서로소인 자연수"라고 하면, 분수 $\frac{a}{b}$가 **기약분수** 형태라는 의미이다.

**예시**:

- $\frac{3}{4}$: 3과 4는 서로소 (최대공약수가 1)
- $\frac{6}{8}$: 6과 8은 서로소가 아님 → 기약분수는 $\frac{3}{4}$

---

## 2. 예제

### 예제 49

$$\frac{\sin\theta + \cos\theta}{\sin\theta - \cos\theta} = \sqrt{5}$$

일 때 $\sin 2\theta$의 값은?

> [!summary]- 풀이
>
> 양변을 제곱:
> $$\frac{(\sin\theta + \cos\theta)^2}{(\sin\theta - \cos\theta)^2} = 5$$
> $$(\sin\theta + \cos\theta)^2 = 5(\sin\theta - \cos\theta)^2$$
>
> 좌변 전개:
> $$\sin^2\theta + 2\sin\theta\cos\theta + \cos^2\theta = 5(\sin^2\theta - 2\sin\theta\cos\theta + \cos^2\theta)$$
> $$1 + 2\sin\theta\cos\theta = 5(1 - 2\sin\theta\cos\theta)$$
> $$1 + \sin2\theta = 5(1 - \sin2\theta)$$
> $$1+\sin2\theta = 5-5\sin2\theta$$
> $$6\sin2\theta = 4$$
> ㅓ3>$$\sin2\theta = \frac{4}{6} = \frac{2}{3}$$
>
> **답**: $\sin 2\theta = \dfrac{2}{3}$

---

### 예제 50

곡선 $y = \cos x$ $(0 \le x \le 2\pi)$ 위의 두 점 $P(\theta, \cos\theta)$, $Q\left(\theta + \frac{\pi}{2}, \cos\left(\theta + \frac{\pi}{2}\right)\right)$에 대하여 선분 $\overline{PQ}$의 길이의 최댓값과 최솟값을 구하여라.

> [!summary]- 풀이
>
> 두 점 사이의 거리 공식을 사용한다:
> $$\overline{PQ} = \sqrt{\left(\theta - \frac{\pi}{2} - \theta\right)^2 + \left(\cos\theta - \cos\left(\theta + \frac{\pi}{2}\right)\right)^2}$$
>
> $\cos\left(\theta + \frac{\pi}{2}\right) = -\sin\theta$를 사용하면:
> $$\overline{PQ} = \sqrt{\left(-\frac{\pi}{2}\right)^2 + (\cos\theta+\sin\theta)^2}$$
> $$= \sqrt{\frac{\pi^2}{4} + (\cos\theta + \sin\theta)^2}$$
>
> $(\cos\theta + \sin\theta)^2$를 전개하면:
> $$(\cos\theta + \sin\theta)^2 = \cos^2\theta + 2\sin\theta\cos\theta + \sin^2\theta$$
> $$= 1 + 2\sin\theta\cos\theta = 1 + \sin 2\theta$$
>
> 따라서:
> $$\overline{PQ}^2 = \frac{\pi^2}{4} + 1 + \sin 2\theta$$
>
> $\sin 2\theta$의 범위는 $-1 \le \sin 2\theta \le 1$이므로:
>
> **최댓값**: $\sin 2\theta = 1$일 때
> $$\overline{PQ}^2 = \frac{\pi^2}{4} + 1 + 1 = \frac{\pi^2}{4} + 2$$
> $$\overline{PQ}_{\max} = \sqrt{\frac{\pi^2}{4} + 2}$$
>
> **최솟값**: $\sin 2\theta = -1$일 때
> $$\overline{PQ}^2 = \frac{\pi^2}{4} + 1 - 1 = \frac{\pi^2}{4}$$
> $$\overline{PQ}_{\min} = \frac{\pi}{2}$$
>
> **답**: 최댓값 $\sqrt{\dfrac{\pi^2}{4}+2}$, 최솟값 $\dfrac{\pi}{2}$

---

### 예제 51

$$\frac{1 - \cos 2\theta}{\sin 2\theta}$$

를 간단히 하시오.

> [!summary]- 풀이
>
> 코사인 배각공식 $\cos 2\theta = 1 - 2\sin^2\theta$를 사용하면:
> $$1 - \cos 2\theta = 1 - (1 - 2\sin^2\theta) = 2\sin^2\theta$$
>
> 사인 배각공식 $\sin 2\theta = 2\sin\theta\cos\theta$를 사용하면:
> $$\frac{1 - \cos 2\theta}{\sin 2\theta} = \frac{2\sin^2\theta}{2\sin\theta\cos\theta}$$
> $$= \frac{\sin\theta}{\cos\theta} = \tan\theta$$
>
> **답**: $\tan\theta$

---

### 예제 52

$0 < x < \pi$에서 $x$에 대한 방정식

$$\cos 2x - \sin x = a(\sin x + 1)$$

이 실근을 갖기 위한 실수 $a$의 범위는?

> [!summary]- 풀이
>
> 코사인 배각공식을 사용하여 $\cos 2x$를 $\sin x$로 표현한다:
> $$\cos 2x = 1 - 2\sin^2 x$$
>
> 주어진 방정식에 대입:
> $$1 - 2\sin^2 x - \sin x = a\sin x + a$$
> $$1 - 2\sin^2 x - \sin x - a\sin x - a = 0$$
> $$-2\sin^2 x - (1+a)\sin x + (1-a) = 0$$
> $$2\sin^2 x + (1+a)\sin x - (1-a) = 0$$
>
> $t = \sin x$로 치환하면 ($0 < x < \pi$이므로 $0 < t \le 1$):
> $$2t^2 + (1+a)t + a - 1 = 0$$
> 인수분해하면
> $$(t+1)(2t+a-1)=0$$
>
> 이 이차방정식이 $(0, 1]$ 범위에서 실근을 가져야 한다.
>
> $t = -1$은 범위 밖, $t = \frac{1-a}{2}$가 $(0, 1]$에 있으려면:
> $$0 < \frac{1-a}{2} \le 1$$
> $$0 < 1-a \le 2$$
> $$-1 < -a \le 1$$
> $$-1 \le a < 1$$
>
> **답**: $-1 < a \le 1$

---

### 예제 53

$$\sin\alpha = \frac{3}{4}$$

일 때 $\cos 2\alpha$의 값을 구하시오.

> [!summary]- 풀이
>
> 코사인 배각공식을 사용한다:
> $$\cos 2\alpha = 1 - 2\sin^2\alpha$$
>
> $\sin\alpha = \frac{3}{4}$를 대입:
> $$\cos 2\alpha = 1 - 2\left(\frac{3}{4}\right)^2$$
> $$= 1 - 2 \cdot \frac{9}{16}$$
> $$= 1 - \frac{9}{8}$$
> $$= -\frac{1}{8}$$
>
> **답**: $\cos 2\alpha = -\dfrac{1}{8}$

---

### 예제 54

$$\sin\theta - \cos\theta = \frac{1}{2}$$

일 때 $\cos^2 2\theta = \frac{b}{a}$이다. $a + b$의 값을 구하시오.

(단, $a, b$는 서로소인 자연수)

> [!summary]- 풀이
>
> 먼저 $\sin 2\theta$를 구한다.
>
> 주어진 식을 제곱:
> $$(\sin\theta - \cos\theta)^2 = \frac{1}{4}$$
> $$\sin^2\theta - 2\sin\theta\cos\theta + \cos^2\theta = \frac{1}{4}$$
> $$1 - 2\sin\theta\cos\theta = \frac{1}{4}$$
> $$2\sin\theta\cos\theta = \frac{3}{4}$$
> $$\sin 2\theta = \frac{3}{4}$$
>
> 이제 $\cos^2 2\theta$를 구한다:
> $$\cos^2 2\theta = 1 - \sin^2 2\theta$$
> $$= 1 - \left(\frac{3}{4}\right)^2$$
> $$= 1 - \frac{9}{16}$$
> $$= \frac{7}{16}$$
>
> 따라서 $\frac{b}{a} = \frac{7}{16}$이고, 7과 16은 서로소이므로:
> $$b = 7, \quad a = 16$$
>
> **답**: $a + b = 23$

---

### 예제 55

이차 방정식 $8x^2 + 7x + a = 0$의 두 근이 $\sin\theta$, $\cos 2\theta$일 때 상수 $a$의 값을 구하시오.

> [!summary]- 풀이
>
> 근과 계수의 관계를 사용한다.
>
> 이차방정식 $8x^2 + 7x + a = 0$의 두 근을 $\alpha$, $\beta$라 하면:
>
> - 근의 합: $\alpha + \beta = -\frac{7}{8}$
> - 근의 곱: $\alpha \cdot \beta = \frac{a}{8}$
>
> 두 근이 $\sin\theta$와 $\cos 2\theta$이므로:
> $$\sin\theta + \cos 2\theta = -\frac{7}{8} \quad \cdots ①$$
> $$\sin\theta \cdot \cos 2\theta = \frac{a}{8} \quad \cdots ②$$
>
> 코사인 배각공식 $\cos 2\theta = 1 - 2\sin^2\theta$를 ①에 대입:
> $$\sin\theta + 1 - 2\sin^2\theta = -\frac{7}{8}$$
> $$-2\sin^2\theta + \sin\theta + 1 + \frac{7}{8} = 0$$
> $$-2\sin^2\theta + \sin\theta + \frac{15}{8} = 0$$
> $$-16\sin^2\theta + 8\sin\theta + 15 = 0$$
> $$16\sin^2\theta - 8\sin\theta - 15 = 0$$
>
> 근의 공식:
> $$\sin\theta = \frac{8 \pm \sqrt{64 + 960}}{32} = \frac{8 \pm \sqrt{1024}}{32} = \frac{8 \pm 32}{32}$$
>
> $$\sin\theta = \frac{40}{32} = \frac{5}{4} \quad \text{또는} \quad \sin\theta = \frac{-24}{32} = -\frac{3}{4}$$
>
> $|\sin\theta| \le 1$이므로 $\sin\theta = -\frac{3}{4}$
>
> 이제 $\cos 2\theta$를 구한다:
> $$\cos 2\theta = 1 - 2\sin^2\theta = 1 - 2\left(-\frac{3}{4}\right)^2$$
> $$= 1 - 2 \cdot \frac{9}{16} = 1 - \frac{9}{8} = -\frac{1}{8}$$
>
> ②에서:
> $$\sin\theta \cdot \cos 2\theta = \left(-\frac{3}{4}\right) \cdot \left(-\frac{1}{8}\right) = \frac{3}{32} = \frac{a}{8}$$
>
> 따라서:
> $$a = 8 \cdot \frac{3}{32} = \frac{3}{4}$$
>
> **답**: $a = \dfrac{3}{4}$

---

### 예제 56

$$\sin\alpha = -\frac{3}{5}$$

($\alpha$는 제4사분면의 각)일 때 $\tan^2\frac{\alpha}{2}$의 값은?

> [!summary]- 풀이
>
> 제4사분면에서 $\sin\alpha < 0$, $\cos\alpha > 0$이다.
>
> $\sin^2\alpha + \cos^2\alpha = 1$을 사용하여 $\cos\alpha$를 구한다:
> $$\cos^2\alpha = 1 - \sin^2\alpha = 1 - \frac{9}{25} = \frac{16}{25}$$
> $$\cos\alpha = \frac{4}{5} \quad (\text{양수})$$
>
> 탄젠트 반각공식을 사용한다:
> $$\tan^2\frac{\alpha}{2} = \frac{1 - \cos\alpha}{1 + \cos\alpha}$$
>
> 값을 대입:
> $$\tan^2\frac{\alpha}{2} = \frac{1 - \frac{4}{5}}{1 + \frac{4}{5}} = \frac{\frac{1}{5}}{\frac{9}{5}} = \frac{1}{9}$$
>
> **답**: $\tan^2\dfrac{\alpha}{2} = \dfrac{1}{9}$

---

### 예제 57

함수 $y = 5\sin x + \cos 2x$의 최댓값을 구하여라.

> [!summary]- 풀이
>
> 코사인 배각공식을 사용하여 $\cos 2x$를 $\sin x$로 표현한다:
> $$\cos 2x = 1 - 2\sin^2 x$$
>
> 함수를 다시 쓰면:
> $$y = 5\sin x + 1 - 2\sin^2 x$$
> $$= -2\sin^2 x + 5\sin x + 1$$
>
> $t = \sin x$로 치환하면 ($-1 \le t \le 1$):
> $$y = -2t^2 + 5t + 1$$
>
> 이것은 아래로 볼록한 포물선이고, 꼭짓점에서 최댓값을 가진다.
>
> 꼭짓점의 $t$ 좌표:
> $$t = -\frac{5}{2 \cdot (-2)} = \frac{5}{4}$$
>
> 하지만 $t = \sin x$의 범위는 $-1 \le t \le 1$이므로, $t = \frac{5}{4}$는 불가능하다.
>
> 따라서 최댓값은 $t = 1$에서 발생한다:
> $$y_{\max} = -2(1)^2 + 5(1) + 1 = -2 + 5 + 1 = 4$$
>
> **답**: 최댓값 = $4$

---

### 예제 58

$$\frac{1 - \tan^2\theta}{1 + \tan^2\theta} = \frac{1}{2}$$

일 때 $\sin^2\frac{\theta}{2}$의 값을 구하시오. (단, $\theta$는 예각)

> [!summary]- 풀이
>
> 좌변을 변형한다. $\tan\theta = \frac{\sin\theta}{\cos\theta}$를 사용하면:
>
> $$\frac{1 - \tan^2\theta}{1 + \tan^2\theta} = \frac{1 - \frac{\sin^2\theta}{\cos^2\theta}}{1 + \frac{\sin^2\theta}{\cos^2\theta}}$$
> $$= \frac{\frac{\cos^2\theta - \sin^2\theta}{\cos^2\theta}}{\frac{\cos^2\theta + \sin^2\theta}{\cos^2\theta}}$$
> $$= \frac{\cos^2\theta - \sin^2\theta}{\cos^2\theta + \sin^2\theta}$$
> $$= \frac{\cos^2\theta - \sin^2\theta}{1}$$
> $$= \cos 2\theta$$
>
> 따라서:
> $$\cos 2\theta = \frac{1}{2}$$
>
> 사인 반각공식을 사용한다:
> $$\sin^2\frac{\theta}{2} = \frac{1 - \cos\theta}{2}$$
>
> 먼저 $\cos\theta$를 구해야 한다. $\cos 2\theta = 2\cos^2\theta - 1$을 사용:
> $$\frac{1}{2} = 2\cos^2\theta - 1$$
> $$\frac{3}{2} = 2\cos^2\theta$$
> $$\cos^2\theta = \frac{3}{4}$$
> $$\cos\theta = \frac{\sqrt{3}}{2} \quad (\theta\text{는 예각이므로 양수})$$
>
> 이제 $\sin^2\frac{\theta}{2}$를 구한다:
> $$\sin^2\frac{\theta}{2} = \frac{1 - \cos\theta}{2} = \frac{1 - \frac{\sqrt{3}}{2}}{2}$$
> $$= \frac{2 - \sqrt{3}}{4}$$
>
> **답**: $\sin^2\dfrac{\theta}{2} = \dfrac{2 - \sqrt{3}}{4}$

---

### 예제 59

$$\tan\theta = \frac{3}{4}$$

($\theta$는 예각)일 때 $\sin 2\theta + \cos 2\theta$의 값을 구하시오.

> [!summary]- 풀이
>
> $\tan\theta = \frac{3}{4}$이므로 직각삼각형을 생각하면:
>
> - 대변 = 3
> - 밑변 = 4
> - 빗변 = $\sqrt{3^2 + 4^2} = 5$
>
> 따라서:
> $$\sin\theta = \frac{3}{5}, \quad \cos\theta = \frac{4}{5}$$
>
> 사인 배각공식:
> $$\sin 2\theta = 2\sin\theta\cos\theta = 2 \cdot \frac{3}{5} \cdot \frac{4}{5} = \frac{24}{25}$$
>
> 코사인 배각공식:
> $$\cos 2\theta = \cos^2\theta - \sin^2\theta = \left(\frac{4}{5}\right)^2 - \left(\frac{3}{5}\right)^2$$
> $$= \frac{16}{25} - \frac{9}{25} = \frac{7}{25}$$
>
> 따라서:
> $$\sin 2\theta + \cos 2\theta = \frac{24}{25} + \frac{7}{25} = \frac{31}{25}$$
>
> **답**: $\sin 2\theta + \cos 2\theta = \dfrac{31}{25}$

---

## 연습문제

배각공식과 반각공식을 활용하여 다음 문제들을 풀어보시오.

1. $\cos^2 15° - \sin^2 15°$의 값을 구하여라.

2. $\sin 2\alpha = \frac{3}{5}$이고 $\alpha$가 제1사분면의 각일 때, $\cos\alpha$의 값을 구하여라.

3. 이차방정식 $x^2 - 3x + 1 = 0$의 두 근을 $\alpha$, $\beta$라 할 때, $\alpha^2 + \beta^2$의 값을 구하여라.

4. $\sin\theta + \cos\theta = \frac{1}{3}$일 때, $\sin 2\theta$의 값을 구하여라.

---

## 관련 주제

- [[09-advanced-trigonometry-2|심화삼각함수(2)]] - 배각공식의 유도
- [[11-advanced-trigonometry-4|심화삼각함수(4)]] - 기타 공식
- [[08-advanced-trigonometry-1|심화삼각함수(1)]] - 덧셈정리

---

**학습 포인트:**

1. **배각공식의 활용**: 배각공식을 이용하여 복잡한 삼각함수 식을 단순화한다.

2. **반각공식의 이해**: 반각공식은 배각공식으로부터 유도되며, $\frac{\theta}{2}$를 포함하는 문제에서 유용하다.

3. **삼각함수와 이차방정식**: 근과 계수의 관계를 활용하여 삼각함수 값을 구하는 방법을 익힌다.

4. **치환을 통한 최댓값/최솟값**: $t = \sin x$ 또는 $t = \cos x$로 치환하여 이차함수로 변환한 후 최댓값과 최솟값을 구한다.

5. **삼각함수의 범위**: $\sin x$, $\cos x$의 범위가 $[-1, 1]$임을 항상 염두에 두어야 한다.
