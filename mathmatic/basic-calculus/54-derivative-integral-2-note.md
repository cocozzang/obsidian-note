---
id: 54-derivative-integral-2-note
aliases: []
tags: []
---

### 예제358
연속함수 $f(x)$ 가 $\int_{0}^{x^{2}}f(t)\ dt = \sin ^{2} \frac{\pi}{2}x$ 를 만족시킬때 $f\left( \frac{1}{4} \right)$ 의 값은 ?

(1) $\frac{\pi}{4}$  (2) $\frac{\pi}{2}$ (3) $\pi$ (4) $2\pi$ (5) $4\pi$

---

$$
2x \cdot f(x^{2})=2\sin \frac{\pi}{2}x \cdot \frac{\pi}{2}\cos \frac{\pi}{2}x
$$

$x=\frac{1}{2}$ 대입

$$
1 \cdot f\left( \frac{1}{4} \right)= 2 \cdot \frac{1}{\sqrt{ 2 }} \cdot \frac{\pi}{2} \cdot \frac{1}{\sqrt{ 2 }}
$$
$$
=\frac{\pi}{2}
$$

### 예제 359
$$
GE: \int_{-1}^{x}f(t)\ dt= xf(x)-x^{3}e^{x}
$$
일때 f(1)의 값을 구하여라 ( 단 $x\neq 0$  )

---

$$
f(x)=1 \cdot f(x)+xf'(x)-(x^{3}e^{x}+3x^{2}e^{x})
$$

$$
f(x)=f(x)+xf'(x)-e^{x}(x^{3}+3x^{2})
$$
$$
xf'(x)=e^{x}(x^{3}+3x^{2})
$$
$$
f'(x)=e^{x}(x^{2}+3x)
$$

$$
f(x)=\int e^{x}(x^{2}+3x)\ dx
$$
$$
=e^{x}(x^{2}+3x)-e^{x}(2x+3)+2e^{x}+C
$$


GE에 x=-1 을 대입하면

$$
\int_{-1}^{-1}f(t)\ dt = -f(-1)+1e^{-1}
$$
$$
0=-f(-1)+e^{-1}
$$
$$
f(-1)=e^{-1}
$$
$$
e^{-1}(1-3)-e^{-1}(-2+3)+2e^{-1}+C=e^{-1}
$$
$$
-2e^{-1}-e^{-1}+2e^{x}+C=e^{-1}
$$
$$
C=2e^{-1}
$$

$$
f(x)=e^{x}(x^{2}+3x)-e^{x}(2x+3)+2e^{x}+2e^{-1}
$$
$$
f(1)=e(1+3)-e(2+3)+2e+2e^{-1}
$$
$$
=4e-5e+2e+2e^{-1}
$$
$$
=e+2e^{-1}
$$


### 예제 360

모든 실수 $x$에 대하여 함수 $f(x)$가 $f(x)= \int_{0}^{x}(x-t)\cos 2t \, dt$ 로 정의될 때,

$f(x)$의 최댓값을 구하면?

① $\dfrac{1}{2}$ ② $\dfrac{1}{3}$ ③ $\dfrac{1}{4}$ ④ $\dfrac{1}{5}$ ⑤ $1$

---

$$
given: f(0)=0
$$

$$
f(x)=x \int_{0}^{x}\cos 2t\ dt - \int_{0}^{x}t\cos 2t\ dt
$$
$$
f'(x)=x\cdot \cos 2x+ \int_{0}^{x}\cos 2t\ dt - x\cos 2x
=\int_{0}^{x}\cos 2t\ dt
$$
$$
=\left[ \frac{1}{2}\sin 2t \right]_{0}^{x}=\frac{1}{2} \sin 2x
$$

$$
f(x)=\int \frac{1}{2} \sin 2x \ dx
$$
$$
=-\frac{1}{4}\cos 2x +C
$$

$$
f(0)=-\frac{1}{4}+C=0
$$
$$
C=\frac{1}{4}
$$

$$
f(x)=-\frac{1}{4}\cos 2x +\frac{1}{4}
$$
$$
f(x)max=f\left( \frac{\pi}{2} \right)=-\frac{1}{4}\cdot (-1)+\frac{1}{4}
$$
$$
=\frac{1}{2}
$$


### 예제 361

두 함수 $f(x)= \tan x \left( -\dfrac{\pi}{2} \leq x \leq \dfrac{\pi}{2} \right)$, $g(x)= f^{-1}(x)$에 대하여 함수 $F(x)$를 다음과 같이 정의한다. $F(x)= \int_{0}^{g(x)} f(t) \, dt$ 이다. 이 때, $F'(1)$의 값은?

① $\dfrac{1}{2}$ ② $\dfrac{1}{\sqrt{2}}$ ③ $1$ ④ $\dfrac{\pi}{4}$ ⑤ $\dfrac{\pi}{2}$

---

$$
F'(x)=g'(x)f(g(x))=g'(x) \cdot x
$$
$$
F'(1)=g'(1)=\frac{1}{f'\left( \frac{\pi}{4} \right)}
$$
$$
=\frac{1}{\left( \tan \frac{\pi}{4} \right)'}=\frac{1}{\sec ^{2}\left( \frac{\pi}{4} \right)}
$$
$$
\cos ^{2}\left( \frac{\pi}{4} \right)
=\left( \frac{1}{\sqrt{ 2 }} \right)^{2}
=\frac{1}{2}
$$

tip: 역함수 미분관계
$$
g(x)=f^{-1}(x),\ f(a)=g(b)
$$
일떄
$$
f(g(x))=x
$$
$$
g'(x)f'(g(x))=1
$$
x=a 대입시
$$
g'(a)f'(g(a))=1
$$
$$
g'(a)f'(b)=1
$$
$$
g'(a)=\frac{1}{f'(b)}
$$


### 예제 362

함수 GE1: $f(x)= (ax+b)e^{x}$이 모든 실수 $x$에 대하여 GE2: $f(x)= 4e^{x}+2+\int_{0}^{x} f(t) \, dt$ 를 만족시킨다.
이 때, 두 상수 $a$, $b$에 대하여 $a^{2}+b^{2}$의 값을 구하시오.

---

GE1, GE2에 x=0 대입
$$
f(0)=4e^{0}+2+0=6
$$
$$
f(0)=(a\cdot 0 +b) e^{0}=b
$$
$b=6$

$$
GE_{1} = f(x)=(ax+6)e^{x}
$$

$$
f(x)=4e^{x}+2+\int_{0}^{x}f(t)\ dt
$$
$$
f'(x)=4e^{x}+f(x)
$$
$$
(ax+6)e^{x}+ae^{x}=4e^{x}+(ax+6)e^{x}
$$
$$
ax+6+a=4+ax+6
$$
$$
a=4
$$
$$
a^{2}+b^{2}=4^{2}+6^{2}=16+36=52
$$


### 예제363
상수 $a$, $b$에 대하여 이차함수 $f(x)= x^{2}+ax+b$는 다음 등식을 만족한다. $$f(x)-2\int_{0}^{x} e^{t+x} f(t) \, dt = 4$$ 이 때, $f(1)$의 값을 구하시오.

---

$$
given: f(0)-0=4
$$

$$
f(0)=0^{2}+a\cdot 0 +b = 4
$$
$$
b=4
$$

$$
f'(x)=2x+a
$$
$$
f(x)=2\int_{0}^{x}e^{x}\cdot e^{t} f(t) \ dt +4
=2e^{x}\int_{0}^{x}e^{t}f(t)\ dt+4
$$
$$
f'(x)=2e^{x}\cdot e^{x}f(x)+2e^{x}\cdot \int_{0}^{x}e^{t}f(t)\ dt
$$

f'(x)를 표현하는 두 식에 x=0 대입
$$
f'(0)=2 \cdot 0+a=a
$$
$$
f'(0)=2e^{0}e^{0}f(0)+2e^{0}\cdot 0=2f(0)
$$
$$
\because f(0)=4
$$
$$
f'(0)=2 \cdot 4=8=a
$$
$$
\therefore a=8,\ b=4
$$

$$
f(x)=x^{2}+8x+4
$$
$$
f(1)=1+8+4=13
$$


### Thm52 극한과 정적분 
두 식 모두 $\frac{0}{0}$ 꼴 이라서 로피탈정리를 활용하여 정리하면 
각 공식의 결과가 나옴을 알수있다.


### 예제 364

연속함수 $f(x)$에 대하여 $a$가 $0$이 아닌 실수일 때 $\displaystyle\lim_{x \to a} \dfrac{1}{x^{2}-a^{2}} \int_{a}^{x} f(t) \, dt$ 의 값을 구하여라.

---

$$
GE=\lim_{ x \to a } \frac{\int_{a}^{x}f(t)\ dt}{x^{2}-a^{2}}
$$
$$
\lim_{ x \to a } \frac{f(x)}{2x}=\frac{f(a)}{2a}
$$

### 예제 365

미분 가능한 함수 $f(x)$에 대하여 $f(2)= 4$, $f'(2)= 2$일 때

$\displaystyle\lim_{x \to 2} \dfrac{1}{x-2} \int_{2}^{x} \{f(t)\}^{2} f'(t) \, dt$ 의 값은?

① $1$ ② $8$ ③ $16$ ④ $32$ ⑤ $64$

---

$$
GE=\lim_{ x \to 2 } \frac{\int_{2}^{x}\{ f(t) \}^{2}f'(t)\ dt}{x-2}
$$
$$
=\lim_{ x \to 2 } \frac{f(x)^{2}f'(x)}{1}
$$
$$
=f(2)^{2} f'(2)
=4^{2} \cdot 2 =32
$$


### 예제 366

$f'(1)= 1$, $f(1)= 2$일 때, $\displaystyle\lim_{x \to 1} \dfrac{1}{x-1} \int_{f(1)}^{f(x)} (t-1) \, dt$ 의 값은?

① $1$ ② $2$ ③ $3$ ④ $4$ ⑤ $5$

---

$$
GE=\lim_{ x \to 1 } \frac{\int_{f(1)}^{f(x)}(t-1)\ dt}{x-1}
$$
$$
=\lim_{ x \to 1 } f'(x)(f(x)-1)
$$
$$
=f'(1)(f(x)-1)=1\cdot(2-1)=1
$$

### 예제 367

함수 $f(x)= \displaystyle\int_{0}^{x} (\sin^{2}t - \cos t) \, dt$ 에 대하여 $\displaystyle\lim_{x \to 0} \dfrac{f(x)}{x}$ 의 값을 구하여라.

---

$$
GE=\lim_{ x \to 0 } \frac{\int_{0}^{x}(\sin ^{2}t-\cos t)\ dt}{x}
$$
$$
=\lim_{ x \to 0 } \sin ^{2}x-\cos x
$$
$$
=\sin ^{2} 0-\cos 0 =0 -1 = -1
$$

### 예제 368

극한값 $\displaystyle\lim_{x \to 1} \int_{1}^{x^{2}} \dfrac{(1+2\cos\pi t)^{3}}{x^{3}-1} \, dt$ 를 구하여라.

① $-\dfrac{3}{2}$ ② $-1$ ③ $-\dfrac{2}{3}$ ④ $-\dfrac{1}{2}$ ⑤ $-\dfrac{1}{3}$

---

$$
GE=\lim_{ x \to 1 } \frac{\int_{1}^{x^{2}}(1+2\cos \pi t)^{3}\ dt}{x^{3}-1}
$$
$$
=\lim_{ x \to 1 } \frac{2x(1+2\cos \pi x^{2})^{3}}{3x^{2}}
$$
$$
=\frac{2\cdot(1-2)^{3}}{3}
$$
$$
=-\frac{2}{3}
$$

### 예제 369

$\displaystyle\lim_{x \to \pi} \dfrac{1}{x-\pi} \int_{-1}^{\cos x} \sin^{2}\theta \cos^{3}\theta \, d\theta$ 의 값은?

① $-1$ ② $0$ ③ $1$ ④ $\pi$ ⑤ $2\pi$

---

$$
GE= \lim_{ x \to \pi } \frac{\int_{-1}^{\cos x} \sin ^{2}\theta \cos ^{3}\theta\ d\theta}{x-\pi}
$$
$$
=\lim_{ x \to \pi } \frac{-\sin x \sin ^{2}(\cos x) \cos ^{3}(\cos x)}{1}
$$
$$
=0
$$