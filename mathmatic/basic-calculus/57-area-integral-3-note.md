---
id: 57-area-integral-3-note
aliases: []
tags: []
---

### 예제384

![[exer384.png]]

---

$$
\int_{0}^{1}(x^{2}+2x+3)\ dx = \int_{0}^{1}x^{2}\ dx + \int_{0}^{1}2x\ dx + \int_{0}^{1}3\ dx
$$
$$
=1-S_{1}-2(1-S_{2})+3
$$
$$
=-S_{1}+2S_{2}+2
$$

### 예제 385

이차방정식 $x^{2}+2006x-2007=0$의 두 근을 $\alpha$, $\beta$라 할 때, 정적분

$$\dfrac{1}{(\alpha-\beta)^{4}}\int_{\alpha}^{\beta}(x-\alpha)(x-\beta)^{2}\,dx$$

의 값은?

① $\dfrac{1}{2}$ ② $\dfrac{1}{4}$ ③ $\dfrac{1}{6}$ ④ $\dfrac{1}{8}$ ⑤ $\dfrac{1}{12}$

---

$$
y=(x-\alpha)(x-\beta)^{2}
$$
의 개형은 아래와 같다 

![[exer385.png|400]]


두 넓이를 각각 A,B라고 했을떄 
$$
\int_{\alpha}^{\beta}(x-\alpha)(x-\beta)^{2}\ dx= A,B
$$
$$
A=\frac{1}{12}(\beta-\alpha)^{4} 
$$

$$
B=-\int_{\beta}^{\alpha}(x-\alpha)(x-\beta)^{2}\ dx
$$

$$
=\int_{\alpha}^{\beta}(x-\alpha)(x-\beta)^{2}\ dx
$$
$$
=\frac{1}{12}(\alpha-\beta)^{4}
$$


4승 내에 부호는 역전되어도 상관없으니 A=B임을 알수있고 

$$
\frac{1}{(\alpha-\beta)^{4}} \cdot \int_{\alpha}^{\beta}(x-\alpha)(x-\beta)^{2}\ dx
$$
$$
=\frac{1}{(\alpha-\beta)^{4}} \cdot \frac{1}{12}(\alpha-\beta)^{4}
$$
$$
=\frac{1}{12}
$$

### 예제386
![[exer386.png]]

---

$$
f(x)=ax^{2}+bx+c
$$
에서 $-x_{2}$ 만큼 평행이동한 함수를 g(x)라 두면 해당 적분은 아래와 같이 표현된다
$$
g(x)=px^{2}+qx+r
$$

$$
\int_{-1}^{1}(px^{2}+qx+r)\ dx
$$
$$
=2\int_{0}^{1} px^{2}+r\ dx
$$
$$
=2 \left[ \frac{1}{3}px^{3}+rx \right]_{0}^{1}
$$
$$
=\frac{2}{3}p+2r
$$
$$
=\frac{1}{3}(2p+6r)
=\frac{1}{3}(2p+2r+4r)
$$

p q r 과 y1, y2,y3에 대한 관계는 함수 g를 통해 아래와 같이 알 수 있다.
$$
g(-1)=p-q+r=y_{1}
$$
$$
g(0)=r=y_{2}
$$
$$
g(1)=p+q+r=y_{3}
$$
$$
y_{3}+y_{1}=2p+2r
$$

$$
\therefore \frac{1}{3}(2p+2r+4r)=\frac{1}{3}(y_{1}+4y_{2}+y_{3})
$$

### Thm50 역함수의 넓이 

$$
\int_{f(a)}^{f(b)}g(x)\ dx = \{b f(b)-af(a)\}-\int_{a}^{b}f(x)\ dx
$$

[[52-integral-inverse-function-note#Thm50 역함수와 정적분| 역함수와 정적분]]
를 참고하면 된다 

함수 f(x)의 역함수를 g(x)라 할때
$$
\int_{a}^{b}f(x)\ dx + \int_{f(a)}^{f(b)}g(x)\ dx = S_{1}+S_{2}
$$
$$
=b f(b)-af(a)
$$


### 예제387
![[exer387.png]]

---

$$
\int_{0}^{16} g(x)\ dx 
= 16 \cdot 2 - \int_{0}^{2}x^{4}\ dx
$$
$$
=32-\left[ \frac{1}{5}x^{5} \right]_{0}^{2}
$$
$$
=32-\frac{32}{5}
$$
$$
=\frac{160-32}{5}=\frac{128}{5}
$$

### 예제388
![[exer388.png]]

---

보면 바로 알아야함
$$
GE=1
$$

### 예제389
$$
\int_{0}^{1}e^{x}\ dx + \int_{1}^{e} \ln x\ dx=?
$$
---

$$
1 \cdot e = e
$$

### 예제390
함수 $f(x)=e^{x}+e^{2x}$ 와  그 역함수 g(x)에 대하여 
$$
\int_{0}^{\ln 2} f(x)\ dx + \int_{2}^{6} g(x)\ dx =?
$$
---

$$
f(0)=1+1=2
$$
$$
f(\ln 2)= 2+4=6
$$

으로
GE는 적분구간이 서로 대응되는 두 함수, 역함수 적분의 합이므로 

$$
GE= \ln 2 \cdot 6= 6 \ln 2
$$