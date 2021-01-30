#  Macroeconomics



## 基本模型范式

1. 基础假定：典型如生产技术、效用偏好、市场结构、初值条件等
2. 参与者行为：典型是某种形式的最优化
3. 均衡
   1. 定义：关键变量以稳定路径变动 $\dfrac{\dot{x}}{x}$ 为常数
   2. 存在性：稳定点与收敛路径
   3. 稳定性：扰动偏离均衡后如何恢复稳定，往往是 tylor 展开；鞍点路径斜率、收敛速度也是 tylor 展开
4. 比较静态分析：稳态对讨论变量求偏导
5. 福利分析：社会计划者问题、福利经济学第一第二定律、举出改进反例
6. 外部干预：是否有帕累托改进，如何改进
7. 实证：检验与反馈



## 索罗模型 Solow Model

说明了实物资本积累在经济增长中的角色；几乎所有增长模型的衡量标杆

近代宏观从通论 (1936) 开始，凯恩斯强调有效需求管理，认为供给没问题。长期内我们都死了，只关注短期财政货币政策，熨平经济波动，让经济活动潜在产出水平，但没有考虑长期增长问题。后来的 IS-LM 模型也是细化了这一个方向。二战后，问题转向供给，索罗 (1956) 认为需求没问题，其模型假设了充分就业、劳动力供给垂直无弹性。光靠财政/货币政策不能在长期做大蛋糕，只有技术进步可以。所以要搞研发，供给侧改革



### 假定

#### 生产函数形式

设定为 $Y_t=F(K_t,A_t,L_t)$，目前只考虑单一产出

由于技术 $A_t$ 不可见，需要和其他东西就结合起来，有三种形式

##### 中性技术进步

当技术进步使得某个经济变量在一规定环境下保持不变时，它就被称为”中性“。

**希克斯中性**

如果技术进步使得边际技术替代率 $MRTS\equiv MP_L/MP_K=\dfrac{\partial Y}{\partial L}/\dfrac{\partial Y}{\partial K}$ 在同样的的 $K/L$ 比率下保持不变，那就成为希克斯中性。生产函数形式为
$$
Y_t=A_tF(K_t,L_t)
$$
**哈罗德中性**

如果技术进步使得资本比率 $Y/K$ 在同样的 $MP_K=\dfrac{\partial Y}{\partial K}$ 下保持不变，那就是哈罗德中性。生产函数形式为
$$
Y_t=F(K_t,A_tL_t)
$$
**索洛中性**

对应哈罗德中性，如果技术进步使得资本比率 $Y/L$ 在同样的 $MP_L=\dfrac{\partial Y}{\partial L}$ 下保持不变，那就是索洛中性。生产函数形式为
$$
Y_t=F(A_tK_t,L_t)
$$



这里的讨论基于劳动增强型的哈罗德中性，因为这样会使模型最终的资本产出比 $K/Y$ 稳定下来，符合长期历史观察的 **卡尔多典型事实**。

具体来说根据后面的推导，只要新古典生产函数形式确定，因为最终收敛到 $k*$，$MP_K=f'(k^*)$ 也就不变。$K=kAL$ 增长速度为 $g+n$，有效劳动 $AL$ 增长速度也是 $g+n$，根据规模报酬不变 $Y$ 的增长速度也是 $g+n$，从而有 $Y/K$ 不变



##### 规模报酬不变

$$
F(cK,cAL)=cF(K,AL)\qquad \forall c\geq0
$$

**注意这里一次齐次的参数只有 $K,L$ 没有 $A$** 

这里隐含了两点：

- 经济规模已足够大，已最大限度专业化分工。否则，加大投入应该可以通过进一步分工获得规模报酬递增的收益
- 除资本、技术和劳动外，其他投入要素（比如土地）不那么重要

由一次齐次性可以变形得到生产函数紧凑形式
$$
F(\frac{K}{AL},1)=\frac{1}{AL}F(K,AL)\\
定义有效劳均量y=\frac{Y}{AL},k=\frac{K}{AL}\\
即有\\
y=F(k,1)=f(k)
$$



##### 边际报酬递减

$$
\frac{\partial F}{\partial K}>0,\frac{\partial^2 F}{\partial K^2}<0\\
\frac{\partial F}{\partial L}>0,\frac{\partial^2 F}{\partial L^2}<0\\
由第一条 K 边际也就有\\
f'(k)>0,f''(k)<0
$$

再加一点初值条件 $f(0)=0$



##### 稻田条件 Inada Condition

$$
lim_{K\to0}\frac{\partial F}{\partial K}=+\infty, lim_{K\to+\infty}\frac{\partial F}{\partial K}=0\\
lim_{L\to0}\frac{\partial F}{\partial L}=+\infty, lim_{K\to+\infty}\frac{\partial F}{\partial L}=0\\
由第一条 K 偏导极限也就有\\
lim_{k\to0}f'(k)=+\infty, lim_{k\to+\infty}f'(k)=0
$$

稻田条件保证经济路径不发散



**新古典生产函数**

同时满足规模报酬不变、边际报酬递减、稻田条件三个条件的生产函数就可称为新古典生产函数。典型代表就是 Cobb-Douglas 生产函数，而且对 CD 形式而言劳动增强型、资本增强型或者希克斯中性都可以通过变形相互转换



#### 偏好

索罗模型没有管消费者偏好，只是假设收入 $\bar{Y}$ 按固定比例 $s$ 储蓄，剩余用于消费。注意这里还没有证明收入等于产出 $\bar{Y}=Y$
$$
\bar{Y}=C+S=(1-s)\bar{Y}+s\bar{Y}
$$



#### 市场结构

存在三个市场：产品市场、资本市场和劳动市场，均假定为完全竞争



#### 初值条件（禀赋）与增长率

知识，资本和劳动初始值给定为 $A_0,L_0,K_0 >0$

模型将时间视为连续便于处理，增长率固定为
$$
\frac{dln(A(t))}{dt}=\frac{1}{A(t)}\frac{dA(t)}{dt}=g\\
\frac{dln(L(t))}{dt}=\frac{1}{L(t)}\frac{dL(t)}{dt}=n
$$
也就是按指数增长
$$
A(t)=A(0)e^{nt}\\
L(t)=L(0)e^{gt}
$$

这里暗含了劳动力一出生就直接开始工作参与生产



### 参与者行为

#### 厂商利润最大化

$$
\mathop{max}_{L,K}\ PY-wL-rK
$$

因为模型中暂时还没有货币，所以需要一个一般等价物，就选最终产出 $Y$。其价格 $P$ 也就标准化为 1，从而 $w,r$ 的含义也变为实际（或者说相对）价格
$$
\mathop{max}_{L,K}\ Y-wL-rK
$$
一阶条件
$$
w=\frac{\partial F}{\partial L}\\
r=\frac{\partial F}{\partial K}
$$
这里可以证明收入 $\bar{Y}$ 等于产出 $Y$，因为收入 $\bar{Y}=wL+rK$，又因 $F$ 一次齐次规模收益不变，从而由欧拉法则有 $F=\dfrac{\partial F}{\partial L}L+\dfrac{\partial F}{\partial K}K$，即可得 $\bar{Y}=Y$



下面考虑紧凑形式，最大化目标函数除以 $AL$，即可得到
$$
\mathop{max}_{k}\ y-\frac{w}{A}-rk
$$
一阶条件
$$
r=f'(k)
$$



#### 消费者

总投资=总储蓄。而且假设用于投资的每单位产出可以获得一单位的新资本，而现有资本则按照折旧率 $\delta$ 进行折旧
$$
S=s\bar{Y}\equiv I=\frac{dK}{dt}+\delta K
$$



### 均衡

#### 定义

每一时期 $t$ 中满足以下全部条件的一组价格对应一组量，包括 $P_t^*$ 和 $Q_t^*$； $r_t^*$ 和 $k_t^*$；  $w_t^*$ 和 $L_t^*$

- 参与者目标最优化：
  - 消费者效用最大化：在需求曲线上
  - 厂商利润最大化：在供给曲线上
- 满足给定约束
- 市场出清



#### 存在性

联立资本积累方程和收入等于产出
$$
\frac{dK}{dt}=s\bar{Y}-\delta K\\
\bar{Y}=Y\\
\Rightarrow\frac{dK}{dt}=sY-\delta K\\
$$
关注有效劳均资本（由于经济总量会随时间不断增长）
$$
k=\frac{K}{AL}\\
lnk=lnK-ln(AL)\\
\text{两边对 t 求导}\\
\frac{1}{k}\frac{dk}{dt}=\frac{1}{K}\frac{dK}{dt}-\frac{1}{A}\frac{dA}{dt}-\frac{1}{L}\frac{dL}{dt}\\
\frac{1}{k}\frac{dk}{dt}=\frac{1}{K}(sY-\delta K)-g-n\\
\frac{dk}{dt}=sf(k)-(\delta+g+n)k
$$
~~此微分方程不一定有解析解，但应该都能求数值解~~

**稳态时，模型中所有变量都以稳定速率增长**

上式变形为
$$
\frac{1}{k}\frac{dk}{dt}=s\frac{f(k)}{k}-(\delta+g+n)
$$
$k$ 增长率为常数当且仅当右侧 $f(k)/k$ 为常数，也就是要求
$$
\frac{\partial [f(k)/k]}{\partial t}=0\\
\Leftrightarrow \frac{\dfrac{\partial f(k)}{\partial k}\dfrac{\partial k}{\partial t}k-\dfrac{\partial k}{\partial t}f(k)}{k^2}=0\\
\Leftrightarrow \frac{\partial k}{\partial t}\frac{\dfrac{\partial f(k)}{\partial k}k-f(k)}{k^2}=0
$$
但由利润最大化一阶条件可知
$$
\frac{w}{A}=f(k)-\frac{\partial f(k)}{\partial k}k\neq0
$$
所以只能要求
$$
\frac{\partial k}{\partial t}=0
$$
也就是说，**要求 $k$ 以稳定速率增长就只能要求 $k$ 完全不变**

回到上面原来的等式
$$
\frac{dk}{dt}=sf(k)-(\delta+g+n)k=0\\
\Leftrightarrow sf(k^*)=(\delta+g+n)k^*
$$
令 $L(k)=sf(k)-(\delta+g+n)k$，考察其零点情况
$$
L'(k)=sf'(k)-(\delta+g+n)\\
L''(k)=sf''(k)
$$
而由边际报酬递减假设和稻田条件可知 $f'(k)>0,f''(k)<0,lim_{k\to0}f'(k)=+\infty,lim_{k\to+\infty}f'(k)=0$

从而可知
$$
L''(k)<0\Rightarrow L'(k) 单调递减\\
lim_{k\to0}L'(k)=+\infty, lim_{k\to+\infty}L'(k)<0\\
$$
介值定理可知 $L'(k)$ 在 $(0,+\infty)$ 至少有一个零点，并且单调，所以有且只有一个零点。进而 $L(k)$ 在 $[0,+\infty)$ 先增后减，而 $L(0)=0$，从而 $\exists k>0$，使得 $L(k)>0$
$$
\begin{align}
lim_{k\to+\infty}L(k)&=lim_{k\to+\infty}k[s\frac{f(k)}{k}-(\delta+g+n)]\\
洛必达法则（可能有问题）&=lim_{k\to+\infty}k[sf'(k)-(\delta+g+n)]\\
&<0
\end{align}
$$
同样由连续函数介值定理和单调性，可知 $L(k)$ 在 $(0,+\infty)$ 有且只有一个零点 $k^*$



从而得出 $k^*=G(n,g,\delta,s)$ 有效劳均资本作为各参数的函数， $y^*=f(k^*),c^*=(1-s)y^*$

索罗模型的核心结论：资本积累不能带来长期增长，技术进步才是劳均资本长期增长的源泉



#### 稳定性

对有效劳均资本积累方程 $\dfrac{dk}{dt}=sf(k)-(n+g+\delta)k$ 在 $k^*$ 处做一阶 Tylor 展开
$$
\begin{align}
\dfrac{dk}{dt}&\approx0+[sf'(k^*)-(n+g+\delta)](k-k^*)\\
其中[sf'(k^*)-(n+g+\delta)]&=[\dfrac{(n+g+\delta)k^*f'(k^*)}{f(k^*)}-(n+g+\delta)]\\
&=(n+g+\delta)[\dfrac{k^*f'(k^*)}{f(k^*)}-1]\\
&=(n+g+\delta)(\alpha_k(k^*)-1)\\
&<0
\end{align}
$$
其中，由 $sf(k^*)-(n+g+\delta)k^*=0$ 替换 $s$，$\dfrac{k^*f'(k^*)}{f(k^*)}$ 为有效劳均资本分得报酬占有效劳均产出的比例，自然小于 1，记为 $\alpha_k(k^*)$

同时 $(n+g+\delta)(1-\alpha_k(k^*))$ 也就是收敛速度（这里说的“速度”是个正数，**注意负号！！**），每期 $k$ 向 $k^*$ 收敛这么多

也就是 $k(t)-k^*=exp[(n+g+\delta)(\alpha_k(k^*)-1))t] (k(0)-k^*)$

### 比较静态分析

$$
sf(k^*)=(\delta+g+n)k^*\\
两边对 s 求导\\
sf'(k^*)\frac{\partial k^*}{\partial s}+f(k^*)=(\delta+g+n)\frac{\partial k^*}{\partial s}\\
\frac{\partial k^*}{\partial s}=\frac{f(k^*)}{\delta+g+n-sf'(k^*)}
$$

由边际报酬递减假设和稻田条件（见上述关于 $L(k)$ 的零点讨论）可知分母部分当 $k=k^*$ 时大于零（这里替换 $\delta+g+n=\dfrac{sf(k^*)}{k^*}$ 比较方便），故 $\dfrac{\partial k^*}{\partial s}>0$

类似地
$$
两边对 n 求导\\
sf'(k^*)\frac{\partial k^*}{\partial n}=k^*+(\delta+g+n)\frac{\partial k^*}{\partial n}\\
\begin{align}
\frac{\partial k^*}{\partial n}&=\frac{k^*}{sf'(k^*)-(\delta+g+n)}\\
&<0
\end{align}
$$
而 $y^*=f(k^*)$，故
$$
\dfrac{\partial y^*}{\partial s}=f'(k^*)\dfrac{\partial k^*}{\partial s}>0\\
\dfrac{\partial y^*}{\partial n}=f'(k^*)\dfrac{\partial k^*}{\partial n}<0
$$

$$
\begin{align}
\frac{\partial lny^*}{\partial lns}&=\frac{s}{y^*}\frac{\partial y^*}{\partial s}\\
&=\frac{s}{y^*}f'(k^*)\frac{f(k^*)}{\delta+g+n-sf'(k^*)}\\
&=\frac{k^*f'(k^*)}{f(k^*)-k^*f'(k^*)}\\
&=\frac{\dfrac{f'(k^*)k^*}{f(k^*)}}{1-\dfrac{f'(k^*)k^*}{f(k^*)}}\\
\end{align}\\
$$

倒数第二个等号为代入 $(\delta+g+n)k=sf(k^*)$



### 福利分析

在 CD 生产函数下，$k^*=(\dfrac{s}{n+g+\delta})^{\dfrac{1}{1-\alpha}}$，从而 $r^*=\alpha k^{\alpha-1}=\dfrac{\alpha}{s}(n+g+\delta)$，不能确定它与 $n$ 的大小关系。从而还是可能存在和 Diamond 模型类似的代际改进方法，从而 Solow 模型的结果不一定是帕累托最优的。另外还可以有黄金律对消费的改进



对于 CD 生产函数下的黄金律储蓄率
$$
\mathop{max}_{s}\ y^*-sy^*\\
=k^{*\alpha}-sk^{*\alpha}\\
=(1-s)(\dfrac{s}{n+g+\delta})^{\dfrac{\alpha}{1-\alpha}}\\
~\\
FOC:-(\dfrac{s}{n+g+\delta})^{\dfrac{\alpha}{1-\alpha}}+(1-s)\dfrac{\alpha}{1-\alpha}(\dfrac{s}{n+g+\delta})^{\dfrac{2\alpha-1}{1-\alpha}}\dfrac{1}{n+g+\delta}=0\\
\dfrac{1-s}{s}=\dfrac{1-\alpha}{\alpha}\\
s=\alpha
$$


## 拉姆塞模型 Ramsey-Cass-Koopmans Model

在 Solow 模型的基础上放松了储蓄率外生的假定，由消费者做选择。并且消费者行动单元设定为家庭

### 假定

与 Solow 模型基本一致，暂且假定不存在资本折旧



#### 生产函数

与 Solow 保持一致



#### 偏好

决策主体单元设为家庭，**数量恒定**，尽管劳动力总量仍然增长 $L=L_0e^{nt}$

**家庭效用函数**
$$
U=\int_{t=0}^{\infty}e^{-\rho t}u(C(t))\frac{L(t)}{H}dt
$$
其中

- $e^{-\rho t}$ 为连续折现
- $u(\cdot)$ 为瞬时效用函数
- $C(t)$ 为**每个**家庭成员在时间 $t$ 的消费。注意为人均形式，效用只能是每个人的，不可能是有效劳均的
- $L(t)$ 为经济总人口
- $H$ 为家庭数量

**瞬时效用函数**采用相对风险规避系数不变（CRRA）的形式
$$
u(C(t))=\frac{C(t)^{1-\theta}}{1-\theta},\quad\theta>0,\quad\rho-n-(1-\theta)g>0
$$
后半部分的约束条件是为了最大化问题中有一个正的贴现率

有时为处理方便也可以用单调变换形式（序数效用单调变换没关系）
$$
u(C(t))=\frac{C(t)^{1-\theta}-1}{1-\theta}
$$
CRRA 瞬时效用函数具有如下良好性质：

- 满足边际效用递减
  - $u'(C)=C^{-\theta}>0$
  - $u''(C)=-\theta C^{-\theta-1}<0$
- 满足稻田条件
  - $lim_{C\to0}u'(C)=+\infty$
  - $lim_{C\to+\infty}u'(C)=0$
- Arrow-Pratt 相对风险规避系数 $-\dfrac{Cu''(C)}{u'(C)}=\theta$
- $lim_{\theta\to1}u(C(t))=lim_{\theta\to1}\dfrac{C(t)^{1-\theta}-1}{1-\theta}=lim_{\theta\to1}\dfrac{C^{1-\theta}}{-1}lnC=lnC$
- 任意两期消费之间的替代弹性 $\dfrac{-\partial ln(C_1/C_2)}{\partial ln(P_1/P_2)}=\dfrac{1}{\theta}$



#### 市场结构

也与 Solow 保持一致，三个竞争性的市场



#### 初值条件（禀赋）与增长率

与 Solow 保持一致，$A_0,L_0,K_0$

再加一点家庭总财富就是社会总资本 $\tilde{a}=K$，暗含了全民所有制（私有制）



### 参与者行为

#### 家庭预算约束

家庭总财富 $\tilde{a}$ 的变动分为：劳动收入 $wL$，资本从生产出分得的报酬 $r\tilde{a}$， 减去总消费 $C$
$$
\frac{d\tilde{a}}{dt}=wL+r\tilde{a}-C_总
$$

其中 $w=\dfrac{\partial F}{\partial L}=Af(k)-\dfrac{K}{L}f'(k)$



#### 家庭最大化

先统一量纲到有效人均量，注意符号

- 有效劳均消费 $c(t)=\dfrac{C_总}{AL}$
- 劳均消费 $C(t)=\dfrac{C_总}{L}=Ac=A_0e^{gt}c$
- 有效劳均财富 $a=\dfrac{\tilde{a}}{AL}$

从而家庭瞬时效用函数变为
$$
\begin{align}
\frac{C(t)^{1-\theta}}{1-\theta}&=\frac{[A(t)c(t)]^{1-\theta}}{1-\theta}\\
&=A(0)^{1-\theta}e^{(1-\theta)gt}\frac{c(t)^{(1-\theta)}}{1-\theta}
\end{align}
$$
家庭效用函数变为
$$
\begin{align}
U&=\int_{t=0}^{\infty}e^{-\rho t}u(C(t))\frac{L(t)}{H}dt\\
&=\int_{t=0}^{\infty}e^{-\rho t}A(0)^{1-\theta}e^{(1-\theta)gt}\frac{c(t)^{(1-\theta)}}{1-\theta}\frac{L(0)e^{nt}}{H}dt\\
&=A(0)^{1-\theta}\frac{L(0)}{H}\int_{t=0}^{\infty}e^{-(\rho-n-(1-\theta)g)t}\frac{c(t)^{(1-\theta)}}{1-\theta}dt
\end{align}
$$
有效劳均财富积累
$$
lna=ln\tilde{a}-lnA-lnL\\
\frac{da}{dt}=\frac{w}{A}+ra-c-(g+n)a
$$


从而有优化问题
$$
\mathop{max}_c\  \int_{t=0}^{\infty}e^{-(\rho-n-(1-\theta)g)t}\frac{c(t)^{(1-\theta)}}{1-\theta}dt\\
s.t.\ \frac{da}{dt}=\frac{w}{A}+ra-c-(g+n)a\\
0\leq c(t)\leq f[k(t)]\\
lim_{t\to\infty}e^{-\rho-n-(1-\theta)gt}a_t=0
$$
约束条件中

- 消费不能超过当期产出

- 考虑禁止庞氏博弈条件，死亡时不留下财富。对应（截断？）垂直终止线的横截条件

注意所有变量都已是有效人均，其中 $c$ 为控制变量， $a$ 为状态变量

**当前值汉密尔顿函数**
$$
H_c=\frac{c^{1-\theta}}{1-\theta}+m(ra+\frac{w}{A}-(n+g)a-c)
$$
其中影子价格 $m$ 在这里为共态变量

最大值条件，应该为内部解
$$
\frac{\partial H_c}{\partial c}=c^{-\theta}-m=0\\
\frac{\partial H_c}{\partial m}=\frac{da}{dt}\\
\frac{\partial H_c}{\partial a}=-\frac{dm}{dt}+(\rho-n-(1-\theta)g)m\\
lim_{t\to\infty}a_tm_te^{-(\rho-n-(1-\theta)g)t}=0
$$
横街条件也就是禁止庞氏骗局条件，死后不留财富，不考虑代际传递

上面第一式两边取对数后求导，整理后有
$$
-\theta\frac{1}{c}\frac{dc}{dt}=\frac{1}{m}\frac{dm}{dt}\\
\frac{1}{m}\frac{dm}{dt}=\rho+\theta g-r
$$
联立后有
$$
\frac{1}{c}\frac{dc}{dt}=\frac{r-\rho-\theta g}{\theta}\\
$$
而状态变量 $a$ 的运动方程
$$
\begin{align}
\frac{da}{dt}&=\frac{w}{A}+ra-c-(g+n)a\\
\end{align}\\
$$




#### 厂商行为

还是和 solow model 一样

- $r=f'(k)$
- $\dfrac{w}{A}=f(k)-kf'(k)$



### 均衡

整合厂商和消费者两方面的行为

- $r=f'(k)$
- $\dfrac{w}{A}=f(k)-kf'(k)$
- $\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{r-\rho-\theta g}{\theta}$
- $\dfrac{da}{dt}=ra+\dfrac{w}{A}-c-(g+n)a$
- 再加上一条 $\tilde{a}=K\Rightarrow a=k,\dfrac{da}{dt}=\dfrac{dk}{dt}$

联立以上五个方程
$$
\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{f'(k)-\rho-\theta g}{\theta}\\
\dfrac{dk}{dt}=f(k)-c-(n+g)k
$$
有效劳均资本运动方程其实也就和 solow model 一致，$f(k)-c$ 就是 solow 的有效劳均储蓄 $sf(k)$。暂时假设不考虑折旧 $\delta$



#### 存在性

稳态要求 $\dfrac{1}{c}\dfrac{dc}{dt}$ 为常数，进而要求 $\partial f'(k)/\partial t=f''(k)\dfrac{dk}{dt}=0$。因为 $f''(k)<0$，也就要求 $\dfrac{dk}{dt}=0$，即 $k$ 为常数。进而有$\dfrac{dc}{dt}=0$

进而有以下均衡状态
$$
f'(k^*)=\rho+\theta g\\
c^*=f(k^*)-(n+g)k^*\\
r^*=f'(k^*)\\
(\dfrac{w}{A})^*=f(k^*)-k^*f'(k^*)
$$
上面各变量都是常数，储蓄率 $s=\dfrac{f(k^*)-c}{f(k^*)}$ 也是常数

**重要结论**

- 即便放松 solow model 的储蓄率外生假定，按照 Ramsey model 的推导仍然为一个常数
- 人均变量 $\dfrac{K}{L},\dfrac{Y}{L},\dfrac{C_总}{L},w（实际工资率）$ 的增长速度均仍然为技术进步速度 $g$，依然和 solow model 一样
- 进而有资本产出比 $\dfrac{K}{Y}$ 长期稳定，也符合卡尔多典型事实
- 分配比例 $\dfrac{wL}{Y},\dfrac{rK}{Y}$ 在稳态时也是常数。这是因为 Ramsey model 隐含了技术进步“无偏”的假定，但现实中往往是有偏的，从而分配比例会随着技术进步流变
- $r^*=f'(k^*)$ 资本回报率也不会一直递减，而是停在均衡处



#### 稳定性

给定初值条件 $\tilde{a_0}, L_0, A_0$，没有 $c_0$

从而有 $k_0=\dfrac{\tilde{a_0}}{A_0L_0}$

对两个微分方程在 $\dfrac{dc}{dt}=0,\dfrac{dk}{dt}=0$ 处进行泰勒展开
$$
\begin{align}
\frac{dc}{dt}&=c\frac{f'(k)-\rho-\theta g}{\theta}\\
&\approx 0+\left.\partial(\frac{dc}{dt})/\partial c\right|_{c=c^*\\k=k^*}(c-c^*)+\left.\partial(\frac{dc}{dt})/\partial k\right|_{c=c^*\\k=k^*}(k-k^*)
\end{align}
$$

$$
\begin{align}
\frac{dk}{dt}&=f(k)-c-(n+g)k\\
&\approx 0+\left.\partial(\frac{dk}{dt})/\partial c\right|_{c=c^*\\k=k^*}(c-c^*)+\left.\partial(\frac{dk}{dt})/\partial k\right|_{c=c^*\\k=k^*}(k-k^*)
\end{align}
$$

对应雅克比矩阵，**尤其要注意 Jacob 的行列关系，不能随意调换（差分方程系统？）**
$$
\begin{pmatrix}
\partial(\dfrac{dc}{dt})/\partial c&\partial (\dfrac{dc}{dt})/\partial k\\
\partial(\dfrac{dk}{dt})/\partial c&\partial (\dfrac{dk}{dt})/\partial k
\end{pmatrix}=
\begin{pmatrix}
\dfrac{f'(k^*)-\rho-\theta g}{\theta}=0&c^*\dfrac{f''(k^*)}{\theta}<0\\
-1&f'(k^*)-(n+g)=\rho+\theta g-n-g>0
\end{pmatrix}
$$
特征值记为 $\lambda_1,\lambda_2$

- $\lambda_1+\lambda_2=矩阵的迹>0$
- $\lambda_1\lambda_2=行列式<0$

故雅克比矩阵特征值一正一负，为鞍点均衡。（如果两个为正，就是发散；两个为负，就是收敛）



再行联立两者路径，令收敛速度 $c-c^*$, $k-k^*$ 的增长率（即 $\dfrac{d(c-c^*)}{dt}\dfrac{1}{c-c^*}$）相等，可以求出线性化的鞍点路径斜率



### 比较静态分析

参考均衡存在性部分，已知均衡时有
$$
f'(k^*)=\rho+\theta g\\
c^*=f(k^*)-(n+g)k^*
$$


求 $\dfrac{\partial k^*}{\partial n}$： 

$f''(k^*)\dfrac{\partial k^*}{\partial n}=0$，因 $f''(k^*)<0$，故 $\dfrac{\partial k^*}{\partial n}=0$。因为劳动力增长并不影响作为决策主体的家庭数量保持 $H$ 不变



求 $\dfrac{\partial c^*}{\partial n}$：

$\dfrac{\partial c^*}{\partial n}=f'(k^*)\dfrac{\partial k^*}{\partial n}-k^*-(n+g)\dfrac{\partial k^*}{\partial n}=-k^*<0$



求 $\dfrac{\partial k^*}{\partial g}$

$f''(k^*)\dfrac{\partial k^*}{\partial g}=\theta$，从而 $\dfrac{\partial k^*}{\partial g}=\theta/f''(k^*)<0$



求 $\dfrac{\partial c^*}{\partial g}$

$\dfrac{\partial c^*}{\partial g}=f'(k^*)\dfrac{\partial k^*}{\partial g}-k^*-(n+g)\dfrac{\partial k^*}{\partial g}=[f'(k^*)-(n+g)]\dfrac{\partial k^*}{\partial g}-k^*$，又因 $f'(k^*)=\rho+\theta g$

$\dfrac{\partial c^*}{\partial g}=[\rho-n-(1-\theta)g]\dfrac{\partial k^*}{\partial g}-k^*$，其中根据模型效用函数部分的假设，$\dfrac{\partial k^*}{\partial g}$ 的系数就是优化问题折现因子，大于零；故整体小于零



### 福利分析

不容易用福利经济学第一定理（为什么？），**假想一个全知全能的社会计划者最大化社会福利，看是不是和市场结果一样**
$$
max\ \int_0^{+\infty}\dfrac{c(t)^{1-\theta}}{1-\theta}e^{-(\rho-n-(1-\theta)g)t}dt\\
s.t.\ \dfrac{dK}{dt}=F(K,AL)-C_总
$$
给定 $K_0$

由 $k=K/AL$，可从约束条件推得 $\dfrac{dk}{dt}=f(k)-c-(g+n)k$

同样用当前值汉密尔顿函数可以解得
$$
\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{f'(k)-\theta g-\rho}{\theta}=\dfrac{r-\theta g-\rho}{\theta}\\
\dfrac{dk}{dt}=f(k)-c-(g+n)k
$$
和市场配置的结果一样，故 Ramsey model 的均衡结果帕累托有效



## 戴蒙德模型 Diamond Model/OLG Model

与 Ramsey 一样，为了储蓄率内生化。但假设人不再是永久生存，而是只活两期



### 假定

#### 生产函数

依然是新古典的 $y=f(k)$



#### 偏好

每一代人只活两期，其效用为 $U_t=\dfrac{C_t^{1-\theta}}{1-\theta}+\dfrac{1}{1+\rho}\dfrac{C_{t+1}^{1-\theta}}{1-\theta}\quad\theta\gt0,\rho\gt-1$。大写 $C$ 为劳均形式 $C=\dfrac{C_总}{L}$



#### 市场结构

三个完全竞争的市场：产品、劳动、资本



#### 增长率

$L_t=(1+n)L_{t-1}$，$n$ 为”非净“增长率

由资本积累恒等式 $K_{t+1}=K_t-\delta K_t+I_t$ 出发，Diamond 模型假设没有折旧，只看投资。老人死时消费完自己的全部资本。从而有 $K_{t+1}=L_t(w_t-C_t)$，括号内均为人均形式



### 参与者行为

#### 厂商行为

$r=f'(k)$

$w=\dfrac{\partial F}{\partial L}=A[f(k)-kf'(k)]$



#### 消费者预算约束

第一期人均劳动收入用于支撑两期消费 $w_t=\dfrac{\partial F}{\partial L}=C_t+\dfrac{C_{t+1}}{1+r_{t+1}}$，其中因为储蓄取决于预期利率，故使用 $t+1$ 期的 $r$



#### 最大化某一代人的效用

$$
max\ U_t=\dfrac{C_t^{1-\theta}}{1-\theta}+\dfrac{1}{1+\rho}\dfrac{C_{t+1}^{1-\theta}}{1-\theta}\\
s.t.\ w_t=\dfrac{\partial F}{\partial L}=C_t+\dfrac{C_{t+1}}{1+r_{t+1}}
$$

直接用拉格朗日乘数法，可以解得 $\dfrac{C_{t+1}}{C_t}=(\dfrac{1+r_{t+1}}{1+\rho})^{\dfrac{1}{\theta}}$，回代约束条件有
$$
\begin{align}
C_t&=\dfrac{(1+\rho)^{\dfrac{1}{\theta}}}{(1+\rho)^{\dfrac{1}{\theta}}+(1+r_{t+1})^{\dfrac{1-\theta}{\theta}}}w_t\\
&=(1-s)w_t
\end{align}
$$
从而储蓄率 $s=\dfrac{(1+r_{t+1})^{\dfrac{1-\theta}{\theta}}}{(1+\rho)^{\dfrac{1}{\theta}}+(1+r_{t+1})^{\dfrac{1-\theta}{\theta}}}$



### 均衡

$K_{t+1}=L_t(w_t-C_t)$，除以 $A_{t+1}L_{t+1}$ 变为**有效劳均形式**：$k_{t+1}=\dfrac{1}{(1+n)A_{t+1}}(w_t-C_t)$

代入 $w_t-C_t=sw_t$ 与 $r=f'(k)$，注意 $w_t=A_t[f(k_t)-k_tf'(k_t)]$
$$
k_{t+1}=\dfrac{1}{(1+n)(1+g)}\dfrac{(1+f'(k_{t+1}))^{\dfrac{1-\theta}{\theta}}}{(1+\rho)^{\dfrac{1}{\theta}}+(1+f'(k_{t+1}))^{\dfrac{1-\theta}{\theta}}}[f(k_t)-k_tf'(k_t)]
$$

此差分方程难以求解，**假设 $\theta=1$ 的特殊情况，再加上 C-D 生产函数的假设**

这样 $k_{t+1}=\dfrac{1}{(1+n)(1+g)}\dfrac{1}{2+\rho}(1-\alpha)k_t^{\alpha}$

均衡采取先求后证，直接令 $k_{t+1}=k_t$ 尝试找不动点

可以求得

- $k^*=(\dfrac{1-\alpha}{(1+n)(1+g)(2+\rho)})^{\dfrac{1}{1-\alpha}}$
- $y^*=(\dfrac{1-\alpha}{(1+n)(1+g)(2+\rho)})^{\dfrac{\alpha}{1-\alpha}}$
- $r^*=f'(k^*)=\dfrac{\alpha}{1-\alpha}(1+n)(1+g)(2+\rho)$
- $w=A[f(k^*)-k^*f'(k^*)]$



#### 稳定性

离散情形下照样 tylor 展开

$k_{t+1}\approx k^*+(\left.\dfrac{dk_{t+1}}{dk_t}\right|_{k_t=k^*})(k_t-k^*)$

其中 
$$
\begin{align}
\left.\dfrac{dk_{t+1}}{dk_t}\right|_{k_t=k^*}&=\dfrac{1}{(1+n)(1+g)}\dfrac{1}{2+\rho}(1-\alpha)\alpha k^{*\alpha-1}\\
&=\dfrac{(1-\alpha)\alpha}{(1+n)(1+g)(2+\rho)}[\dfrac{1-\alpha}{(1+n)(1+g)(2+\rho)}]^{\dfrac{\alpha-1}{1-\alpha}}\\
&=\alpha\\
&\in(0,1)
\end{align}
$$
一阶导数在

- $(0,1)$ 则为平滑收敛
- $(-1,0)$ 则为阻尼震荡收敛
- 绝对值大于 1 则为发散



### 比较静态分析

$\dfrac{\partial s}{\partial r}=(1+\rho)^{\dfrac{1}{\theta}}[(1+\rho)^{\dfrac{1}{\theta}}+(1+r)^{\dfrac{1-\theta}{\theta}}]^{-2}\dfrac{1-\theta}{\theta}(1+r)^{\dfrac{1-2\theta}{\theta}}$

符号取决于 $\dfrac{1-\theta}{\theta}$

- 当 $\theta>1$ 时 ，$\dfrac{\partial s}{\partial r}<0$
- 当 $\theta=1$ 时 ，$\dfrac{\partial s}{\partial r}=0$
- 当 $\theta<1$ 时 ，$\dfrac{\partial s}{\partial r}>0$

和欧文费雪的跨期选择洞见一样，利率在这里同时有收入效应又有替代效应，要看消费效用函数的替代弹性 $\dfrac{1}{\theta}$



### 福利分析

因为代际偏好不同，没有代表性的效用函数可言，也不能轻易加权，也就不能用社会计划者方法。

但可以举出一个明确的反例，证明存在改进方法，也就是说 Diamond 的均衡不是帕累托有效的

$r^*=(1+n)(1+g)(2+\rho)\dfrac{\alpha}{1-\alpha}$ 有可能小于 $n$

那么，**每一期都向变老的人卖一个收益为 (1+n) 的理财产品，由下一期买入同样产品的人的投入资金来偿付。永续滚动，也就是社保。**

对比 Ramsey 模型，尽管 Ramsey 中每个人也是活无限长时间，但作为决策单元的家庭数量 H 是假定有限的

至于 $r^*<n$ 的情况是怎么造成，由于 $r^*=f'(k^*)$ 而 $f'(\cdot)$ 又是递减的，所以原因在于 $k^*$ 太大，**过度投资**、储蓄率过高（优质资产荒）。缺少代际转移的市场。（并不是说货币宽松）



### 一般情况

$\theta\neq 1$ 时的情况更为复杂，可能会出现多个不同的均衡点（以及虚假的均衡点），具体收敛到哪一个可能视乎路径依赖、信念。甚至可能只会收敛到零的情况。见 Romer 4th p67



## 罗默模型 Romer Model

内生技术进步

### 假设

技术研发不能放到完全竞争市场中，肯定要在垄断竞争、寡头、垄断中选一个。从而原来的新古典生产函数扩大为三个变量，也就不再是规模报酬不变的了。不能再套用完全竞争中的分配 $\bar{Y}=Y=rK+wL$，那样就没有分配能留给技术研发 $A$ 了

**基本假设从 Ramsey Model 开始**

**劳动力暂且固定为 $L$，不是研究重点。但也可以放松这个假设**

效用函数仍然为 $\dfrac{c^{1-\theta}}{1-\theta}$

人均（不是有效人均）财富积累过程 $\dfrac{da}{dt}=ra+w-c$；对比 Ramsey 的有效人均积累过程，其实是一致的，这里的形式是因为劳动力总量已固定



#### 生产函数

$$
Y=L^{1-\alpha}\mathop{\sum}^A_{i=1}x_i^{\alpha}
$$

生产只用两个要素 $L$ 和 $x_i$

- 其中 $x_i$ 是中间投入品
- $A$ 为技术
- $Y$ 为最终产品



最终产品 $Y$ 最终分配用于消费、储蓄和研发，从而 
$$
Y=Lc+K+R
$$
其中，

- $R$ 用于研发
- $K=\sum^A_{i=1}x_i$，资本用于生产中间投入品



#### 研发

假设就按照大数定理，砸钱就能砸出研发成果；且假定专利永久保护到无穷

$\dfrac{dA}{dt}=\dfrac{R}{\eta}$，$\eta$ 为研究成功概率倒数



#### 市场结构

产品市场、劳动市场 $Y、L$ 仍然是完全竞争的，但中间投入品市场 $x_i$ 假设为垄断竞争。研发专利市场 $A$ 自由进入，无超额利润



#### 禀赋

$a_0$ 给定，且 $La=AP_A$，即个人财富持有形式就是专利，$P_A$ 为专利价格



### 参与者行为

#### 最终产品厂商

最大化利润，成本部分为劳动工资和中间投入品费用（也暗含了最终产品销售价格标准化 1）
$$
\mathop{max}_{L,x_i}\ L^{1-\alpha}\mathop{\sum}^A_{i=1}x_i^{\alpha}-wL-\mathop{\sum}^A_{i=1}p_ix_i
$$
一阶条件：

- $w=(1-\alpha)\dfrac{Y}{L}$
- $p_i=\alpha L^{1-\alpha}x_i^{\alpha-1}$



#### 中间投入品厂商

最大化利润，需要有专利才能生产中间品，假定中间投入品边际成本为 1（也可以理解为相对于中间品向最终厂商销售价格的标准化成本价格）
$$
\mathop{max}_{x_i}\ p_ix_i-x_i\\
s.t.\ p_i=\alpha L^{1-\alpha}x_i^{\alpha-1}
$$
约束条件即中间投入品厂商面临的需求曲线，就是最终产品厂商由一阶条件推导出的引致需求

可以解得每种投入品的价格和数量都一样

- $p_i^*=\dfrac{1}{\alpha}$
- $x_i^*=L\alpha^{\dfrac{2}{1-\alpha}}$



因为每个投入品数量都一样，原生产函数就可以写为
$$
Y=L^{1-\alpha}Ax^\alpha
$$
这里 $L$ 为常数（最开始的假设），$x$ 也是常数

从而增长率可以有 $\dfrac{1}{Y}\dfrac{dY}{dt}=\dfrac{1}{A}\dfrac{dA}{dt}$

同样因为每个投入品数量都一样，资本就可以写为 $K=Ax\Leftrightarrow x=\dfrac{K}{A}$

回代生产函数
$$
Y=K^\alpha(AL)^{1-\alpha}
$$
可以算出中间商利润
$$
\begin{align}
\pi_i^*&=(p_i^*-1)x_i^*\\
&=\dfrac{1-\alpha}{\alpha}L\alpha^{\dfrac{2}{1-\alpha}}
\end{align}
$$


#### 研发部分

最大化研发专利**出售利润**
$$
\begin{align}
\mathop{max}&\quad \dfrac{dA}{dt}P_A-R\\
&=\dfrac{dA}{dt}P_A-\eta\dfrac{dA}{dt}\\
&=0
\end{align}
$$
第一个等号代入了$\dfrac{dA}{dt}=\dfrac{R}{\eta}$；第二个等号是由于自由进入，最优化利润将会是零利润。从而得到 $P_A=\eta$

由于无限期专利保护，每期现金流为年金，记为 $\pi$ （**符号就是中间商最大化利润，要在自主生产和出售之间无差异**）
$$
lim_{n\to\infty}\sum\pi(\dfrac{1}{1+r}+\dfrac{1}{(1+r)^2}+\cdots+\dfrac{1}{(1+r)^n})=P_A\\
\pi\dfrac{\dfrac{1}{1+r}}{1-\dfrac{1}{1+r}}=P_A\\
P_A=\dfrac{\pi}{r}
$$
从而 $P_A=\dfrac{\pi}{r}$

$r$ 为每期贴现利率

严格来说要用跨一期的持有/出售专利的无套利方程 $rP_A=\pi+\dfrac{dP_A}{dt}$，左侧为出售专利，右侧为持有专利。稳态时 $\dfrac{dP_A}{dt}$ 为常数，设为零就有上面的结论



#### 消费者行为

$$
max\ \int_0^{\infty}\dfrac{{c}^{1-\theta}}{1-\theta}e^{-\rho t}dt\\
s.t.\ \dfrac{da}{dt}=ra+w-c
$$

可以解得

- $\dfrac{dc}{dt}=\dfrac{c(r-\rho)}{\theta}$
- $\dfrac{da}{dt}=ra+w-c$



### 均衡

联立以下各个方程

- $\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{r-\rho}{\theta}$，消费路径
- $p_i^*=\dfrac{1}{\alpha}$，中间投入品价格
- $x_i^*=L\alpha^{\dfrac{2}{1-\alpha}}$，中间投入品数量
- $Y=L^{1-\alpha}Ax^\alpha$，中间投入品数量都一样的情况下的产出
- $Y=Lc+K+R$ 消费、储蓄、研发三部分分配，$K=Ax$（所有 $x$ 都相等)， $\dfrac{R}{\eta}=\dfrac{dA}{dt}$ （研发成功概率）
- $P_A=\eta=\dfrac{\pi}{r}$，专利出售价格与年金（或者中间商最大化利润）贴现，由研发厂商零利润所得
- $\pi=\dfrac{1-\alpha}{\alpha}L\alpha^{\dfrac{2}{1-\alpha}}$，中间商最大化利润



**平衡增长路径**
$$
\begin{align}
Y&=L^{1-\alpha}Ax^\alpha\\
&=Lc+Ax+\eta\dfrac{dA}{dt}\\
\dfrac{Y}{A}&=L^{1-\alpha}x^\alpha\\
&=L\dfrac{c}{A}+x+\eta\dfrac{1}{A}\dfrac{dA}{dt}
\end{align}
$$
已经知道 $L,x,\eta$ 都是常数，所以 $\dfrac{Y}{A}$ 也是常数（倒数第二个等式）

- $\dfrac{1}{Y}\dfrac{dY}{dt}=\dfrac{1}{A}\dfrac{dA}{dt}$

从而若 $\dfrac{1}{A}\dfrac{dA}{dt}$ 也是常数，（最后一个等式）也就有

- $\dfrac{c}{A}$ 也是常数，也就是 $\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{1}{A}\dfrac{dA}{dt}$



也就有 
$$
\dfrac{1}{A}\dfrac{dA}{dt}=\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{r-\rho}{\theta}=\dfrac{1}{\theta}(\dfrac{1}{\eta}\dfrac{1-\alpha}{\alpha}L\alpha^{\dfrac{2}{1-\alpha}}-\rho)
$$
其中实际利率 $r=\dfrac{\pi}{\eta}=\dfrac{1}{\eta}\dfrac{1-\alpha}{\alpha}L\alpha^{\dfrac{2}{1-\alpha}}$



**这就是以前的外生技术进步速度 $g$**，注意人口水平 $L$ 在其中扮演的角色，人越多进步越快（在全球尺度内，不能只看某一国家/民族）



分配上，同样由上面的联立方程组加上

- $w=(1-\alpha)\dfrac{Y}{L}$ ，最终产品最优化的劳动工资

可以得到 $Y-Ax=wL+rAP_A$，其中

- $Y-Ax$ 去除中间投入品后才是 GDP
- $La=AP_A$，专利形式持有财富




### 福利分析

由于垄断，可以推断市场结果不是帕累托最优的，同样解社会计划者问题
$$
\mathop{max}_{c,x}\ \int_0^{\infty}\dfrac{c^{1-\theta}}{1-\theta}e^{-\rho t}dt\\
s.t.\ Y=L^{1-\alpha}Ax^{\alpha}=Lc+Ax+\eta\dfrac{dA}{dt}\\
即 \dfrac{dA}{dt}=\dfrac{1}{\eta}(L^{1-\alpha}Ax^{\alpha}-Lc-Ax)
$$
注意社会计划问题中的约束条件没有设置研发部门，而是直接用 $\eta\dfrac{dA}{dt}$ 这部分划拨研发报酬

两个控制变量、一个状态变量，同样套用动态最优化方法，可以解得
$$
\dfrac{1}{c}\dfrac{dc}{dt}=\dfrac{1}{\theta}(\dfrac{1}{\eta}\dfrac{1-\alpha}{\alpha}L\alpha^{\dfrac{1}{1-\alpha}}-\rho)
$$

并且产品数量 $x_i^*=L\alpha^{\dfrac{1}{1-\alpha}}$ ，将大于市场的产品数量水平 $L \alpha^{\dfrac{2}{1-\alpha}}\ (0<\alpha<1)$

即市场垄断就是生产不足



市场定价下，明明是垄断竞争的成本加成定价，但却是零利润（自由进入）。原因是要买专利，买到专利才能生产中间投入品，才有垄断的能力。市场计划下就是边际定价，专利只能白给，但这样就没有人研发了。也就是垄断不可避免。



## 没有资本的模型

两部门划分，一部分人生产 $Y$，另一部分人研发 $A$
$$
Y=[(1-\alpha_K)K]^\alpha[(1-\alpha_L)AL]^{1-\alpha}\\
\dfrac{dK}{dt}=sY\\
\dfrac{dA}{dt}=(\alpha_K K)^{\beta}(\alpha_L L)^{\gamma}A^{\theta}\\
\dfrac{1}{L}\dfrac{dL}{dt}=n
$$

- $\alpha_K,\alpha_L$ 分别为研发人员比例；技术 $A$ 不用在部门间划分，作为知识自由流动
- $\beta,\gamma$ 为非线性研发的幂参数。$A$ 的幂参数 $\theta$ 可正可负，因为不一定参考文献越多越能突破
- 只要 $\beta+\theta>1$ 就规模报酬递增，因为 $L$ 按规定速度增长，视为外生给定。当然 $\beta+\theta<1$ 更现实



若去除资本参与
$$
Y=(1-\alpha_L)AL\\
\dfrac{dA}{dt}=(\alpha_L L)^{\gamma}A^{\theta}\\
\dfrac{1}{L}\dfrac{dL}{dt}=n
$$
可以推得 $\dfrac{Y}{L}=(1-\alpha_L)A$，人均收入只取决于 $\dfrac{1}{A}\dfrac{dA}{dt}$

而 $\dfrac{1}{A}\dfrac{dA}{dt}=(\alpha_L L)^{\gamma}A^{\theta-1}=g_A$

从而有 $\dfrac{1}{g_A}\dfrac{dg_A}{dt}=\gamma n+(\theta-1)g_A$

$\dfrac{dg_A}{dt}=\gamma ng_A+(\theta -1)g_A^2$，令其等于零，就可以讨论 $\theta$ 与 1 的大小，规模报酬问题

当 $\theta \neq 1$ 时，有 $g_A^*=\dfrac{\gamma}{1-\theta}n$



## 讨论

怎么做大蛋糕、怎么分蛋糕。目前只讨论过增长，靠技术；如何分净，没有讨论过分公平



### 罗默模型中的垄断问题

大的平台与技术创新，似乎这样的垄断成为了造富机器。垄断是技术发展必须的代价吗？

或者国家买单，然后重新分配给研发。这又会有寻租问题

更长的历史角度来看，从强制劳动到受薪劳动。企业寻求技术突破就是为了垄断地位



三个问题：

- 激励
- 信息
- 承诺可信：难以告赢政府



### 罗默模型中的人口问题

人口 $L$ 进入罗默模型内，并且偏导数为正。与索罗模型的结论相反：人一方面摊薄了现有的资源、另一方面又可以提高研发成功的可能。再考虑人的异质性，最聪明的人应该去做研发而不是金融或者公务员。“学而优则仕”在宏观上的激励是不利于经济长期发展的 



### 趋同与赶超

- Solow 模型：
  - 绝对趋同：参数都一样的话，无论初始状态，均衡应该是一样的。差距最终会消失
  - 条件趋同：各自的参数因为地理、文化等等各种条件不同，只能收敛到各自的均衡上。差距永远无法抹平
- Ramsey 模型：和 Solow 一样
- Diamond 模型：$\theta\neq 1$ 时
  - 路径依赖：即使条件参数完全一样，因为初始状态不同也有可能收敛到不同均衡
  - 信念：一个区间内可以收敛到不同的均衡
- Romer 模型：不趋同、不收敛，差距永远存在，不仅横截总量大、增长速度还快



国家、地区的俱乐部



## 消费

### 永久收入假说

弗里德曼、莫迪利亚尼，与凯恩斯的绝对收入假说认为消费只取决于当期收入 $C=\bar{C}+cY_D$，很不一样

凯恩斯对消费的见解有三点：

- 边际消费稳定
- 平均消费递减
- 当期消费不看利率

**推导**
$$
\mathcal{L}=\mathop{\sum}_{t=1}^Tu(C_t)+\lambda(A_0+\mathop{\sum}_{t=1}^{T}Y_t-\mathop{\sum_{t=1}^{T}}C_t)
$$
就是在终生预算约束下最大化终生消费效用，求解上述拉格朗日函数就可以得出下面的结论

永久收入定义如下，终生可得资源平均分到一生中的每个时期，**也就是当期的消费**
$$
\dfrac{1}{T}(A_0+\mathop{\sum}_{t=1}^{T} Y_t)=C_t
$$
暂时收入定义为当期收入与永久收入之差，**也就是当期的储蓄**
$$
Y_t-\dfrac{1}{T}(A_0+\mathop{\sum}_{t=1}^{T} Y_t)=S_t
$$

**模型意义**

- 暂时性的收入变化（意外之财/减税）对消费影响很小
- 收入在时间上的分布不太影响消费，但很影响储蓄。经济个体用储蓄和借债来平滑消费路径
- 关于储蓄的典型观点可能是片面的。比如说穷人储蓄率低，可能不仅是因为维持生活就很困难，还可能因为一生都很难维持现在的水平，所以也是取决于收入在时间上的分布



### 不确定性与随机游走

永久收入假说 加上 二次效用函数假设 意味着消费服从**霍尔随机游走**，**这里需要二次效用函数的假设支持**

**推导**
$$
\mathcal{L}=E[\mathop{\sum}_{t=1}^T(C_t-\dfrac{a}{2}C_t^2)]+\lambda(A_0+E\mathop{\sum}_{t=1}^{T}Y_t-\mathop{\sum_{t=1}^{T}}C_t)
$$
加入不确定性后，结论基本不变，只是加了期望。也就满足确定性等价
$$
C_1=\dfrac{1}{T}(A_0+\mathop{\sum}_{t=1}^{T} E_1[Y_t])
$$
而且有重要结论：**在每一期对下期消费的预期就等于当期消费。也就是说消费变化无法预测**
$$
C_1=E_1[C_t]
$$
因果可以是反过来的，预期未来消费上升，现在的消费就会相应调整上升

永久收入假说 加上 二次效用函数假设 意味着消费服从**霍尔随机游走**
$$
C_t=C_{t-1}+e_t\\
E_{t-1}[e_t]=0，白噪音
$$
另外，通过迭代变形可以有
$$
C_2=C_1+\dfrac{1}{T-1}(\sum_{t=2}^{T}E_2[Y_t]-\sum_{t=2}^TE_1[Y_t])
$$
也就是两期的消费变动等于经济个体对其终生资源的估计的变化量（**信息变化**）除以一生中剩余的时期数

霍尔随机游走的意义：

- 消费者根据预期信息**的变化**修正自己的消费，已经预期到的不会产生影响（类似理性预期）。也就是 $E_2(Y_t)-E_1(Y_t)$ 产生影响，不是 $E_1(Y_2-Y_1)$ 产生影响
- 消费变动反映了一生永久收入的“意外变动”（不是暂时性变动），从而外界无法预测消费的变动



### 利率与储蓄

也与凯恩斯的不一样

欧文费雪跨期选择，替代和收入效应

放开永久收入基础部分折现和利率 $\rho=r=0$ 的假设，并且使用 CRRA 效用函数。不考虑不确定性

**推导**
$$
\mathcal{L}=\mathop{\sum_{t=1}^{T}\dfrac{1}{(1+\rho)^t}\dfrac{C_t^{1-\theta}}{1-\theta}}+\lambda(A_0+\mathop{\sum}_{t=1}^{T}\dfrac{1}{(1+r)^t}Y_t-\mathop{\sum_{t=1}^{T}}\dfrac{1}{(1+r)^t}C_t)
$$
同样由拉格朗日乘数法可以得出欧拉方程，整理有
$$
\dfrac{C_{t+1}}{C_t}=(\dfrac{1+r}{1+\rho})^{1/\theta}
$$

由于不一定有 $r$ 等于 $\rho$，故消费不一定遵从随机游走



**只考虑两期**

假定没有初始财富，且 $\rho=0$

图形上预算线围绕着 $(Y_1,Y_2)$ 旋转

可能同时有替代效应和收入效应，Slutsky/Hicks 分解



### 消费与风险资产

基于消费的 CAPM



### 超越永久收入假说的更多理论

效用三阶导数为正，有预防性储蓄



### 实证

用 $C_t$ 对 当期收入 $Y_t$ 回归

- 家庭截面数据，斜率显著小于 1，因为暂时性收入的波动较大
- 国家时序数据，斜率接近 1，因为暂时性收入波动接近 0
- 白人截距比黑人高，因为白人永久收入较高



## 投资

投资对长期增长至关重要，在短期波动又很大

投资的主体是厂商，有点像公司金融；储蓄的主体是家庭



### 资本使用成本和资本合意存量

因为厂商用的资本很多都是自有资本而不是租赁，所以 $r_k$没有准确的观察值

注意资本是个存量，投资是个流量。政策可以有离散的变化，但是资本存量不可能出现离散的阶跃



### 投资的 q 理论

考虑内部调整成本。**假定不存在外部调整成本，从而资本品购买价格恒等于 1**
$$
\mathop{max}_{I}\ \pi=\int_{t=0}^{\infty}e^{-rt}[\pi(K(t))k(t)-I(t)-C(I(t))]dt\\
s.t.\ \dfrac{dk}{dt}=I(t)
$$

其中：

- $\pi(K(t))$：关于行业总量资本 $K(t)$ 的利润函数。其中合理假定行业最终产品需求曲线向下，从而有 $\pi'(\cdot)<0$
- $k(t)$：企业自身资本
- $I(t)$：投资
- $C(I(t))$：资本存量调整成本，**不是消费**。并且假定有 $C(0)=0,C'(0)=0,C''(\cdot)>0$

最大值原理可以得出一阶条件：

- $1+C'(I(t))=q(t)$，左边为投资边际成本，右边为投资的边际收益
- $\pi(K(t))=rq(t)-\dfrac{dq}{dt}$，左边为利润的边际收益，右边为利润的边际成本（利息机会成本和资产价格变动）
- $\mathop{lim_{t\to\infty}}e^{-rt}q(t)k(t)=0$，横街条件



现值汉密尔顿函数的乘数就是 q
$$
q(t)=\int_{\tau=t}^{\infty}e^{-r(\tau-t)}\pi((K(\tau))d\tau
$$

可以理解为在 $t$ 时刻投资一单位资本后带来的未来边际收益折现到时刻 $t$ 的值

此 q 为边际 q。而资本市场价值与重置成本之比的托宾 q 是平均 q。一般来说，在调整成本规模报酬递减下，边际 q 是要小于平均 q 的。但两者大小关系并不固定



### 比较静态分析

永久变化和暂时变化



### 不确定性

政策消息发布、等待期间、正式实施三个时间段/点



### 弯折的调整成本和固定调整成本



### 不完美金融市场




## 失业

劳动市场不是一般的完全竞争市场，研究关心这些问题：

1. 平均失业率在长期内的决定因素：究竟是摩擦性的还是非瓦尔拉斯性（结构性）的
2. 劳动市场的周期性行为：劳动供给不太可能是经济波动的关键原因；想不想找工作不那么重要，关键是用人需求
3. 劳动需求变动导致就业大幅度波动，但实际工资却只有较小影响：实际工资粘性



### 效率工资模型

努力程度函数抽象形式有
$$
e(w,w_a,u),\quad e_1(\cdot)\gt0\quad e_2(\cdot)<0,\quad e_3(\cdot)>0
$$
其中

- $w$：厂商工资
- $w_a$：行业工资
- $u$：失业率

各下标表示偏导数，也就是说厂商实际给到自己的工资越高越努力；行业工资越高（相对厂商给得就少了）越不努力 ；失业率越高越努力（怕被炒）

#### 萨默斯（Summers, 1988）

努力程度如下表出
$$
e=
\begin{cases}
(\dfrac{w-x}{x})^\beta&w\gt x\\
0&其他
\end{cases}\\
x=(1-bu)w_a
$$
其中 $0<\beta<1$，$b>0$。$b$ 就是工人赋予失业的相对权重（相对于 1）。 $x$ 是劳动力市场条件的测度指标，也被称为劳动力市场指数

考虑代表性厂商优化问题
$$
\mathop{max}_{L,w}\ F(eL)-wL
$$
一阶条件会有 $F'(eL)$=$\dfrac{w}{e(w)}$ 这就是**有效劳动成本**

并且要求 $\dfrac{we'(w)}{w}=1$，也就是努力程度的工资弹性是 1。这个条件也是最小化上述有效劳动成本的一阶条件

代入萨默斯的具体努力程度函数，有 $w=\dfrac{1-bu}{1-\beta}w_a$。均衡时厂商工资等于行业工资 $w=w_a$，进而可得均衡失业率 $u_{EQ}=\dfrac{\beta}{b}$



**模型意义**

1. 均衡失业率只取决于努力程度函数的参数，与生产函数无关。从而生产函数的改进不会改善失业
2. 中等大小的 $\beta$ 会导致大量失业。注意到 $\beta$ 就是努力程度函数中 $e$ 对厂商相对工资 $\dfrac{w-x}{x}$ 的弹性
3. 正常情况下，总失业变化时，厂商调整工资货价格的激励很小



### 夏皮罗-施蒂格利茨模型

延续效率工资。观点是厂商监督能力有限，以效率工资激励员工不偷懒

假定有数量为 $\bar{L}$ 的大量工人和数量为 $N$ 的大量厂商



**工人行为**

代表性工人终生效用还是典型形式
$$
U=\int_{t=0}^{\infty}e^{-\rho t}u(t)dt,\quad \rho\gt 0\\
u(t)=
\begin{cases}
w(t)-e(t)&有工作时\\
0&失业时
\end{cases}
$$
瞬时效用就是有工作时等于工资减努力程度，失业时等于 0

工人在任何时刻有三种可能状态：

- 就业并且努力工作，用 E 表示
- 就业并且不努力工作，用 S 表示
- 失业，用 U 表示

并且努力程度只有两个水平可选：$e=0$ 或者 $e=\bar{e}$

关于状态转移的假设：

1. 工人从 $t_0$ 时刻开始工作，到 $t$ 时刻为止的 $t-t_0$ 时间段内失业事件发生的分布服从泊松分布，从而在 $t$ 时刻仍在岗位上的概率为
   $$
   P(t)=e^{-b(t-t_0)},\quad b>0
   $$
   也就是有无记忆性，就业时长服从指数分布。$b$ 作为泊松分布的期望，可以理解为单位时间内工作中断的概率

2. 厂商察觉工人偷懒的事件也服从泊松过程，此外生概率记为 $q$，并且与 $b$ 独立。偷懒一经发现即被解雇。从而如果一个员工偷懒，经过时间 $\tau$ 后仍在岗的概率为 $e^{-q\tau}e^{-b\tau}$，既没有被发现也没有被意外解雇

3. 失业工人在单位时间内找到新工作的概率为 $a$。工人把 $a$ 视为给定的，但是对于经济体整体而言 $a$ 是内生的

现在考虑各状态下工人终生效用期望的折现值 $V_i,\ i=E,S,U$。因为状态转移服从泊松过程，所以我们不用管历史状态，也不用管未来状态的可能路径。

使用“动态规划”，**只考虑一个又一个极短的时间段，按概率转移、逐期迭代**

考虑一个在时刻 0 就业并且努力工作的人
$$
V_E(\Delta t)=\int_{t=0}^{\Delta t}e^{-bt}e^{-\rho t}(w-\bar{e})dt+e^{-\rho\Delta t}[e^{-b\Delta t}V_E(\Delta t)+(1-e^{-b\Delta t})V_U(\Delta t)]
$$
等号右边第一项是 $[0,\Delta t]$ 区间内的效用流折现，第二项是 $\Delta t$ 之后的效用：就业的概率是 $e^{-b\Delta t}$，失业的概率是 $1-e^{-b\Delta t}$。而且只考虑稳态，如果最开始时努力工作是工人的最优选择，那么之后仍然是最优选择，不会试图偷懒。

解上面的方程，并且令 $\Delta t$ 趋向于零，可以得出 $V_{i}(\Delta t)=V_{i}$
$$
V_E=\dfrac{1}{\rho+b}[(w-\bar{e})+bV_U]
$$
也可以用**资产定价理解**，一种资产在工人就业时的期望收益率为 $\rho$。单位时间的总损益就是单位时间内的红利加上单位时间内的期望资本损益
$$
\rho V_E=(w-\bar{e})-b(V_E-V_U)
$$
整理一下就是和再上面一条式子一样的

同理，考虑工人偷懒和失业的情况的情况，有
$$
\rho V_S=w-(b+q)(V_S-V_U)\\
\rho V_U=a(V_E-V_U)
$$


**厂商行为**
$$
\pi(t)=F(\bar{e}L(t))-w(t)[L(t)+S(t)],\quad F'(\cdot)>0,\quad F''(\cdot)<0
$$
其中：

- $L$ 为努力工作雇员数量，只有努力工作的人有产出
- $S$ 为偷懒的雇员数量

厂商的问题是设置一个**”足够高“**的工资水平 $w$，让受雇工人**”完全不“**偷懒，并且选择工人数量 $L$



**不偷懒条件**

需要让工人的 $V_E\geq V_S$，而且因为努力程度除了 0 只有 $\bar{e}$，所以厂商不必付太高的工资，只要使得 $V_E=V_S$

从而可以得到 $V_E-V_U=\dfrac{\bar{e}}{q}$。认真工作的溢价对努力程度成正比，对厂商检查能力成反比

同样可以得到均衡工资水平
$$
w=\bar{e}+(a+b+\rho)\dfrac{\bar{e}}{q}
$$
继续替换 $a$，由单位时间内失业的人数等于新找到工作的人数这一均衡条件
$$
a=\dfrac{NLb}{\bar{L}-NL}
$$
从而最终不偷懒条件为
$$
w=\bar{e}+(\dfrac{\bar{L}}{\bar{L}-NL}b+\rho)\dfrac{\bar{e}}{q}
$$


**均衡**

因为当工资 $w<\bar{e}$ 时工人效用为负，肯定不会工作。所以在 (NL, w) 坐标系中劳动供给是一条 $w=\bar{e}$ 与 $L=\bar{L}$ 构成的反 L 型曲线

如果厂商可以完全监督员工：

- 没有人偷懒，那么厂商利润函数变为 $\pi(t)=F(\bar{e}L(t))-w(t)L(t)$。即 $S(t)=0$

- 只有一阶条件 $\bar{e}F'(\bar{e}L)=w$，当 $w=\bar{e}$ 时考虑典型厂商则有 $F'(\bar{e}\bar{L}/N)=1$。但假设有 $F'(\bar{e}\bar{L}/N)>1$，此假设意味着厂商劳动需求与上面的反 L 型劳动供给曲线相较于 L 型角点上方，如果不是劳动供给有上限，在完全监督能力的支持下厂商愿意雇佣更多的劳动

如果厂商没有完全监督能力：

- 考虑上面的不偷懒条件。实际均衡出现在不偷懒条件曲线和厂商劳动需求曲线的交点
- 因为不偷懒条件的支持，厂商劳动需求曲线仍然是上面的一阶条件，即 $S(t)=0$



### 合同模型

劳资长期关系的存在意味着，工资不必每期都调整，以使得劳动市场出清，只要工人预期获得的收入流相比外来机会更加有利，就愿意留在现在的工作岗位上。



**厂商行为**
$$
E(\pi)=\mathop{\sum_{i=1}^{K}}p_i[A_iF(L_i)-w_iL_i],\quad F'(\cdot)>0,\quad F''(\cdot)<0
$$
其中下标 $i$ 为可能所处的各个“状态”。 $A$  不仅可以反应技术，也可能反映经济总体产出、公司业绩等等影响利润的因素。 $L_i$ 和 $w_i$ 是当 $A$ 的实现值为 $A_i$ 时的劳动数量和工资。 

厂商最大化期望利润，所以是风险中性的



**工人行为**

假设每个工人工作量都是相等的（不同于效率工资模型），代表性工人效用如下
$$
u=U(C)-V(L),\quad U'(\cdot)>0,\quad U''(\cdot)<0,\quad V'(\cdot)>0,\quad V''(\cdot)>0\\
E(u)=\mathop{\sum_{i=1}^{K}}p_i[U(C_i)-V(L_i)]
$$
且消费 $C$ 就等于工资收入 $wL$

因为消费边际效用递减，所以工人是风险规避的



**均衡**

为了工人愿意工作，工资必须提供到某个最低水平的期望效用 $u_0$。**一旦签订合同，就不再有劳动流动了。所以合同的唯一约束是其提供的平均效用水平，而不是单独某个状态 $i$ 下的效用水平**



#### 隐性合同

针对 $A$ 的每一个实现值都确定了相应的工资和劳动小时数。实际上合同并不会明确地把就业和工资确定为状态的函数（？）

根据上面的劳资行为逻辑，有拉格朗日函数
$$
\mathcal{L}=\sum_{i=1}^{K}p_i[A_iF(L_i)-C_i]+\lambda(\sum_{i=1}^Kp_i[U(C_i)-V(L_i)]-u_0)
$$
关于 $C_i$ 的一阶条件有 $U'（C_i)=\dfrac{1}{\lambda}$

也就是说在各个状态 $i$ 下，消费的边际效用都保持不变，由消费边际效用递减可知消费的量也保持不变。也就是工资总额保持不变。所以风险中性的厂商会给风险规避的工人提供完全保险

关于 $L_i$ 的一阶条件是 $p_iA_iF'(L_i)=\lambda p_iV'(L_i)$，代入上面所得的 $\lambda=\dfrac{1}{U'(C_i)}$
$$
A_iF'(L_i)=\dfrac{V'(L_i)}{U'(C)}
$$
从而可以确定 $L_i=L_i(A_i)$，就业量与 $A_i$ 正相关



### 搜寻和匹配模型

强调搜寻摩擦



#### 莫滕森-皮萨里德斯模型

经济由**工人和职位**组成

工人数量是等于 1 的连续体。每个工人要么就业要么失业：

- 就业工人单位时间内产出固定为外生的 $y$，而单位时间工资 $w(t)$ 是内生且随时间变化的，效用也是 $w(t)$；就业人数记为 $E(t)$
- 失业工人在单位时间内获得一个外生不变的收入 $b\ge0$（或者看做是他闲暇的效用）；失业人数记为 $U(t)$
- 工人折现是 $r>0$

职位要么有人负责要么空缺：

- 有人负责职位单位时间内产出为 $y$，劳动成本为 $w(t)$，岗位固定维护成本外生为 $c$；有人负责岗位数记为 $F(t)$
- 空缺职位没有产出也没有劳动成本，只有岗位固定维护成本 $c$；空缺岗位数记为 $V(t)$
- 职位可以被厂商任意新创建或者撤销



单位时间内应聘洽谈次数为匹配函数表出
$$
M(t)=M(U(t),V(t)),\quad M_U>0,M_V>0
$$
类似夏皮罗-斯蒂格利茨模型假定单位时间内工作中断概率为外生的 $\lambda$，且每次洽谈都会谈成，直接入职。那么有
$$
\dot{E(t)}=M(U(t),V(t))-\lambda E(t)
$$
假定匹配函数规模报酬不变，定义 $\theta(t)=V(t)/U(t)$，空缺除以失业的比率概括了劳动力市场的饱和程度， $\theta$ 越小竞争越激烈
$$
M(U(t),V(t))=U(t)M(1,\theta(t))\equiv U(t)m(\theta(t))
$$
其中 $m(\theta)\equiv M(1,\theta)$，根据 $M(\cdot)$ 的形式假设，$m(\theta)$ 是 $\theta$ 的增函数。

一般也仍然选择 CD 函数形式 $m(\theta)=k\theta^{\gamma},\quad k>0,0<\gamma<1$

- 工作觅得率 $a(t)=M(t)/U(t)=m(\theta(t))$，随 $\theta$ 递增；$a$ 越大，工人越有利

- 空缺填补率 $\alpha(t)=M(t)/V(t)=\dfrac{m(\theta(t))}{\theta(t)}$，随 $\theta$ 递减；$\alpha$ 越大，厂商越有利



**均衡**

同样类似夏皮罗-斯蒂格利茨模型的状态转移迭代过程、资产定价理解

多了自身状态的变动项($\dot{V(t)}$)是因为经济可能不处在稳态而产生的“资本收益”。夏皮罗模型只考虑稳态（？）

- $rV_E(t)=w(t)+\dot{V_E(t)}-\lambda[V_E(t)-V_U(t)]$

- $rV_U(t)=b+\dot{V_U(t)}+a(t)[V_E(t)-V_U(t)]$
- $rV_F(t)=[y-w(t)-c]+\dot{V_F(t)}-\lambda[V_F(t)-V_V(t)]$
- $rV_V(t)=-c+\dot{V_V(t)}+\alpha(t)[V_F(t)-V_V(t)]$

另外四个条件

- 使用 CD 函数形式的就业工人数量动态 $\dot{E(t)}=U(t)^{1-\gamma}V(t)^{\gamma}-\lambda E(t)$
- 纳什议价过程假设：工人获得匹配所得剩余中比例为 $\phi$ 的部分 $[V_E(t)-V_U(t)]/\phi=[V_F(t)-V_V(t)]/(1-\phi)$
- 新的职位空缺可以被随意创造或消除 $V_V(t)=0$
- 就业初始水平 $E(0)$ 给定



整合上述各式，并且令变动项 $\dot{V(t)}=0$ 可以得到 
$$
w=b+\dfrac{(a+\lambda+r)\phi}{\phi a+(1-\phi)a+\lambda+r}(y-b)
$$

$$
rV_V=-c+\dfrac{(1-\phi)a}{\phi a+(1-\phi)a+\lambda+r}(y-b)
$$

接下来要在 $(E,rV_V)$ 坐标系内确定就业水平

在稳态时 $\dot{E(t)}=0$，单位时间内新匹配数就等于中断岗位数 $\lambda E$。从而有

-  工作觅得率 $a=\dfrac{M(U,V)}{U}=\dfrac{\lambda E}{1-E}$ （因为 $E+U=1$ ），随 E 递增
- 空缺填补率 $\alpha =\dfrac{M(U,V)}{V}=k^{1/\gamma}(\lambda E)^{(\gamma-1)/\gamma}(1-E)^{(1-\gamma)/\gamma}$m，随 E 递减；其中 $V=K^{-1/\gamma}(\lambda E)^{1/\gamma}(1-E)^{-(1-\gamma)/\gamma}$







## 通货膨胀与货币政策



### 声誉模型



### 泰勒规则



## Present 技巧

- 怎么讲模型：讲故事、讲逻辑、核心链条，快速带到模型。需要假设读者都会基础模型，然后强调新模型扩展和放松的关键点
- 怎么讲实证：讲清楚识别策略，一定要因果关系（相关不算数）。
- PPT 不要很乱，就只要几个核心点。学业界大佬 PPT（学术/产品发布会）
- PPT 时间不够，不要语速加快，要有取舍的主动砍掉内容