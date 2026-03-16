---
id: 44-integration-substitution-1-note
aliases: []
tags: []
---

### 예제281

다음 부정적분을 구하여라

1 $$
    \int \sin ^{2} \frac{x}{2}\ dx
    $$

2 $$
    \int \cos 3x \sin x\ dx
    $$
3 $$
    \int \tan 2x\ dx
    $$

---

1 $$
    \int \sin ^{2} \frac{x}{2}\ dx
    = \int \frac{1-\cos x}{2}\ dx
    = \frac{1}{2}x - \frac{1}{2}\sin x+C
    $$

2
note:

$$
\cos\alpha \sin\beta= \frac{1}{2}(\sin(\alpha+\beta)-\sin(\alpha-\beta))
$$

$$
\int \cos 3x \cdot \
sin x\ dx
= \int \frac{1}{2}(\sin 4x - \sin 2x)\ dx
$$

$$
= \frac{1}{2} -\frac{1}{4}\cos 4x+ \frac{1}{2} \cos 2x +C
$$

3 $$
    \int \tan 2x\ dx
    = \int \frac{\sin 2x}{\cos 2x}\ dx
    = -\frac{1}{2}\int \frac{-2\sin 2x}{\cos 2x}\ dx
    $$

$$
=-\frac{1}{2}\ln |\cos 2x| +C
$$

### 예제 282

점(0,1)을 지나는 곡선 y=f(x) 위의 임의의 점 (x,y)에서의
접선의 기울기가 $2\cos x +e^{x}$ 일때 f(x)를 구하여라

---

$$
\int 2\cos x + e^{x}\ dx
= 2\sin x +e ^{x}+C
$$

$$
f(x)=2\sin x +e^{x}+C
$$

$$
\because f(0)=2\sin x +e^{x}+C = 0 + 1+C = 1
$$

$$
\therefore C=0
$$

$$
f(x)=2\sin x+e^{x}
$$

### 예제283

실수 전체의 집합에서 정의된 함수 f(x)에 대하여

$$
f'(x)=\frac{x}{x^{2}+1}, f(0)=3
$$

일때 $f(\sqrt{ e^{2}-1 })$ 의 값을 구하여라

---

$$
f(x)=
\int \frac{x}{x^{2}+1}\ dx
= \frac{1}{2}\int \frac{2x}{x^{2}+1}\ dx
=\frac{1}{2}\ln|x^{2}+1|+C
$$

$$
f(0)=0+C=3
$$

$$
C+3
$$

$$
f(x)=\frac{1}{2}\ln(x^{2}+1)+3
$$

$$
f(\sqrt{ e^{2}-1 })
=\frac{1}{2}\ln e^{2}+3
=4
$$

여기까지가 43강 내용

### Thm45 치환적분

#### 중요한 치환적분

1 $$
    \int \cos ^{3}x\ dx
    $$

---

$$
=\int \cos x \cos ^{2}x\ dx
=\int \cos x (1-\sin ^{2}x)\ dx
$$

$$
\text{put}\ \sin x = t \implies
\cos x \cdot dx = dt
$$

$$
\int \cos x(1-\sin^{2}x)\ dx
= \int 1-t^{2} \ dt
$$

$$
=t-\frac{1}{3}t^{3}+C
=-\frac{1}{3}\sin ^{3}x+\sin x+C
$$

2 $$
    \int \sin ^{5}x \ dx
    $$

---

$$
=\int \sin x \cdot \sin ^{4}x\ dx
=\int \sin x (1-\cos ^{2}x)^{2}\ dx
$$

$$
\text{put}\ \cos x=t \implies
\sin x \cdot dx = -dt
$$

$$
=\int (1-t^{2})^{2} \ (-dt)
=\int -(1-t^{2})^{2} \ dt
=\int -t^{4}+2t^{2}-1\ dt
$$

$$
= -\frac{1}{5}t^{5}+\frac{2}{3}t^{3}-t+C
$$

$$
=-\frac{1}{5}\cos ^{5}x+\frac{2}{3}\cos ^{3}x-\cos x+C
$$

3 $$
    \int xe^{x^{2}}\ dx
    $$

---

$$
\text{put}\ x^{2}=t \implies
2x\cdot dx = dt
$$

$$
= \frac{1}{2} \int 2xe^{x^{2}}\ dx
= \frac{1}{2}\int e^{t}\ dt
$$

$$
= \frac{1}{2}e^{t}+C
$$

$$
= \frac{1}{2}e^{x^{2}}+C
$$

4 $$
    \int \frac{\ln x}{x}\ dx
    $$
$$
    \text{put}\ \ln x=t \implies
    \frac{1}{x}dx = dt
    $$

$$
= \int t \ dt
$$

$$
= \frac{1}{2}t^{2}+C
$$

$$
=\frac{1}{2}(\ln x)^{2}+C
$$

### 예제284

함수 $f(x)=\int x e^{x^{2}}\ dx$에 대하여 $f(0)=0$일때 $f(2)$의 값을 구하여라

---

$$
\text{put}\ x^{2}=t \implies
2x \cdot dx = dt
$$

$$
f(x)=\int xe^{x^{2}}\ dx
=\frac{1}{2}\int  2x e^{x^{2}}\ dx
=\frac{1}{2}\int e^{t}\ dt
$$

$$
=\frac{1}{2} e^{x^{2}}+C
$$

$$
\because f(0)= \frac{1}{2}+C=0
$$

$$
C=-\frac{1}{2}
$$

$$
f(x)=\frac{1}{2}e^{x^{2}}-\frac{1}{2}
$$

$$
f(2)=\frac{1}{2}e^{4}-\frac{1}{2}
=\frac{1}{2}(e^{4}-1)
$$

### 예제285

함수

$$
f(x)=\int \frac{\cos(\ln x)}{x}\ dx
$$

에 대하여 $f(1)=1$일때 $f\left( e^{\frac{\pi}{2}} \right)$의 값을 구하여라

---

$$
\text{put}\ \ln x=t \implies
\frac{1}{x} dx=dt
$$

$$
f(x)=\int \cos t \ dt
$$

$$
=\sin t+C
=\sin(\ln x)+C
$$

$$
\because f(1)=\sin(\ln 1)+C=1
$$

$$
C=1
$$

$$
f(x)=\sin(\ln x)+1
$$

$$
f\left( e^{\frac{\pi}{2}} \right)
=\sin\left( \frac{\pi}{2} \right)+1
=2
$$

### 예제 286

$$
\int(1-\cos ^{3}x)\cos x \sin x \ dx
$$

를 구하여라

---

$$
\text{put}\ \cos x=t \implies
\sin x\ dx=-dt
$$

$$
GE=\int t-t^{4}\ (-dt)
=\int t^{4}-t\ dt
$$

$$
=\frac{1}{5}t^{5}-\frac{1}{2}t^{2}+C
$$

$$
=\frac{1}{5}\cos ^{5}x-\frac{1}{2}\cos ^{2}x+C
$$

### 예제287

$\int 2x e^{x^{2}}\ dx$를 구하여라

---

$$
\text{put}\ x^{2}=t \implies
2x \cdot dx = dt
$$

$$
GE=\int e^{t}\ dt
$$

$$
=e^{t}+C
=e^{x^{2}}+C
$$

### 예제288

$$
\int \frac{3(\ln x)^{2}}{x}\ dx
$$

를 구하여라

---

$$
\text{put}\ \ln x = t \implies
\frac{1}{x}\cdot dx = dt
$$

$$
GE=\int 3t^{2}\ dt
= t^{3}+C
$$

$$
=(\ln x)^{3}+C
$$

### 예제289

$$
\int (\sin ^{3}x+1)\cos x\ dx
$$

를 구하여라

---

$$
\text{put}\ \sin x=t \implies
\cos x \cdot dx = dt
$$

$$
GE= \int (t^{3}+1) dt
=\frac{1}{4}t^{4}+t+C
$$

$$
=\frac{1}{4}\sin^{4}x+\sin x+C
$$

### 예제290

$$
\int \frac{\sqrt{ ln x }}{x}\ dx
$$

를 구하여라

---

$$
 \text{put}\ \ln x=t \implies
 \frac{1}{x}\cdot dx = dt
$$

$$
GE=\int \sqrt{ t }\ dt
= \int t^{\frac{1}{2}}\ dt
$$

$$
=\frac{2}{3}t^{\frac{3}{2}}+C
$$

$$
=\frac{2}{3}(\ln x)^{\frac{3}{2}}+C
$$

$$
=\frac{2}{3}\cdot \ln x \cdot \sqrt{ \ln x }+C
$$

### 예제291

$$
f(x)=\int \frac{x}{\sqrt{ x+1 }}\ dx,\
f(0)=1
$$

일때 f(3)을 구하여라

---

$$
\text{put}\ \sqrt{ x+1 }=t \implies
x+1=t^{2} \implies
$$

$$
\frac{d}{dx}(x+1)=\frac{d}{dx}t^{2} \implies
$$

$$
1=\frac{dt^{2}}{dt} \cdot \frac{dt}{dx}
$$

$$
dx=2t \cdot dt
$$

$$
f(x)=\int \frac{x}{t}\cdot 2t \ dt
$$

$$
\because x+1=t^{2}
$$

$$
\therefore x=t^{2}-1
$$

$$
f(x)=\int \frac{t^{2}-1}{t}2t\ dt
=\int 2t^{2}-2\ dt
$$

$$
= \frac{2}{3}t^{3}-2t+C
$$

$$
=\frac{2}{3}(x+1)\sqrt{ x+1 }-2\sqrt{ x+1 }+C
$$

$$
f(0)=\frac{2}{3}\cdot 1 \cdot 1 -2 \cdot 1+C=1
$$

$$
\frac{2}{3}-2+C=1
$$

$$
C=3-\frac{2}{3}=\frac{7}{3}
$$

$$
f(x)=\frac{2}{3}(x+1)\sqrt{ x+1 }-2\sqrt{ x+1 }+\frac{7}{3}
$$

$$
f(3)=\frac{2}{3} \cdot 4 \cdot 2 -2 \cdot 2 + \frac{7}{3}
$$

$$
=\frac{16}{3}-4+\frac{7}{3}=\frac{23}{3}-\frac{12}{3}
$$

$$
=\frac{11}{3}
$$

### 예제292

$$
f'(x)=\frac{x-3}{(x-1)^{3}}\ ,\
f(0)=2
$$

일때 f(2)의 값을 구하여라

---

$$
f(x)=\int \frac{x-3}{(x-1)^{3}}\ dx
$$

$$
\text{put}\ x-1=t \implies
dx=dt
$$

$$
x=t+1
$$

$$
f(x)=\int \frac{t+1-3}{t^{3}}\ dt
$$

$$
=\int t^{-2}-2t^{-3}\ dt
$$

$$
=-t^{-1}+t^{-2}+C
$$

$$
=-(x-1)^{-1}+(x-1)^{-2}+C
$$

$$
=-\frac{1}{x-1}+\frac{1}{(x-1)^{2}}+C
$$

$$
f(0)=1+1+C=2
$$

$$
C=0
$$

$$
f(x)=-\frac{1}{x-1}+\frac{1}{(x-1)^{2}}
$$

$$
f(2)=-1+1=0
$$

### 예제 293

$f(x) = \int \frac{2}{1-e^{x}} dx$ 일 때, $f(2) - f(1)$의 값을 구하여라.

---

$$
\text{put}\ 1-e^{x}=t \implies
-e^{x}dx=dt
$$

$$
e^{x}=1-t
$$

$$
dx=-\frac{1}{e^{x}}dt
=\frac{1}{t-1}dt
$$

$$
f(x)=\int \frac{2}{t} \cdot \frac{1}{t-1}\ dt
=\int \frac{2}{t(t-1)}\ dt
$$

$$
=2\int \frac{1}{t-t-1} \left( \frac{1}{t}-\frac{1}{t-1} \right)\ dt
$$

$$
=2\int -1 \cdot \left( \frac{1}{t}-\frac{1}{t-1} \right)\ dt
$$

$$
=2 (\ln|t-1|-\ln |t|)+C
$$

$$
=2\ln| \frac{t-1}{t}| +C
$$

$$
=2\ln | \frac{1-e^{x}-1}{1-e^{x}}|+C
$$

$$
=2 \ln | \frac{-e^{x}}{1-e^{x}}| +C
$$

$$
=2\ln| \frac{e^{x}}{e^{x}-1}|+C
$$

$$
f(2)-f(1)
=2\ln| \frac{e^{2}}{e^{2}-1}|+C-2\ln | \frac{e}{e-1}| -C
$$

$$
=2 \cdot \ln\left( \frac{e^{2}}{e^{2}-1} \cdot \frac{e-1}{e} \right)
$$

$$
= 2 \ln \left( \frac{e^{2}}{(e-1)(e+1)} \cdot \frac{e-1}{e} \right)
$$

$$
= 2 \ln \left(\frac{e}{e+1}\right)
$$
