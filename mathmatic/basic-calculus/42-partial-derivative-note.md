---
id: 42-partial-derivative-note
aliases: []
tags: []
---

### Def4 이변수 함수에서의 편도함수

간단한 수준에서 편도함수를 구하는 방법을 알아보자
자세한 증면은 대학미적분학에서 한다



### 예제267
$f(x,y)=x^{3}+x^{2}y^{3}-2y^{2}$ 일때 $f_{x}(1,1),\ f_{y}(1,1)$을 구하여라

---
$$
f_{x}=\frac{\partial f}{\partial x}=3x^{2}+2xy^{3}
$$
$$
f_{x}(1,1)=3+2=5
$$

$$
f_{y}=\frac{\partial f}{\partial y}=3x^{2}y^{2}-4y
$$
$$
f_{y}(1,1)=-1
$$

### 에제268
$f(x,y)=\sin\left( \frac{x}{1+y} \right)$ 일때
$\frac{\partial f}{\partial x},\\ \frac{\partial f}{\partial y}$ 를 구하여라

---

$$
\frac{\partial f}{\partial x}=\cos\left( \frac{x}{1+y} \right)\cdot \frac{1}{1+y}
$$
$$
\frac{\partial f}{\partial y}=\cos\left( \frac{x}{1+y} \right)\cdot \frac{-x}{(1+y)^{2}}
$$


### 예제269
$f(x,y)=\ln(3x^{5}+2y^{3})+e^{2x}$의 $f_{x}, f_{y}$를 구하여라

---
$$
f_{x}=\frac{15x^{4}}{3x^{5}+2y^{3}}+2e^{2x}
$$
$$
f_{y}=\frac{6y^{2}}{3x^{5}+2y^{3}}
$$


### 예제270
$z=e^{xy}\cos x \sin y$ 의 편도함수 $\frac{\partial z}{\partial x},\ \frac{\partial z}{\partial y}$ 를 구하려라 

---
$$
\frac{\partial z}{\partial x}
=\sin y(ye^{xy}\cdot \cos x+e^{xy}(-\sin x))
$$
$$
=\sin y\cdot e^{xy}(y\cos x-\sin x)
$$

$$
\frac{\partial z}{\partial y}
=\cos x(xe^{xy}\sin y+e^{xy}\cos y)
$$
$$
=\cos x\cdot e^{xy}(x\sin y+\cos y)
$$

### 예제271
$z=x\sin y+y\sec x$의 편도함수 $\frac{\partial z}{\partial x},\ \frac{\partial z}{\partial y}$를 구하여라

---

$$
\frac{\partial z}{\partial x}
=\sin y+y\tan x\sec x
$$
$$
\frac{\partial z}{\partial y}
=x\cos y+\sec x
$$

$$
(\sec x)' = \left( \frac{1}{\cos x} \right)'
=\frac{\sin x}{\cos ^{2}x}=\tan x\sec x
$$


### 예제272
$\mu=e^{x^{2}+xy+z^{2}}$ 의 편도함수 $\frac{\partial \mu}{\partial x},\ \frac{\partial \mu}{\partial y},\ \frac{\partial \mu}{\partial z}$ 를 구하여라

---
$$
\frac{\partial \mu}{\partial x}
=(2x+y)e^{x^{2}+xy+z^{2}}
$$
$$
\frac{\partial \mu}{\partial y}
=xe^{x^{2}+xy+z^{2}}
$$
$$
\frac{\partial \mu}{\partial z}=2ze^{x^{2}+xy+z^{2}}
$$


### Thm42 이변수 함수에 대한 연쇄법칙 


### 예제273
$\mu=x^{2}+xe^{y},\ x=\sin t,\ y=\ln t$ 일떄 t에 관한 $\mu$ 의 전도함수 
$\frac{d\mu}{dt}$를 구하여라

---
$$
\frac{d\mu}{dt}=\frac{d\mu}{dx}\cdot \frac{dx}{dt}+\frac{d\mu}{dy}\cdot \frac{dy}{dt}
$$
$$
\frac{d\mu}{dx}=2x+e^{y}
$$
$$
\frac{dx}{dt}=\cos t
$$
$$
\frac{d\mu}{dy}=xe^{y}
$$
$$
\frac{dy}{dt}=\frac{1}{t}
$$
$$
\frac{d\mu}{dt}=(2x+e^{y})\cos t+\frac{1}{t}\cdot xe^{y}
$$

### 예제274
원기둥의 높이는 매초 4cm의 속도로 감소하고 밑면의 반지름은 
매초 1cm의 속도로 증가할때 높이가 50cm이고 반지름이 20cm인 순간에
부피의 변화속도를 구하여라

---

$$
V=f(r,h)=\pi r^{2}h
$$
$$
r=t,\
h=-4t
$$
$$
V'=\frac{dV}{dt}=\frac{dV}{dr}\cdot \frac{dr}{dt}+\frac{dV}{dh}\cdot \frac{dh}{dt}
$$
$$
\frac{dV}{dr}=2\pi rh,\ 
\frac{dr}{dt}=1
$$
$$
\frac{dV}{dh}=\pi r^{2},\ 
\frac{dh}{dt}=-4
$$
$$
\frac{dV}{dt}=2\pi rh-4\pi r^{2}
=2\pi r(h-2r)
$$
$$
\frac{dV}{dt}_{h=50,\ r=20}
=40\pi(50-40)
=400\pi(cm^{3}\text{/}\sec)
$$


### 예제275
생산함수 P는 노동L과 자본C와 관계가 있으며 다음과 같은 공식을 
만족한다고 하자 $P=3.5L^{\frac{6}{5}}C^{\frac{1}{2}}$
L=12이고 C=4일때 노동의 변화율은 2.5이며 자본의 변화율은 0.5이다
생산의 증가율을 구하면? (단 $12^{\frac{1}{5}=1.643}$으로 계산한다)
(1) 약 11.7
(2) 약 22.2
(3) 약 31.1
(4) 약 43.1

--- 

$$
P'=\frac{dP}{dt}=\frac{dP}{dL}\cdot \frac{dL}{dt}+\frac{dP}{dC}\cdot \frac{dC}{dt}
$$

$$
given: P'_{L=12,\ C=4} 일떄\ \frac{dL}{dt}=2.5,\ \frac{dC}{dt}=0.5
$$
$$
\frac{dP}{dL}=3.5\cdot \frac{6}{5}L^{\frac{1}{5}}C^{\frac{1}{2}}
$$
$$
\frac{dP}{dC}=3.5 \cdot \frac{1}{2}C^{-\frac{1}{2}}L^{\frac{6}{5}}
$$
$$
P'_{L=12,\ C=4}
=3.5\cdot \frac{6}{5}L^{\frac{1}{5}}C^{\frac{1}{2}}\cdot 2.5
+3.5\cdot \frac{1}{2}C^{-\frac{1}{2}}L^{\frac{6}{5}}\cdot 0.5
$$
$$
=\frac{35}{10}\cdot \frac{25}{10}\cdot \frac{6}{5}\cdot 2 \cdot 12^{\frac{1}{5}}
+ \frac{35}{10}\cdot \frac{1}{2} \cdot \frac{1}{2} \cdot \frac{1}{2} \cdot 12^{\frac{6}{5}}
$$


$$
좌항=\frac{7}{2}\cdot \frac{5}{2} \cdot \frac{6}{5} \cdot 2 \cdot 12^{\frac{1}{5}}
$$
$$
좌향=21\cdot 12^{\frac{1}{5}}
$$
$$
우항=\frac{7}{2}\cdot \frac{1}{8}\cdot 12^{\frac{6}{5}}
$$
$$
우항=\frac{7}{16}\cdot 12 \cdot 12^{\frac{1}{5}}=\frac{21}{4} \cdot 12^{\frac{1}{5}}
$$

$$
P'_{L=12,\ C=4}=21\cdot 12^{\frac{1}{5}}+\frac{21}{4}\cdot 12^{\frac{1}{5}}
$$
$$
=21\cdot 12^{\frac{1}{5}}\left( 1+\frac{1}{4} \right)
$$
$$
=21\cdot 12^{\frac{1}{5}}\left( \frac{5}{4} \right)
$$
$$
=\frac{105}{4}\cdot \frac{1643}{1000}
$$
$$
=\frac{21}{4}\cdot \frac{1643}{200}
$$

여기서 계산기 조지면 아래와 같음
$$
=43.12875
$$
