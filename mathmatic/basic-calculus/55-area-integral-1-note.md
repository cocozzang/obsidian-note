---
id: 55-area-integral-1-note
aliases: []
tags: []
---

### 예제370

$$
f(x)=e^{x}+\int_{0}^{2}f(t)\ dt,\ f(1)=?
$$

---

$$
f(x)=e^{x}+k
$$

$$
k=\int_{0}^{2}e^{t}+k\ dt
=[e^{t}+kt]_{0}^{2}
$$

$$
=e^{2}+2k-e^{0}
$$

$$
k=e^{2}+2k-1
$$

$$
-k=e^{2}-1
$$

$$
k=1-e^{2}
$$

$$
f(1)=e^{1}+1-e^{2}
$$

### 예제371

$$
f(x)=\cos 2x+4x+\int_{0}^{\pi}f(t)\ dt,\ f(\pi)=?
$$

---

$$
f(x)=\cos 2x + 4x+k
$$

$$
k=\int_{0}^{\pi} \cos 2t+4t+k\ dt
=\left[ \frac{1}{2}\sin 2t+2t^{2}+kt \right]_{0}^{\pi}
$$

$$
=0+2\pi^{2}+k\pi-0-0-0
$$

$$
k=2\pi^{2}+k\pi
$$

$$
k(1-\pi)=2\pi^{2}
$$

$$
k=\frac{2\pi^{2}}{1-\pi}
$$

$$
f(\pi)=\cos 2\pi+4\pi+\frac{2\pi^{2}}{1-\pi}
$$

$$
=4\pi+\frac{2\pi^{2}}{1-\pi}+1
$$

### 예제372

$$
f(x)=\frac{12}{7}x^{2}-2x \int_{1}^{2}f(t)\ dt + \left( \int_{1}^{2}f(t)\ dt \right)^{2}
$$

일떄

$$
10 \cdot \int_{1}^{2}f(x)\ dx=?
$$

---

$$
\text{put}\ k=\int_{1}^{2}f(t)\ dt
$$

$$
f(x)=\frac{12}{7}x^{2}-2xk+k^{2}
$$

$$
k=\int_{1}^{2} \frac{12}{7}t^{2}-2tk+k^{2}\ dt
$$

$$
=\left[ \frac{4}{7}t^{3}-kt^{2}+k^{2}t \right]_{1}^{2}
$$

$$
k=\frac{4}{7}\cdot 8 -4k+2k^{2}-\frac{4}{7}+k-k^{2}
$$

$$
=4-3k+k^{2}
$$

$$
k^{2}-4k+4=0
$$

$$
(k-2)^{2}=0
$$

$$
k=2
$$

$$
10 \int_{1}^{2}f(x)\ dx = 10k=20
$$

### 예제 373

함수 $f(x)$가 $f(x)= x^{5}+x^{4}+x^{3}+x^{2}+x+\displaystyle\int_{-1}^{1} f(t) \, dt$ 를 만족할 때, $f(0)$의 값은?

① $-\dfrac{4}{5}$ ② $-\dfrac{5}{7}$ ③ $-\dfrac{16}{15}$ ④ $\dfrac{7}{9}$ ⑤ $\dfrac{15}{23}$

---

$$
\text{put}\ k= \int_{-1}^{1}f(t)\ dt
$$

$$
f(x)=x^{5}+x^{4}+x^{3}+x^{2}+x+k
$$

$$
k=\int_{-1}^{1}t^{5}+t^{4}+t^{3}+t^{2}+t+k\ dt
$$

$$
=2\int_{0}^{1} t^{4}+t^{2}+k\ dt
$$

$$
=2\left[ \frac{1}{5}t^{5}+\frac{1}{3}t^{3}+kt \right]_{0}^{1}
$$

$$
=2\left( \frac{1}{5}+\frac{1}{3}+k \right)=\frac{2}{5}+\frac{2}{3}+2k
$$

$$
k=-\frac{16}{15}
$$

$$
f(0)=-\frac{16}{15}
$$

### 예제 374

함수 $f(x)$, $g(x)$가 $f(x)= 3x^{2}\displaystyle\int_{0}^{1} g(x) \, dx$, $g(x)= 1+2\displaystyle\int_{0}^{x} f(t) \, dt$ 를 만족할 때,

$f(1)+g(1)$의 값은?

① $11$ ② $13$ ③ $15$ ④ $17$ ⑤ $19$

---

$$
\text{put}\ k= \ \int_{0}^{1}g(x)\ dx
$$

$$
f(x)=3kx^{2}
$$

$$
g'(x)=6kx^{2}
$$

$$
g(x)=2kx^{3}+C
$$

$$
g(0)=1=C
$$

$$
g(x)=2kx^{3}+1
$$

$$
k=\int_{0}^{1}2kx^{3}+1\ dx
$$

$$
=\left[ \frac{1}{2}kx^{4}+x \right]_{0}^{1}
=\frac{k}{2}+1
$$

$$
\frac{k}{2}=1
$$

$$
k=2
$$

$$
f(x)=6x^{2}
$$

$$
g(x)=4x^{3}+1
$$

$$
f(1)+g(1)=6+4+1=11
$$

### 예제375

다음 식을 만족시키는 함수 f(x)를 구하여라

$$
f(x)=x+\int_{0}^{\pi}f(t) \sin t\ dt
$$

---

$$
\text{put }k= \int_{0}^{\pi}f(t) \sin t\ dt
$$

$$
f(x)=x+k
$$

$$
k=\int_{0}^{\pi}(t+k)\sin t\ dt
$$

$$
=[(t+k)(-\cos t)-(1 \cdot -\sin t)]_{0}^{\pi}
$$

$$
=[-(t+k)(\cos t)+\sin t]_{0}^{\pi}
$$

$$
=(\pi+k)+0+(0+k)-0
$$

$$
k=\pi+2k
$$

$$
k=-\pi
$$

$$
f(x)=x-\pi
$$

### 예제 376

함수 $f(x)$에 대하여 $f(x)= x - \displaystyle\int_{1}^{e} \dfrac{f(t)}{t} \, dt$ 가 성립할 때, $f(e)$의 값은?

(단, $e$는 자연로그의 밑이다.)

① $-\dfrac{e+1}{2}$ ② $\dfrac{e-1}{2}$ ③ $\dfrac{e+1}{2}$ ④ $e-1$ ⑤ $e-2$

---

$$
f(x)=x-k
$$

$$
k= \int_{1}^{e} \frac{t-k}{t}\ dt
=\int_{1}^{e} 1- \frac{k}{t}\ dt
$$

$$
=[t-k\ln|t|]_{1}^{e}
$$

$$
=e-k-1+k\ln 1
$$

$$
k=e-k-1
$$

$$
2k=e-1
$$

$$
k=\frac{e-1}{2}
$$

$$
f(x)=x-\frac{e-1}{2}
$$

$$
f(e)=\frac{e+1}{2}
$$

