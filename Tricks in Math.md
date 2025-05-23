# Tricks in Math 数学中的二级结论

> Informatik verbindet dich und mich.
>
> 信息将你我连结
>
> Zeit und Raum trennen dich und mich.
>
> 时空将你我分开



[TOC]

## 不等式

### 均值不等式

> 你可能更熟悉其中的基本不等式（算术-几何平均值不等式），即 $\sqrt{x_1x_2}\leq\dfrac{x_1+x_2}{2}$​

**结论**
$$
\dfrac{n}{\sum_{i=1}^{n} \dfrac{1}{x_i}} \le \sqrt[n]{\prod_{i=1}^nx_i} \le \dfrac{\sum_{i=1}^{n} x_i }{n} \le \sqrt{\dfrac{ \sum_{i=1}^{n} x_i ^2}{n}}
$$

当且仅当 $x_1=x_2=\cdots=x_n$​ 时取等。



二维形式
$$
\dfrac{2}{\dfrac{1}{x_1}+\dfrac{1}{x_2}} \leq \sqrt{x_1x_2}\leq\dfrac{x_1+x_2}{2}\leq\sqrt{\dfrac{x_1^2+x_2^2}{2}}
$$

当且仅当 $x_1=x_2$ 时取等。



### 柯西不等式

**结论**
$$
(\displaystyle\sum_{i=1}^n x_i y_i)^2 \leq (\displaystyle\sum_{i=1}^n x_i^2) (\displaystyle\sum_{i=1}^n y_i^2)
$$
当且仅当 $\dfrac {x_1}{y_1} = \dfrac {x_2}{y_2} = \cdots = \dfrac {x_n}{y_n}$​ 时取等。



二维形式
$$
(ac+bd)^2\leq(a^2+b^2)(c^2+d^2)
$$
当且仅当 $\dfrac a c = \dfrac b d$ 时取等。



### 琴生不等式

**简介**

反映了下凸函数的基本性质

**结论**
$$
\dfrac{\sum^n_{i=1}f(x_i)}{n} \geq f(\dfrac{\sum^n_{i=1}f(x_i)}{n})
$$
当且仅当 $x_1=x_2=\cdots=x_n$​ 时取等。



二维形式
$$
f(\dfrac{x_1+x_2}{2})\geq \dfrac{f(x_1)+f(x_2)}{2}
$$
当且仅当 $x_1=x_2$ 时取等。

**加权琴生不等式**
$$
t f(x_1) + (1-t) f(x_2) \geq f (t x_1 + (1-t) x_2 ),\; 0 \leq t \leq 1
$$
当且仅当 $x_1=x_2$ 时取等。



### 糖水不等式

**简介**

它的直观意义是：往糖水里加糖，会变得更甜。（假设糖在糖水中的质量比例能代表糖水甜度，且加糖后含糖比例不超出糖水的饱和度范围）

**结论**

假设 $0 < a < b, c > 0$，则有 $\dfrac {a+c} {b+c} > \dfrac a b$。



### 双换元技巧

1. 已知正实数 $x,y$ 满足 $5x^2+4xy-y^2=1$，求 $12x^2+8xy-y^2$​ 的最小值

$$
5x^2+4xy-y^2=(5x-y)(x+y)=1\\
\begin{cases}
5x-y=m\\
x+y=n
\end{cases}\\
\begin{aligned}
12x^2+8xy-y^2=\dfrac{3m^2+27n^2+66mn}{36}&=\dfrac{1}{12}(m^2+9n^2)+\dfrac{6}{11}\\
&\geq \dfrac{1}{6}\sqrt{9m^2n^2}+\dfrac{6}{11}=\dfrac{3}{7}
\end{aligned}
$$

2. 已知正实数 $x,y$ 满足 $\dfrac{8}{3x^2+2xy}+\dfrac{3}{xy+2y^2}=1$，求 $xy$ 的最小值

$$
\dfrac{8}{x(3x+2y)}+\dfrac{3}{y(x+2y)}=1
\\\Longrightarrow\; \dfrac{8y}{3x+2y}+\dfrac{3x}{x+2y}=xy
\\\begin{cases}
3x+2y=m\\
x+2y=n
\end{cases}\\
xy=\dfrac{8y}{3x+2y}+\dfrac{3x}{x+2y}=\dfrac{6m-2n}{n}+\dfrac{3(n-m)}{2m}\geq \dfrac 2 5\\
$$

3. 已知正实数 $x,y$ 满足 $\sqrt{9x^2-1}+\sqrt{9y^2-1}=9xy$，求 $4x^2+y^2$ 的最小值

$$
\begin{aligned}
  & \begin{cases}
      \sqrt{9x^2-1}=m \\
      \sqrt{9y^2-1}=n
    \end{cases}
  \\
  & \Longrightarrow\; m+n=\sqrt{(m^2+1)(n^2+1)}\\
  & \Longrightarrow\; m^2n^2-2mn+1=0\\
  & \Longrightarrow\; mn=1\\
& 4x^2+y^2=\dfrac 4 9 m^2 + \dfrac 1 9 n^2+ \dfrac 5 9 \geq 1 
\end{aligned}
$$



## 数的运算

### 对数运算

**和差**
$$
\log_\alpha M N=
\log_\alpha\!M+\log_\alpha\!N
$$

$$
\begin{aligned}
\log_\alpha\ M\!N&=\log_\alpha\ \beta^m\!\beta^n\\
&=\log_\alpha\ \beta^{m+n}\\
&=(m+n)\log_\alpha\!\beta\\
&=m\log_\alpha\!\beta+n\log_\alpha\!\beta\\
&=\log_\alpha\ \beta^m+\log_\alpha\ \beta^n\\
&=\log_\alpha\!M+\log_\alpha\!N\\
\log_\alpha\!\frac{M}{N}&=\log_\alpha\!M+\log_\alpha\!\frac{1}{N}\\
&=\log_\alpha\!M-\log_\alpha\!N
\end{aligned}
$$
**换底公式**
$$
\log_\alpha\!x=\frac{\log_\beta\!x}{\log_\beta\!\alpha}
$$


设 $\log_\alpha\!x=t \;\Longrightarrow\; x=\alpha^{t}$ 

对其两边取对数，则有 $\log_\beta x=\log_\beta \alpha^{t}$

即 $\log_\beta x = t \log_\beta \alpha$

又 $\log_\alpha x=t$

$\Longrightarrow \; \log_\alpha x=\dfrac{\log_\beta\!x}{\log_\beta \alpha}$​

**次方公式**
$$
\log_{\alpha^n} x^m
=\frac{m}{n}\log_\alpha\!x
$$

$$
\begin{aligned}
\log_{\alpha^n}\ {x^m}&=\frac{\ln\ x^m}{\ln\ \alpha^n}\\
&=\frac{m\ln\!x}{n\ln\!\alpha}\\
&=\frac{m}{n}\log_\alpha\!x
\end{aligned}
$$
**互换**
$$
M^{\log_\alpha\!N}=N^{\log_\alpha\!M}
$$


设 $b = {\log_\alpha\!N} ,\;c = {\log_\alpha\!M}$

则有 $N=\alpha^b,\;M=\alpha^c$​

即 $M^{\log_\alpha\!N}=(\alpha^c)^b,\;N^{\log_\alpha\!M}=(\alpha^b)^c$

**倒数**
$$
\log_\alpha\!\theta=\frac{1}{\log_\theta\!\alpha}
$$

$$
\begin{aligned}
\log_\alpha\!\theta&=\dfrac{1}{\dfrac{\ln\!\alpha}{\ln\!\theta}}\\
&=\frac{1}{\log_\theta\!\alpha}
\end{aligned}
$$
**链式**
$$
\log_\gamma\!\beta\log_\beta\!\alpha=\log_\gamma\!\alpha
$$

$$
\begin{aligned}
\log_\gamma\!\beta\log_\beta\!\alpha&=\frac{\ln\!\alpha}{\ln\!\beta}\ \frac{\ln\!\beta}{\ln\!\gamma}\\
&=\frac{\ln\!\alpha}{\ln\!\gamma}\\
&=\log_\gamma\!\alpha
\end{aligned}
$$



## 初等函数

### 函数的性质



### 对勾函数换元法

**结论**

对于类似 $f(k)=\dfrac{k(1+k^2)}{(1+2k^2)(2+k^2)}, k>0$​ 的函数，探究其定义域内的最值时，可转化为对勾函数。

**证明**

对于 $1+k^2$，$ 1+mk+k^2 $ 这样的式子，除以 $k$ 即可得到 $k+\dfrac{1}{k}$ 的形式。
当令 $t=k+\dfrac{1}{k}$  时，有 $k^2+\dfrac{1}{k^2}=t^2-2$。
所以形如 $k^{2n}+mk^n+1$ 的式子都易于转化为对勾函数。

**应用**

$\dfrac{k^4+3k^2+1}{(k^2+1)(k^2+k+1)}=\dfrac{k^2+3+\frac{1}{k^2}}{(k+\frac{1}{k})(k+1+\frac{1}{k})}=\dfrac{t^2+1}{t\cdot(t+1)}$

令 $m=\dfrac{t^2+1}{t\cdot(t+1)}$ ，则  $ t^2 + 1 = m(t^2+t) \;\Rightarrow\; (m-1)t^2+mt-1=0 $

$\Delta=m^2+4(m-1)\geq 0 \;\Rightarrow\; m \geq 2\sqrt{2}-2$

经检验，此时 $t=\sqrt{2}+1$，满足条件，故 $(\dfrac{k^4+3k^2+1}{(k^2+1)(k^2+k+1)})_{min}=2\sqrt{2}-2$​



### 泰勒展开

> 在导数中，有很多不等式就是使用泰勒展开推导的，比如$e^x \geq x+1,\quad \ln x \leq x-1$

**几何级数（这个高中很少用）**
$$
\dfrac{1}{1-x} = \sum^{\infty}_{n=0} x^n= 1+ x +x^2+ \cdots +x^n +\cdots \quad \forall x: \left| x \right| < 1
$$
**二项式级数**
$$
(1+x)^\alpha = \sum^{\infty}_{n=0} \binom{\alpha}{n} x^n= 1+ \alpha x + \dfrac{\alpha (\alpha -1)}{2!} x^2 + \cdots + \dfrac{\alpha (\alpha -1) \cdots (\alpha - n +1)}{n!} x^n + \cdots \quad \forall x: \left| x \right| < 1
$$
**指数函数**
$$
e^{x} = \sum^{\infty}_{n=0} \dfrac{x^n}{n!}= 1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + \cdots +\dfrac{x^n}{n!} +\cdots \quad \forall x
$$
**自然对数**
$$
\ln(1+x) = \displaystyle\sum^{\infty}_{n=1} \dfrac{(-1)^{n+1}}n x^n = x - \dfrac{x^2}2 + \dfrac{x^3}3 - \cdots +\dfrac{(-1)^{n+1}}n x^n +\cdots \quad \forall x\in (-1,1]
$$
**三角函数**
$$
\begin{aligned}
\sin x &= \sum^{\infty}_{n=0} \cfrac{(-1)^n}{(2n+1)!} x^{2n+1} = x - \cfrac{x^3}{3!} + \cfrac{x^5}{5!} - \cdots \quad \forall x\\[6pt]
\cos x &= \sum^{\infty}_{n=0} \cfrac{(-1)^n}{(2n)!} x^{2n} = 1 - \cfrac{x^2}{2!} + \frac{x^4}{4!} - \cdots \quad \forall x\\[6pt]
\tan x &= \sum^{\infty}_{n=1} \frac{B_{2n} (-4)^n \left(1-4^n\right)}{(2n-1)!} x^{2n-1} = x + \cfrac{x^3}{3} + \cfrac{2 x^5}{15} + \cdots \quad \forall x:|x| < \cfrac{\pi}{2}\\[6pt]
\end{aligned}
$$



### 帕德近似

> 相比泰勒展开，帕德近似会有更高的精确度

**指数型**
$$
e^x<\dfrac{1}{1-x} \quad \forall x < 1
$$

$$
e^x>\dfrac{2+x}{2-x} \quad \forall x<0\\
e^x<\dfrac{2+x}{2-x} \quad \forall 0<x<2
$$
**对数型**
$$
\ln x<\dfrac{2x-2}{x+1} \quad \forall x<1\\
\ln x>\dfrac{2x-2}{x+1} \quad \forall x>1
$$



### 导数常用不等式

> 以下不等式的证明大多只需移项，然后求导即可，特殊的会另作说明。

**切线型**
$$
e^x \geq ex, \quad \ln x \leq \dfrac{x}{e}
$$
**对数均值不等式**
$$
\sqrt{x_1x_2}\leq\dfrac{x_1-x_2}{\ln x_1 - \ln x_2}\leq \dfrac{x_1+x_2}{2}
$$
证明时需要不等式两边同除 $x_2$，令 $\dfrac{x_1}{x_2}=t$​​，然后求导即可。
$$
e^\frac{x_1+x_2}{2}\leq\dfrac{e^{x_1}-e^{x_2}}{x_1-x_2}\leq\dfrac{e^{x_1}-e^{x_2}}{2}
$$
可以通过将 $x_1,x_2$ 分别替换为 $\ln t, -\ln t$ 来证明飘带不等式 $\dfrac{1}{2}(x-\dfrac{1}{x})$，$\dfrac{2x-2}{x+1}$

**双撇函数型**
$$
\ln x > \dfrac{1}{2}(x-\dfrac{1}{x}) \quad \forall x<1\\
\ln x < \dfrac{1}{2}(x-\dfrac{1}{x}) \quad \forall x>1
$$

$$
\ln x > \sqrt{x}- {1 \over \sqrt{x}} \quad \forall x<1\\
\ln x < \sqrt{x}- {1 \over \sqrt{x}} \quad \forall x>1
$$

**反比例函数型**
$$
\ln x \geq 1 - \dfrac{1}{x} = \dfrac{x-1}{x}
$$
将 $\dfrac{1}{x}$ 代入 $\ln x \leq x-1$，再同乘 $-1$​ 容易证得

**二次函数型**
$$
\ln x \leq x^2-x
$$
通过 $x^2-x \geq x -1$，$\ln x\leq x-1$​ 推得。
$$
\ln x \leq \dfrac{1}{2}(x^2-1)
$$
通过 $\dfrac{1}{2}(x^2-1) \geq x -1$，$\ln x\leq x-1$​ 推得。



### 洛必达法则

**简介**

洛必达法则是利用导数来计算具有不定型的极限的方法。（实际是伯努利发现的qwq）

**结论**

当 $\displaystyle\lim_{x \to c}{f(x)}=\displaystyle\lim_{x \to c}{g(x)}=0$ 或 $\lim_{x \to c}{|f(x)|}=\lim_{x \to c}{|g(x)|}=\infty$ 其中一者成立，此时有
$$
\lim_{x \to c}\dfrac{f(x)}{g(x)}=\lim_{x\to c}\dfrac{f^{'}(x)}{g{'}(x)}
$$
如果式子不满足分数形式，也可以通过运算转为分数形式。
$$
\lim_{x \to c} f(x) = 0,\  \lim_{x \to c} g(x) = \infty\\
\lim_{x \to c} f(x)g(x) = \lim_{x \to c} \frac{f(x)}{1/g(x)} \ 或 \ \lim_{x \to c} \frac{g(x)}{1/f(x)}
$$

$$
\lim_{x \to c} f(x) = \infty,\  \lim_{x \to c} g(x) = \infty\\ \lim_{x \to c} (f(x) - g(x)) = \lim_{x \to c} \frac{1/g(x) - 1/f(x)}{1/(f(x)g(x))} \!
$$



### 根与系数的关系/韦达定理

**结论**


$$
\begin{cases} x_1 + x_2 + \dots + x_{n-1} + x_n = -\dfrac{a_{n-1}}{a_{n}} \\ 
(x_1 x_2 + x_1 x_3+\cdots + x_1 x_n) + (x_2x_3 + x_2x_4+\cdots + x_2x_n)+\cdots + x_{n-1}x_n = \dfrac{a_{n-2}}{a_{n}} \\
{} \quad \vdots \\ x_1 x_2 \dots x_n = (-1)^n \dfrac{a_0}{a_n}\end{cases}
$$
**证明**

利用乘法原理，容易证明。

对于 $a_nx^n  + a_{n-1}x^{n-1} +\cdots + a_1 x+ a_0 = a_n(x-x_1)(x-x_2)\cdots (x-x_n)$，我们展开右式比对系数，即可得到结论。

**推论**

这里提供最为常用的两个情况。

当 $n=2$ 时，对于 $ax^2+bx+c =0$，有 $x_1+x_2=-\dfrac{b}{a},\quad x_1x_2=\dfrac{c}{a}$

当 $n=3$ 时，对于 $ax^3 + bx^2 + cx + d=0$，有 $x_1+x_2+x_3=-\dfrac{b}{a}, \quad x_1x_2x_3=-\dfrac{d}{a}$​

P.S. 当且仅当 $\Delta \geq 0$ 时（根的判别式），方程才有实数根，但**无论方程有无实数根**，实系数一元二次方程的根与系数之间适合韦达定理。在解题时多加注意。

**韦达定理的逆定理**

给定一个**一元二次**多项式 ，如果有两个数 $x_1,x_2$，满足 $x_1+x_2=-\dfrac{b}{a}$ 和 $x_{1}x_{2}={\dfrac{c}{a}}$，则 $x_1,x_2$就是多项式 $ax^2+bx+c$ 的两根。



## 平面几何

### 极化恒等式

**结论**

对于两个向量 $x,\;y$，有 $x\cdot y=\dfrac{1}{4}((x+y)^2-(x-y)^2)$​

**证明**
$$
\begin{aligned}
(x+y)^2 &= x^2 + y^2 + 2x \cdot y \\
(x-y)^2 &= x^2 + y^2 - 2x \cdot y
\end{aligned}
$$
两式相减，得
$$
x \cdot y = \frac{1}{4} ((x+y)^2 - (x-y)^2)
$$
**推论**

平行四边形
$$
\overrightarrow{AD} \cdot \overrightarrow{AB} = \frac{1}{4} \left( |\overrightarrow{AC}|^2 - |\overrightarrow{BD}|^2 \right)
$$
<img src="https://s2.loli.net/2025/04/04/YnZFRqBlrAgULWK.png" alt="极化恒等式" style="zoom: 40%;"/>

三角形
$$
\overrightarrow{AB} \cdot \overrightarrow{AC} = |\overrightarrow{AD}|^2 - |\overrightarrow{DB}|^2 = |\overrightarrow{AD}|^2 - \frac{1}{4} |\overrightarrow{BC}|^2
$$
<img src="https://s2.loli.net/2025/04/04/dn3U7VwXx5zfA8T.png" alt="Screenshot 2024-12-08 084642.png" style="zoom: 40%;" />



### 奔驰定理

**结论**

对于 $\triangle ABC$ 内一点 $P$，记 $S_A=S_{\triangle PBC}, S_B=S_{\triangle PAC},S_C=S_{\triangle PAB}$，则 $S_A\cdot \overrightarrow{PA} + S_B\cdot \overrightarrow{PB}+S_C\cdot\overrightarrow{PC}=\overrightarrow{0}$​

**证明**

考虑将向量 $\overrightarrow{AP}$ 分解，延长 $AP$ 交 $BC$ 于 $Q$ 。

<img src="https://s2.loli.net/2025/05/10/FnflevUa1YrPTjp.png" style="zoom:80%;" />

容易得到 $\overrightarrow{AP}=\dfrac{S_B+S_C}{S_{△ABC}}\cdot\overrightarrow{AQ}$ ，且$\overrightarrow{AQ}=\dfrac{S_B}{S_B+S_C}\cdot\overrightarrow{AB}+\dfrac{S_C}{S_B+S_C}\cdot\overrightarrow{AC}$

代入化简得 $\overrightarrow{AP}=\dfrac{S_B}{S_{△ABC}}\cdot\overrightarrow{AB}+\dfrac{S_C}{S_{△ABC}}\cdot\overrightarrow{AC}$

同理 $\overrightarrow{BP}=\dfrac{S_A}{S_{△ABC}}\cdot\overrightarrow{BA}+\dfrac{S_C}{S_{△ABC}}\cdot\overrightarrow{BC}$

$\overrightarrow{CP}=\dfrac{S_A}{S_{△ABC}}\cdot\overrightarrow{CA}+\dfrac{S_B}{S_{△ABC}}\cdot\overrightarrow{CB}$

所以 $S_A\cdot\overrightarrow{AP}+S_B\cdot\overrightarrow{BP}+S_C\cdot\overrightarrow{CP}$

$=\dfrac{S_AS_B}{S_{△ABC}}\cdot(\overrightarrow{AB}+\overrightarrow{BA})+\dfrac{S_BS_C}{S_{△ABC}}\cdot(\overrightarrow{BC}+\overrightarrow{CB})+\dfrac{S_CS_A}{S_{△ABC}}\cdot(\overrightarrow{CA}+\overrightarrow{AC})$

$=\overrightarrow{0}+\overrightarrow{0}+\overrightarrow{0}=\overrightarrow{0}$ ，结论得证。

**推论**

三角形的重心（三条中线的交点）

<img src="https://s2.loli.net/2025/05/10/GVnEX9TKv1meyFU.png" style="zoom:80%;" />

设重心为 $G$，容易得到 $S_A=S_B=S_C=\frac{1}{3}S_{△ABC}$

那么 $\overrightarrow{GA}+\overrightarrow{GB}+\overrightarrow{GC}=\overrightarrow{0}$​​ 



三角形的外心（外接圆圆心）

<img src="https://s2.loli.net/2025/05/10/wiUEvnzoBrbQjMk.png" style="zoom: 80%;" />

设外心为 $O$，由圆的性质可得 $\angle BOC=2\angle A$ ， $OA=OB=OC$

由面积公式$S_A=\frac{1}{2}OB\cdot OC\cdot sin2A$​ 得

$S_A:S_B:S_C=sin2A:sin2B:sin2C$

所以 $sin2A\cdot\overrightarrow{OA}+sin2B\cdot\overrightarrow{OB}+sin2C\cdot\overrightarrow{OC}=\overrightarrow{0}$​



三角形的内心（三条角平分线交点）

<img src="https://s2.loli.net/2025/05/10/yDLoxlIN5OFGBqa.png" style="zoom:80%;" />

当点 $P$是三角形的内心 $I$ 时，由圆的性质可得 $ID=IE=IF$

由面积公式 $S_A=\frac{1}{2}ID\cdot a$ 得

$S_A:S_B:S_C=a:b:c$

所以 $a\cdot\overrightarrow{IA}+b\cdot\overrightarrow{IB}+c\cdot\overrightarrow{IC}=\overrightarrow{0}$

注：由正弦定理可知 $a:b:c=sinA:sinB:sinC$

所以也可以写成 $sinA\cdot\overrightarrow{IA}+sinB\cdot\overrightarrow{IB}+sinC\cdot\overrightarrow{IC}=\overrightarrow{0}$​



### 常用三角恒等式

**诱导公式**

可用如下口诀将联系记忆起来：“奇变偶不变，符号看象限”。意思为，当k为奇数时，sin变为cos，cos变为sin，tan变为cot，cot变为tan，sec变为csc，csc变为sec；而k为偶数时，三角函数则不变换。对于正负号，则要看最后角所在的象限进行判断，可以使用如下口诀：**ASTC** (All Students Take Calculus) 用来记忆。

- 第一象限的 A 即是 All（全部皆正）。
- 第二象限的 S 即是 **Sin**e & Co**S**ecant（正弦以及余割为正）。
- 第三象限的 T 即是 **Tan**gent & **Cot**angent（正切以及余切为正）。
- 第四象限的 C 即是 **Cos**ine & Se**C**ant（余弦以及正割为正）。

$$
\sin\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z} \\
\cos\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z} \\
\tan\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z} \\
\cot\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z} \\
\sec\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z} \\
\csc\left(\frac{k\pi}{2}\pm\alpha\right),k\in\mathbb{Z}
$$

**毕达哥拉斯三角恒等式**
$$
\sin^2\theta + \cos^2\theta = 1
$$

**角的和差恒等式**
$$
\sin(\alpha \pm \beta) = \sin \alpha \cos \beta \pm \cos \alpha \sin \beta \\
\cos(\alpha \pm \beta) = \cos \alpha \cos \beta \mp \sin \alpha \sin \beta \\
\tan(\alpha \pm \beta) = \frac{\tan \alpha \pm \tan \beta}{1 \mp \tan \alpha \tan \beta}
$$

**二倍角公式**
$$
\begin{aligned}
\sin 2\theta &= 2 \sin \theta \cos \theta \ \\ &= \frac{2 \tan \theta} {1 + \tan^2 \theta}\\[1em]
\cos 2\theta &= \cos^2 \theta - \sin^2 \theta \\ &= 2 \cos^2 \theta - 1 \\ 
&= 1 - 2 \sin^2 \theta \\ &= \frac{1 - \tan^2 \theta} {1 + \tan^2 \theta}\\[1em]
\tan 2\theta &= \frac{2 \tan \theta} {1 - \tan^2 \theta} \ \\ &= \frac{1}{1-\tan\theta}-\frac{1}{1+\tan\theta}
\end{aligned}
$$
**降次公式**
$$
\begin{aligned}
\sin^2\theta &= \frac{1-\cos 2\theta}{2}\\
\tan^2\theta &= \frac{1-\cos 2\theta}{1+\cos 2\theta}\\
\cos^2\theta &= \frac{1+\cos 2\theta}{2}
\end{aligned}
$$
**半角公式**
$$
\begin{aligned}
\sin\frac{\theta}{2} &= \pm \sqrt{\frac{1 - \cos\theta}{2}} \\[1em]
\cos\frac{\theta}{2} &= \pm \sqrt{\frac{1 + \cos\theta}{2}} \\[1em]
\tan \frac{\theta}{2}
&= \frac{1 - \cos \theta}{\sin \theta}\\
&= \frac{\sin \theta}{1 + \cos \theta}\\
&= \pm \sqrt\frac{1 - \cos \theta}{1 + \cos \theta}
\end{aligned}
$$

**其他恒等式**

> 除了第一个等式，其他的几乎用不到（

当 $\alpha + \beta +  \gamma = \pi$ 时成立
特别地，第一个等式对于 $\alpha + \beta +  \gamma = n\pi$ 也成立
$$
\begin{aligned}\tan \alpha + \tan \beta + \tan \gamma &= \tan \alpha \tan \beta \tan \gamma\\
   \sin \alpha + \sin \beta + \sin \gamma &= 4\cos\left(\frac{\alpha}{2}\right)\cos\left(\frac{\beta}{2}\right)\cos\left(\frac{\gamma}{2}\right) \\
   \cos \alpha + \cos \beta + \cos \gamma &= 4\sin\left(\frac{\alpha}{2}\right)\sin\left(\frac{\beta}{2}\right)\sin \left(\frac{\gamma}{2}\right) + 1 
\end{aligned}
$$



### 中线长定理/对角线定理

**结论**

已知有 $\triangle ABC$，边 $AC$ 的中点为 $D$， 存在 $AB^2+AC^2=2(AD^2+BD^2)$

**证明**
$$
\angle ADB + \angle ADC = 180^\circ\\
\cos \angle ADB = -\cos \angle ADC\\
\frac{AD^2+BD^2-AB^2}{2AD \cdot BD} = -\frac{AD^2+CD^2-AC^2}{2AD \cdot CD}\\
AB^2+AC^2=2(AD^2+BD^2) \iff (2AD)^2+BC^2=2AB^2+2AC^2
$$



### 垂径定理

**结论**

垂直于弦的直径平分弦且平分这条弦所对的两条弧。

**应用**

在涉及圆的题目中，这个定理出现频率极高。

可以利用垂径定理将弧长转换为半径和圆心到直线距离，便于进一步处理。



### 参数方程

有时，利用参数方程把两个变量x，y间接地联系起来，会使计算更加容易。

例如，对于圆和椭圆的参数方程，我们只需用一个变量即可表示$x,\;y$

$\text{圆:}
\begin{cases}
x=r\cos t \\
y=r\sin t & & 
\end{cases} $

$\text{椭圆:}
\begin{cases}
x=a\cos t \\
y=b\sin t & & 
\end{cases} $​

对于直线，我们令 $t$ 为直线上动点 $A$ 到定点 $M(x_0, y_0)$ 的距离

那么，经过点 $ M $，与 $x$轴夹角为 $\alpha$ 的直线可以表示为$\begin{cases} x=x_0+t\cos \alpha \\ y=y_0+t\sin \alpha && \end{cases} $



### 角平分线定理

**结论**

<img src="https://s2.loli.net/2025/04/04/MpwdG5vbfrRUzPt.png" style="zoom: 40%;" />

**证明**

证内角平分线定理：

在 $\triangle ABC$ 中，在 $BC$ 边上任取一点 $D$。过点 $C$ 做 $AD$ 的平行线，与 $BA$ 的延长线相交于点 $E$。
$$
\angle BAD = \angle AEC \\
\angle CAD = \angle ACE \\
\triangle DBA \sim \triangle CBE \; \Rightarrow \; {DB \over DC}={AB \over AE} \\
\angle BAD = \angle CAD \; \Rightarrow \; \angle AEC = \angle ACE \; \Rightarrow \; \triangle ACE为等腰三角形\\
\; \Rightarrow \; AC=AE \; \Rightarrow \; {DB \over DC} = {AB \over AE} = {AB \over AC} \\
$$
<img src="https://s2.loli.net/2025/04/04/NwhxynZaHW3R1Mr.png" style="zoom: 40%;" />

证外角平分线定理：

在 $\triangle ABC$ 中，令 $AB > AC$。在 $BC$ 的延长线上取一点 $D$。过点 $C$ 做 $AD$ 的平行线，与 $BA$ 边相交于点 $E$。在 $BA$ 的延长线上任取一点 $F$。
$$
\angle FAD = \angle AEC \\
\angle CAD = \angle ACE \\
\triangle DBA \sim \triangle CBE\;\Rightarrow\;{DB \over DC}={AB \over AE} \\
$$
易证得，三角形外角平分线与对边直线的交点，必定落在较短的邻边的一侧。
$$
\angle FAD = \angle CAD\;\Rightarrow \;\angle AEC = \angle ACE\;\Rightarrow \;\triangle ACE 为等腰三角形
\\
\;\Rightarrow \;AC = AE\;\Rightarrow \;{DB \over DC} = {AB \over AE} = {AB \over AC}
$$
<img src="https://s2.loli.net/2025/04/04/zpHAsvbDfXhtWF9.png" style="zoom: 40%;" />

**推论**

证内角平分线逆定理：

$ AC=\dfrac{AB\cdot DC}{DB}=AE\;\Rightarrow\;\triangle ACE\text{ 为等腰三角形}\;\Rightarrow\;\angle AEC=\angle ACE\;\Rightarrow\;\angle BAD=\angle CAD $

证外角平分线逆定理：

易证得，三角形一边所在直线上符合要求的点，必定落在较短的邻边的一侧。

$AC=\dfrac{AB\cdot DC}{DB}=AE\;\Rightarrow\;\triangle ACE\text{ 为等腰三角形}\;\Rightarrow\;\angle AEC=\angle ACE\;\Rightarrow\;\angle FAD=\angle CAD$

**应用**

求 $\angle ABC$ 的角平分线所在直线：

设角平分线和 $AC$ 交于 $D$，那么有 $\dfrac{|AD|}{|CD|}=\dfrac{|AB|}{|CB|}=\dfrac{\lambda_1}{\lambda_2}$

根据 $\lambda_2\overrightarrow{AD}=\lambda_1\overrightarrow{DC}$，求出 $D$ 点坐标

再将 $A, D$ 的坐标代入两点式，求解出方程

也可利用角平分线上任意一点到 $l_{AB}, l_{BC}$ 距离相等求解



### 隐形圆（矩形）

**结论**

已知矩形 $ABCD$ 和任意一点 $O$，存在 $|OA|^2+|OC|^2=|OB|^2+|OD|^2$ 

**证明**

设  $ O(x_0, y_0)，A(x_1, y_1)，B(x_2, y_1)，C(x_2, y_2)，D(x_1, y_2)$

那么有 $|OA|^2=(x_0-x_1)^2+(y_0-y_1)^2$，$|OC|^2，|OB|^2，|OD|^2$ 同理可得

相加并整理，左边=右边，故上述结论正确

<img src="https://s2.loli.net/2025/04/04/HZvBU6jMOEeGVbR.jpg" style="zoom: 50%;" />



### 椭圆的焦点三角形

**结论**

已知椭圆 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1(a>b>0)$，其焦点分别为 $F_1$ 和 $F_2$，任取椭圆上一点 $P$，满足 $S_{\triangle PF_1F_2} = \displaystyle b^2tan{\theta \over 2} = b^2 \dfrac{\sin\theta}{\cos\theta+1}$​

$C_{\triangle PF_1F_2}=2a+2c$

**证明**
$$
令 r_1=|PF_1|，r_2=|PF_2|，\theta=\angle F_1PF_2 \\[1ex]
\begin{cases}
r_1+r_2=2a \\[1ex]
\cos\theta=\frac{r_1^2+r_2^2-4c^2}{2r_1r_2}
\end{cases}
\; \Rightarrow \; r_1r_2=\frac{2b^2}{\cos\theta+1} \\
S={1 \over 2}r_1r_2\sin\theta = b^2tan{\theta \over 2} = b^2 \frac{\sin\theta}{\cos\theta+1} \\
C=r_1+r_2+|F_1F_2|=2a+2c
$$
<img src="https://s2.loli.net/2025/04/04/1cOmpT7HzUlCBfA.png" style="zoom: 60%;" />



### 点差法

**结论**

已知椭圆 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1(a>b>0)$，直线 $l$ 与椭圆相交于 $A,B$ 两点，存在 $k_{OM}k_{AB}=-\dfrac{b^2}{a^2}$​

**证明**

设 $A(x_1, y_1), B(x_2, y_2)$，代入椭圆方程得
$$
\begin{cases}
\dfrac{x_1^2}{a^2}+\dfrac{y_1^2}{b^2}=1 \\[1ex]
\dfrac{x_2^2}{a^2}+\dfrac{y_2^2}{b^2}=1
\end{cases}
$$
两式相减得
$$
\dfrac{x_1^2-x_2^2}{a^2}+\dfrac{y_1^2-y_2^2}{b^2}=0\Rightarrow\dfrac{(y_1-y_2)(y_1+y_2)}{(x_1-x_2)(x_1+x_2)}=-\dfrac{b^2}{a^2}
$$
因为 $M$ 是 $AB$ 的中点，所以
$$
k_{OM}=\dfrac{\dfrac{y_1+y_2}{2}-0}{\dfrac{x_1+x_2}{2}-0}=\dfrac{y_1+y_2}{x_1+x_2} \\
k_{OM}k_{AB}=-\dfrac{b^2}{a^2}
$$
<img src="https://s2.loli.net/2025/04/04/8X9V37kOGzoFY2d.png" style="zoom: 140%;" />

**推论**

做 $A$ 点关于原点的对称点 $A'$，由三角形中位线定理可得 $k_{BA}k_{BA^{'}}=-\dfrac{b^2}{a^2}$（注意此处的 $AA^{'}$ 需过坐标原点）

<img src="https://s2.loli.net/2025/04/04/CjRPZH8K9vrdTyV.png" style="zoom: 140%;" />



### 点到焦点距离（参数形式）

**结论**

已知椭圆 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1(a>b>0)$，其焦点分别为 $F_1$ 和 $F_2$，椭圆上任意一点 $P(x_0, y_0)$，满足 $|PF_1|=a+ex_0,\;|PF_2|=a-ex_0$，其中 $e$ 表示椭圆的离心率

类似地，对于双曲线 $\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}=1(a>0,b>0)$，有 $|PF_1|=|a+ex_0|,\;|PF_2|=|a-ex_0|$

**证明**
$$
\begin{aligned}
\left|P F_1\right| & =\sqrt{\left(x_0+c\right)^2+y_0^2} \\
& =\sqrt{x_0^2+2 c x_0+c^2+b^2\left(1-\frac{x_0^2}{a^2}\right)} \\
& =\sqrt{\left(1-\frac{b^2}{a^2}\right) x_0^2+2 c x_0+b^2+c^2} \\
& =\sqrt{\frac{c^2}{a^2} x_0^2+2 c x_0+a^2} \\
& =a+e x_0
\end{aligned}
$$



### 点到焦点距离（三角函数形式）

**结论**

已知椭圆 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1(a>b>0)$，其焦点分别为 $F_1$ 和 $F_2$，椭圆上任意一点 $P$，满足 $|PF_1|=\dfrac{b^2}{a-sgn(y_{P}) \cdot c\cos\alpha} $​

类似地，在双曲线中，有$|PF_1|=\dfrac{b^2}{a+sgn(y_{P}) \cdot c\cos\alpha}$

**证明**

由余弦定理，有 $ m^2+(2c)^2 - (2a-m)^2 = 2 \cdot 2c \cdot m \cos \alpha $，整理得 $m=\dfrac{b^2}{a - c\cos\alpha}$，可求得 $|PF_1|,\;|PF_2|$，在双曲线中同理

**推论**

$|AB|=|AF_1|+|BF_1|=\dfrac{2ab^2}{a^2-c^2\cos^2\alpha}$

<img src="https://s2.loli.net/2025/04/04/e8pjwEq5mHY1Jva.png" style="zoom: 100%;" />



### 基于对勾函数的范围问题

**结论**

在题目中，经常会出现 $\dfrac{x_1}{x_2}=A$ 或 $\dfrac{y_1}{y_2}=A$ 的条件（$A$ 为定值），想要利用韦达定理，可以转换成 $\dfrac{x_1}{x_2}+\dfrac{x_2}{x_1}=A+\dfrac{1}{A}$ 或 $\dfrac{y_1}{y_2}+\dfrac{y_2}{y_1}=A+\dfrac{1}{A}$，再根据对勾函数的图像列出不等式。

**例子**

已知椭圆 $\Gamma: \dfrac{x^2}{4}+y^2=1$ 的左右顶点分别为 $A$，$B$，过点 $D(-1, 0)$ 的直线 $l$ 交 $\Gamma$ 于 $M$，$N$ 两点（$M$ 在 $x$ 轴上方），记 $\triangle AND$ 的面积为 $S_1$，$\triangle BMD$ 的面积为 $S_2$，求 $\dfrac{S_1}{S_2}$ 的取值范围

解 ： 由题，设 $N(x_1, y_1)$，$M(x_2,y_2)$，那么 $\dfrac{S_1}{S_2}=\dfrac{-y_1}{3y_2}$

设 $l：y=k(x+1), k\neq0$，与 $\Gamma$ 联立，有 $(4k^2+1)x^2+8k^2x+4k^2-4=0$

$\Longrightarrow\;$ $x_1+x_2=-\dfrac{8k^2}{4k^2+1},\; x_1x_2=\dfrac{4k^2-4}{4k^2+1}$

$\Longrightarrow\;$ $\dfrac{y_1}{y_2}+\dfrac{y_2}{y_1}=\dfrac{k^2(x_1+1)^2+k^2(x_2+1)^2}{k^2(x_1+1)(x_2+1)}\in[-\dfrac{3}{10},-2)$，当斜率不存在时取到 $-\dfrac{3}{10}$

$\Longrightarrow\;$ $\dfrac{y_1}{y_2}\in(-\dfrac{1}{3},-3)$ $\;\Rightarrow\;$ $\dfrac{S_1}{S_2} \in (\dfrac{1}{9}, 1)$​



### 齐次化

### 极点极线

## 数列

### 常用数列求和公式

> 有时在导数大题需要把数列的求和形式（$S_n$）拆成多项，然后再将 $a_n$ 做差比较大小
>
> 例子：
> $$
> n \in \N^+，证明 \ln^22+\ln^2\frac{2}{3}+\cdots+\ln^2\frac{n+1}{n}<\frac{n}{n+1}
> $$

1. 

$$
a_n=\frac{1}{n(n+1)}=\frac{1}{n}-\frac{1}{n+1}\\
S_n=1-\frac{1}{n+1}=\frac{n}{n+1}
$$

2. 


$$
a_n=\ln\dfrac{n}{n+1}\\
S_n=\ln(\frac{1}{2}\cdot \frac{2}{3} \cdots \frac{n}{n+1})=\ln\dfrac{1}{n+1}
$$



### 不动点

> 对于求解分式形式的递推式，此方法较为有效。

**结论**

将递推式中的 $a_n,a_{n+1}$ 替换为 $x$ 并求解，分为三种情况。

**第一种情况**——仅存在一解 $x_0$

此时我们将等式两边同时减去 $x_0$，取倒数并化简，得到 $\{\dfrac{1}{a_n-x_0}\}$
，不难发现，$\{\dfrac{1}{a_n-x_0}\}$ 为 $A.P.$

**第二种情况**——存在两解 $x_1,\;x_2$

将等式两边分别同时减去 $x_1,\;x_2$，得到两个等式，两式相除并化简，得到 $\{\dfrac{a_n-x_1}{a_n-x_2}\}$
，同样不难发现，$\{\dfrac{a_n-x_1}{a_n-x_2}\}$ 为 $G.P.$

**第三种情况**——在实数域内无解

此时，该数列**大多**为周期数列。
我们可以仿照上述方式，求得数列通项，在此不多作介绍。

**证明**

在高考范围内，不需要了解，此处贴个[链接](https://www.cnblogs.com/ResurgamLiBoyi/p/16619819.html)。



### 数列放缩



## 立体几何

### 空间中距离、角度的计算



### 仿射坐标系



## 组合数学

### 错位排列数

**简介**

错位排列（derangement）是没有任何元素出现在其有序位置的排列。即，对于 $1\sim n$ 的排列 $P$，如果满足 $P_i\neq i$，则称 $P$ 是 $n$ 的错位排列。

**结论**
$$
D_n=(n-1)(D_{n-1}+D_{n-2})
$$

$$
D_n=nD_{n-1}+{(-1)}^n
$$

$$
D_n=\begin{cases}
    \left\lceil\frac{n!}{\mathrm{e}}\right\rceil, & \text{if }n\text{ is even}, \\
    \left\lfloor\frac{n!}{\mathrm{e}}\right\rfloor,            & \text{if }n\text{ is odd}.
\end{cases}
$$

**证明**

此处提供对于第一个递推关系的证明。

假设考虑到第 $n$ 个信封，初始时暂时把第 $n$ 封信放在第 $n$ 个信封中，然后考虑两种情况的递推：

-   前面 $n-1$ 个信封全部装错；
-   前面 $n-1$ 个信封有一个没有装错其余全部装错。

对于第一种情况，前面 $n-1$ 个信封全部装错：因为前面 $n-1$ 个已经全部装错了，所以第 $n$ 封只需要与前面任一一个位置交换即可，总共有 $D_{n-1}\times (n-1)$ 种情况。

对于第二种情况，前面 $n-1$ 个信封有一个没有装错其余全部装错：考虑这种情况的目的在于，若 $n-1$ 个信封中如果有一个没装错，那么把那个没装错的与 $n$ 交换，即可得到一个全错位排列情况，没装错的有 $n-1$ 种情况，所以此处总共有 $D_{n-2}\times (n-1)$ 种情况。

其他情况，不可能通过一次操作来把它变成一个长度为 $n$ 的错排。

于是可得，错位排列数满足递推关系：

$$
D_n=(n-1)(D_{n-1}+D_{n-2})
$$



### 鹊巢原理/抽屉原理





## 概率论



## 杂项

> Warning：以下的Trick仅在部分模拟题中出现（T8联考），不属于课内知识。**不建议**任何高中生在未掌握之前的Trick前，就钻研本章节内容。
>
> P.S. 其实大概率不会再考了（

### ~~数论入门~~

感兴趣的话，请自行查看[OI Wiki](https://oi-wiki.org/math/number-theory/basic/)上的相关内容



### 琼斯多项式

**简介**

在数学的纽结理论中，琼斯多项式是沃恩·琼斯在1984年发现的纽结多项式。是用于判定两个扭结是否相等的一个有力工具。

**结论**
$$
V(平凡结)=1\\
t^{-1}V(L_+)-tV(L_-)=(t^{1 \over 2}-t^{-{1 \over 2}})V(L_0)\\
V(L \cup O)=-(t^{1 \over 2}+t^{-{1 \over 2}})V(L)
$$
<img src="https://s2.loli.net/2025/04/04/HYAKJ28TkdcStGI.png" style="zoom: 40%;" />

**应用**

利用第二条公式，我们可以递归计算出扭结的琼斯多项式。

此处以三叶结 $3_1$​​ 为例，

我们先指定一个方向，再对交叉点进行判定。
$$
t^{-1}V(O)-tV(3_1)=(t^{1\over2}-t^{-{1\over2}})V(K_1)\\
t^{-1}V(O\;O)-tV(K_1)=(t^{1\over2}-t^{-{1\over2}})V(O)\\
V(O\;O)=-(t^{1 \over 2}+t^{-{1 \over 2}})\\
V(K_1)=-t^{-2.5}-t^{-0.5}\\
V(3_1)=t^{-1}+t^{-3}-t^{-4}\\
$$
这里得到的是左手三叶结的琼斯多项式。

将 $t$ 换成 $t^{-1} $ 就可以得到 $V(3_1)=t^1+t^3-t^4$，这是右手三叶结的琼斯多项式

<img src="https://s2.loli.net/2025/04/04/n2Y3IgUdZDi6NAw.png" style="zoom: 80%;" />



### 快速计算整数个数

> 充分发挥 OI 优良传统（？）

**结论**

对于 $a,b \in \Z$ ，我们有以下计算技巧

|        形式         | 整数个数 |
| :-----------------: | :------: |
|      $[a, b]$       | $a-b+1$  |
| $[a,b)\quad (a, b]$ |  $a-b$   |
|       $(a,b)$       | $a-b-1$  |

若给定的 $a,b \notin Z$，则对应向上/向下取整到最近的整数，并表示为闭区间。

