---
id: 53-derivative-integral-1-note
aliases: []
tags: []
---

### Thm51 정적분의 정리(미분과 정적분)
(1)
$$
\frac{d}{dx} \int_{a}^{x}f(t)\ dt
$$

유도과정
$$
\int_{a}^{x}f(t)\ dt = [F(t)]_{a}^{x}=F(x)-F(a)
$$
$$
\frac{d}{dx}(F(x)-F(a))= f(x)
$$

(2)
$$
\frac{d}{dx} \int_{x}^{x+a}f(t)\ dt
$$

유도과정
$$
\int_{x}^{x+a}f(t)\ dt=[F(t)]_{x}^{x+a}=F(x+a)-F(x)
$$
$$
\frac{d}{dx}(F(x+a)-F(a))=f(x+a)-f(x)
$$

(3)
$$
\frac{d}{dx} \int_{h(x)}^{g(x)} f(t)\ dt
$$

유도과정
$$
\int_{h(x)}^{g(x)}f(t)\ dt=[F(t)]_{h(x)}^{g(x)}
$$
$$
=F(g(x))-F(h(x))
$$

$$
\frac{d}{dx}(F(g(x))-F(h(x)))
$$
$$
=g'(x)\cdot F'(g(x))- h'(x) \cdot F'(h(x))
$$


### 예제347
아래 세가지 식을 각각 증명하여라 
(1) 
$$
\frac{d}{dx}\int_{a}^{x}xf(t)\ dt
=\int_{a}^{x}f(t)\ dt+xf(x)
$$
(2)
$$
\frac{d}{dx} \int_{a}^{x}(x-t)f(t)\ dt
=\int_{a}^{x}f(t)\ dt
$$
(3)
$$
\frac{d}{dx}\int_{ax+b}^{cx+d} f(t)\ dt
=cf(cx+d)-af(ax+b)
$$
---

(1) 
$$
\frac{d}{dx}\int_{a}^{x}xf(t)\ dt 
=\frac{d}{dx} x\cdot \int_{a}^{x}f(t)\ dt
$$
$$
=xf(x)+1 \cdot \int_{a}^{x}f(t)\ dt
$$

(2)
$$
\frac{d}{dx}\int_{a}^{x}(x-t)f(t)\ dt
=\frac{d}{dx}\left\{ x \int_{a}^{x}f(t)\ dt - \int_{a}^{x}t f(t)\ dt \right\}
$$
$$
=1 \cdot \int_{a}^{x}f(t)\ dt + xf(x) - xf(x)
$$
$$
=\int_{a}^{x} f(t)\ dt
$$

(3)
$$
\frac{d}{dx}\int_{ax+b}^{cx+d}f(t)\ dt
=\frac{d}{dx}(F(cx+d)-F(ax+b))
$$
$$
=cf'(cx+d)-af'(ax+b)
$$

### 예제348
다항함수 f(x)가 $\int_{2}^{x}f(t)\ dt=x^{2}+ax+2$를 만족시킬때 f(10)의 값을 구하여라

---

양변미분하면
$$
f(x)=2x+a
$$

적분구간의 양끝이 동일하면 적분값은 0이 되므로 준식에 2를 대입하면
$$
\int_{2}^{2}f(t)\ dt = 2^{2}+2a+2 = 0
$$
$$
\therefore a= -3
$$

$$
f(x)=2x-3
$$
$$
f(10)=20-3=17
$$

### 예제349
다항함수 f(x)가 모든 실수 x에 대하여 
$$
\int_{1}^{x}f(t)\ dt = x^{3}-2ax^{2}+ax
$$
를 만족시킬때 f(3)의 값을 구하여라

---

$$
f(x)=3x^{2}-4ax+a
$$

$$
\int_{1}^{1}f(t)\ dt=1-2a+a=0
$$
$$
a=1
$$

$$
f(x)=3x^{2}-4x+1
$$
$$
f(3)=27-12+1=16
$$

### 예제350 
모든 실수 x에 대하여 미분가능한 함수 f(x)에 대해
$$
f(x)=x^{2} \cos x+\int_{\pi}^{x}t f(t)\ dt,\ \  f'(\pi)=?
$$
---

$$
f'(x)=x^{2}(-\sin x)+2x \cos x+xf(x)
$$
$$
f'(\pi)=\pi^{2} \cdot (-0) + 2\pi \cdot (-1) + \pi f(\pi)
$$
$$
=-2\pi+ \pi f(\pi)
$$
$$
=-2\pi + \pi(-\pi^{2}+0)
$$
$$
=-\pi^{3}-2\pi
$$

### 예제351
두 함수 $f(x)=ax+b$ 와 $g(x)=e^{x}$  가 
$$
f(g(x))=\int_{0}^{x}f(t)g(t)\ dt - xe^{x} + 3
$$
을 만족할때 f(2)의 값은 ?
(1) 4 
(2) 2 
(3) 0 
(4) -2 
(5) -4

---

$$
g'(x)f'(g(x))=f(x)g(x)-(xe^{x}+e^{x})
$$
$$
e^{x}a=e^{x}(ax+b)-e^{x}(x+1)
$$
$$
a=ax+b-x-1
$$
$$
x(a-1)+b-1-a=0
$$
$$
a=1,\ b=2
$$

$$
f(x)=x+2
$$
$$
f(2)=4
$$


### 예제352
함수 f(x)는 연속함수이고 모든 실수 x에 대하여 다음 등식이 성립한다 
$$
GE:\ f(x)-2\int_{0}^{x}e^{t}f(t)\ dt = 1
$$
이때 f''(0)의 값은? (단 e는 자연로그의 밑이고 f''(x)는 f(x)의 이계도함수이다 )

---

$$
f'(x)-2(e^{x}f(x))=0 \tag{ex1}
$$
$$
f''(x)-2\{ e^{x}f(x)+e^{x}f'(x) \}=0
$$
$$
f''(x)=2(e^{x}f(x)+e^{x}f'(x))
$$
$$
f''(0)=2(e^{0}f(0)+e^{0}f'(0))
$$
$$
=2(f(0)+f'(0))
$$

f(0)와 f'(0)값 구하기 
GE에 x=0을 대입

$$
f(0)-2\int_{0}^{0}e^{t}f(t)\ dt = 1
$$
$$
f(0)-0=1
$$

ex1에 x=0대입
$$
f'(x)=2(e^{x}f(x))
$$
$$
f'(0)=2f(0)=2
$$

$$
\because f(0)=1,\ f'(0)=2
$$
$$
f''(0)=2(1+2)=6
$$

### 예제353
실수 전체의 집합에서 미분가능한 함수 f(x)가 
$$
f(x)=e^{x}-1+ \int_{0}^{x}f(t)\ dt
$$
를 만족할때 보기의 설명중 올은것을 모두 골라라? ( e 는 자연로그의 밑이다 )

(ㄱ) $f(0)=0$ 이다 
(ㄴ) $f'(0)=0$ 이다 
(ㄷ) 모든실수 x에 대하여 $f'(x)>f(x)$ 이다 

---

$$
f(0)=e^{0}-1+0 =1-1=0
$$

(ㄱ)은 참이다 

$$
f'(x)=e^{x}+f(x)
$$
$$
f'(0)=e^{0}+f(0)=1+0=1
$$
(ㄴ) 은 거짓


$$
f'(x)=e^{x}+f(x)
$$
이고 $e^{x}>0$ 임으로 
(ㄷ)은 참이다

(ㄱ), (ㄷ)


### 예제354
$$
F(x)=\int_{0}^{x}(x-t) \cos t \ dt
$$
일떄 F(x)의 도함수를 구하여라

---

$$
F(x)=x\int_{0}^{x} \cos t\ dt - \int_{0}^{x} t\cos t\ dt
$$
$$
F'(x)= 1 \cdot \int_{0}^{x} \cos t\ dt + x\cdot \cos x - x\cos x
$$
$$
=\int_{0}^{x}\cos t\ dt
$$
$$
=[\sin t]_{0}^{x}=\sin x-0
$$

$$
F'(x)=\sin x
$$


### 예제 355
함수 $f(x)=x^{3}-x$가 
$$
\frac{d}{dx}\int_{a}^{x}f(t)\ dt = \int_{a}^{x} \frac{d}{dt}f(t)\ dt
$$
를 만족할떄 실수 a의 갯수를 구하여라

---

$$
given: f(x)=[f(t)]_{a}^{x}
$$
$$
f(x)=f(x)-f(a)
$$
$$
f(a)=a^{3}-a=0
$$
$$
\because a(a^{2}-1)=0
$$
$$
a=0,\ a=\pm 1
$$
3개이다


### 예제356
$$
\lim_{ x \to 0 } \int_{0}^{x} \frac{e^{t} \cos t}{x} \ dt=?
$$
---

$$
GE= \lim_{ x \to 0 } \frac{\int_{0}^{x}e^{t}\cos t\ dt}{x}
$$
$$
=\lim_{ x \to 0 } \frac{e^{x}\cos x}{1}
= 1\cdot1=1
$$

### 예제357
실수 전체에서 정의된 함수 
$$
F(x)=\int_{0}^{x}(1-t)e^{t}\ dt
$$
의 최댓값은?

---

$$
F'(x)=(1-x)e^{x}
$$
$$
F'(1)=0
$$
으로 F(x)는 x=1 에서 극점을 갖는다

$$
F''(x)=(1-x) e^{x}+(-1)e^{x}
$$
$$
=e^{x}- x e^{x}-e^{x}
=-xe^{x}
$$

F''(1)은 -e로 결과가 음 이므로 x=1에서 하나의 극댓값을 가진다.

$$
\therefore F(x)_{max}=F(1)=\int_{0}^{1}(1-t)e^{t}\ dt
$$
$$
=[(1-t)e^{t}-(-1 \cdot e^{t})]_{0}^{1}
$$
$$
=0+e-(1+1)
$$
$$
=e-2
$$

