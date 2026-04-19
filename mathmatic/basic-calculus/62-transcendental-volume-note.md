---
id: 62-transcendental-volume-note
aliases: []
tags: []
---

### 예제 419
아래 그림은 함수 $y = x^2$과 $x = 1$, $y = 0$으로 둘러
싸인 부분에 구간 $[0,\ 1]$을 $5$등분하여 직사각형을
내접시킨 것이다. 어두운 부분을 $x$축 둘레로 회전
시켜서 생긴 회전체의 부피는?
① $\dfrac{213}{5^5}\pi$ $\quad$ ② $\dfrac{237}{5^5}\pi$ $\quad$ ③ $\dfrac{256}{5^5}\pi$

④ $\dfrac{271}{5^5}\pi$ $\quad$ ⑤ $\dfrac{354}{5^5}\pi$
![[exer419.png|300]]

---

곡선의 회전체부피에서 4개의 원기둥 부피를 뺸 값
$$
V=\int_{0}^{1} \pi y^{2} \ dx 
- \frac{1}{5}\pi \left( \left( \frac{1}{5} \right) ^{4}+\left( \frac{2}{5} \right)^{4} + \left( \frac{3}{5} \right)^{4} + \left( \frac{4}{5} \right)^{4}\right)
$$
$$
=\pi \int_{0}^{1}x^{4}\ dx
- \frac{\pi}{5^{5}}(1^{4}+2^{4}+3^{4}+4^{4})
$$
$$
\pi\left[ \frac{1}{5}x^{5} \right]_{0}^{1} - \frac{\pi}{5^{5}}(1+16+81+256)
$$
$$
=\frac{\pi}{5}-\frac{354}{5^{5}}\pi
$$
$$
=\frac{625-354}{5^{5}}\pi
$$
$$
=\frac{271}{5^{5}}\pi
$$

### 예제 420

곡선 $y = \dfrac{1}{2}\ln x$와 $x$축, $y$축 및 직선 $y = \ln 2$로 둘러싸인 영역을 $y$축의 둘레로 회전
시켜 생기는 회전체의 부피를 $V$라 할 때, $\dfrac{V}{\pi}$의 값을 소수점 아래 둘째 자리까지
구하시오.

---

![[exer420.png| 400]]

$$
2y=\ln x
$$
$$
x=e^{2y},\ x^{2}=e^{4y}
$$

$$
V= \pi \int_{0}^{\ln 2} x^{2}\ dy
$$
$$
V=\pi \int_{0}^{\ln 2} e^{4y}\ dy
$$
$$
=\pi\left[ \frac{1}{4}e^{4y} \right]_{0}^{\ln 2}
$$
$$
=\frac{\pi}{4}(e^{4\ln 2}-1)
=\frac{\pi}{4}(2^{4}-1)
$$
$$
=\frac{15}{4}\pi
$$

$$
\frac{V}{\pi}=\frac{15}{4}=3.75
$$

### 예제 421

곡선 $y = 5\sqrt{\ln x}$와 $x$축 및 직선 $x = e$로 둘러싸인 부분을 $x$축 둘레로 회전하여 생
기는 회전체의 부피를 $V$라 할 때, $\dfrac{V}{\pi}$의 값을 구하시오.

---


$$
V=\pi\int_{1}^{e}y^{2}\ dx
$$
$$
=\pi \int_{1}^{e} 25\ln x\ dx
$$
$$
=25\pi \int_{1}^{e} \ln x\ dx
$$
$$
=25\pi [x\ln x-x]_{1}^{e}
$$
$$
=25\pi(e-e+1)
$$
$$
=25\pi
$$

$$
\frac{V}{\pi}=\frac{25\pi}{\pi}=25
$$

### 예제422
![[exer422.png]]

---

$$
given: \frac{dV}{dt}=a
$$

$$
V=\pi \int_{0}^{h}x^{2}\ dy
=\pi \int_{0}^{h}\sin ^{2}y\ dy
$$
$$
=\pi \int_{0}^{h} \frac{1-\cos 2y}{2}\ dy = \frac{\pi}{2}\int_{0}^{h}1-\cos 2y\ dy
$$
$$
=\frac{\pi}{2}\left[ y-\frac{1}{2} \sin 2y \right]_{0}^{h}
$$
$$
=\frac{\pi}{2}\left({h-\frac{1}{2} \sin 2 h}\right)
$$

$$
\frac{dV}{dt}= \frac{d}{dt} \cdot\frac{\pi}{2}\left( h-\frac{1}{2}\sin 2h \right) \cdot \frac{dh}{dh}
$$
$$
= \frac{\pi}{2}(1-\cos 2h) \cdot \frac{dh}{dt}
=a
$$

$$
\frac{dV}{dt}_{h=\frac{\pi}{4}}
=\frac{\pi}{2}\left( 1-\cos \frac{\pi}{2} \right)\cdot \frac{dh}{dt}=a
$$
$$
=\frac{\pi}{2} \cdot \frac{dh}{dt}=a
$$
$$
\frac{dh}{dt}= \frac{2a}{\pi}
$$

### 예제 423
곡선 $y = \cos 2x$와 $x$축, $y$축, $x = \dfrac{\pi}{2}$으로 둘러싸인 부분을 $x$축의 둘레로 회전시켜
생기는 회전체의 부피는? $\left(\text{단},\ 0 \leq x \leq \dfrac{\pi}{2}\right)$
① $\dfrac{\pi^2}{4}$ $\quad$ ② $\dfrac{\pi^2}{2}$ $\quad$ ③ $\dfrac{3}{4}\pi^2$ $\quad$ ④ $\pi^2$ $\quad$ ⑤ $2\pi^2$

---

![[exer423.png|400]]


$$
V=\pi\int_{0}^{\frac{\pi}{4}} y^{2}\ dx + \pi \int_{\frac{\pi}{4}} ^{\frac{\pi}{2}} y^{2} \ dx
$$
$$
=\pi\left( \int_{0}^{\frac{\pi}{4}}\cos ^{2}2x\ dx + \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \cos ^{2}2x\ dx \right)
$$
$$
=\frac{\pi}{2}\left( \int_{0}^{\frac{\pi}{4}}1+\cos 4x \ dx + \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} 1+\cos 4x\ dx \right)
$$
$$
=\frac{\pi}{2}\left( \left[ x+\frac{1}{4}\sin 4x \right]_{0}^{\frac{\pi}{4}}+\left[ x+\frac{1}{4} \sin 4x \right]_{\frac{\pi}{4}}^{\frac{\pi}{2}} \right)
$$
$$
=\frac{\pi}{2}\left( \frac{\pi}{4} + \frac{\pi}{2}-\frac{\pi}{4} \right)
$$
$$
=\frac{\pi^{2}}{4}
$$

### 예제 424
타원 $4x^2 + y^2 = 4$를 $x$축의 둘레로 회전시켜 생기는 회전체의 부피와 $y$축의 둘레로
회전시켜 생기는 회전체의 부피의 합은?
① $\dfrac{8}{3}\pi$ $\quad$ ② $\dfrac{16}{3}\pi$ $\quad$ ③ $8\pi$ $\quad$ ④ $\dfrac{32}{3}\pi$ $\quad$ ⑤ $\dfrac{40}{3}\pi$

---

![[exer424.png|400]]

$$
V_{sum}= \pi \int_{-2}^{2} x^{2}\ dy+ \pi \int_{-1}^{1} y^{2} \ dx
$$

$$
x^{2}=\frac{4-y^{2}}{4},\ 
y^{2}=4(1-x^{2})
$$

$$
V_{sum}=\frac{\pi}{4}\int_{-2}^{2}4-y^{2}\ dy + 4\pi \int_{-1}^{1}1-x^{2}\ dx
$$
$$
=\frac{\pi}{2}\int_{0}^{2}4-y^{2}\ dy + 8\pi \int_{0}^{1}1-x^{2}\ dx
$$
$$
=\frac{\pi}{2}\left[ 4y-\frac{1}{3}y^{3} \right]_{0}^{2}+8\pi\left[ x-\frac{1}{3}x^{3} \right]_{0}^{1}
$$
$$
=\frac{\pi}{2}\left( 8-\frac{8}{3} \right)+8\pi\left( 1-\frac{1}{3} \right)
$$
$$
=\frac{\pi}{2}\left( \frac{16}{3} \right)+8\pi\left( \frac{2}{3} \right)
$$
$$
=\frac{8}{3}\pi+\frac{16}{3}\pi=\frac{24}{3}\pi
$$
$$
=8\pi
$$

### 예제 425
곡선 $y = \tan x$와 $x$축 및 직선 $x = \dfrac{\pi}{3}$로 둘러싸인 부분을 $x$축 둘레로 회전시켜 생
기는 회전체의 부피는?
① $\dfrac{\pi^2}{3}$ $\quad$ ② $\sqrt{2}\,\pi + \dfrac{\pi^2}{3}$ $\quad$ ③ $\sqrt{2}\,\pi - \dfrac{\pi^2}{3}$
④ $\sqrt{3}\,\pi + \dfrac{\pi^2}{3}$ $\quad$ ⑤ $\sqrt{3}\,\pi - \dfrac{\pi^2}{3}$

---

![[exer425.png|300]]

$$
V=\pi \int_{0}^{\frac{\pi}{3}} y^{2}\ dx = \pi \int_{0}^{\frac{\pi}{3}} \tan ^{2}x\ dx
$$
$$
=\pi \int_{0}^{\frac{\pi}{3}} \sec ^{2}x-1\ dx
$$
$$
\pi[\tan x-x]_{0}^{\frac{\pi}{3}}= \pi\left( \sqrt{ 3 }-\frac{\pi}{3} \right)
$$
$$
=\sqrt{ 3 }\pi-\frac{\pi^{2}}{3}
$$

### 예제 426
곡선 $y = \ln x$와 $x$축 및 직선 $x = e$로 둘러싸인 부분을 $x$축의 둘레로 회전시켜 생
기는 회전체의 부피는?
① $(e-1)\pi$ $\quad$ ② $(e-2)\pi$ $\quad$ ③ $(e-3)\pi$ $\quad$ ④ $(e-4)\pi$ $\quad$ ⑤ $(e-5)\pi$

---

$$
V = \pi \int_{1}^{e} \{f(x)\}^2 \, dx = \pi \int_{1}^{e} (\ln x)^2 \, dx
$$

#### $(\ln x)^{2}$적분
$$\int (\ln x)^2 \, dx = x(\ln x)^2 - \int x \cdot \left( \frac{2\ln x}{x} \right) \, dx$$
$$\int (\ln x)^2 \, dx = x(\ln x)^2 - 2 \int \ln x \, dx$$
$$\int (\ln x)^2 \, dx = x(\ln x)^2 - 2(x\ln x - x) + C$$
$$\int (\ln x)^2 \, dx = x(\ln x)^2 - 2x\ln x + 2x + C$$

$$V = \pi \left[ x(\ln x)^2 - 2x\ln x + 2x \right]_{1}^{e}$$

**$x = e$ 대입:**

$$e(\ln e)^2 - 2e\ln e + 2e = e(1)^2 - 2e(1) + 2e = e - 2e + 2e = e$$

**$x = 1$ 대입:**

$$1(\ln 1)^2 - 2(1)\ln 1 + 2(1) = 0 - 0 + 2 = 2$$

**최종 계산:**

$$V = \pi (e - 2) = (e - 2)\pi$$

 정답: ② $(e - 2)\pi$


### 예제 427
어떤 입체의 밑면은 곡선 $y = \ln x$와 $x$축 및 직선 $x = e$로 둘러싸인 평면이고,
$x$축에 수직인 평면으로 이 입체를 자른 단면은 한 변이 밑면에 있는 정삼각
형이다. 이 입체의 부피를 구하여라.
① $\dfrac{\sqrt{3}}{4}(e+2)$ $\quad$ ② $\dfrac{\sqrt{3}}{4}(e+1)$ $\quad$ ③ $\dfrac{\sqrt{3}}{4}e$
④ $\dfrac{\sqrt{3}}{4}(e-1)$ $\quad$ ⑤ $\dfrac{\sqrt{3}}{4}(e-2)$

---

![[exer427.png|300]]

$$
S\triangle=\frac{\sqrt{ 3 }}{4}y^{2}
$$

$$
V=\frac{\sqrt{ 3 }}{4}\int_{1}^{e} (\ln x)^{2} \ dx
$$
$$
=\frac{\sqrt{ 3 }}{4}(e-2)
$$

### 예제 428
좌표평면 위에 두 곡선 $y = \sin x$, $y = \cos x\ \left(\dfrac{\pi}{4} \leq x \leq \dfrac{5\pi}{4}\right)$으로 둘러싸인 도형을 밑면
으로 하고, $x$축에 수직인 평면으로 자른 단면이 정사각형으로 이루어진 입체의 부
피는?
① $\dfrac{\pi}{4}$ $\quad$ ② $\dfrac{\pi}{2}$ $\quad$ ③ $\pi$ $\quad$ ④ $2\pi$ $\quad$ ⑤ $4\pi$

---

![[exer428.png|400]]

$$
V=\int_{\frac{\pi}{4}}^{\frac{5}{4}\pi}(\sin x-\cos x)^{2}\ dx
$$
$$
=\int_{\frac{\pi}{4}}^{\frac{5}{4}\pi} 1-2\sin x\cos x\ dx
$$
$$
=\int_{\frac{\pi}{4}}^{\frac{5}{4}\pi} 1-\sin 2x\ dx
$$
$$
=\left[ x+\frac{1}{2}\cos 2x \right]_{\frac{\pi}{4}}^{\frac{5}{4}\pi}
$$
$$
=\frac{5}{4}\pi-\frac{\pi}{4}+0-0 
$$
$$
=\pi
$$

### 예제429 
![[exer429.png]]

---

![[exer429-1.png]]