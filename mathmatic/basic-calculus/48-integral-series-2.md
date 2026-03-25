---
id: b3e7f1a2-9c4d-4e8f-b2a1-6d3c5f7e9b0a
aliases:
  - 정적분과 무한급수(2)
  - 일반화된 구분구적법
  - 정적분의 응용
tags:
  - 정적분
  - 무한급수
  - 구분구적법
  - 리만합
  - 정적분의응용
pages: 142-145
subject: 대학기초수학
title: 정적분과 무한급수(2)
topics:
  - 일반화된 정적분-무한급수 변환
  - 우합과 좌합의 오차
  - 비등분 구간의 넓이와 무한등비급수
  - 정적분의 기하학적 응용
---

# 정적분과 무한급수 (2)

> 이전 강의: [[47-fundamental-theorem|정적분과 부정적분의 관계]]
> 다음 강의: [[49-integral-series-3|정적분과 무한급수(3)]]

---

## 핵심 공식 정리

### 일반화된 구분구적법 변환 공식

분할 간격이 $\frac{1}{n}$이 아닌 경우에도 정적분으로 변환할 수 있다.

$$
\lim_{n \to \infty} \sum_{k=1}^{n} f\!\left(a + \frac{b-a}{n}k\right) \cdot \frac{b-a}{n} = \int_{a}^{b} f(x)\, dx
$$

**분모에 상수항이 있는 경우:**

$$
\lim_{n \to \infty} \frac{\sum_{k=1}^{n} f\!\left(a + \frac{k}{n}\right)}{an+1}
= \lim_{n \to \infty} \frac{n}{an+1} \cdot \int_{a}^{a+1} f(x)\, dx
= \frac{1}{a} \int_{a}^{a+1} f(x)\, dx
$$

**$S_k$ 형태로 주어진 경우 ($S_k = \frac{1}{2n} \cdot f\!\left(\frac{k}{2n}\right)$):**

$$
\lim_{n \to \infty} \sum_{k=1}^{2n} S_k = \int_{0}^{1} f(x)\, dx
$$

---

## 예제 303

**문제**: 다항함수 $f(x)$와 실수 $a$에 대하여

$$
\lim_{n \to \infty} \frac{f\!\left(a+\frac{1}{n}\right)+f\!\left(a+\frac{2}{n}\right)+\cdots+f\!\left(a+\frac{n}{n}\right)}{an+1}
$$

과 같은 것은? (단, $a \neq 0$)

① $\frac{1}{a}$　　② $\int_{0}^{1}f(x)\,dx$　　③ $a\int_{0}^{1}f(x)\,dx$　　④ $\int_{a}^{a+1}f(x)\,dx$　　⑤ $\frac{1}{a}\int_{a}^{a+1}f(x)\,dx$

> [!summary]- 풀이
>
> 주어진 식을 시그마 형태로 정리한다.
>
> $$\lim_{n \to \infty} \sum_{k=1}^{n} \frac{f\!\left(a+\frac{k}{n}\right)}{an+1}$$
>
> 분모 $an+1$을 분자의 $\frac{1}{n}$과 분리하기 위해 $\frac{n}{n}$을 곱하는 형태로 변형한다.
>
> $$= \lim_{n \to \infty} \frac{n}{an+1} \cdot \sum_{k=1}^{n} f\!\left(a+\frac{k}{n}\right) \cdot \frac{1}{n}$$
>
> 시그마 부분은 구분구적법에 의해 정적분으로 변환된다 ($x$가 $a$에서 $a+1$까지).
>
> $$= \lim_{n \to \infty} \frac{n}{an+1} \cdot \int_{a}^{a+1} f(x)\, dx$$
>
> 극한값을 계산한다.
>
> $$\lim_{n \to \infty} \frac{n}{an+1} = \lim_{n \to \infty} \frac{1}{a+\frac{1}{n}} = \frac{1}{a}$$
>
> $$\therefore \quad \frac{1}{a}\int_{a}^{a+1}f(x)\,dx$$
>
> **정답: ⑤**

---

## 예제 304

**문제**: 함수 $f(x)=x^{3}+x$일 때,

$$
\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n}f\!\left(1+\frac{2k}{n}\right)
$$

의 값을 구하시오.

> [!summary]- 풀이
>
> 주어진 식에서 $\frac{1}{n}$과 $\frac{2k}{n}$의 구조를 분석한다.
>
> $\frac{2k}{n}$에서 분할 간격이 $\frac{2}{n}$이므로, $x$의 범위는 $1$부터 $1+2=3$까지이다.
>
> 구분구적법 변환: $\frac{1}{n} = \frac{1}{2} \cdot \frac{2}{n}$ 이므로
>
> $$\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n}f\!\left(1+\frac{2k}{n}\right) = \frac{1}{2}\int_{1}^{3}(x^{3}+x)\,dx$$
>
> 정적분을 계산한다.
>
> $$= \frac{1}{2}\left[\frac{1}{4}x^{4}+\frac{1}{2}x^{2}\right]_{1}^{3}$$
>
> $$= \frac{1}{2}\left[\left(\frac{81}{4}+\frac{9}{2}\right)-\left(\frac{1}{4}+\frac{1}{2}\right)\right]$$
>
> $$= \frac{1}{2}\left(\frac{81-1}{4}+\frac{9-1}{2}\right) = \frac{1}{2}\left(20+4\right)$$
>
> $$\therefore \quad 12$$

---

## 예제 305

**문제**: 함수 $f(x)=x^{2}$에 대하여 그림과 같이 구간 $[0,1]$을 $2n$등분한 후,
구간 $\left[\frac{k-1}{2n},\, \frac{k}{2n}\right]$를 밑변으로 하고 높이가 $f\!\left(\frac{k}{2n}\right)$인 직사각형의 넓이를 $S_k$라 하자.
(단, $n$은 자연수이고 $k=1,2,3,\ldots,2n$이다.)
[보기]에서 옳은 것을 모두 고른 것은?

$$
\text{ㄱ.} \quad \lim_{n \to \infty}\sum_{k=1}^{n}S_k = \int_{0}^{\frac{1}{2}}x^{2}\,dx
\qquad
\text{ㄴ.} \quad \lim_{n \to \infty}\sum_{k=1}^{n}(S_{2k}-S_{2k-1})=0
\qquad
\text{ㄷ.} \quad \lim_{n \to \infty}\sum_{k=1}^{n}(S_{2k})=\frac{1}{2}\int_{0}^{1}x^{2}\,dx
$$

![예제305 그래프](./images/04-integral/exer305.png)

> [!summary]- 풀이
>
> 우선 $S_k$의 정의를 확인한다.
>
> $$S_k = \frac{1}{2n} \cdot f\!\left(\frac{k}{2n}\right) = \frac{1}{2n} \cdot \left(\frac{k}{2n}\right)^2$$
>
> 전체 합의 기준값을 먼저 구해두자.
>
> $$S = \lim_{n \to \infty}\sum_{k=1}^{2n} S_k = \lim_{n \to \infty}\sum_{k=1}^{2n}\frac{1}{2n}\cdot f\!\left(\frac{k}{2n}\right) = \int_{0}^{1}x^{2}\,dx$$
>
> ---
>
> **(ㄱ) 검토**
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}S_k = \lim_{n \to \infty}\sum_{k=1}^{n}\frac{1}{2n}\cdot f\!\left(\frac{k}{2n}\right)$$
>
> sigma 범위가 $1 \sim 2n$에서 $1 \sim n$으로 절반만큼 줄었으므로, 적분 상한도 절반인 $\frac{1}{2}$로 줄어든다.
>
> $$= \int_{0}^{\frac{1}{2}}x^{2}\,dx \quad \checkmark \quad \text{(참)}$$
>
> ---
>
> **(ㄴ) 검토**
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}(S_{2k}-S_{2k-1}) = \lim_{n \to \infty}\sum_{k=1}^{n}S_{2k} - \lim_{n \to \infty}\sum_{k=1}^{n}S_{2k-1}$$
>
> 좌항 ($S_{2k}$ 부분):
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}\frac{1}{2n}\cdot f\!\left(\frac{2k}{2n}\right) = \frac{1}{2}\int_{0}^{1}x^{2}\,dx$$
>
> 우항 ($S_{2k-1}$ 부분):
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}\frac{1}{2n}\cdot f\!\left(\frac{2k-1}{2n}\right) = \frac{1}{2}\int_{0}^{1}x^{2}\,dx$$
>
> 두 값이 동일하므로 차는 $0$이다. $\checkmark$ **(참)**
>
> ---
>
> **(ㄷ) 검토**
>
> $$\lim_{n \to \infty}\sum_{k=1}^{n}S_{2k} = \lim_{n \to \infty}\sum_{k=1}^{n}\frac{1}{2n}\cdot f\!\left(\frac{2k}{2n}\right)$$
>
> $dx = \frac{2}{2n} = \frac{1}{n}$으로 보면, $\frac{1}{n} = \frac{1}{2} \cdot \frac{2}{n}$이므로
>
> $$= \frac{1}{2}\int_{0}^{1}x^{2}\,dx \quad \checkmark \quad \text{(참)}$$
>
> **ㄱ, ㄴ, ㄷ 모두 참 → 정답: ⑤**

---

## 예제 306

**문제**: 연속인 증가함수 $f(x)$에 대하여

$$
g(n)=\sum_{k=1}^{n}f\!\left(a+\frac{b-a}{n}k\right)\frac{b-a}{n}, \qquad h(n)=\sum_{k=0}^{n-1}f\!\left(a+\frac{b-a}{n}k\right)\frac{b-a}{n}
$$

라고 할 때, 다음 중 옳은 것은? (단, $a < b$, $f(a) > 0$)

![예제306 그래프](./images/04-integral/exer306.png)

> [!summary]- 풀이
>
> $g(n)$은 **우합(right sum)**, $h(n)$은 **좌합(left sum)**이다.
>
> $f(x)$가 연속인 **증가함수**이므로:
> - 우합 $g(n)$은 항상 정적분보다 **크다** (직사각형이 곡선 위로 올라감)
> - 좌합 $h(n)$은 항상 정적분보다 **작다** (직사각형이 곡선 아래에 머묾)
>
> $$h(n) < \int_{a}^{b}f(x)\,dx < g(n)$$
>
> 그리고 $n$이 커질수록 두 합 모두 정적분 값에 수렴한다.
>
> $$\lim_{n \to \infty} g(n) = \lim_{n \to \infty} h(n) = \int_{a}^{b}f(x)\,dx$$
>
> 또한 $g(n)$은 $n$이 커질수록 **감소**하여 정적분에 가까워지고,
> $h(n)$은 $n$이 커질수록 **증가**하여 정적분에 가까워진다.
>
> 따라서:
> - ① $g(10) < g(20)$ → **거짓** ($g$는 감소하므로 $g(10) > g(20)$)
> - ② $h(10) > h(20)$ → **거짓** ($h$는 증가하므로 $h(10) < h(20)$)
> - ③ $g(10) < h(20)$ → **거짓** (항상 $g(n) > \int > h(n)$)
> - ④ $g(n) > \int_{a}^{b}f(x)\,dx$ → **참** ✓
> - ⑤ $h(n) > \int_{a}^{b}f(x)\,dx$ → **거짓**
>
> **정답: ④**

---

## 예제 307

**문제**: 다음은 정적분 $\int_{0}^{1}(x^{2}+1)\,dx$의 근삿값의 오차의 한계를 구하는 과정의 일부이다.

그림 (가), (나)와 같이 폐구간 $[0,1]$을 $n$등분하여 얻은 $n$개의 직사각형들의 넓이의 합을 각각 A, B라 하자.
$A-B \leq 0.12$가 되는 $n$의 최솟값을 구하시오.

![예제307 그래프](./images/04-integral/exer307.png)

> [!summary]- 풀이
>
> 그림 (가)의 A는 **우합(right sum)**, 그림 (나)의 B는 **좌합(left sum)**이다.
>
> 우합과 좌합의 차이에서, 우합의 마지막 직사각형과 좌합의 첫 번째 직사각형만 남게 된다.
>
> $$A - B = \frac{1}{n}\bigl(f(1) - f(0)\bigr)$$
>
> $f(x) = x^{2}+1$이므로 $f(1)=2$, $f(0)=1$을 대입한다.
>
> $$A - B = \frac{1}{n}(2 - 1) = \frac{1}{n}$$
>
> 조건 $A-B \leq 0.12$에 대입하면
>
> $$\frac{1}{n} \leq 0.12 = \frac{12}{100} = \frac{3}{25}$$
>
> $$n \geq \frac{25}{3} = 8.333\ldots$$
>
> $n$은 자연수이므로
>
> $$\therefore \quad n_{\min} = 9$$

---

## 예제 308

**문제**: 아래 그림과 같이 $x$좌표가 각각 $1, \frac{2}{3}, \left(\frac{2}{3}\right)^{2}, \left(\frac{2}{3}\right)^{3}, \ldots, \left(\frac{2}{3}\right)^{n-1}, \ldots$인
$x$축 위의 점에서 $y$축에 평행한 직선을 그어 $y=x^{2}$과 만나는 점을 한 꼭짓점으로 하는 직사각형을 한없이 만든다.
이 직사각형들이 곡선 $y=x^{2}$에 의하여 잘려진 윗부분들의 넓이의 합은?

① $\frac{5}{57}$　　② $\frac{2}{19}$　　③ $\frac{7}{57}$　　④ $\frac{8}{57}$　　⑤ $\frac{3}{19}$

![예제308 그래프](./images/04-integral/exer308.png)

> [!summary]- 풀이
>
> 구하는 넓이를 $S$, 직사각형들의 전체 넓이 합을 $RS$라 하면
>
> $$S = RS - \int_{0}^{1}x^{2}\,dx$$
>
> 각 분할 구간의 밑변 길이가 일정하지 않으므로 RS를 정적분으로 바로 변환할 수 없다. **무한등비급수** 형태로 표현한다.
>
> $n$번째 직사각형:
> - 밑변 = $\left(\frac{2}{3}\right)^{n-1} - \left(\frac{2}{3}\right)^{n}$
> - 높이 = $f\!\left(\left(\frac{2}{3}\right)^{n-1}\right) = \left(\frac{2}{3}\right)^{2(n-1)}$
>
> $$RS = \sum_{n=1}^{\infty}\left[\left(\frac{2}{3}\right)^{n-1}-\left(\frac{2}{3}\right)^{n}\right]\cdot\left(\frac{2}{3}\right)^{2(n-1)}$$
>
> $$= \sum_{n=1}^{\infty}\left(1-\frac{2}{3}\right)\cdot\left(\frac{2}{3}\right)^{n-1}\cdot\left(\frac{4}{9}\right)^{n-1}$$
>
> $$= \sum_{n=1}^{\infty}\frac{1}{3}\cdot\left(\frac{2}{3}\right)^{n-1}\cdot\left(\frac{4}{9}\right)^{n-1} = \sum_{n=1}^{\infty}\frac{1}{3}\cdot\left(\frac{8}{27}\right)^{n-1}$$
>
> 무한등비급수 공식 $\frac{a}{1-r}$을 적용한다.
>
> $$RS = \frac{\frac{1}{3}}{1-\frac{8}{27}} = \frac{\frac{1}{3}}{\frac{19}{27}} = \frac{1}{3}\cdot\frac{27}{19} = \frac{9}{19}$$
>
> 정적분을 계산한다.
>
> $$\int_{0}^{1}x^{2}\,dx = \left[\frac{1}{3}x^{3}\right]_{0}^{1} = \frac{1}{3}$$
>
> 따라서
>
> $$S = \frac{9}{19} - \frac{1}{3} = \frac{27}{57} - \frac{19}{57} = \frac{8}{57}$$
>
> **정답: ④**

---

## 예제 309

**문제**: 다음 그림에서 $P_1, P_2, \ldots, P_k, \ldots, P_{n-1}$은 직각삼각형의 빗변 $BA$를 $n$등분한 점이다.
$\overline{BC}=a$, $\overline{CA}=b$라고 할 때,

$$
\lim_{n \to \infty} \frac{1}{n}\sum_{k=1}^{n}\overline{CP_k}^{2}
$$

의 값은?

① $\frac{a^{2}+b^{2}}{2}$　　② $\frac{a^{2}+b^{2}}{3}$　　③ $\frac{a^{2}+b^{2}}{4}$　　④ $3(a^{2}+b^{2})$　　⑤ $2(a^{2}+b^{2})$

![예제309 그래프](./images/04-integral/exer309.png)

> [!summary]- 풀이
>
> 빗변의 길이를 먼저 구한다.
>
> $$\overline{AB} = \sqrt{a^{2}+b^{2}}$$
>
> $P_k$는 $B$에서 빗변을 $n$등분한 $k$번째 점이므로
>
> $$\overline{BP_k} = \frac{\sqrt{a^{2}+b^{2}}}{n}\cdot k$$
>
> 코사인 법칙으로 $\overline{CP_k}^{2}$을 구한다. $\angle B$에서 $\cos B = \frac{a}{\sqrt{a^{2}+b^{2}}}$이므로
>
> $$\overline{CP_k}^{2} = \overline{BP_k}^{2} + a^{2} - 2\cdot a\cdot\overline{BP_k}\cdot\cos B$$
>
> $$= \left(\frac{\sqrt{a^{2}+b^{2}}}{n}k\right)^{2} + a^{2} - 2\cdot a\cdot\frac{\sqrt{a^{2}+b^{2}}}{n}k\cdot\frac{a}{\sqrt{a^{2}+b^{2}}}$$
>
> $$= (a^{2}+b^{2})\left(\frac{k}{n}\right)^{2} + a^{2} - 2a^{2}\cdot\frac{k}{n}$$
>
> 구분구적법을 적용한다. ($\frac{k}{n} \to x$, $\frac{1}{n} \to dx$, 구간 $[0,1]$)
>
> $$\lim_{n \to \infty}\frac{1}{n}\sum_{k=1}^{n}\overline{CP_k}^{2} = \int_{0}^{1}\left[(a^{2}+b^{2})x^{2} - 2a^{2}x + a^{2}\right]dx$$
>
> $$= \left[\frac{a^{2}+b^{2}}{3}x^{3} - a^{2}x^{2} + a^{2}x\right]_{0}^{1}$$
>
> $$= \frac{a^{2}+b^{2}}{3} - a^{2} + a^{2} = \frac{a^{2}+b^{2}}{3}$$
>
> **정답: ②**

---

## 학습 포인트

1. **분모에 상수항이 있는 경우**: $\frac{n}{an+1} \to \frac{1}{a}$로 극한 처리 후 정적분으로 변환
2. **분할 간격이 $\frac{2}{n}$인 경우**: $\frac{1}{n} = \frac{1}{2}\cdot\frac{2}{n}$으로 분리하여 계수 $\frac{1}{2}$를 앞으로 빼기
3. **우합과 좌합의 오차**: 증가함수에서 $A-B = \frac{1}{n}(f(b)-f(a))$
4. **비등분 구간**: 정적분 대신 **무한등비급수**로 변환하여 계산
5. **기하학적 응용**: 코사인 법칙 → $\overline{CP_k}^2$ 표현 → 구분구적법으로 정적분 변환

---

**관련 강의**:
- [[46-definite-integral-intro|정적분의 정의와 무한급수]]
- [[47-fundamental-theorem|정적분과 부정적분의 관계]]
- [[49-integral-series-3|정적분과 무한급수(3)]]
