---
id: c3d4e5f6-a7b8-4c9d-b1e2-f3a4b5c6d7e8
aliases:
  - 정적분과 부정적분의 관계
  - 미적분학의 기본정리
  - Thm48
  - 정적분 계산
tags:
  - 정적분
  - 부정적분
  - 미적분학의기본정리
  - 정적분계산
  - 무한급수와정적분
pages: 140-141
subject: 대학기초수학
title: 정적분과 부정적분의 관계
topics:
  - 정적분과 부정적분의 관계 (Thm 48)
  - 미적분학의 기본정리 증명
  - 무한급수를 정적분으로 변환하여 계산
  - 정적분 구간 변환 기법
---

# 47강: 정적분과 부정적분의 관계

## 1. 정적분과 부정적분의 관계

### Thm (48): 정적분과 부정적분의 관계

$$
\boxed{
(1)\quad \frac{d}{dx}\int_{a}^{x}f(t)\,dt = f(x)
}
$$

$$
\boxed{
(2)\quad \int f(x)\,dx = F(x)+C \text{라 하면} \quad \int_{a}^{b}f(x)\,dx = \bigl[F(x)\bigr]_{a}^{b} = F(b)-F(a)
}
$$

---

### (1)의 증명

**i) $f(t) \geq 0$일 때**

정적분의 정의에 의해 그림에서 $S(x) = \int_{a}^{x}f(t)\,dt$임을 알 수 있다.

$x$의 증분 $\Delta x$에 대한 $S(x)$의 증분을 $\Delta S$라 할 때,

먼저 $\Delta x > 0$이면

$$\Delta S = S(x+\Delta x) - S(x)$$

즉, 그림에서 빗금 친 부분의 넓이이다. 이 때, $[x,\ x+\Delta x]$에서 $f(t)$의 최솟값을 $m$, 최댓값을 $M$이라 하면

$$m\Delta x \leq \Delta S \leq M\Delta x \quad \cdots \odot$$

만약 $\Delta x < 0$일 때도 같은 방법으로

$$M\Delta x \leq \Delta S \leq m\Delta x \quad \cdots \odot$$

임을 알 수 있다.

$\odot$, $\odot$에서 양변을 $\Delta x$로 나누면

$$m \leq \frac{\Delta S}{\Delta x} \leq M$$

샌드위치 극한에 의해 $\lim_{\Delta x \to 0}m = \lim_{\Delta x \to 0}M = f(x)$이므로

$$\lim_{\Delta x \to 0}\frac{\Delta S}{\Delta x} = f(x) \quad \Leftrightarrow \quad S'(x) = f(x)$$

**ii) $f(t) \leq 0$일 때도** 같은 방법으로 $S'(x) = f(x)$임을 알 수 있다.

$$\therefore \quad \frac{d}{dx}\int_{a}^{x}f(t)\,dt = \frac{d}{dx}S(x) = S'(x) = f(x) \quad \square$$

---

### (2)의 증명

$\frac{d}{dx}\int_{a}^{x}f(t)\,dt = f(x)$의 양변을 부정적분해 보면

$$\int_{a}^{x}f(t)\,dt = F(x)+C \quad \cdots \odot$$

양변에 $x=a$를 대입하면

$$0 = F(a)+C \quad \therefore\ C = -F(a)$$

이를 $\odot$에 대입하면

$$\int_{a}^{x}f(t)\,dt = F(x)-F(a)$$

양변에 $x=b$를 대입하면

$$\therefore \quad \int_{a}^{b}f(t)\,dt = F(b)-F(a) \quad \Leftrightarrow \quad \int_{a}^{b}f(x)\,dx = F(b)-F(a) = \bigl[F(x)\bigr]_{a}^{b} \quad \square$$

---

## 2. 예제

### 예제 300

$$\lim_{n \to \infty}\sum_{k=1}^{n}\left(3+\frac{2k}{n}\right)^{3}\frac{1}{n}$$

을 다음 각 경우로 고치고 그 값을 구하여라.

> [!summary]- 풀이
>
> **준식 변형**: $\frac{1}{n} = \frac{1}{2}\cdot\frac{2}{n}$이므로
>
> $$\text{준식} = \frac{1}{2}\lim_{n\to\infty}\sum_{k=1}^{n}\left(3+\frac{2k}{n}\right)^{3}\cdot\frac{2}{n}$$
>
> ---
>
> **(1) 정적분 구간 길이 = 2**
>
> $3+\frac{2k}{n} = x$로 치환하면 $dx = \frac{2}{n}$
>
> 적분구간: $k=1 \to 3+0=3$, $k=n \to 3+2=5$
>
> $$= \frac{1}{2}\int_{3}^{5}x^{3}\,dx = \frac{1}{2}\left[\frac{1}{4}x^{4}\right]_{3}^{5} = \frac{1}{2}\left(\frac{625}{4}-\frac{81}{4}\right) = \frac{544}{8} = \boxed{68}$$
>
> ---
>
> **(2) 정적분 구간 길이 = 1**
>
> (1)에서 그래프와 적분구간을 $\frac{1}{2}$배 압축 ($x \to 2x$):
>
> $$2\cdot\frac{1}{2}\int_{\frac{3}{2}}^{\frac{5}{2}}(2x)^{3}\,dx = 8\int_{\frac{3}{2}}^{\frac{5}{2}}x^{3}\,dx = 8\left[\frac{1}{4}x^{4}\right]_{\frac{3}{2}}^{\frac{5}{2}}$$
>
> $$= \frac{8}{4}\left(\frac{625}{16}-\frac{81}{16}\right) = \frac{625}{8}-\frac{81}{8} = \boxed{68}$$
>
> ---
>
> **(3) 정적분 구간 길이 = 3**
>
> (2)에서 그래프와 적분구간을 $3$배 확장 ($x \to \frac{1}{3}x$):
>
> $$\frac{1}{3}\cdot 8\int_{\frac{9}{2}}^{\frac{15}{2}}\left(\frac{1}{3}x\right)^{3}\,dx = \frac{8}{3}\cdot\frac{1}{27}\int_{\frac{9}{2}}^{\frac{15}{2}}x^{3}\,dx = \frac{8}{81}\left[\frac{1}{4}x^{4}\right]_{\frac{9}{2}}^{\frac{15}{2}}$$
>
> $$= \frac{2}{81}\left(\frac{15^{4}}{16}-\frac{9^{4}}{16}\right) = \frac{5^{4}}{8}-\frac{3^{4}}{8} = \frac{625}{8}-\frac{81}{8} = \boxed{68}$$

---

### 예제 301

다음 극한값을 구하여라.

**(1)**

$$\lim_{n \to \infty}\sum_{k=1}^{n}\left(1+\frac{3k}{n}\right)\frac{1}{n}$$

> [!summary]- 풀이
>
> $1+\frac{3k}{n} = x$로 치환하면 $dx = \frac{3}{n}$이므로 $\frac{1}{n} = \frac{1}{3}\cdot\frac{3}{n}$
>
> 적분구간: $k=1 \to 1$, $k=n \to 4$
>
> $$= \frac{1}{3}\int_{1}^{4}x\,dx = \frac{1}{3}\left[\frac{1}{2}x^{2}\right]_{1}^{4} = \frac{1}{6}(16-1) = \frac{15}{6} = \boxed{\frac{5}{2}}$$

**(2)**

$$\lim_{n \to \infty}\frac{1^{4}+2^{4}+3^{4}+\cdots+n^{4}}{n^{5}}$$

> [!summary]- 풀이
>
> $$\text{준식} = \lim_{n \to \infty}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{4}\frac{1}{n}$$
>
> $\frac{k}{n} = x$로 치환하면 $dx = \frac{1}{n}$
>
> 적분구간: $k=1 \to 0$, $k=n \to 1$
>
> $$= \int_{0}^{1}x^{4}\,dx = \left[\frac{1}{5}x^{5}\right]_{0}^{1} = \boxed{\frac{1}{5}}$$

**(3)**

$$\lim_{n \to \infty}\frac{1}{n^{4}}\{(3n-1)^{3}+(3n-2)^{3}+\cdots+(3n-n)^{3}\}$$

> [!summary]- 풀이
>
> $$\text{준식} = \lim_{n \to \infty}\sum_{k=1}^{n}(3n-k)^{3}\cdot\frac{1}{n^{4}} = \lim_{n \to \infty}\sum_{k=1}^{n}(3n-k)^{3}\cdot\left(\frac{1}{n}\right)^{3}\cdot\frac{1}{n}$$
>
> $$= \lim_{n \to \infty}\sum_{k=1}^{n}\left(3-\frac{k}{n}\right)^{3}\frac{1}{n}$$
>
> $3-\frac{k}{n} = x$로 치환하면 $dx = -\frac{1}{n}$
>
> 적분구간: $k=1 \to 3$, $k=n \to 2$
>
> $$= -\int_{3}^{2}x^{3}\,dx = \int_{2}^{3}x^{3}\,dx = \left[\frac{1}{4}x^{4}\right]_{2}^{3} = \frac{81}{4}-\frac{16}{4} = \boxed{\frac{65}{4}}$$
>
> > [!tip] 적분구간 역순 성질
> > $$\int_{b}^{a}f(x)\,dx = -\int_{a}^{b}f(x)\,dx$$
> > $dx$가 음수로 나오면 적분구간이 역순이 되고, $-$부호를 붙여 구간을 바꿀 수 있다.

**(4)**

$$\lim_{n \to \infty}\frac{(1+2+\cdots+n)(1^{4}+2^{4}+\cdots+n^{4})}{(1^{2}+2^{2}+\cdots+n^{2})(1^{3}+2^{3}+\cdots+n^{3})}$$

> [!summary]- 풀이
>
> 각 합을 $\frac{1}{n}$을 인수로 갖는 리만합으로 변환한다:
>
> $$\text{준식} = \lim_{n \to \infty}\frac{\frac{1}{n}\sum_{k=1}^{n}\frac{k}{n}\cdot\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{4}}{\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{2}\cdot\frac{1}{n}\sum_{k=1}^{n}\left(\frac{k}{n}\right)^{3}}$$
>
> $\frac{k}{n} = x$로 치환 ($dx=\frac{1}{n}$, 구간 $[0,1]$):
>
> $$= \frac{\int_{0}^{1}x\,dx\cdot\int_{0}^{1}x^{4}\,dx}{\int_{0}^{1}x^{2}\,dx\cdot\int_{0}^{1}x^{3}\,dx} = \frac{\left[\frac{1}{2}x^{2}\right]_{0}^{1}\cdot\left[\frac{1}{5}x^{5}\right]_{0}^{1}}{\left[\frac{1}{3}x^{3}\right]_{0}^{1}\cdot\left[\frac{1}{4}x^{4}\right]_{0}^{1}} = \frac{\frac{1}{2}\cdot\frac{1}{5}}{\frac{1}{3}\cdot\frac{1}{4}} = \frac{\frac{1}{10}}{\frac{1}{12}} = \boxed{\frac{6}{5}}$$

---

### 예제 302

다음은 $\displaystyle\lim_{n \to \infty}\sum_{k=1}^{n}\left(3-\frac{2k}{n}\right)^{2}\frac{4}{n}$를 정적분으로 나타낸 것이다. **틀린 것**은?

$$\text{①}\ \int_{1}^{3}2x^{2}\,dx \qquad \text{②}\ \int_{-2}^{0}2(x+3)^{2}\,dx \qquad \text{③}\ \int_{-1}^{0}4(2x+3)^{2}\,dx \qquad \text{④}\ \int_{0}^{1}4(2x+3)^{2}\,dx$$

> [!summary]- 풀이
>
> **기준 정적분 구하기**: $3-\frac{2k}{n} = x$로 치환하면 $dx = -\frac{2}{n}$이므로 $\frac{4}{n} = -2\cdot\left(-\frac{2}{n}\right)$
>
> 적분구간: $k=1 \to 3$, $k=n \to 1$
>
> $$\text{준식} = -2\int_{3}^{1}x^{2}\,dx = 2\int_{1}^{3}x^{2}\,dx = \int_{1}^{3}2x^{2}\,dx$$
>
> ---
>
> **① $\int_{1}^{3}2x^{2}\,dx$** → **참** ✅ (위에서 구한 기준값)
>
> ---
>
> **② $\int_{-2}^{0}2(x+3)^{2}\,dx$** → **참** ✅
>
> ①에서 그래프와 적분구간을 $-3$만큼 평행이동 ($x \to x+3$):
> 구간 $[1,3] \to [-2,0]$, 피적분함수 $x^{2} \to (x+3)^{2}$
>
> ---
>
> **③ $\int_{-1}^{0}4(2x+3)^{2}\,dx$** → **참** ✅
>
> ②에서 $x$축 방향으로 $\frac{1}{2}$배 압축 ($x \to 2x$):
> 구간 $[-2,0] \to [-1,0]$, 적분값 보정 위해 $\times 2$, 피적분함수 $x \to 2x$
>
> $$2\int_{-1}^{0}2(2x+3)^{2}\,dx = \int_{-1}^{0}4(2x+3)^{2}\,dx$$
>
> ---
>
> **④ $\int_{0}^{1}4(2x+3)^{2}\,dx$** → **거짓** ❌
>
> ③의 적분구간은 $[-1, 0]$이어야 하는데 $[0, 1]$로 잘못 표기되었다.
>
> $$\therefore \text{ 답: } \boxed{④}$$

---

## 관련 주제

- [[46-definite-integral-intro|46강: 정적분의 정의와 무한급수]]
- [[48-integral-series-2|48강: 정적분과 무한급수 (2)]]

---

**학습 포인트:**
1. Thm 48 (1): $\frac{d}{dx}\int_{a}^{x}f(t)\,dt = f(x)$ — 적분한 뒤 미분하면 원래 함수로 돌아온다.
2. Thm 48 (2): 정적분 = $[F(x)]_{a}^{b} = F(b)-F(a)$ — 부정적분을 구한 뒤 위끝·아래끝을 대입한다.
3. 무한급수 → 정적분 변환 시, $dx$가 음수이면 적분구간이 역순이 되고 부호를 조정한다.
4. 정적분 구간 변환(평행이동·압축·확장)은 피적분함수와 구간이 함께 변한다.
