---
id: 45-integration-by-parts-note
aliases: []
tags: []
---

### Thm46 부분적분

$$
\int f'(x)g(x)\ dx = f(x)g(x)-\int f(x)\cdot g'(x)\ dx
$$

곱의 미분인 아래식에서

$$
(f(x)\cdot g(x))'=f'(x)g(x)+f(x)g'(x)
$$

$$
f'(x)g(x)=(f(x)g(x))'-f(x)g'(x)
$$

으로 정리하여 양변을 적분하면

$$
\int f'(x)g(x)\ dx=f(x)g(x)-\int f(x)g'(x)\ dx
$$

thm46의 공식이 유도된다

적 그 (적분 그대로), 적 미 (적분 미분)

#### 적분우선순위 지수 > 삼각 > 다항 > 로그

ex)

$$
\int \ln x \cdot x \ dx
$$

를 적분할떄는 위 우선순위에 따라 다항함수 부분인 x를 적분하는 방향으로 부분적분을 진행한다

$$
=\frac{1}{2}x^{2}\cdot \ln x - \int \frac{1}{2}x^{2} \cdot \frac{1}{x} \ dx
$$

$$
=\frac{1}{2}x^{2} \cdot \ln x - \int \frac{1}{2}x\ dx
$$

$$
=\frac{1}{2}x^{2} \cdot \ln x - \frac{1}{4}x^{2}+C
$$

#### 유형1 다항함수 x 지수함수

(1)

$$
\int xe^{2x}\ dx
$$

$$
=x\cdot \frac{1}{2}e^{2x}-\int 1 \cdot \frac{1}{2}e^{2x}\ dx
$$

$$
=\frac{1}{2}xe^{2x}-\frac{1}{4}e^{2x}+C
$$

(2)

$$
\int x^{2}e^{3x}\ dx
$$

$$
=x^{2}\cdot \frac{1}{3}e^{3x}-\int 2x \cdot \frac{1}{3}e^{3x}\ dx
$$

$$
=\frac{1}{3}x^{2}e^{3x}-\left\{  2x\cdot \frac{1}{9}e^{3x}-\int 2 \cdot \frac{1}{9}e^{3x}\ dx \right\}
$$

$$
=\frac{1}{3}x^{2}e^{3x}-\frac{2}{9}xe^{3x}+\frac{2}{27}e^{3x}+C
$$

#### 유형2 다항함수 x 삼각함수

(1)

$$
\int x\sin 3x\ dx
$$

$$
=x\cdot \frac{-1}{3}\cos 3x- \int 1 \cdot -\frac{1}{3}\cos 3x\ dx
$$

$$
=-\frac{1}{3}x\cos 3x + \frac{1}{9} \sin 3x + C
$$

(2)

$$
\int x^{3} \cos x\ dx
$$

이런문제처럼 다항함수차수가 3차식인 경우 부분적분을 3번적용해야하기 떄문에
유형1, 유형2에 한해서 아래 방법을 사용할수있다.
그.적-미.적+미적-미.적+...

$$
=x^{3}\sin x-3x^{2}\cdot(-\cos x)+6x\cdot(-\sin x)-6\cos x+C
$$

$$
=x^{3}\sin x+3x^{2}\cos x-6x\sin x-6\cos x+C
$$

#### 유형3 다항함수 x 로그함수

(1)

$$
\int \ln x\ dx
$$

---

$$
\int \ln x\ dx=x\ln x-\int x\cdot \frac{1}{x}\ dx
$$

$$
=x\ln x-x+C
$$

(2)

$$
\int x\ln x\ dx
$$

---

$$
\int x\ln x\ dx
= \frac{1}{2}x^{2}\ln x-\int \frac{1}{2}x^{2}\cdot \frac{1}{x}\ dx
$$

$$
=\frac{1}{2}x^{2}\ln x-\frac{1}{4}x^{2}+C
$$

(3)

$$
\int(\ln x)^{2}\ dx
$$

---

$$
\int(\ln x)^{2}\ dx
=x(\ln x)^{2}-\int x \cdot 2\ln x \cdot \frac{1}{x}\ dx
$$

$$
=x(\ln x)^{2}-2(x\ln x-x)+C
$$

#### 유형4 지수함수 x 삼각함수

$$
\int e^{x}\cos x\ dx
$$

---

$$
\int e^{x}\cos x\ dx=e^{x}(\cos x)-\int(e^{x}(-\sin x))\ dx
$$

$$
=e^{x}\cos x+\int e^{x} \sin x\ dx
$$

$$
=e^{x}\cos x+e^{x}\sin x-\int e^{x}\cos x\ dx
$$

$$
\int e^{x}\cos x\ dx = e^{x}\cos x+e^{x}\sin x-\int e^{x}\cos x\ dx
$$

$$
2\int e^{x}\cos x\ dx= e^{x}\cos x+e^{x}\sin x
$$

$$
\int e^{x}\cos x\ dx = \frac{1}{2}e^{x}(\cos x+\sin x)+C
$$

### 예제294

곡선 $y=f(x)$위의 점 (x,y)에서의 접선의 기울기가 $x\ln x$이고
$f(1)=\frac{3}{4}$일때 f(4)를 구하여라

---

$$
f(x)=\int x\ln x\ dx
$$

$$
=\frac{1}{2}x^{2}\ln x-\int \frac{1}{2}x^{2}\cdot \frac{1}{x}\ dx
$$

$$
=\frac{1}{2}x^{2}\ln x-\frac{1}{4}x^{2}+C
$$

$$
f(1)=\frac{1}{2}\cdot 1 \ln 1 - \frac{1}{4} \cdot 1 + C = \frac{3}{4}
$$

$$
=\frac{1}{2} \cdot 0 -\frac{1}{4}+C
=-\frac{1}{4}+C = \frac{3}{4}
$$

$$
C= 1
$$

$$
f(x)=\frac{1}{2}x^{2} \ln x - \frac{1}{4}x^{2} + 1
$$

$$
f(4)=\frac{1}{2}\cdot 16 \cdot \ln 4 - \frac{1}{4} \cdot 16 + 1
$$

$$
=8\ln 4 - 4+1
$$

$$
=8\ln 4-3
$$

$$
=16\ln 2 - 3
$$

### 예제295

$$
f'(x)=\cos x\ln(\sin x), f\left( \frac{\pi}{2} \right)=0
$$

일때 $f\left( \frac{\pi}{6} \right)$을 구하여라

---

$$
f(x)=\int \cos x \ln(\sin x)\ dx
$$

$$
\text{put}\ \sin x=t \implies
\cos x\ dx=dt
$$

$$
f(x)=\int \ln t\ dt
$$

$$
=t\ln t-t+C
$$

$$
=\sin x \ln (\sin x)-\sin x+C
$$

$$
f\left( \frac{\pi}{2} \right)
=\sin \frac{\pi}{2}\ln\left( \sin \frac{\pi}{2} \right)-\sin \frac{\pi}{2}+C=0
$$

$$
=\ln 1-1+C=0
$$

$$
C=1
$$

$$
f(x)=\sin x\ln(\sin x)-\sin x+1
$$

$$
f\left( \frac{\pi}{6} \right)
=\sin \frac{\pi}{6}\ln\left( \sin \frac{\pi}{6} \right)-\sin \frac{\pi}{6}+1
$$

$$
=\frac{1}{2}\cdot \ln\left( \frac{1}{2} \right)-\frac{1}{2}+1
$$

$$
=-\frac{1}{2}\ln 2+\frac{1}{2}
$$

$$
= \frac{1}{2}(1-\ln 2)
=\frac{1}{2}(\ln e-\ln 2)
=\frac{1}{2}\ln \frac{e}{2}
$$

### 예제296

$f'(x)=e^{x}\sin x$이고 $f(0)=\frac{1}{2}$일때 $f(\pi)$를 구하여라

---

$$
f(x)=\int e^{x}\sin x\ dx
$$

$$
=e^{x}\sin x-\int e^{x}\cos x\ dx
$$

$$
=e^{x}\sin x-\left\{ e^{x}\cos x-\int e^{x}(-\sin x)\ dx \right\}
$$

$$
=e^{x}\sin x-e^{x}\cos x-\int e^{x}\sin x\ dx
$$

$$
2f(x)=2\int e^{x} \sin x\ dx
= e^{x}\sin x-e^{x}\cos x
$$

$$
f(x)=\frac{1}{2}(e^{x}\sin x-e^{x}\cos x)+C
$$

$$
f(0)=\frac{1}{2}(1\cdot 0 - 1 \cdot 1)+C
= \frac{1}{2}\cdot -1 +C=\frac{1}{2}
$$

$$
C=1
$$

$$
f(x)=\frac{1}{2}(e^{x}\sin x-e^{x}\cos x)+1
$$

$$
f(\pi)= \frac{1}{2}(e^{\pi}\cdot 0 - e^{\pi} \cdot -1)+1
$$

$$
=\frac{1}{2}e^{\pi}+1
$$

### 예제297

$$
f(x)=\int(x-2)e^{x}\ dx,\ f(0)=3,\ f(x)=?
$$

---

$$
\int(x-2)e^{x}\ dx = (x-2)e^{x}-\int 1 \cdot e^{x}\ dx
$$

$$
=e^{x}(x-2-1)+C
=e^{x}(x-3)+C
$$

$$
f(0)=e^{0}\cdot -3+C
=-3+C=3
$$

$$
C=6
$$

$$
f(x)=e^{x}(x-3)+6
$$

### 예제298

$$
f(x)=\int x^{2}\cos 2x\ dx,\ f(\pi)=\frac{\pi}{2},\ f(x)=?
$$

---

$$
f(x)=x^{2}\left( \frac{1}{2}\sin 2x \right)-2x\cdot\left( -\frac{1}{4} \cos 2x \right)+2\left( -\frac{1}{8}\sin 2x \right)+C
$$

$$
=\frac{1}{2}x^{2}\sin 2x+\frac{1}{2}x\cos 2x-\frac{1}{4}\sin 2x +C
$$

$$
f(\pi)=\frac{1}{2}\pi^{2}\sin 2\pi+\frac{1}{2}\pi \cos 2\pi-\frac{1}{4}\sin 2\pi+C
$$

$$
=\frac{1}{2}\pi^{2}\cdot 0 +\frac{1}{2}\pi \cdot 1 -\frac{1}{4}\cdot 0 +C
$$

$$
=\frac{1}{2}\pi+C= \frac{\pi}{2}
$$

$$
C=0
$$

$$
f(x)
=\frac{1}{2}x^{2}\sin 2x+\frac{1}{2}x\cos 2x-\frac{1}{4}\sin 2x
$$

### 예제299

$$
f(x)=e^{2x-1},\ \int f^{-1}(x)\ dx=?
$$

---

$$
x=e^{2y-1}
$$

$$
\ln x=2y-1
$$

$$
2y=\ln x+1
$$

$$
y=\frac{1}{2}\ln x+\frac{1}{2}=f^{-1}(x)
$$

$$
\int f^{-1}(x)\ dx
=\int \frac{1}{2}\ln x+\frac{1}{2}\ dx
=\frac{1}{2}\int \ln x+1\ dx
$$

$$
=\frac{1}{2}\left( x\ln x-x+x \right)+C
$$

$$
=\frac{1}{2}x\ln x+C
$$
