---
id: 65-improper-double-integral-note
aliases: []
tags: []
---

### 예제445
$$
\int_{-\infty}^{-2} \frac{2}{x^{2}-1}\ dx =?
$$
---

$$
=\lim_{ b \to -\infty } \int_{b}^{-2}\left( \frac{1}{x-1}-\frac{1}{x+1} \right)\ dx
$$
$$
=\lim_{ b \to -\infty } [\ln|x-1| - \ln|x+1|]_{b}^{-2}
$$
$$
=\lim_{ b \to -\infty } \left[ \ln \left| \frac{x-1}{x+1} \right| \right]_{b}^{-2}
$$
$$
=\lim_{ b \to -\infty } \ln |\frac{-3}{-1}| - \ln| \frac{b-1}{b+1}|
$$
$$
=\ln 3 - \ln 1 = \ln 3
$$

### 예제446
$$
\int_{-\infty}^{\infty} \frac{2x}{(x^{2}+1)^{2}}\ dx =?
$$
---

$$
GE=\int_{-\infty}^{0} \frac{2x}{(x^{2}+1)^{2}}\ dx + \int_{0}^{\infty} \frac{2x}{(x^{2}+1)^{2}} \ dx 
$$

$$
x^{2}+1=t,\ 2x\cdot dx=dt
$$
$$
0+1=1,\ (-\infty)^{2}+1=\infty,\ (\infty)^{2}+1=\infty
$$

$$
GE=\int_{\infty}^{1} \frac{1}{t^{2}}\ dt + \int_{1}^{\infty} \frac{1}{t^{2}}\ dt
$$
$$
=\int_{1}^{\infty} - \frac{1}{t^{2}}\ dt + \int_{1}^{\infty} \frac{1}{t^{2}}\ dt
$$
$$
=\int_{1}^{\infty} \frac{1}{t^{2}}-\frac{1}{t^{2}}\ dt
$$
$$
=\int_{1}^{\infty} 0 \ dt = 0
$$


### 예제447
$$
\int_{-\infty}^{0} xe^{x}\ dx =?
$$
---

$$
GE= [xe^{x}-e^{x}]_{-\infty}^{0}
$$
$$
=\lim_{ x \to -\infty } -1-(xe^{x}-e^{x})
$$
$$
=-1- \lim_{ x \to \infty } \left( \frac{x}{e^{-x}}-e^{x} \right)
$$
$$
=-1- \lim_{ x \to -\infty } \left( \frac{1}{-e^{-x}}-0 \right)
$$
$$
=-1
$$

### 예제448
$$
\int_{-\infty}^{\ln 2} \frac{\pi}{4}e^{2x} \ dx =?
$$
---

$$
=\frac{\pi}{4}\left[ \frac{1}{2}e^{2x} \right]_{-\infty}^{\ln 2}
$$
$$
=\frac{\pi}{8}(4-0)
$$
$$
=\frac{\pi}{2}
$$

### 예제449
$$
\int_{0}^{\infty} x^{2}e^{-\frac{x}{2}}\ dx =?
$$
---

$$
=\left[ x^{2}\cdot \left( -2e^{-\frac{x}{2}} \right) - 2x\left( 4e^{-\frac{x}{2}} \right) + 2\left( -8e^{-\frac{x}{2}} \right) \right]_{0}^{\infty}
$$
$$
=\left[ \frac{-2x^{2}}{e^{\frac{x}{2}}}-\frac{8x}{e^{\frac{x}{2}}}-\frac{16}{e^{\frac{x}{2}}} \right]_{0}^{\infty}
$$
$\lim_{ x \to \infty } \frac{x^{n}}{e^{x}}$ 의 극한값은 항상 0 에 수렴하므로 

$$
=0-(0-0-16)
$$
$$
=16
$$


### 예제450
$$
\int_{-\infty}^{\ln 2} \frac{1}{4} e^{2x}\ dx=?
$$
---

$$
=\frac{1}{4}\left[ \frac{1}{2}e^{2x} \right]_{-\infty}^{\ln 2}
$$
$$
=\frac{1}{8}(4-0)
=\frac{1}{2}
$$


### thm59 일반영역에서의 중적분 문제유형정리1
중적분개념과 계산만 간단히 알아보고 자세한 내용은 대학미적분학 강의에서 진행한다.
계산시 편미분처럼 적분대상이 아닌 변수는 상수취급한다.


### 예제 451
$\displaystyle\int_0^3 \int_0^1 \sqrt{x+y}\ \,dxdy$의 값은?
① $\dfrac{4}{15}(32 + 9\sqrt{3})$ $\quad$ ② $\dfrac{4}{15}(32 - 9\sqrt{3})$ $\quad$ ③ $\dfrac{4}{15}(31 + 9\sqrt{3})$ $\quad$ ④ $\dfrac{4}{15}(31 - 9\sqrt{3})$

---

$$
GE= \int_{0}^{3} \int_{0}^{1}(x+y)^{\frac{1}{2}}\ dxdy
$$
$$
=\int_{0}^{3} \left[ \frac{2}{3}(x+y)^{\frac{3}{2}} \right]_{0}^{1}\ dy
$$
$$
=\int_{0}^{3} \frac{2}{3}(1+y)^{\frac{3}{2}}-\frac{2}{3}y^{\frac{3}{2}}\ dy
$$
$$
=\left[ \frac{2}{3} \cdot \frac{2}{5} (1+y)^{\frac{5}{2}}-\frac{2}{3} \cdot \frac{2}{5}y^{\frac{5}{2}} \right]_{0}^{3}
$$
$$
=\frac{4}{15}\left[ (1+y)^{\frac{5}{2}}-y^{\frac{5}{2}} \right]_{0}^{3}
$$
$$
=\frac{4}{15}\left( (4^{\frac{5}{2}}-1)-(3^{\frac{5}{2}}-0) \right)
$$
$$
=\frac{4}{15}(2^{5}-1-9\sqrt{ 3 })
$$
$$
=\frac{4}{15}(31-9\sqrt{ 3 })
$$

### thm60 일반영역에서의 중적분 문제유형정리 2
중적분개념과 계산만 간단히 알아보고 자세한 내용은 대학미적분학 강의에서 진행한다.


### 예제 452
$D$가 포물선들 $y = 2x^2$, $y = 1 + x^2$에 의해 유계된 영역이라 할 때
$\displaystyle\iint_D (x + 2y)\,dA$를 구하여라.

---

![[exer452.png|400]]
$$
GE=\int_{-1}^{1}\int_{2x^{2}}^{1+x^{2}}(x+2y)\ dydx
$$

$$
\int_{2x^{2}}^{1+x^{2}}(x+2y)\ dy
=[xy+y^{2}]_{2x^{2}}^{1+x^{2}}
$$
$$
=x(1+x^{2})-2x^{3}+(1+x^{2})^{2}-4x^{4}
$$
$$
=x+x^{3}-2x^{3}+x^{4}+2x^{2}+1-4x^{4}
$$
$$
=-3x^{4}-x^{3}+2x^{2}+x+1
$$

$$
GE=\int_{-1}^{1}(-3x^{4}-x^{3}+2x^{2}+x+1)\ dx
$$
$$
=2\int_{0}^{1}(-3x^{4}+2x^{2}+1)\ dx
$$
$$
=2\left[ -\frac{3}{5}x^{5}+\frac{2}{3}x^{3}+x \right]_{0}^{1}
$$
$$
=2\left( -\frac{3}{5}+\frac{2}{3}+1 \right)
$$
$$
=2\left( -\frac{9}{15}+\frac{10}{15}+\frac{15}{15} \right)
$$
$$
=\frac{32}{15}
$$


### 예제453
$$
\int_{1}^{\ln 2}\int_{0}^{3y} e^{x+y}\ dxdy =?
$$
---

$$
\int_{0}^{3y} e^{x+y}\ dx 
=[e^{x+y}]_{0}^{3y}
$$
$$
=e^{4y}-e^{y}
$$

$$
GE=\int_{1}^{\ln 2} e^{4y}-e^{y}\ dy
$$
$$
=\left[ \frac{1}{4}e^{4y}-e^{y} \right]_{1}^{\ln 2}
$$
$$
=\frac{1}{4}2^{4}-\frac{1}{4}e^{4} -2 +e
$$
$$
=4-2-\frac{1}{4}e^{4}+e
$$
$$
=2+e-\frac{e^{4}}{4}
$$

