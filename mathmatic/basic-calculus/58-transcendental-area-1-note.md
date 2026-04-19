---
id: 58-transcendental-area-1-note
aliases: []
tags: []
---

### 예제391
![[exer391.png]]

---

$$
A=\int_{p}^{q} \frac{\ln x}{\ln a}-\frac{\ln x}{\ln b}\ dx
=\frac{1}{\ln a} \int_{p}^{q} \ln x \ dx - \frac{1}{\ln b} \int_{p}^{q} \ln x\ dx
$$
$$
B=\int_{p}^{q} \frac{\ln x}{\ln b}\ d x
=\frac{1}{\ln b} \int_{p}^{q} \ln x \ dx
$$


$$
\frac{\alpha}{\beta}= \frac{\ln b}{\ln a}-1
$$
$$
=\log_{a}b-1
$$

### 예제 392

곡선 $y=3\sqrt{x-9}$와 이 곡선 위의 점 $(18,\ 9)$에서의 접선 및 $x$축으로 둘러싸인 영역의 넓이를 구하시오.

---

$$
y=3(x-9)^{\frac{1}{2}}
$$
$$
y'=\frac{1}{2}(x-9)^{-\frac{1}{2}}\cdot 1
$$
$$
=3 \cdot \frac{1}{2\sqrt{ x-9 }}
$$
$$
y'_{x=18}=\frac{3}{2\cdot 3}=\frac{1}{2}
$$
$$
y_{\tan}=\frac{1}{2}x
$$

$$
S=\frac{1}{2} \cdot 18 \cdot 9- \int_{9}^{18} 3\sqrt{ x-9 }\ dx
$$
$$
=81-3\left[ \frac{2}{3}(x-9)^{\frac{3}{2}} \right]_{9}^{18}
$$
$$
=81-2\left[ (x-9)^{\frac{3}{2}} \right]_{9}^{18}
$$
$$
=81-2(27)
=81-54
=27
$$


### 예제393 (풀이 생략)
![[exer393.png]]

---

### **1. 각 영역의 넓이 구하기**

**삼각형의 넓이 $A_n$:**

밑변 $P_n Q_n = (n+1) - n = 1$, 높이 $Q_n P_{n+1} = f(n) - f(n+1)$ 입니다.

$$A_n = \frac{1}{2} \times 1 \times \{f(n) - f(n+1)\} = \frac{e^{-n} - e^{-(n+1)}}{2}$$

**곡선 아래의 넓이와 $B_n$의 관계:**

구간 $[n, n+1]$에서 직사각형(밑변 1, 높이 $f(n)$)의 넓이는 $f(n)$입니다.

이미지에서 보듯, 이 직사각형의 넓이는 **(정적분 영역) + (삼각형 $A_n$)** 과 같습니다.

따라서 $\int_{n}^{n+1} f(x) dx = f(n) - (A_n + B_n)$ 관계가 성립하는지 확인해 봅시다.

- 곡선 위쪽 사다리꼴의 넓이: $A_n + B_n + \int_{n}^{n+1} f(x) dx = f(n) \cdot 1$ 가 아니므로 기하학적으로 확인이 필요합니다.
    
- 사실상 $\int_{n}^{n+1} f(x) dx$는 곡선 아래 면적이고, $f(n)$은 높이가 $f(n)$인 직사각형 면적입니다.
    
- 그림에서 $f(n) = \int_{n}^{n+1} f(x) dx + A_n + B_n$ 이 성립함을 알 수 있습니다.
    

---

### **2. 보기 검증**

#### **ㄱ. $\int_{n}^{n+1} f(x) dx = f(n) - (A_n + B_n)$**

위 분석에 따라 $f(n)$(전체 직사각형)에서 $A_n$과 $B_n$을 빼면 곡선 아래의 넓이인 정적분 값이 나옵니다.

> **ㄱ: 참 (True)**

#### **ㄴ. $\sum_{n=1}^{\infty} A_n = \frac{1}{2e}$**

$A_n = \frac{1}{2}(e^{-n} - e^{-(n+1)})$ 이므로 이는 망원급수(Telescoping series) 형태입니다.

$$\sum_{n=1}^{\infty} A_n = \frac{1}{2} \left[ (e^{-1} - e^{-2}) + (e^{-2} - e^{-3}) + \dots \right]$$

항들이 상쇄되어 첫 번째 항만 남습니다.

$$\sum_{n=1}^{\infty} A_n = \frac{1}{2} e^{-1} = \frac{1}{2e}$$

> **ㄴ: 참 (True)**

#### **ㄷ. $\sum_{n=1}^{\infty} B_n = \frac{3-e}{2e(e-1)}$**

ㄱ의 식을 $B_n$에 대해 정리하면:

$B_n = f(n) - A_n - \int_{n}^{n+1} f(x) dx$

전체 합을 구하면:

$$\sum B_n = \sum f(n) - \sum A_n - \int_{1}^{\infty} f(x) dx$$

1. $\sum_{n=1}^{\infty} f(n) = \sum_{n=1}^{\infty} (e^{-1})^n = \frac{e^{-1}}{1-e^{-1}} = \frac{1}{e-1}$
    
2. $\sum_{n=1}^{\infty} A_n = \frac{1}{2e}$ (ㄴ에서 구함)
    
3. $\int_{1}^{\infty} e^{-x} dx = [-e^{-x}]_{1}^{\infty} = 0 - (-e^{-1}) = \frac{1}{e}$
    

따라서,

$$\sum B_n = \frac{1}{e-1} - \frac{1}{2e} - \frac{1}{e} = \frac{1}{e-1} - \frac{3}{2e}$$

통분하면:

$$\frac{2e - 3(e-1)}{2e(e-1)} = \frac{2e - 3e + 3}{2e(e-1)} = \frac{3-e}{2e(e-1)}$$

> **ㄷ: 참 (True)**


ㄱ, ㄴ, ㄷ 모두 참이다



### 예제 394
자연수 $n$에 대하여 구간 $[0,\ \pi]$에서 두 곡선 $y=\dfrac{1}{n}\sin x$, $y=\dfrac{1}{n+1}\sin x$
로 둘러싸인 부분의 넓이를 $S_{n}$이라 할 때, $\displaystyle\lim_{n \to \infty}\sum_{k=1}^{n} S_{k}$의 값은?
① $1$ ② $\sqrt{2}$ ③ $2$ ④ $\dfrac{\pi}{2}$ ⑤ $\pi$

---

$$
S_{n}=\int_{0}^{\pi} \frac{1}{n}\sin x\ dx - \int_{0}^{\pi} \frac{1}{n+1}\sin x\ dx
$$
$$
=\left( \frac{1}{n}- \frac{1}{n+1} \right)\int_{0}^{\pi}\sin x\ dx
$$
$$
=\left( \frac{1}{n}- \frac{1}{n+1} \right) [-\cos x]_{0}^{\pi}
$$
$$
=2\left( \frac{1}{n}- \frac{1}{n+1} \right)
$$

$$
\lim_{ n \to \infty } \sum_{k=1}^{n}S_{k}
=2\left( \frac{1}{k}-\frac{1}{k+1} \right)
$$
telescoping sum 임 으로
$$
=\lim_{ n \to \infty } 2\left( 1-\frac{1}{n+1} \right)
=2
$$

## 예제 395

자연수 $n$에 대하여 구간 $[(n-1)\pi,\ n\pi]$에서 곡선 $y=\left(\dfrac{1}{2}\right)^{n}\sin x$와
$x$축으로 둘러싸인 부분의 넓이를 $S_{n}$이라 하자.
$\displaystyle\sum_{n=1}^{\infty}S_{n}=\alpha$일 때, $50\alpha$의 값을 구하시오.

---

$$
S_{n}=\left( \frac{1}{2} \right)^{n} \cdot \int_{0}^{\pi}\sin x\ dx
$$
$$
=\left( \frac{1}{2} \right)^{n} \cdot [-\cos x]_{0}^{\pi}
$$
$$
=\left( \frac{1}{2} \right)^{n}(1-(-1))
$$
$$
=\left( \frac{1}{2} \right)^{n}\cdot 2
=\left( \frac{1}{2} \right)^{n-1}
$$

$$
\sum_{n=1}^{\infty}S_{n}=\alpha
=\sum_{n=1}^{\infty} \left( \frac{1}{2} \right)^{n-1}
$$
$$
=\frac{1}{1-\frac{1}{2}}=2
$$
$$
50\alpha=2 \cdot 50 = 100
$$


## 예제 396

각 항이 양수인 수열 $\{a_{n}\}$은 모든 자연수 $n$에 대하여 다음 두 조건을 만족한다.

> (가) $a_{n} > a_{n+1}$
>
> (나) 곡선 $y=\dfrac{1}{x}$과 두 직선 $x=a_{n+1}$, $x=a_{n}$ 및 $x$축으로 둘러싸인 부분의
> 넓이는 $1$이다.

$a_{1}=2$일 때, $\displaystyle\sum_{n=1}^{\infty}a_{n}$의 값은? (단, $e$는 자연로그의 밑이다.)

① $\dfrac{e}{e-1}$ $\quad$ ② $\dfrac{2e}{e-1}$ $\quad$ ③ $\dfrac{2e+1}{e}$ $\quad$ ④ $\dfrac{2e+3}{e}$ $\quad$ ⑤ $\dfrac{3e+1}{2e+1}$

---

![[exer396.png]]

$$
S=\int_{a_{n+1}}^{a_{n}} \frac{1}{x}\ dx=1
$$
$$
=[\ln x]_{a_{n+1}}^{a_{n}}
$$
$$
=\ln \frac{a_{n}}{a_{n+1}}=1
$$
$$
\frac{a^{n}}{a_{n+1}}=e
$$
$$
a_{n}=e \cdot a_{n+1}
$$
$$
a_{n+1}= \frac{1}{e} \cdot a_{n}
$$
공비가 $\frac{1}{e}$ 인 수열이다. 초항이 2라면

$$
\sum_{n=1}^{\infty}a_{n}= \frac{2}{1-\frac{1}{e}}
$$
$$
=\frac{2e}{e-1}
$$


### 예제397
![[exer397.png]]

---

$$
S_{n}=\int_{e^{n}}^{e^{n+1}} \ln x\ dx- \frac{1}{2} \cdot (2n+1) \cdot (e^{n+1}-e^{n})
$$
$$
=[x\ln x-x]_{e^{n}}^{e^{n+1}}-\left( n+\frac{1}{2} \right)(e^{n+1}-e^{n})
$$
$$
=e^{n+1}(n+1)-e^{n+1}-n\cdot e^{n}+e^{n}- \left( n+\frac{1}{2} \right)(e^{n+1}-e^{n})
$$
$$
=n \cdot e^{n+1}-ne^{n}+e^{n}-ne^{n+1}+ne^{n}-\frac{1}{2}e^{n+1}+\frac{1}{2}e^{n}
$$
$$
=e^{n} -\frac{1}{2}e^{n+1}+\frac{1}{2}e^{n}
$$
$$
=\frac{1}{2}e^{n}(3-e)
$$
$$
=\frac{(3-e)}{2} \cdot e^{n}
$$

$$
\sum_{n=1}^{\infty} \frac{1}{S_{n}}= \frac{2}{3-e} \cdot \left( \frac{1}{e} \right)^{n}
$$
$$
= \frac{2}{3-e} \cdot \frac{\frac{1}{e}}{1-\frac{1}{e}}
$$
$$
=\frac{2}{3-e} \cdot \frac{1}{e-1}
=\frac{2}{(3-e)(e-1)}
$$

역함수를 이용한 풀이 
$$
S_{n}= \frac{1}{2}(2e^{n}+e^{n+1})\cdot 1- \int_{n}^{n+1} f^{-1}(x)\ dx
$$
$$
=\frac{1}{2}(e^{n}+e^{n+1})-\int_{n}^{n+1}e^{x}\ dx
$$
$$
=\frac{1}{2}e^{n}+\frac{1}{2}e^{n+1}-e^{n+1}+e^{n}
$$
$$
=\frac{3}{2}e^{n}-\frac{1}{2}e^{n+1}
$$
$$
=\frac{1}{2}e^{n}\cdot(3-e)
$$
