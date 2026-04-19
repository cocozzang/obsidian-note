---
id: 64-arc-length-2-note
aliases: []
tags: []
---

### 예제437
![[exer437.png]]

---

$$
l=\int_{0}^{4} \sqrt{ (-12t\sin(3t^{2}+1))^{2}+(12t\cos(3t^{2}+1))^{2} }\ dt
$$
$$
=\int_{0}^{4}\sqrt{ 12^{2}t^{2}(\sin ^{2}(3t^{2}+1)+\cos ^{2}(3t^{2}+1)) }\ dt
$$
$$
=\int_{0}^{4} 12t \ dt
=[6t^{2}]_{0}^{4}
$$
$$
=96
$$

$$
원둘레 = 2\pi \cdot 2= 12
$$
($\pi=3$ 으로 두고 계산한다)

$$
\frac{96}{12}=8
$$
정확히 8바퀴 회전하므로 최고점을 8번통과한다


### 예제 438
다음 곡선의 길이를 구하여라. (단, $0 \leq t \leq 2\pi$)
$$\begin{cases} x = \cos t\,(1 - \cos t) \\ y = \sin t\,(1 - \cos t) \end{cases}$$
---

$$
x=\cos t-\cos ^{2}t = \cos t- \frac{1+\cos 2t}{2}
$$
$$
\frac{dx}{dt}=-\sin t-\frac{1}{2} \cdot 2 \sin 2t= -\sin t+\sin 2t
$$
$$
y=\sin t-\sin t\cos t=\sin t- \frac{1}{2}\sin 2t
$$
$$
\frac{dy}{dt}=\cos t-\cos 2t
$$

$$
\left( \frac{dx}{dt} \right)^{2} + \left( \frac{dy}{dt} \right)^{2}
=\sin ^{2}t+\sin ^{2}2t -2\sin t\sin 2t +\cos ^{2}t+\cos ^{2} 2t -2\cos t \cos 2t
$$
$$
=1+1-2\sin t \sin 2t- 2\cos t \cos 2t
$$
$$
=2-2(\sin t \sin 2t+\cos t \cos 2t)
$$
$$
=2-2(\sin t \cdot 2\sin t \cos t+\cos t(1-2\sin ^{2}t))
$$
$$
=2-2(2\sin t^{2}\cos t+\cos t-2\sin t^{2}\cos t)
$$
$$
=2-2\cos t
$$

$$
l=\int_{0}^{2\pi} \sqrt{ \left( \frac{dx}{dt} \right)^{2}+\left( \frac{dy}{dt} \right)^{2} }\ dt
$$
$$
=\int_{0}^{2\pi}\sqrt{ 2-2\cos t }\ dt
$$
$$
=\int_{0}^{2\pi}\sqrt{ 2-2\left( 1-2\sin ^{2} \frac{t}{2} \right) } \ dt
$$
$$
=\int_{0}^{2\pi}\sqrt{ 2-2+4\sin ^{2} \frac{t}{2} }\ dt
$$
$$
=\int_{0}^{2\pi}2 \left|\sin \frac{t}{2} \right| \ dt
$$

구간 $[0,2\pi]$ 에서 $\frac{t}{2}$ 는 항상 양이므로 절대값은 무시해도 된다.

$$
=2 \int_{0}^{2\pi} \sin \frac{t}{2}\ dt
$$

$$
=2\left[ -2\cos \frac{t}{2} \right]_{0}^{2\pi}
$$
$$
=-4(-1-1) = 8
$$

곡선의 길이 $l=8$ 이다


### 예제439
![[exer439.png]]

---

주케이블을 중간 바닥을 원점으로 한 곡선그래프로 볼수있고
주케이블의 길이를 입자의 운동거리로 볼수잇다.

$$
x=x,\ y= \frac{e^{x}+e^{-x}}{2}
$$
$$
\frac{dy}{dx}=\frac{e^{x-e^{x}}}{2}
$$
$$
S_{위치변화량}= 2\int_{0}^{1} |\vec{V}| \ dx
$$
$$
=2\int_{0}^{1}\sqrt{ 1^{2}+ \left( \frac{dy}{dx} \right)^{2}}\ dx
$$
$$
=2\int_{0}^{1}\sqrt{ 1+\frac{(e^{x}-e^{-x})^{2}}{4} }\ dx
$$
$$
=2\int_{0}^{1}\sqrt{ \frac{e^{2x}+e^{-2x}+4}{4} }\ dx
$$
$$
\because e^{2x}+4+e^{-2x}
=e^{2x}+4e^{x}e^{-x}+e^{-2x}
=(e^{x}+e^{-x})^{2}
$$
$$
=2\int_{0}^{1}\sqrt{ \frac{(e^{x}+e^{-x})^{2}}{4} }\ dx
=2\int_{0}^{1} \frac{e^{x}+e^{-x}}{2}\ dx
$$
$$
=[e^{x}-e^{-x}]_{0}^{1}
$$
$$
=e-\frac{1}{e}-1+1
$$
$$
=e-\frac{1}{e}
$$


### 예제 440
실수 전체의 집합에서 이계도함수를 갖고 $f(0) = 0$, $f(1) = \sqrt{3}$을 만족시키는 모든
함수 $f(x)$에 대하여 $\displaystyle\int_0^1 \sqrt{1 + \{f'(x)\}^2}\,dx$의 최솟값은?
① $\sqrt{2}$ $\quad$ ② $2$ $\quad$ ③ $1 + \sqrt{2}$ $\quad$ ④ $\sqrt{5}$ $\quad$ ⑤ $1 + \sqrt{3}$

---

y=f(x)를 좌표평면상에서의 입자의 위치함수로 본다면
GE는 입자의 운동거리로 볼수있다.
f(x)는 이계도함수를 가지므로 f(x)는 최소 삼차함수이다.
입자는 가속운동을 한다고 봐야한다.

GE의 최소값은 직선이라고 생각해볼수도있는데 
3차 이상의 다항함수가 (0,0) $(1,\sqrt{ 3 })$ 을 지나면서 직선일 수 있다.
라는 명제가 참이라면 GE의 최소값은 직선이라고 할 수도 있겠다.

---
위의 풀이의 논리전개에서 오류가 존재하는데 
이계도함수가 존재한다고 해서 
입자가 가속운동을 하거나 $f''(x)\neq 0$ 하게 되는것은 아니다.

f(x)가 일차함수 또는 상수함수여도 
이계도함수는 갖는다 단지 이계도함수의 값이 0일 뿐이다.
f(x)가 이계도함수를 가진다는 의미는 
f(x)가 정의역구간내에서 연속적이고 미분가능하고
그 도함수또한 정의역 구간내에서 연속이고 미분가능하다는 의미이다

그러므로 
문제에서의 f(x)는 일차함수(직선)가 되어도 전혀문제 없기떄문에
답은 그냥 2이다.


### 예제 441
$x = 0$에서 $x = 6$까지 곡선 $y = \dfrac{1}{3}(x^2 + 2)^{\frac{3}{2}}$의 길이를 구하시오.

---

$$
\frac{dy}{dx}=\frac{1}{3} \cdot \frac{3}{2}(x^{2}+2)^{\frac{1}{2}}(2x)
$$
$$
=x\sqrt{x^{2}+2}
$$

$$
l=\int_{0}^{6}\sqrt{ 1+x^{2}(x^{2}+2) }\ dx
$$
$$
=\int_{0}^{6}\sqrt{ x^{4}+2x^{2}+1 }\ dx
$$
$$
=\int_{0}^{6}\sqrt{ (x^{2}+1)^{2} }\ dx
$$
$$
=\int_{0}^{6}(x^{2}+1)\ dx = 78
$$


### 예제442
![[exer442.png]]

---

![[exer442-1.png|400]]

$$
P(x,y)= \begin{cases}
x=\theta-\sin\theta \\
y=1-\cos\theta
\end{cases}
$$
$$
\frac{dx}{d\theta}=1-\cos\theta
$$
$$
\frac{dy}{d\theta}=\sin\theta
$$
$$
\sqrt{ \left( \frac{dx}{d\theta}^{2}\right)+\left( \frac{dy}{d\theta}^{2}  \right) }
=\sqrt{ (1-\cos\theta)^{2}+\sin ^{2}\theta }
$$
$$
=\sqrt{ 2-2\cos\theta }
$$
$$
=\sqrt{ 2-2\left( 1-2\sin ^{2} \frac{\theta}{2} \right) }
$$
$$
=\sqrt{ 4\sin ^{2} \frac{\theta}{2} }
=2 \left|\sin \frac{\theta}{2}\right|
$$

$$
l=\int_{0}^{2\pi} 2 \left|\sin \frac{\theta}{2} \right| d\theta
$$
$$
\because 0\leq \frac{\theta}{2} \leq \pi
$$

$$
=\int_{0}^{2\pi} 2\sin \frac{\theta}{2} \ d\theta
$$
$$
=\left[ -4\cos \frac{\theta}{2} \right]_{0}^{2\pi}
$$
$$
=-4(-1-1)= 8
$$

$$
3l= 3\cdot 8 = 24
$$

### 예제443
![[exer443.png]]

442번과 같은문제인데 위치함수와 같은 조건들이 문제에서 추가제공된 문제이다.
움직인거리 l은 8이다.


### 예제444
![[exer444.png]]

---

$$
\frac{dx}{d\theta}=3\cos ^{2}\theta(-\sin\theta)=-3\sin\theta \cdot \cos ^{2}\theta
$$
$$
\frac{dy}{d\theta}=3\sin ^{2}\theta(\cos\theta)=3\cos\theta \cdot \sin ^{2}\theta
$$

$$
\sqrt{ \left( \frac{dx}{d\theta} \right)^{2}+\left( \frac{dy}{d\theta} \right)^{2} }
=\sqrt{ 9\sin ^{2}\theta \cos ^{4}\theta+9\cos ^{2}\theta \sin ^{4}\theta }
$$
$$
=\sqrt{ 9\sin ^{2}\theta \cos ^{2}\theta(\cos ^{2}\theta+\sin ^{2}\theta) }
$$
$$
=\sqrt{ 9\sin ^{2}\theta \cos ^{2}\theta }
=3\sin\theta \cos\theta
=\frac{3}{2}\sin 2\theta
$$

$$
l=\int_{0}^{\frac{\pi}{2}} \frac{3}{2} \sin 2\theta\ d\theta
$$
$$
=\left[ -\frac{3}{4}\cos 2\theta \right]_{0}^{\frac{\pi}{2}}
$$
$$
=-\frac{3}{4}(-1-1)
=\frac{3}{2}
$$