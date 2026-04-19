---
id: 60-volume-integral-1-note
aliases: []
tags: []
---

### 예제406
![[exer406.png]]

---

![[exer406-1.png|600]]
$$
x^{2}+y^{2}=r^{2}
$$
$$
V_{y}=\pi \int_{-\frac{3}{2}r}^{r} x^{2} dy
$$
$$
=\pi \int_{-\frac{3}{2}r}^{r}r^{2}-y^{2}\ dy
$$

### 예제407
![[exer407.png]]

---

$$
V=\pi\int_{0}^{3}x_{1}^{2}-x_{2}^{2}\ dy
$$

$$
x_{1}^{2}=9-y^{2}
$$
$$
x_{2}^{2}=6-2y
$$

$$
V= \pi \int_{0}^{3} 9-y^{2}-6+2y\ dx
=\pi \int_{0}^{3}3+2y-y^{2}\ dy
$$
$$
=\pi\left[ 3y+y^{2}-\frac{1}{3}y^{3} \right]_{0}^{3}
$$
$$
=\pi(9+9-9)=9\pi
$$

$$
\frac{1}{\pi}V 
=\frac{1}{\pi}9\pi
=9
$$


### 예제 408

곡선 $y = x(1-x)$와 $x$축으로 둘러싸인 도형을 $x$축의 둘레로 회전시킬 때 만들어지는
회전체의 부피는?

① $\dfrac{\pi}{6}$ $\quad$ ② $\dfrac{\pi}{10}$ $\quad$ ③ $\dfrac{\pi}{15}$ $\quad$ ④ $\dfrac{\pi}{20}$ $\quad$ ⑤ $\dfrac{\pi}{30}$

---

$$
V_{x}=\pi \int_{0}^{1}y^{2}\ dx
$$
$$
=\pi \int_{0}^{1} (x-x^{2})^{2}\ dx
=\pi \int_{0}^{1}x^{2}-2x^{3}+x^{4}\ dx
$$
$$
=\pi \left[ \frac{1}{3}x^{3}-\frac{2}{4}x^{4}+\frac{1}{5}x^{5} \right]_{0}^{1}
$$
$$
=\pi\left( \frac{1}{3}-\frac{1}{2}+\frac{1}{5} \right)
$$
$$
=\pi\left( \frac{10-15+6}{30} \right)
=\frac{\pi}{30}
$$

### 예제 409

곡선 $y = \sqrt{x}$와 $x$축 및 직선 $x = 4$로 둘러싸인 도형을 $x$축을 중심으로 회전시켜
얻은 회전체의 부피는?

① $8\pi$ $\quad$ ② $7\pi$ $\quad$ ③ $6\pi$ $\quad$ ④ $5\pi$ $\quad$ ⑤ $4\pi$

---

$$
V_{x}=\pi \int_{0}^{4} y^{2}\ dx
$$
$$
=\pi \int_{0}^{4}x\ dx
=\pi \left[ \frac{1}{2}x^{2} \right]_{0}^{4}
$$
$$
\frac{16}{2}\pi = 8\pi
$$

### 예제 410

곡선 $y = a(1-x^2)$과 $x$축으로 둘러싸인 도형을 $y$축의 둘레로 회전시켜 생기는 회전
체의 부피가 $16\pi$일 때, 양수 $a$의 값을 구하시오.

---

$$
V_{y}=\pi \int_{0}^{a}x^{2}\ dy
$$
$$
=\pi \int_{0}^{a}\left( 1-\frac{1}{a}y \right)\ dy
$$
$$
=\pi\left[ y-\frac{1}{2a}y^{2} \right]_{0}^{a}
$$
$$
=\pi\left( a-\frac{1}{2}a \right)
=\frac{1}{2}a\pi =16\pi
$$
$$
a=32
$$

### 예제411
![[exer411.png]]

---

![[exer411-1.png|400]]

(1) $0 \leq h \leq r$
$$
V=\pi r^{2}h
$$
$$
\frac{dV}{dh}=\pi r^{2}
$$
변화량이 일정하다

(2) $r\leq h \leq 2r$
$$
V=\pi r^{2} \cdot  r + \pi \int_{r}^{h} x^{2} \ dy
$$
$$
=\pi r^{3}+\pi \int_{r}^{2r}y^{2}\ dy
$$
$$
=\pi r^{3}+ \pi \left[ \frac{1}{3}y^{3} \right]_{r}^{h}
$$
$$
=\pi r^{3}+\pi \left( \frac{1}{3}h^{3}-\frac{1}{3}r^{3} \right)
$$
$$
=\frac{2}{3}\pi r^{3}+\frac{\pi}{3}h^{3}
$$
$$
\frac{dV}{dh}=\pi h^{2}
$$
0~r까지는 일정한 변화율을 가지고 r~2r까지 변화율이 이차함수와 같은 개형으로 나타난다
그러므로 정답은 3번이다
