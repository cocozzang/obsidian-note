---
id: 56-area-integral-2-note
aliases: []
tags: []
---

### 예제377

$$
\int_{0}^{2} |x^{2}(x-1)|\ dx =?
$$

---

f(x)는 x=0에서 극점을 가지고 오른쪾꼬리가 위로 향하는 개형
그래프를 직접 그려보면 적분구간 0,1에서 음이 되므로

$$
GE=-\int_{0}^{1}x^{2}(x-1)\ dx + \int_{1}^{2}x^{2}(x-1)\ dx
$$

$$
=\frac{1}{12}(1-0)^{4}+\int_{1}^{2}x^{3}-x^{2}\ dx
$$

$$
=\frac{1}{12}+\left[ \frac{1}{4}x^{4}-\frac{1}{3}x^{3} \right]_{1}^{2}
$$

$$
=\frac{1}{12}+\frac{1}{4}(16-1)-\frac{1}{3}(8-1)
$$

$$
=\frac{1}{12}+\frac{15}{4}-\frac{7}{3}
$$

$$
=\frac{1+45-28}{12}=\frac{18}{12}=\frac{3}{2}
$$

### 예제 378

자연수 $n$에 대하여, 두 곡선

$$y = x^{2}-2, \quad y = -x^{2}+\dfrac{2}{n^{2}}$$

로 둘러싸인 도형의 넓이를 $S_{n}$이라 할 때, $\displaystyle\lim_{n \to \infty} S_{n}$의 값은?

① $\dfrac{16}{3}$ ② $\dfrac{14}{3}$ ③ $4$ ④ $\dfrac{10}{3}$ ⑤ $\dfrac{8}{3}$

---

$n \to \infty$ 이므로

$$
y=-x^{2}+\frac{2}{n^{2}} \implies y=-x^{2}
$$

넓이S_n 은

$$
y=x^{2}-2,\ y=-x^{2}
$$

로 둘러쌓인 넓이라고 볼수 있다

$$
S_{n}=\frac{|a-a'|}{6}(\beta-\alpha)^{3}
$$

알파 베타 구하기 (두 함수의 교점)

$$
x^{2}-2=-x^{2}
$$

$$
2x^{2}=2
$$

$$
x= \pm 1
$$

$$
S_{n}=\frac{|1-(-1)|}{6}(1-(-1))^{3}
$$

$$
=\frac{1}{3} \cdot 2^{3}=\frac{8}{3}
$$

### 예제379

![exer379|1000](./images/04-integral/exer379.png)

---

$$
S=\frac{1}{6}(b-a)^{3}=36
$$

$$
b-a = 6
$$

$$
b=a+6
$$

$$
\overline{PQ}=\sqrt{ (b-a)^{2}+(b^{2}-a^{2})^{2} }
$$

$$
=\sqrt{ 36+(a^{2}+12a+36-a^{2})^{2} }
$$

$$
=\sqrt{ 36+(12a+36)^{2} }
$$

$$
\lim_{ a \to \infty } \frac{\overline{PQ}}{a}
=\lim_{ a \to \infty } \frac{\sqrt{ 36+(12a+36)^{2} }}{a}
$$

$$
=\frac{12}{1}=12
$$

### 예제380

![exer380|1000](./images/04-integral/exer380.png)

---

$$
f(x)=-x^{2}+2x,\ g(x)=bx,\ h(x)=ax
$$

![exer380-1|300](./images/04-integral/exer380-1.png)

g와 f로 둘러쌓인 넓이$S_{B}$는 f와 h로 둘러쌓인 넓이$S_{A}$의 두배이다 

f h 교점과 f g 교점은 아래와 같다
$$
ax=-x^{2}+2x
$$
$$
x(x-2+a)=0
$$
$$
x=0,\ 2-a
$$

$$
bx=-x^{2}+2x
$$
$$
x(x-2+b)=0
$$
$$
x=0,\ 2-b
$$


$$
S_{A}=\frac{1}{6}(2-a)^{3}
$$
$$
S_{B}=\frac{1}{6}(2-b)^{3}
$$

$$
2 \cdot \frac{1}{6}(2-a)^{3}= \frac{1}{6}(2-b)^{3}
$$
$$
2(2-a)^{3}=(2-b)^{3}
$$
$$
\sqrt[3]{ 2 }(2-a)=2-b
$$
$$
b=a-2 \cdot \sqrt[3]{ 2 }+2
$$
라는 관계식을 가지는 a,b임으로 보기중에 적절한 그래프는 3번이다 


### 예제381
![[exer381.png]]

---

$$
S_{\triangle_{ABC}}= \frac{3}{4}\cdot \frac{1}{6} (b-a)^{3}
$$
$$
=\frac{(b-a)^{3}}{8}
$$


### 예제382
![[exer382.png]]

---

![[exer382-1.png|300]]

$$
S_{n}=\int_{0}^{\frac{1}{n}} \left( x-\frac{1}{n} \right)^{2}\ dx
$$
$$
=\int_{-\frac{1}{n}}^{0}\left( x+\frac{1}{n}-\frac{1}{n} \right)^{2}\ dx
$$
$$
=\left[ \frac{1}{3}x^{3} \right]_{-\frac{1}{n}}^{0}
=0-\left( \frac{1}{3} \cdot -\frac{1}{n^{3}} \right)
$$
$$
=\frac{1}{3n^{3}}
$$

$$
\lim_{ n \to \infty } n^{3}S_{n}=
\lim_{ n \to \infty } n^{3} \cdot \frac{1}{3n^{3}}
=\frac{1}{3}
$$


### 예제383
![[exer383.png]]

---

![[exer383-1.png|300]]


$$
B=2A
$$
각 교점의 x은 $\pm\sqrt{ a },\ \pm \sqrt{ b }$

$$
\frac{1}{6}\cdot (2\sqrt{ b })^{3}=2 \cdot \frac{1}{6} \cdot (2\sqrt{ a })^{3}
$$
$$
2\sqrt{ b }=\sqrt[3]{ 2 } \cdot 2\sqrt{ a }
$$
$$
4b=\sqrt[3]{ 4 }\cdot 4 a
$$
$$
b=\sqrt[3]{ 4 } \cdot a
$$

정답은 1번이다