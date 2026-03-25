---
id: 46-definite-integral-intro-note
aliases: []
tags: []
---

### Def(5) 정적분의 정의

#### 핵심 1) 무한급수식을 정적분으로 바꾸는 기본방식

$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n} f\left( a+\frac{b-a}{n}k \right)\cdot \frac{b-a}{n}
$$

$$
\lim \Sigma \implies \int
$$

$$
a+\frac{b-a}{n}k \implies x
$$

$$
\frac{b-a}{n} \implies dx
$$

$$
dx=\Delta x= x_{2}-x_{1}
=\left( a+\frac{b-a}{n}\cdot 2 \right)-\left( a+\frac{b-a}{n} \cdot 1 \right)
=\frac{b-a}{n}
$$

정적분의 적분구간은
무한급수의 첫번쨰값을 가지는 함수값과
무한급수의 마지막값을 가지는 함수값으로 정해진다.

k=1일떄

$$
a+\frac{b-a}{n}k =a
$$

k=n 일떄

$$
a+\frac{b-a}{n}k=b
$$

위 단계를 거치면 아래에 식이 나오는것을 알수있다.

$$
\int_{a}^{b}f(x)\ dx
$$

### Thm47 정적분과 무한급수

$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n} f\left( a+\frac{p}{n}k \right)\cdot \frac{p}{n}
$$

#### 위 준식을 정적분으로 바꾸는 여러방식

##### (1) $a+\frac{p}{n}k=x$ 로 두면

$$
dx=a+\frac{p}{n}\cdot 2 - \left( a+\frac{p}{n} \cdot 1 \right)=\frac{p}{n}
$$

적분구간

$$
\lim_{ n \to \infty } a+\frac{p}{n} \cdot 1 = a
$$

$$
\lim_{ n \to \infty } a+\frac{p}{n} \cdot n = a+p
$$

$$
\int_{a}^{a+p} f(x)\ dx
$$

---

##### (2) $\frac{p}{n}k=x$로 두면

$$
dx = \frac{p}{n}\cdot 2 - \left( \frac{p}{n} \cdot 1 \right)=\frac{p}{n}
$$

적분구간

$$
\lim_{ n \to \infty } \frac{p}{n} \cdot 1 = 0
$$

$$
\lim_{ n \to \infty } \frac{p}{n} \cdot n = p
$$

$$
\int_{0}^{p} f(a+x)\ dx
$$

(1)에서 -a만큼 그래프가 평행이동하고 아래띁 위끝또한 -a 만큼 줄어들었다

---

##### (3) $\frac{k}{n}=x$로 두면

$$
dx= \frac{1}{n} \cdot 2 - \frac{1}{n} \cdot 1 = \frac{1}{n}
$$

적분구간

$$
\lim_{ n \to \infty } \frac{1}{n} \cdot 1 = 0
$$

$$
\lim_{ n \to 1 } \frac{1}{n} \cdot n = 1
$$

$$
p\int_{0}^{1}f(a+px)\ dx
$$

---

##### (4) $\frac{k}{2n}=x$로 두면

$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}f\left( a+\frac{p}{n}k \right)\cdot \frac{p}{n}
=\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( a+2p\cdot \frac{k}{2n} \right) \cdot \frac{2p}{2n}
$$

$$
dx= \frac{1}{2n} - \frac{2}{2n}  = \frac{1}{2n}
$$

적분구간

$$
\lim_{ n \to \infty } \frac{1}{2n} \cdot 1 = 0
$$

$$
\lim_{ n \to 1 } \frac{1}{2n} \cdot n = \frac{1}{2}
$$

$$
2p \int_{0}^{\frac{1}{2}}f(a+2px)\ dx
$$

(3)과 (4)의에서 x의 계수가 다른데
(3)의 f(x)그래프가 x축에서 2배 만큼 압축되었다고 생각하면된다.

---

##### 간단예제

$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}f\left( 1+\frac{5}{n}k \right)\cdot \frac{1}{n}
$$

위 무한급수식을 정적분으로 바꿔보자
(1) $1+\frac{5}{n}k=x$
(2)$\frac{5}{n}k=x$
(3)$\frac{k}{n}=x$

---

(1)

$$
dx=\frac{5}{n}
$$

$$
\text{lower limit}=1,\ \text{upper limit}=6
$$

$$
GE=\int_{1}^{6}f(x) \cdot \frac{1}{n} \cdot \frac{5}{5}
$$

$$
=\frac{1}{5}\int_{1}^{6}f(x)\ dx
$$

(2)

$$
\frac{1}{5}\int_{0}^{5}f(1+x)\ dx
$$

(3)

$$
\int_{0}^{1}f(1+5x)\ dx
$$

