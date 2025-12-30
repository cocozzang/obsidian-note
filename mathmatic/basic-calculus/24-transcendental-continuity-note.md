---
id: 24-transcendental-derivative-3-note
aliases: []
tags: []
---

예제135
모든 실수 x에 대하여 미분가능한 함수 f(x)가 다음 조건을 만족할 때
$f(2)\times f'(2)$의 값을 구하여라
조건1 : $f(x)>0$이고 $f'(0)=2$이다 
조건2: 임의의 두 실수 x,y에 대하여 $f(x+y)=f(x)f(y)$이다 

조건2의 식에 x,y=0 대입
$$
f(0)=f(0)\cdot f(0)
$$

$$
\frac{f(0)}{f(0)}=f(0)
$$

$$
f(0)=1
$$

y로 편미분 후 y=0대입
$$
f'(x+y)=f(x)f'(y)
$$

$$
\text{exp1: } f'(x)=f(x)\cdot f'(0)
$$



exp1을 변형
$$
\frac{f'(x)}{f(x)}=f'(0)=2
$$

$$
\frac{f'(x)}{f(x)}=\{\ln f(x)\}'
$$

$$
\int \frac{f'(x)}{f(x)}dx=\ln f(x)=2x+C
$$

$$
f(x)=e^{2x+C}
$$

$$
f(0)=e^{C}=1
$$

$$
\therefore C=0 \ , \ f(x)=e^{2x}
$$


$$
f'(x)=2e^{2x}\ ,\ f'(2)=2e^{4}
$$

$$
f(2)+f'(2)=e^{4}+2e^{4}=2e^{8}
$$

예제136
실수 전체의 집합에서 정의된 함수 
$$
f(x)=\begin{cases}
\frac{a-\cos 2x}{x^{2}}  & (x\neq 0)\\
b & (x=0)
\end{cases}
$$
가 x=0에서 연속이 되도록 상수 a,b의 값을 정할때 a+b의 값을 구하여라


$$
f(0)=b
$$

아래식이 참일때 f(x)는 x=0에서 연속
$$
\lim_{ x \to 0 } \frac{a-\cos 2x}{x^{2}}=b
$$

극한 분수식이 유한확정값b를 가지므로 
$$
a=\lim_{ x \to 0 } \cos 2x=1
$$

$$
b=\lim_{ x \to 0 } \frac{1-(1-2\sin ^{2}x)}{x^{2}}
=\lim_{ x \to 0 } \frac{2\sin ^{2}x}{x^{2}}=2
$$

a=1 , b=2
a+b=3

예제137
함수 
$$
f(x)=\begin{cases}
e^{x}\cdot \cos x & (x\geq 0) \\
2x^{2}+px+q & (x<0)
\end{cases}
$$
가 x=0에서 미분가능 할때 p+g를 구하여라 (단 p,g는 상수)

연속성확인
$$
f(0)=\lim_{ x \to 0^{+} } f(x)=\lim_{ x \to 0^{-} } f(x)
$$

$$
f(0)=e^{0}\cdot \cos 0
=1\cdot 1 =1
$$

$$
\lim_{ x \to 0^{+} } f(x)= \lim_{ x \to 0^{+} } e^{0}\cdot \cos 0 =1 
$$

$$
\lim_{ x \to 0^{-} } f(x)=\lim_{ x \to 0^{-} } 2x^{2}+px+q
=q
$$

$$
q=1
$$

x=0에서 좌미분 우미분확인

$$
\begin{cases}
f'_{+}(0)=ex\cdot \cos x-e^{x}\cdot\sin x = 1\cdot 1 - 1\cdot 0=1 \\
f'_{-}(0)=4x+p=p
\end{cases}
$$
$$
p=1
$$
$$
p+q=1+1=2
$$

예제138
함수 
$$
f(x)=\begin{cases}
(1+x)^{\frac{1}{\sin x}} & (-\pi < x < \pi,\ x\neq 0)  \\
k & (x=0)
\end{cases}
$$
가 x=0에서 연속일때 k의 값을 구하여라 

$f(0)=\lim_{ x \to 0 }f(x)$일떄 f(x)는 연속임으로

$$
\lim_{ x \to 0 } f(x)
=\lim_{ x \to 0 } (1+x)^{\frac{1}{\sin x}}
=\lim_{ x \to 0 }(1+x)^{\frac{1}{x}}=e 
$$

$$
\therefore k=e
$$

예제139
구간$\left( -\frac{\pi}{2}, \frac{\pi}{2} \right)$에서 연속인 함수 f(x)가 $f(x)=\frac{2x}{\ln(1+\sin x)}$일때 f(0)의 값을 구하여라 

$$
f(0)=\lim_{ x \to 0 } f(x)
=\lim_{ x \to 0 } \frac{2x}{\ln(1+\sin x)}
$$

$$
=\lim_{ x \to 0 } \frac{1}{\ln (1+\sin x)^{\frac{1}{2x}}}
=\lim_{ x \to 0 } \frac{1}{\ln (1+\sin x)^{\frac{1}{\sin x}\cdot \frac{\sin x}{2x}}}
$$

$$
=\lim_{ x \to 0 } \frac{1}{1\cdot \frac{\sin x}{2x}}
=\frac{1}{1\cdot\frac{1}{2}}=2
$$

예제140
함수 
$$
f(x)=\begin{cases}
e^{x} & (x\leq 1) \\
a\cdot \sin \pi x+b & (x>1)
\end{cases}
$$
가 x=1에서 미분가능하도록 상수 a,b의 값을 정할떄 $\frac{b}{a}$의 값을 구하여라

연속성
$$
f(1)=\lim_{ x \to 1^{-} }f(x) =\lim_{ x \to 1^{+} } f(x)
$$

$$
e^{1}=e^{1}=a\cdot \sin \pi+b=a\cdot 0+b=b
$$

$$
b=e
$$

좌미분 우미분 비교
$$
f'(x)=\begin{cases}
e^{x} & (x<1)  \\
a\pi \cos \pi x  & (x>1)
\end{cases}
$$

$$
f'_{-}(1)=f'_{+}(1)
$$

$$
e^{1}=a\pi \cos \pi \cdot 1
$$

$$
=a\pi \cdot -1=e
$$

$$
a=-\frac{e}{\pi}
$$

$$
\frac{b}{a}= \frac{e}{-\frac{e}{\pi}}=-\pi
$$

예제141
함수 
$$
f(x)=\begin{cases}
e^{x-a} & (x<1) \\
\ln x+b & (x \geq 1)
\end{cases}
$$
가 x=1에서 미분가능하기 위한 $a+\ln b$의 값을 구하여라 (단 a,b는 상수)

$$
given: f(1)=\lim_{ x \to 1^{-} } f(x)=\lim_{ x \to 1^{+} } f(x)
$$

$$
\ln 1+b=e^{1-a}=\ln 1+b
$$

$$
e^{1-a}=b
$$

$$
\exp 1:\ \ln b=1-a
$$


$$
given: f'_{-}(1)=f'_{+}(1)
$$

$$
f'(x)=\begin{cases}
e^{x-a} & (x < 1) \\
\frac{1}{x}  & (x>1)
\end{cases}
$$

$$
f'_{-}(1)=f'_{+}(1)
$$

$$
e^{1-a}=\frac{1}{1}
$$

$$
\ln 1=1-a
$$

$$
a=1
$$

$$
\exp 1=\ln b=1-a=1-1=0
$$

$$
a+\ln b=1+0=1
$$

$(\ln x)'=\frac{1}{x}$이 맞았던가? 유도해보자
$$
\begin{align}
\text{put}\ \log_{a}x=f(x) \\

(\log_{a} x)'=f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} \\
=\lim_{ h \to 0 } \frac{\log_{a}(x+h)-\log_{a}x}{h} \\
=\lim_{ h \to 0 } \frac{\log_{a} \frac{x+h}{x}}{h} \\
=\lim_{ h \to 0 } \frac{\log_{a}\left( 1+\frac{h}{x} \right)}{h} \\
=\lim_{ h \to 0 } \log_{a}\left( 1+\frac{h}{x} \right)^{\frac{x}{h}\cdot \frac{1}{x}} \\
=\log_{a}e\cdot \frac{1}{x} \\
=\frac{1}{x}\cdot \ln a  \\
\therefore (\ln x)'=\frac{1}{x}
\end{align} 
$$

예제142
함수
$$
f(x)=\begin{cases}
\frac{\sin (x^{2})}{x} & (x \neq 0)  \\
0 & (x=0)
\end{cases}
$$
일때 f'(x)의 x=0에서의 연속성을 조사하여라


f'(x)가 x=0에서의 연속성조사

$$
\text{condition}:\ f'(0)=\lim_{ x \to 0 } f'(x)
$$

$$
f'(0)=\lim_{ h \to 0 } \frac{f(0+h)-f(0)}{h}
=\lim_{ h \to 0 } \frac{\frac{\sin h^{2}}{h}-0}{h}
=\lim_{ h \to 0 } \frac{\sin h ^{2}}{h^{2}}
=1
$$


$$
\lim_{ x \to 0 } f'(x)
=\lim_{ x \to 0 } \frac{2x^{2}\cos x^{2}-\sin x^{2}}{x^{2}}
=\lim_{ x \to 0 } 2\cos x^{2}-1
=2-1=1
$$

$$
\because f'(0)=\lim_{ x \to 0 } f'(x)
$$
f'(x)는 x=0에서 연속이다

중요: f'(0) 전개식에서 $f(0+h)$는 f(x)의 $\frac{\sin(x^{2})}{x}$에 대응하는 식이고 f(0)은 0임을 알아야한다.


예제143
함수 
$$
f(x)=\begin{cases}
x\sin \frac{1}{x} & (x\neq 0) \\
0 & (x=0)
\end{cases}
$$
일때 f(x)의 x=0에서의 연속성과 미분가능성을 조사하여라 ( 참고 $(\sin \frac{1}{x})' \neq \cos \frac{1}{x}$)

연속성조사
$$
condition: f(0)=\lim_{ x \to 0^{+} } f(x)=\lim_{ x \to 0^{-} } f(x)=0
$$

$\lim_{ x \to 0 } x\sin \frac{1}{x}$ 에서 sin은 무한대로 발산함으로 샌드위치 정리를 이용

우극한
$$
lim_{ x \to 0+ } -1 \leq \ \sin \frac{1}{x} \leq 1
$$

$$
lim_{ x \to 0+ } -x \leq \ x\sin \frac{1}{x} \leq x
$$

$$
\because 0\leq \lim_{ x \to 0^{+} } x\sin \frac{1}{x} \leq 0 
$$

$$
\lim_{ x \to 0^{+} } x\sin \frac{1}{x}=0
$$

좌극한
$$
\lim_{ x \to 0^{-} }  -1\leq \sin \frac{1}{x} \leq 1
$$

$$
\lim_{ x \to 0^{-} } -x \geq x\sin \frac{1}{x} \geq x
$$

$$
\because 0 \geq \lim_{ x \to 0^{-} } x\sin \frac{1}{x} \geq 0
$$

$$
\lim_{ x \to 0^{-} } x\sin \frac{1}{x}=0
$$

f(x)는 x=0에서 연속이다.

미분가능성 조사
$$
condition: f'_{-}(0)=f'_{+}(0)
$$

$x\sin \frac{1}{x}$을 미분하는 방법을 모르니 미분계수 정의를 이용 f'(0)을 구해보자

$$
f'(0)=\lim_{ h \to 0 } \frac{f(0+h)-f(0)}{h}
=\lim_{ h \to 0 } \frac{h\sin \frac{1}{h}-0}{h}
=\lim_{ h \to 0 } \sin \frac{1}{h}
$$

$\lim_{ h \to 0 } \sin \frac{1}{h}$은 극한값이 존재하지 않는다
즉 f'(0)가 존재하지 않는다.

그러므로 f(x)는 x=0에서 미분불가능
