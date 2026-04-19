---
id: 61-volume-integral-2-note
aliases: []
tags: []
---

### 예제412
![[exer412.png]]

---

$$
(3,0),\  (5,4)
$$
$$
\frac{4-0}{5-3}=2
$$
$$
y=2(x-3)
$$
$$
\frac{y}{2}+3=x
$$

$$
V_{y}= \pi \int_{0}^{4}x^{2}\ dy
$$
$$
=\pi \int_{0}^{4} \left( \frac{y}{2}+3 \right)^{2}\ dy
$$
$$
=\pi \int_{0}^{4}\left( 3+ \frac{x}{2} \right)^{2} \ dx
$$

### 예제 413

좌표평면에서 두 곡선 $y = x^2$, $y^2 = x$로 둘러싸인 부분을 $x$축의 둘레로 회전시켜 생
기는 회전체의 부피는?

① $\dfrac{3}{5}\pi$ $\quad$ ② $\dfrac{3}{7}\pi$ $\quad$ ③ $\dfrac{3}{8}\pi$ $\quad$ ④ $\dfrac{1}{3}\pi$ $\quad$ ⑤ $\dfrac{3}{10}\pi$

---

![[exer413.png|300]]

$$
\text{put } y_{1}=x^{2},\ y_{2}^{2}=x
$$
$$
V_{x}=\pi \int_{0}^{1}(y_{2}^{2})^{2}\ dx- \pi \int_{0}^{1}(y_{1})^{2}\ dx
$$
$$
=\pi \int_{0}^{1}x\ dx - \pi \int_{0}^{1}x^{4}
$$
$$
=\pi\left[ \frac{1}{2}x^{2} \right]_{0}^{1}-\pi \left[ \frac{1}{5}x^{5} \right]_{0}^{1}
$$
$$
=\pi\left( \frac{1}{2}-\frac{1}{5} \right)
$$
$$
=\frac{3}{10}\pi
$$

### 예제414
![[exer414.png]]

---

$$
V_{도넛}= 회전체의\ 단면적\ X\ 중심의\ 회전원주 
$$

$$
V_{y}=\sqrt{ 2 }^{2} \cdot 2\pi (\overline{OB}+1)
$$
$$
=4\pi \overline{OB}+4\pi
=12\pi
$$
$$
\overline{OB}=\frac{8}{4}=2
$$

### thm56-1 구의 일부의 부피를 구하는 공식

![[thm56-1.png|300]]

$$
V_{구의\ 부피}= \frac{4}{3}\pi r^{3}
$$
$$
V_{구의\ 일부의\ 부피}= \frac{\pi}{2}h\left( a^{2}+\frac{1}{3}h^{2} \right)
$$

회전체의 부피를 적분으로 구할수도 있지만 위의 공식으로 구할수도 있다.

####  thm56-1 연습문제 
위 회전체는 r=2인 구이다. 잘려진 왼쪽부분의 구의 부피를 구하여라
![[thm56-1-1.png|400]]

---
(1) 구의 일부의 부피 공식활용
$$
h=1-(-2)=3
$$
$$
a=\sqrt{ 2^{2}-1^{2} }=\sqrt{ 3 }
$$
$$
V=\frac{\pi}{2} \cdot 3\left( 3+\frac{1}{3}\cdot 9 \right)
$$
$$
=\frac{18}{2}\pi=9\pi
$$
(2) 적분을 이용한 회전체 부피구하는 방법
$$
x^{2}+y^{2}=2^{2}
$$
$$
V=\pi \int_{-2}^{1} y^{2}\ dx
=\pi \int_{-2}^{1}4-x^{2}\ dx
$$
$$
=\pi\left[ 4x-\frac{1}{3}x^{3} \right]_{-2}^{1}
$$
$$
\pi\left( 4\cdot 3 - \frac{1}{3} \cdot 9 \right)
$$
$$
=\pi(12-3)=9\pi
$$




### 예제 415

반지름의 길이가 $5\text{cm}$인 반구 모양의 그릇에 매초 수면의 높이가 $1\text{cm}$씩 증가하도
록 물이 흘러 들어가고 있다. 수면의 높이가 $3\text{cm}$인 순간에 부피의 증가 속도는?
(단, 단위는 $\text{cm}^3$)

① $20\pi$ $\quad$ ② $21\pi$ $\quad$ ③ $22\pi$ $\quad$ ④ $23\pi$ $\quad$ ⑤ $24\pi$

---

![[exer415.png|400]]

$$
a^{2}=5^{2}-(5-t)^{2}=10t-t^{2}
$$
$$
a=\sqrt{ 10t-t^{2} },\ h=t
$$

$$
V=\frac{\pi}{2}t\left( 10t-t^{2}+\frac{1}{3}t^{2} \right)
$$
$$
=\frac{\pi}{2} (10t^{2} -\frac{2}{3}t^{3})
$$
$$
\frac{dV}{dt}=\frac{\pi}{2}(20t-2t^{2})
$$
$$
\frac{dV}{dt}_{t=3}=\frac{\pi}{2}(60-18)
$$
$$
=\frac{42}{2}\pi 
=21\pi
$$

### 예제416
![[exer416.png]]

---

반구의 절반부피는 구가 그릇에 들어간 부분부피

![[exer416-1.png|400]]

쇠공의 반지름을 x로 두면 관계식은 아래와 같다
$$
h=30,\ a=\sqrt{ x^{2}-(30-x)^{2} }=\sqrt{ 60x-900 }
$$

$$
V_{쇠공}=\frac{\pi}{2} \cdot 30 \cdot \left( 60x-900+\frac{1}{3}30^{2} \right)
=\frac{1}{2} \cdot \frac{1}{2} \cdot \frac{4}{3}\pi 30^{3}
$$
$$
15\pi(60x-600)=10\cdot 30^{2}\pi=9000\pi
$$
$$
60x-600=600
$$
$$
60x=1200
$$
$$
x=20
$$

### 예제417
![[exer417.png]]

---

![[exer417-1.png|400]]

$$
V_{구면아래부피} 
=\frac{1}{3} \pi \left( \frac{\sqrt{ 3 }}{2} \right)^{2} \cdot \frac{3}{2} 
- \frac{\pi}{2} \cdot \frac{1}{2} \left( \left( \frac{\sqrt{ 3 }}{2}^{2} + \frac{1}{3} \cdot \left( \frac{1}{2}^{2} \right) \right) \right)
$$
$$
=\frac{1}{3}\pi \cdot \frac{3}{4} \cdot \frac{3}{2} - \frac{\pi}{4}\left( \frac{3}{4}+ \frac{1}{12} \right)
$$
$$
=\frac{3}{8}\pi-\frac{\pi}{4} \cdot \frac{10}{12}
$$
$$
=\frac{3}{8}\pi-\frac{5}{24}\pi
$$
$$
=\frac{4}{24}\pi 
=\frac{\pi}{6}
$$

### 예제418
![[exer418.png]]

---

![[exer418-1.png|400]]

$$
회전체\ 단면적 = \pi(최대반경)^{2}
$$
$$
=\pi(1+x^{2})
$$

아래는 잘못된 적분식이다.
회전체의 단면적을 $\pi(1+x^{2})$으로 두면 x값에 따라 부피가 항상 증가하기떄문에
전체회전체부피를 표현하지못한다. 
회전체의 부피에서 단조증가가 끝나는지점(절반)까지만 해당식으로 표현하는 것이 맞다
$$
V=\int_{0}^{\sqrt{ 2 }} \pi(1+x^{2})\ dx
$$
$$
=\left[ \pi x+\frac{1}{3}\pi x^{3} \right]_{0}^{\sqrt{ 2 }}
$$
$$
=\sqrt{ 2 }\pi+\frac{\pi}{3}2\sqrt{ 2 }
$$
$$
=\sqrt{ 2 }\pi\left( 1+\frac{2}{3} \right)
$$
$$
=\frac{5}{3}\sqrt{ 2 }\pi
$$

올바른 식은 아래와 같다.
$$
V=2\int_{0}^{\frac{\sqrt{ 2 }}{2}} \pi(1+x^{2})\ dx
$$
$$
=2\left[ \pi x+\frac{1}{3}\pi x^{3} \right]_{0}^{\frac{\sqrt{ 2 }}{2}}
$$
$$
=2\left( \frac{\sqrt{ 2 }}{2}\pi+ \frac{\pi}{3} \left( \frac{2\sqrt{ 2 }}{8} \right) \right)
$$
$$
=2\pi\left( \frac{\sqrt{ 2 }}{2}+\frac{\sqrt{ 2 }}{12} \right)
$$
$$
=2\pi \cdot \frac{7\sqrt{ 2 }}{12}
$$
$$
=\frac{7}{6}\sqrt{ 2 }\pi
$$