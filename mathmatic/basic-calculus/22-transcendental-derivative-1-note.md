---
id: 22-transcendental-derivative-1-note
aliases: []
tags: []
---

## thm24 삼각함수의 도함수

$$
(\sin x)'=\cos x
$$

$$
(\cos x)'=-\sin x
$$

$$
(\tan x)'=\sec ^{2}x
$$

$$
(\cot x)'=-\csc^{2}x
$$

$$
(\sec x)'= \sec x \cdot \tan x
$$

$$
(\csc x)'=-\csc x \cdot \cot x
$$

## thm25 지수 로그 함수의 도함수

$$
(e^{x})'=e^{x}
$$

$$
(a^{x})'=a^{x} \cdot \ln a
$$

$$
(\ln x)'=\frac{1}{x}
$$

$$
(\log_{a}x)'=\frac{1}{x}\cdot \frac{1}{\ln a}
$$

### 삼각함수의 도함수 유도과정

[[11-advanced-trigonometry-4#합차를 곱으로 변환하는 공식]]

#### $(\sin x)'=\cos x$

$$
\text{put} f(x)=\sin x
$$

$$
(\sin x)'=f('x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\sin(x+h)-\sin x}{h}
=\lim_{ h \to 0 } \frac{2\cos\left( x+\frac{h}{2} \right)\cdot \sin\left( \frac{h}{2} \right)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\cancel{2}\cdot \cos\left( x+\frac{h}{2} \right)\cdot \sin\left( \frac{h}{2} \right)}{\frac{h}{2}}
$$

$$
=\lim_{ h \to 0 } \frac{\cos\left( x+\frac{h}{2} \right)\cdot \cancel{\sin\left( \frac{h}{2} \right)}}{\cancel{\frac{h}{2}}}
$$

$$
=\lim_{ h \to 0 } \cos\left( x+\frac{h}{2} \right)=\cos(x)
$$

$$
(\sin x)'=\cos(x)
$$

#### $(\cos x)'=-\sin x$

$$
\text{put}\ f(x)=\cos x
$$

$$
(\cos x)'=f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\cos(x+h)-\cos x}{h}
$$

$$
=\lim_{ h \to 0 } \frac{-2\sin (x+\frac{h}{2})\cdot \sin(\frac{h}{2})}{h}
$$

$$
=\lim_{ h \to 0 } -\sin\left( x+ \frac{h}{2} \right)=-\sin x
$$

$$
(\cos x)'= -\sin x
$$

#### $(\tan x)'=\sec ^{2}x$

note: 몫의 미분

$$
\left( \frac{f(x)}{g(x)} \right)'= \frac{f'(x)\cdot g(x)-f(x)\cdot g'(x)}{\{g(x)\}^{2}}
$$

$$
(\tan x)'=\left( \frac{\sin x}{\cos x} \right)'=\frac{(\sin x)'\cdot \cos x-\sin x\cdot (\cos x)'}{\cos ^{2}x}
$$

$$
=\frac{\cos ^{2} x+\sin ^{2}x}{\cos ^{2}x}=\frac{1}{\cos ^{2}x}=\sec ^{2}x
$$

$$
(\tan x)'=\sec ^{2}x
$$

#### $(\cot x)'=-\csc ^{2}x$

$$
(\cot x)'=\left( \frac{\cos x}{\sin x} \right)'=\frac{(-\sin x)\cdot \sin x-\cos x\cdot \cos x}{\sin ^{2}x}
$$

$$
=\frac{-\sin ^{2}x-\cos ^{2}x}{\sin ^{2}x}=\frac{-1}{\sin ^{2}x}=-\csc ^{2}x
$$

$$
(\cot x)'=-\csc ^{2}x
$$

#### $(\sec x)'=\sec x\cdot \tan x$

$$
\left( \frac{1}{\cos x} \right)'=\frac{0\cdot(-\sin x)-1\cdot (-\sin x)}{\cos ^{2}x}
$$

$$
=\frac{\sin x}{\cos ^{2}x}=\frac{1}{\cos x}\cdot \frac{\sin x}{\cos x}
=\sec x \cdot \tan x
$$

$$
(\sec x)'= \sec x \cdot \tan x
$$

#### $(\csc x)'=-\csc x\cdot \cot x$

$$
(\csc x)'=\left(\frac{1}{\sin x}\right)'
=\frac{0\cdot \sin x-1\cdot \cos x}{\sin ^{2}x}
$$

$$
=\frac{-1}{\sin x}\cdot \frac{\cos x}{\sin x}
=-\csc x\cdot \cot x
$$

$$
(\csc x)'=-\csc x \cdot \cot x
$$

### 지수로그함수의 도함수 유도과정

[[13-transcendental-limit-1#(3) 극한값 e의 정리]]

#### $(e^{x})'=e^{x}$ , $(a^{x})'=a^{x} \cdot \ln a$ 의 유도

$$
\text{put}\ f(x)=a^{x}
$$

$$
(a^{x})'=f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
$$

$$
=\lim_{ h \to 0 }  \frac{a^{x+h}-a^{x}}{h}
=\lim_{ h \to 0 } \frac{a^{h}-1}{h}\cdot a^{x}
=ax\cdot \ln a
$$

$$
\therefore (a^{x})'=ax\cdot \ln a
$$

$$
(e^{x})'=ex
$$

ex) $(3^{2x})'=2\cdot 3^{2x}\cdot \ln a$

#### $(\ln x)'=\frac{1}{x}$ , $(\log_{a}x)'=\frac{1}{x} \cdot \frac{1}{\ln a}$ 의 유도

$$
\text{put} f(x)=\log_{a}x
$$

$$
(\log_{a}x)'=f'(x)
=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
$$

$$
=\lim_{ h \to 0 } \frac{\log_{a}(x+h)-\log_{a}x}{h}
=\lim_{ h \to 0 } \frac{1}{h} \cdot \log_{a} \left( \frac{x+h}{x} \right)
$$

$$
=\lim_{ h \to 0 } \frac{1}{h} \cdot \log_{a}\left( 1+\frac{h}{x} \right)
=\lim_{ h \to 0 } \log_{a}\left( 1+\frac{h}{x} \right)^{\frac{x}{h}\cdot \frac{1}{x}}
$$

$$
=\frac{1}{x} \cdot \log_{a}e
=\frac{1}{x} \cdot \frac{1}{\log_{e}a}
=\frac{1}{x} \cdot \frac{1}{\ln a}
$$

$$
\therefore (\log_{a}x)'=\frac{1}{x}\cdot \frac{1}{\ln a}
$$

$$
(\ln x)'=\frac{1}{x}
$$

ex) $(\log_{2} 3x^{3})=9x^{2} \cdot\frac{1}{3x^{3}} \cdot \frac{1}{\ln 2}=\frac{3}{x}\cdot \frac{1}{\ln 2}$
