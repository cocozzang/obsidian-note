---
id: 52-integral-inverse-function-note
aliases: []
tags: []
---

### 예제333

함수 $f(x)=\tan(\sin x)$에 대하여

$$
\int_{-\frac{\pi}{6}}^{\frac{\pi}{6}} f(x)\ dx =?
$$

---

$$
f(-x)=\tan(\sin-x)
$$

$$
=\tan(-\sin x)
$$

$$
=-\tan (\sin x)
$$

$$
=-f(x)
$$

f(x)는 기함수임으로

$$
GE=0
$$

### 예제334

$$
\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}|x|\cos x\ dx=?
$$

$$
2\pi,\ \pi-1,\ \frac{\pi}{2}+1,\ \pi-2,\ \frac{\pi}{2}-1
$$

---

우함수 x 우함수 꼴임으로

$$
GE= 2\int_{0}^{\frac{\pi}{2}}|x|\cos x\ dx
$$

$$
\int x\cos x\ dx=x\sin x-\int 1\cdot \sin x\ dx
$$

$$
=x\sin x+\cos x
$$

$$
GE=2[x\sin x+\cos x]_{0}^{\frac{\pi}{2}}
$$

$$
=2\left( \frac{\pi}{2}+0-0-1 \right)
$$

$$
=\pi-2
$$

### 예제335

$$
f(x)=ax^{2}+bx+c,\ \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}f(x)\cdot \sin x\ dx=4
$$

일때 b의 값을 구하여라

---

$$
\text{put} g(x)=f(x)\cdot \sin x
$$

$$
=ax^{2}\sin x+bx\sin x+c\sin x
$$

$ax^{2}\sin x$, $c\sin x$는 기함수 임으로 GE의 적분구간내에서 0이 된다

$$
GE= \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}g(x)\ dx =4
$$

$$
=0+0\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}bx\sin x\ dx
$$

$$
=2\int_{0}^{\frac{\pi}{2}}bx\sin x\ dx = 4
$$

$$
=2b[x(-\cos x)-1 \cdot (-\sin x)]_{0}^{\frac{\pi}{2}}
$$

$$
=2b[-x\cos x+\sin x]_{0}^{\frac{\pi}{2}}
$$

$$
=2b(0+1-0-0)
$$

$$
=2b\cdot 1=4
$$

$$
b=2
$$

### 예제336

연속함수 f(x)가 $f(x)+f(-x)=\sin \frac{\pi}{2}+1$ 을 만족할떄

$$
\int_{-\pi}^{\pi}f(x)\ dx=?
$$

---

f(x)와 f(-x)는 x=0에서 대칭함으로
GE는 아래 두가지식으로 표현가능하다

$$
GE=\int_{-\pi}^{0}f(x)+f(-x)\ dx
$$

$$
GE=\int_{0}^{\pi}f(x)+f(-x)\ dx
$$

$$
GE=\int_{0}^{\pi}f(x)+f(-x)\ dx
$$

$$
=\int_{0}^{\pi}\sin \frac{x}{2}+1\ dx
$$

$$
=\left[ -2\cos \frac{x}{2}+x \right]_{0}^{\pi}
$$

$$
=0+\pi-2-0
$$

$$
=\pi-2
$$

### 예제337

연속함수 f(x)가 $f(x)+f(1-x)=1$를 만족할때

$$
\int_{0}^{1}f(x)\sin \pi x\ dx=?
$$

---

$$
\text{put } g(x)=f(x)\cdot \sin \pi x
$$

$$
GE=\int_{0}^{1}g(x)\ dx
=\int_{0}^{\frac{1}{2}}g(x)+g(1-x)\ dx
$$

$$
g(x)+g(1-x)=f(x)\cdot \sin \pi x+f(1-x)\cdot \sin(\pi-\pi x)
$$

$$
\because \sin(x+\pi)=-\sin(x)
$$

$$
=f(x) \cdot \sin \pi x+f(1-x) \cdot (-\sin(-\pi x))
$$

$$
=f(x) \cdot \sin \pi x+f(1-x) \cdot \sin \pi x
$$

$$
=\sin \pi x (f(x)+f(1-x))
$$

$$
GE=\int_{0}^{\frac{1}{2}} \sin \pi x(f(x)+f(1-x))\ dx
$$

$$
=\int_{0}^{\frac{1}{2}}\sin \pi x \cdot 1 \ dx
$$

$$
=\left[ -\frac{1}{\pi}\cos \pi x\right]_{0}^{\frac{1}{2}}
$$

$$
=-\frac{1}{\pi}(0-1)
$$

$$
=\frac{1}{\pi}
$$

### 예제338

연속함수 f(x)가 $f(x)+f(\pi-x)=2\sin ^{2}x+1$ 을 만족할떄

$$
\int_{0}^{\pi}f(x)\ dx =?
$$

---

$f(x),\ f(\pi-x)$는 $x=\frac{\pi}{2}$에서 대칭한다

$$
GE=\int_{0}^{\frac{\pi}{2}}f(x)+f(\pi-x)\ dx
$$

$$
=\int_{0}^{\frac{\pi}{2}}2\sin ^{2}x+1\ dx
$$

$$
=2\left[ \frac{1-\cos 2x}{2} \right]_{0}^{\frac{\pi}{2}}+[x]_{0}^{\frac{\pi}{2}}
$$

$$
=[x-\cos 2x]_{0}^{\frac{\pi}{2}}+\frac{\pi}{2}
$$

$$
=\frac{\pi}{2}+1-0-1+\frac{\pi}{2}
$$

$$
=\pi
$$

### 예제339

$$
f(x)=\frac{2x}{x^{2}+1},\ \int_{0}^{\frac{1}{2}}\{f(x)+f(1-x)\}\ dx=?
$$

---

$$
GE=\int_{0}^{1}f(x)\ dx
$$

$$
=\int_{0}^{1} \frac{2x}{x^{2}+1}\ dx
$$

$$
[\ln (x^{2}+1)]_{0}^{1}
$$

$$
=\ln 2 - \ln 1
$$

$$
=\ln 2
$$

### 예제340

모든실수 x에 대하여 미분가능한 함수 f(x)가 다음조건을 만족한다
$f(1-x)=1-{f(x)}$
다음중 항상 성립한다고 할 수 없는것은?

$$
1) f(0)+f(1)=1,\ 2) f'(0)=f'(1),\ 3) \int_{0}^{1}f(x)\ dx =\frac{1}{2}
$$

$$
 (4)\  f\left( \frac{1}{2} \right)=\frac{1}{2},\ (5)\ f(0)=0
$$

---

$$
given:\ f(1-x)+f(x)=1 \tag{ex1}
$$

(1)
ex1에 0을 대입

$$
f(1-0)+f(0)=1
$$

(1)은 참이다

(2)
ex1를 미분하면

$$
-f'(1-x)+f'(x)=0
$$

x=0 대입

$$
-f'(1)+f'(0)=0
$$

$$
f'(0)=f'(1)
$$

(2)도 참이다

(3)

$$
\int_{0}^{1}f(x)\ dx
=\int_{0}^{\frac{1}{2}} f(x)+f(1-x)\ dx
$$

$$
=\int_{0}^{\frac{1}{2}}1 \ dx
$$

$$
=[x]_{0}^{\frac{1}{2}}=\frac{1}{2}
$$

3은 참이다

(4)
ex1에 x=1/2 를 대입

$$
f\left( 1-\frac{1}{2} \right)+f\left( \frac{1}{2} \right)=2f\left( \frac{1}{2} \right)=1
$$

$$
f\left( \frac{1}{2} \right)=\frac{1}{2}
$$

4는 참

(5)
ex1에 x=0 대입

$$
f(1)+f(0)=1
$$

$$
f(0)=1-f(1)
$$

f(1)이 1이라는 사실은 확정할수없으므로 (5)가 거짓이다

### 예제341

함수 f(x)가 구간 $0\leq x \leq 1$ 에서 $f(x)+f(1-x)=|x-\frac{1}{2}|$ 을 만족시킬때

$$
\int_{0}^{1} f(x)\ dx=?
$$

$$
\frac{1}{8},\ \frac{1}{4},\ \frac{1}{2},\ 1,\ 2
$$

---

$$
GE=\int_{0}^{\frac{1}{2}}f(x)+f(1-x)\ dx
$$

$$
=\int_{0}^{\frac{1}{2}}|x-\frac{1}{2}|\ dx
$$

$$
=\int_{0}^{\frac{1}{2}}-x+\frac{1}{2}\ dx
$$

$$
=\left[ -\frac{1}{2}x^{2}+\frac{1}{2}x \right]_{0}^{\frac{1}{2}}
$$

$$
=\frac{1}{2}\left( -\frac{1}{4}+\frac{1}{2}-0-0 \right)
$$

$$
=\frac{1}{2} \cdot \frac{1}{4}=\frac{1}{8}
$$

### Thm50 역함수와 정적분

함수 f(x)의 역함수를 g(x)라 할때
$$
\int_{a}^{b}f(x)\ dx + \int_{f(a)}^{f(b)}g(x)\ dx = S_{1}+S_{2}
$$
$$
=b f(b)-af(a)
$$


#### 기하학적 해석
![thm50|400](./images/04-integral/thm50.md)

그래프 y=f(x)는 x,y축을 바꾼 g(x)와 동일하기 떄문에
너무 당연한 공식이다.

####  대수적 접근 
이를 부분적분을 활용하여 증명해보자 (강의증명)

$$
\int_{f(a)}^{f(b)}g(x)\ dx = \{b f(b)-a f(a)\}-\int_{a}^{b}f(x)\ dx
$$

를 증명해보자 

$$
\int_{f(a)}^{f(b)} g(x)\ dx 를
$$

함수 f 에 관한 식으로 바꾸어보자 

$$
g(x)=y \implies f(y)=x
$$
$$
f'(y)=\frac{dx}{dy}
$$
$$
f'(y)dy=dx
$$
$$
f(a) \implies f(a)=a
$$
$$
f(b) \implies f(b)=b
$$

$g(x) \implies y$
$dx\implies f'(y)dy$
$f(a) \implies a$
$f(b) \implies b$
로 바꿀수있다

$$
\int_{f(a)}^{f(b)}g(x)\ dx
=\int_{a}^{b} y \cdot f'(y)dy
$$
$$
=[yf(y)]_{a}^{b}-\int_{a}^{b}1 \cdot f(y)dy
$$
$\int f(y)dy \implies \int f(x)\ dx$
$$
=\{b\cdot f(b)-a f(a)\}-\int_{a}^{b}f(x)\ dx
$$
임을 알 수 있다


### 예제342
함수 $f(x)=xe^{x},\ (0\leq x \leq 1)$ 의 역함수 g(x)에 대하여 
$$
\int_{0}^{e}g(x)\ dx=?
$$
---

$$
=e \cdot 1 - \int_{0}^{1}f(x)\ dx
$$
$$
=e-\int_{0}^{1}xe^{x}\ dx
$$
$$
=e-[xe^{x}-1\cdot e^{x}]_{0}^{1}
$$
$$
=e-(e-e-0+1)
$$
$$
=e-1
$$


### 예제343
함수 f(x)에 대하여 $f(0)=\frac{1}{5},\ f(1)=1$일때 
$$
\int_{0}^{1}f(x)\ dx + \int_{\frac{1}{5}}^{1}f^{-1}(x)\ dx=?
$$
---

$$
b f(b)-af(a)=1f(1)-0\cdot f(0)=1
$$


### 예제344 
$$
\int_{0}^{1}e^{x}\ dx + \int_{1}^{e}\ln x \ dx=?
$$
---

$$
b f(b)- a f(a)=1 \cdot e - 0 \cdot 1= e
$$


### 예제345
함수 $f(x)=e^{x}+e^{2x}$ 와 그 역함수 g(x)에 대하여 
$$
\int_{0}^{\ln 2}f(x)\ dx + \int_{2}^{6}g(x)\ dx=?
$$
---

$$
b f(b)-af(a)= \ln 2 \cdot 6 - 0 \cdot 2 = 6\ln 2
$$


### 예제346
함수 $f(x)=\tan x\left( -\frac{\pi}{2}< x < \frac{\pi}{2} \right)$의 역함수를 g(x)라고 할때 
$$
\int_{0}^{1}g(x)\ dx = ?
$$
---

$$
GE = b f(b)- a f(a) - \int_{a}^{b} f(x)\ dx
$$
$$
=\frac{\pi}{4} \cdot 1 - 0 \cdot 0 - \int_{0}^{\frac{\pi}{4}}f(x)\ dx
$$
$$
\frac{\pi}{4}-\int_{0}^{\frac{\pi}{4}}\tan x\ dx
$$
$$
=\frac{\pi}{4}-\left( -[\ln \cos x]_{0}^{\frac{\pi}{4}} \right)
$$
$$
= \frac{\pi}{4} + \ln \frac{1}{\sqrt{ 2 }}-\ln 1
$$
$$
=\frac{\pi}{4} - \ln \sqrt{ 2 }
$$

