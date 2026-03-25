---
id: 47-fundamental-theorem-note
aliases: []
tags: []
---

### 예제300
$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( 3+\frac{2k}{n} \right)^{3} \frac{1}{n}
$$

을 다음 각 경우로 고치고 그 값을 구하여라 

(1) 정적분 구간 길이 =2 

---
$$
3+\frac{2k}{n}=x
$$
$$
dx=\frac{2}{n}
$$
$$
\frac{1}{2}\int_{3}^{5}x^{3}\ dx
$$
$$
=\frac{1}{2}\cdot\left[ \frac{1}{4}x^{4} \right]_{3}^{5}
$$
$$
=\frac{1}{2}\left( \frac{5^{4}}{4}-\frac{3^{4}}{4} \right)
$$
$$
=\frac{625}{8}-\frac{81}{8}=\frac{544}{8}=68
$$

(2) 정적분 구간 길이 = 1

---
$$
2\cdot \frac{1}{2} \int_{\frac{3}{2}}^{\frac{5}{2}} (2x)^{3}\ dx
$$
$$
8\int_{\frac{3}{2}}^{\frac{5}{2}}x^{3}\ dx
=8\left[ \frac{1}{4}x^{4} \right]_{\frac{3}{2}}^{\frac{5}{2}}
$$
$$
=\frac{8}{4}\left( \frac{625}{16}-\frac{81}{16} \right)
$$
$$
=\frac{625}{8}-\frac{81}{8}=68
$$

(3) 정적분 구간 길이 = 3

---
$$
8\int_{\frac{3}{2}}^{\frac{5}{2}}x^{3}\ dx \implies 
$$
$$
\frac{1}{3}\cdot 8 \int_{\frac{9}{2}}^{\frac{15}{2}} \left( \frac{1}{3}x \right)^{3}\ dx
$$
$$
=\frac{8}{3}\int_{\frac{9}{2}}^{\frac{15}{2}} \frac{1}{27}x^{3}\ dx
$$
$$
=\frac{8}{3^{4}}\int_{\frac{9}{2}}^{\frac{15}{2}}x^{3}\ dx
$$
$$
=\frac{8}{3^{4}}\left[ \frac{1}{4}x^{4} \right]_{\frac{9}{2}}^{\frac{15}{2}}
$$
$$
=\frac{2}{3^{4}}\left( \frac{15^{4}}{2^{4}}-\frac{9^{4}}{2^{4}} \right)
$$
$$
=\frac{5^{4}}{2^{3}}-\frac{3^{4}}{2^{3}}
=\frac{625}{8}-\frac{81}{8}
=68
$$

### 예제301
다음 극한값을 구하여라 
(1)
$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( 1+\frac{3k}{n} \right) \frac{1}{n}
$$
---

$$
\text{put}\ 1+\frac{3k}{n}=x
$$
$$
=\frac{1}{3}\int_{1}^{4}x\ dx
=\frac{1}{3}\left[ \frac{1}{2}x^{2} \right]_{1}^{4}
$$

$$
=\frac{1}{6}\left( 16-1 \right)
$$
$$
=\frac{15}{6}=\frac{5}{2}
$$

(2)
$$
\lim_{ n \to \infty } \frac{1^{4}+2^{4}+3^{4}\dots+n^{4}}{n^{5}}
$$
---
$$
GE=\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( \frac{k}{n} \right)^{4} \frac{1}{n}
$$
$$
\text{put}\ \frac{k}{n}=x
$$
$$
dx=\frac{1}{n}
$$
$$
=\int_{0}^{1}x^{4}\ dx
=\left[ \frac{1}{5}x^{5} \right]_{0}^{1}
$$
$$
$$
$$
=\frac{1}{5}
$$

(3)
$$
\lim_{ n \to \infty } \frac{1}{n^{4}}\{(3n-1)^{3}+(3n-2)^{3}+\dots+(3n-n)^{3}\}
$$
---
$$
GE=\lim_{ n \to \infty }\Sigma_{k=1}^{n} (3n-k)^{3} \frac{1}{n^{4}}
=\lim_{ n \to \infty } \Sigma_{k=1}^{n}(3n-k)^{3}\left( \frac{1}{n} \right)^{3} \frac{1}{n}
$$
$$
=\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( 3-\frac{k}{n} \right)^{3} \frac{1}{n}
$$
$$
\text{put}\ 3-\frac{k}{n}=x
$$
$$
dx=-\frac{1}{n}
$$
$$
GE=-\int_{3}^{2}x^{3}\ dx
=-\left[ \frac{1}{4}x^{4} \right]_{3}^{2}
$$
$$
=-\frac{1}{4}(16-81)
=\frac{65}{4}
$$

tip:
$$
\int_{b}^{a}f(x)\ dx = -\int_{a}^{b}f(x)\ dx
$$
$$
-\int_{3}^{2}x^{3}\ dx=\int_{2}^{3}x^{3}\ dx
$$
로 변환해서 풀어도 된다.
정적분에서 적분구간이 역순일떈 적분값에 -가 곱해지는 결과가 되는 성질이 있나보다 


(4)
$$
\lim_{ n \to \infty } \frac{(1+2+\dots+n)(1^{4}+2^{4}+\dots+n^{4})}{(1^{2}+2^{2}+\dots+n^{2})(1^{3}+2^{3}+\dots+n^{3})}
$$
---

$$
GE=\lim_{ n \to \infty } \frac{\Sigma_{k=1}^{n}k \cdot \Sigma_{k=1}^{n}k^{4}}{\Sigma_{k=1}^{n}k^{2} \cdot \Sigma_{k=1}^{n}k^{3}}
$$
$$
=\lim_{ n \to \infty } \frac{\Sigma_{k=1}^{n} \frac{k}{n} \cdot \Sigma_{k=1}^{n} \frac{k^{4}}{n^{4}} }{\Sigma_{k=1}^{n} \frac{k^{2}}{n^{2}}\cdot \Sigma_{k=1}^{n} \frac{k^{3}}{n^{3}}}
$$

$$
=\lim_{ n \to \infty } \frac{\frac{1}{n}\Sigma_{k=1}^{n} (\frac{k}{n}) \cdot \frac{1}{n}\Sigma_{k=1}^{n} (\frac{k}{n})^{4}}{\frac{1}{n} \Sigma_{k=1}^{n} (\frac{k}{n})^{2} \cdot \frac{1}{n}\Sigma_{k=1}^{n} (\frac{k}{n})^{3}}
$$
$$
=\frac{\int_{0}^{1}x\ dx \cdot \int_{0}^{1}x^{4}\ dx}{\int_{0}^{1}x^{2}\ dx \cdot \int_{0}^{1} x^{3}\ dx}
$$
$$
=\frac{\left[ \frac{1}{2}x^{2} \right]_{0}^{1} \cdot \left[ \frac{1}{5}x^{5} \right]_{0}^{1}}{\left[ \frac{1}{3}x^{3} \right]_{0}^{1}\cdot\left[ \frac{1}{4}x^{4} \right]_{0}^{1}}
$$
$$
=\frac{\frac{1}{2}\cdot \frac{1}{5}}{\frac{1}{3}\cdot \frac{1}{4}}
$$
$$
=\frac{\frac{1}{10}}{\frac{1}{12}}=\frac{12}{10}=\frac{6}{5}
$$

### 예제302
아래 보기는 
$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( 3- \frac{2k}{n} \right)^{2} \frac{4}{n}
$$
를 정적분으로 나타낸 것이다 틀린것은 ?

(1)
$$
\int_{1}^{3}2x^{2}\ dx
$$
(2)
$$
\int_{-2}^{0}2(x+3)^{2}\ dx
$$
(3)
$$
\int_{-1}^{0}4(2x+3)^{2}\ dx
$$

(4)
$$
\int_{0}^{1}4(2x+3)^{2}\ dx
$$


$$
\lim_{ n \to \infty } \Sigma_{k=1}^{n}\left( 3- \frac{2k}{n} \right)^{2} \frac{4}{n}
$$
$$
\text{put}\ 3-\frac{2k}{n}=x
$$
$$
dx=-\frac{2}{n}
$$
$$
GE=-2\int_{3}^{1}x^{2}\ dx
$$
$$
-2\int_{3}^{1}x^{2}\ dx
$$

(1)은 참이다
$$
=2\int_{1}^{3}x^{2}\ dx 
=\int_{1}^{3}2x^{2}\ dx 
$$

(2)도 참이다 (1)에서 그래프와 적분구간이 -3만큼 평행이동 된것이므로

(3)도 참이다 (2)번그래프가 x=0방향으로 2배만큼 압축되고 적분구간도 1/2만큼 줄어든 것에 2배를 곱하엿으므로

(4)이 틀렸다