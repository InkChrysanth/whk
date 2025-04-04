# Tricks in Math 数学中的二级结论

> Informatik verbindet dich und mich.
>
> 信息将你我连结
>
> Zeit und Raum trennen dich und mich.
>
> 时空将你我分开

## 初等函数

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

**几何级数**
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
\begin{aligned}
e^x&<\dfrac{2+x}{2-x} \quad \forall x<2\\
e^x&>\dfrac{2+x}{2-x} \quad \forall x>2
\end{aligned}
$$
**对数型**
$$
\begin{aligned}
\ln x&<\dfrac{2x-2}{1+x} \quad \forall x<1\\
\ln x&>\dfrac{2x-2}{1+x} \quad \forall x>1
\end{aligned}
$$

### 洛必达法则

**简介**

洛必达法则（L'Hôpital's rule）是利用导数来计算具有不定型的极限的方法。（实际是伯努利发现的qwq）

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



## 平面向量

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

平行四边形： 
$$
\overrightarrow{AD} \cdot \overrightarrow{AB} = \frac{1}{4} \left( |\overrightarrow{AC}|^2 - |\overrightarrow{BD}|^2 \right)
$$
<img src="https://s2.loli.net/2025/04/04/YnZFRqBlrAgULWK.png" alt="极化恒等式" style="zoom: 40%;"/>

三角形：
$$
\overrightarrow{AB} \cdot \overrightarrow{AC} = |\overrightarrow{AD}|^2 - |\overrightarrow{DB}|^2 = |\overrightarrow{AD}|^2 - \frac{1}{4} |\overrightarrow{BC}|^2
$$
<img src="https://s2.loli.net/2025/04/04/dn3U7VwXx5zfA8T.png" alt="Screenshot 2024-12-08 084642.png" style="zoom: 40%;" />

## 三角函数

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

> 除了第一个等式，其他几乎用不到（

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
AB^2+AC^2=2(AD^2+BD^2)
$$



## 平面几何

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
y=r\sin t 
\end{cases} $

$\text{椭圆:}
\begin{cases}
x=a\cos t \\
y=b\sin t 
\end{cases} $​

对于直线，我们令 $t$ 为直线上动点 $A$ 到定点 $M(x_0, y_0)$ 的距离

那么，经过点 $ M $，与 $x$轴夹角为 $\alpha$ 的直线可以表示为$ \begin{cases} x=x_0+t\cos \alpha \\ y=y_0+t\sin \alpha && \end{cases} $



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



### 隐形圆1

**结论**

已知矩形 $ABCD$ 和任意一点 $O$，存在 $|OA|^2+|OC|^2=|OB|^2+|OD|^2$ 

**证明**

设  $ O(x_0, y_0)，A(x_1, y_1)，B(x_2, y_1)，C(x_2, y_2)，D(x_1, y_2)$

那么有 $|OA|^2=(x_0-x_1)^2+(y_0-y_1)^2$，$|OC|^2，|OB|^2，|OD|^2$ 同理可得

相加并整理，有 $ LHS=RHS $，故上述结论正确

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
\cos\theta=\dfrac{r_1^2+r_2^2-4c^2}{2r_1r_2}
\end{cases}
\; \Rightarrow \; r_1r_2=\dfrac{2b^2}{\cos\theta+1} \\
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



### 点到焦点距离1

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

### 点到焦点距离2

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

$\Longrightarrow\;$ $\dfrac{y_1}{y_2}\in(-\dfrac{1}{3},-3)$ $\;\Rightarrow\;$ $\dfrac{S_1}{S_2} \in (\dfrac{1}{9}, 1)$

### 齐次化

### 极点极线

## 数列

### 不动点

> 对于求解分式形式的递推式，此方法更为有效。

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

## 杂项

> Warning：以下的Trick仅在部分模拟题中出现（T8联考），不属于课内知识。不建议任何高中生在未掌握之前的Trick前，就钻研本章节内容。
>
> PS：其实大概率不会再考了（

### 数论入门

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
