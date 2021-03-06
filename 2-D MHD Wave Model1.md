[TOC]

#### **2-D MHD Wave Model**

##### **Start with the general equations & simplify**

###### Ideal MHD: A model for plasma as a perfectly conducting fluid:

- Mass density: $\rho$
- Current density: $\boldsymbol{J}$
- Fluid velocity: $\boldsymbol{v}$
- Kinetic pressure: $P$

**Ideal MHD equations:**
$$
\begin{aligned}
1)\quad &\frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \boldsymbol{v}) = 0 \qquad Mass \; conservation\\
2)\quad &\rho \frac{d \boldsymbol{v}}{dt} = \boldsymbol{J} \times \boldsymbol{B}- \nabla P \quad Momentum\; equation \Rightarrow  Plasma \; equilibrium \ \boldsymbol{J} \times \boldsymbol{B} = \nabla P\\
3)\quad &\mu_0 \ \boldsymbol{J} = \nabla \times \boldsymbol{B} \qquad \quad \; \;Ampere's \; Law \\
4)\quad &\frac{\partial \boldsymbol{B}}{\partial t} = -\nabla \times \boldsymbol{E} \quad \;\quad \; \;\,\,Faraday's \; Law   \\
5)\quad &\boldsymbol{E} +\boldsymbol{v} \times \boldsymbol{B} =0 \quad \;\quad \; \;\,\,\; Ohm's \;law \; (\sigma=\infin) \\
6)\quad &\frac{d}{dt}(\frac{P}{\rho^\gamma}) = 0 \qquad\qquad\;\;\, Equation\;of\;state\;(energy\;conservation) \;\; e.g.\;ideal\;gas\;law:PV = \rho KT  \\
7)\quad &\nabla \cdot \boldsymbol{B}=0 \qquad\qquad\quad \;\;\;No\;magnetic\;monopoles\;(definition\;of\;\boldsymbol{B})
\end{aligned}
$$

**Simplifications:**

*1) Linearization*
$$
\boldsymbol{B} = \boldsymbol{B_0}+\boldsymbol{B_1}(t)
$$
In fact, there are the similar linearization form for $\boldsymbol{v}$, $\boldsymbol{J}$, $\boldsymbol{E}$, $\rho$, $P$……  In order to remain linear, we need $|B_0| \gg |B_1|$ and $\rho_0 \gg \rho_1$ so that the effect of $\boldsymbol{B_1}(t)$ and $\boldsymbol{\rho_1 (t)}$ on the $Alf\acute{v}en \ speed \ v_A = \frac{B}{\sqrt{\mu_0 \rho}}$  can be neglected.

*2) Cold plasma* the fluid kinetic pressure is small enough to be neglected
$$
P \rightarrow 0
$$
Thus, for plasma equilibrium,
$$
\begin{aligned}
&\boldsymbol{J_0} = 0 \; ,since \; \boldsymbol{J_0} \times \boldsymbol{B_0} = \nabla P \\
\Rightarrow &\ \nabla \times \boldsymbol{B_0} =0   \\
\Rightarrow &\ \boldsymbol{B} = \nabla \gamma  \\
&\therefore \ \nabla \cdot \boldsymbol{B}=0 \Rightarrow \nabla^2\gamma = 0
\end{aligned}
$$
*3) Stationary plasma：*
$$
\boldsymbol{v_0}=\boldsymbol{0}  \Rightarrow \boldsymbol{E_0} = 0
$$
*4) 2D magnetic field:*
$$
\boldsymbol{B_0} = B_0(x,y) \ \hat{z}
$$
$\Rightarrow$ **"Box model" magnetic field**

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201019123024695.png" alt="image-20201019123024695" style="zoom:67%;" />

Then with these assumptions, we have:$P_1 = \rho_1 = 0$ (because of eq.6 with $P=0$)

To $1st$ order:
$$
\begin{aligned}
\frac{d\boldsymbol{v}}{dt}  &= \frac{{d(\boldsymbol{v_0} + \boldsymbol{v_1})}}{dt} \\
                            &= \frac{d \boldsymbol{v_1}}{dt} \\
                            &= \frac{\partial \boldsymbol{v_1}}{\partial t}+ \boldsymbol{v_1} \cdot \nabla\boldsymbol{v_1}  \\
                            &= \frac{\partial \boldsymbol{v_1}}{\partial t}\;\;(neglecting\; the \; 2rd\; order\; smallness)
\end{aligned}
$$
From eq.2 and eq.3, we can derive:
$$
\begin{aligned}
\rho \frac{\partial \boldsymbol{v_1}}{\partial t} =& \frac{1}{\mu_0}(\nabla \times \boldsymbol{B})\times \boldsymbol{B}\\
\rho \frac{\partial \boldsymbol{v_1}}{\partial t} =& \frac{1}{\mu_0}(\nabla \times (\boldsymbol{B_0}+\boldsymbol{B_1}))\times (\boldsymbol{B_0}+\boldsymbol{B_1})\\
\rho \frac{\partial \boldsymbol{v_1}}{\partial t} =& \frac{1}{\mu_0}
\{
(\nabla \times \boldsymbol{B_0}) \times  \boldsymbol{B_0} +
(\nabla \times \boldsymbol{B_0}) \times  \boldsymbol{B_1} +
(\nabla \times \boldsymbol{B_1}) \times  \boldsymbol{B_0} +
(\nabla \times \boldsymbol{B_1}) \times  \boldsymbol{B_1}
\}
\end{aligned}
$$

Considering the Cold plasma condition $\nabla \times \boldsymbol{B_0} =0$ and neglecting  $the \; 2rd\; order\; smallness$


$$
\begin{aligned}
\rho \frac{\partial \boldsymbol{v_1}}{\partial t} = \frac{1}{\mu_0}
\{
(\cancel{\nabla \times \boldsymbol{B_0})} &\times  \boldsymbol{B_0} +
(\cancel{\nabla \times \boldsymbol{B_0})} \times  \boldsymbol{B_1} +
(\nabla \times \boldsymbol{B_1}) \times  \boldsymbol{B_0} +
(\cancel{\nabla \times \boldsymbol{B_1}) \times  \boldsymbol{B_1}}
\}
\\
&\Rightarrow
\boxed{\rho \frac{\partial \boldsymbol{v_1}}{\partial t} = \frac{1}{\mu_0}
(\nabla \times \boldsymbol{B_1}) \times  \boldsymbol{B_0}}
\end{aligned}
$$
Cross the background magnetic field $\boldsymbol{B_0}$ on both sides of this formula ($\boldsymbol{\hat{z}}$ along the z axis)

<span style='color:pink'>(P.S. I think the there is a minus before the $v_A^2$ )</span>

$$
\begin{aligned}
	\frac{\partial \boldsymbol{v}_{\boldsymbol{1}}}{\partial t}\times \boldsymbol{B}_{\boldsymbol{0}}&=\frac{1}{\mu _0\rho}\left( \left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}} \right) \times \boldsymbol{B}_{\boldsymbol{0}} \right) \times \boldsymbol{B}_{\boldsymbol{0}}\quad \quad \text{Tips}:\left( \boldsymbol{A}\times \boldsymbol{B} \right) \times \boldsymbol{B}=\left( \boldsymbol{A}\cdot \boldsymbol{B} \right) \boldsymbol{B}-\left( \boldsymbol{B}\cdot \boldsymbol{B} \right) \boldsymbol{A}\\
	&=\frac{1}{\mu _0\rho}\left( \left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}} \right) \cdot \boldsymbol{B}_{\boldsymbol{0}} \right) \boldsymbol{B}_{\boldsymbol{0}}-B_{0}^{2}\left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}} \right) \\
	&=-\frac{B_{0}^{2}}{\mu _0\rho}\left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}}-\frac{\left( \left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}} \right) \cdot \boldsymbol{B}_{\boldsymbol{0}} \right)}{B_{0}^{2}}\boldsymbol{B}_{\boldsymbol{0}} \right)\\
	&=-\frac{B_{0}^{2}}{\mu _0\rho}\left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}}-\frac{\left( |\nabla \times \boldsymbol{B}_{\boldsymbol{1}}| |\cancel{\boldsymbol{B}_{\boldsymbol{0}}|}cos\theta  \right) \cancel{|\boldsymbol{B}_{\boldsymbol{0}}|}\boldsymbol{\hat{z}}}{\cancel{B_{0}^{2}}} \right)\\
	&=-\frac{B_{0}^{2}}{\mu _0\rho}\left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}}-|\nabla \times \boldsymbol{B}_{\boldsymbol{1}}| cos\theta  \right) \boldsymbol{\hat{z}}\\
	&=-\frac{B_{0}^{2}}{\mu _0\rho}\left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}}-\left( \left( \nabla \times \boldsymbol{B}_{\boldsymbol{1}} \right) \cdot \{\hat{z} \right) \boldsymbol{\hat{z}}\}\right)\\
	&=-\,\,v_{A}^{2}\left( \nabla _{\bot}\times \boldsymbol{B}_{\boldsymbol{1}} \right)\\
	\Rightarrow \frac{\partial \boldsymbol{v}_{\boldsymbol{1}}}{\partial t}\times \boldsymbol{B}_{\boldsymbol{0}}&=-v_{A}^{2}\,\,\left( \left( \frac{\partial B_{1z}}{\partial y}-\frac{\partial B_{1y}}{\partial z} \right) \boldsymbol{\hat{x}}+\left( \frac{\partial B_{1x}}{\partial z}-\frac{\partial B_{1z}}{\partial x} \right) \boldsymbol{\hat{y}} \right)\\
\end{aligned}
$$

*x - component*
$$
\begin{aligned}
 \frac{\partial \boldsymbol{v_1}}{\partial t} \times \boldsymbol{B_0} \cdot \boldsymbol{\hat{x}}& = -\ v_A^2\ \big((\frac{\partial B_{1z}}{\partial y}-\frac{\partial B_{1y}}{\partial z}) \boldsymbol{\hat{x}} \cdot \boldsymbol{\hat{x}}
    \big)
    \\
    \boldsymbol{\hat{x}} \times \frac{\partial \boldsymbol{v_1}}{\partial t} \cdot \boldsymbol{B_0} & = -\ v_A^2\ \big(\frac{\partial B_{1z}}{\partial y}-\frac{\partial B_{1y}}{\partial z}
    \big) \\
\end{aligned}
$$

$$
\boxed{ B_0 \frac{\partial v_{1y}}{\partial t}  = -\ v_A^2\ \big(\frac{\partial B_{1z}}{\partial y}-\frac{\partial B_{1y}}{\partial z}
    \big)} \tag{8}
$$

*y - component*
$$
\begin{aligned}
 \frac{\partial \boldsymbol{v_1}}{\partial t} \times \boldsymbol{B_0} \cdot \boldsymbol{\hat{y}}& = -\ v_A^2\ \big((\frac{\partial B_{1x}}{\partial z}-\frac{\partial B_{1z}}{\partial x}) \boldsymbol{\hat{y}} \cdot \boldsymbol{\hat{y}}
    \big)
    \\
    \boldsymbol{\hat{y}} \times \frac{\partial \boldsymbol{v_1}}{\partial t} \cdot \boldsymbol{B_0} & = -\ v_A^2\ \big(\frac{\partial B_{1x}}{\partial z}-\frac{\partial B_{1z}}{\partial x}
    \big) \\
\end{aligned}
$$

$$
\boxed{ B_0 \frac{\partial v_{1x}}{\partial t}  = +\ v_A^2\ \big(\frac{\partial B_{1x}}{\partial z}-\frac{\partial B_{1z}}{\partial x}
    \big) }  \tag{9}\\
$$

Faraday's law: $\frac{\partial \boldsymbol{B_1}}{\partial t} = -\nabla \times \boldsymbol{E}$ and Ohm's law:$\boldsymbol{E}+\boldsymbol{v_1} \times \boldsymbol{B_0} =0 \Rightarrow E_x = -v_{1y} B_0 \ \& \ E_y = v_{1x}B_0$ based on those assumptions mentioned above in **linear cold stationary plasma**.

If we expand the Faraday's law:
$$
\begin{aligned}
&(\frac{\partial B_{1x}}{\partial t},\frac{\partial B_{1y}}{\partial t},\frac{\partial B_{1z}}{\partial t}) \\
 =   &- \left| \begin{matrix}
	\hat{i}&		\hat{j}&		\hat{k}\\
	\frac{\partial}{\partial x}&		\frac{\partial}{\partial y}&		\frac{\partial}{\partial z}\\
	E_x&		E_y&		E_z\\
\end{matrix} \right| \\
= &- (\ \frac{\partial E_z}{\partial y}-\frac{\partial E_y}{\partial z},\ \frac{\partial E_x}{\partial z}-\frac{\partial E_z}{\partial x},\ \frac{\partial E_y}{\partial x}-\frac{\partial E_x}{\partial y} \ )
 \end{aligned}
$$
Then we can get the formula in component form considering the $E_z = 0$:

<span style='color:pink'>(P.S. I think the there is a minus before the $B_0$ in equation (10) & (11))</span>


$$
\begin{aligned}
x - compoent: \frac{\partial B_{1x}}{\partial t} &= \frac{\partial E_y}{\partial z}= +B_0 \frac{\partial v_{1x}}{\partial z}   \tag{10}
\end{aligned}
$$

$$
\begin{aligned}
y - compoent: \frac{\partial B_{1y}}{\partial t} &= -\frac{\partial E_x}{\partial z}= +B_0 \frac{\partial v_{1y}}{\partial z}   \tag{11}
\end{aligned}
$$

$$
\begin{aligned}
z - compoent: \frac{\partial B_{1z}}{\partial t} &= -(\frac{\partial E_y}{\partial x}-\frac{\partial E_x}{\partial y}) = -(\frac{\partial (B_0v_{1x})}{\partial x}+\frac{\partial (B_0v_{1y})}{\partial y})   \tag{12}
\end{aligned}
$$

$\frac{\partial}{\partial t}(8)\ \& \ (11) \ \Rightarrow$
$$
\begin{aligned}
\frac{1}{v_A^2} \frac{\partial^2v_{1y}}{\partial t^2} = - \frac{1}{B_0}\Big(\frac{\partial}{\partial y}\big( \frac{\partial B_{1z}}{\partial t}\big)-\frac{\partial}{\partial z}\big( \frac{\partial B_{1y}}{\partial t}\big)\Big) \\
\frac{1}{v_A^2} \frac{\partial^2v_{1y}}{\partial t^2} = - \frac{1}{B_0}\Big(\frac{\partial}{\partial y}\big( \frac{\partial B_{1z}}{\partial t}\big)- B_0\frac{\partial^2 v_{1y}}{\partial z^2}\Big) \\
\end{aligned}
$$

$$
\boxed{ \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)v_{1y} = + \frac{1}{B_0}\frac{\partial}{\partial y}\big( \frac{\partial B_{1z}}{\partial t}\big)} \tag{13}
$$

$\frac{\partial}{\partial t}(9)\ \& \ (10) \ \Rightarrow$

$$
\begin{aligned}
\frac{1}{v_A^2} \frac{\partial^2v_{1x}}{\partial t^2} = + \frac{1}{B_0}\Big(\frac{\partial}{\partial z}\big( \frac{\partial B_{1x}}{\partial t}\big)-\frac{\partial}{\partial x}\big( \frac{\partial B_{1z}}{\partial t}\big)\Big) \\
\frac{1}{v_A^2} \frac{\partial^2v_{1y}}{\partial t^2} = + \frac{1}{B_0}\Big( \frac{\partial^2 v_{1x}}{\partial z^2}- \frac{\partial}{\partial x}\big( \frac{\partial B_{1z}}{\partial t}\big)\Big) \\
\end{aligned}
$$

$$
\boxed{ \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)v_{1x} = + \frac{1}{B_0}\frac{\partial}{\partial x}\big( \frac{\partial B_{1z}}{\partial t}\big)} \tag{14}
$$

Thus, using the equation (12):

$$
\boxed{ \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)
\left( \begin{array}{c}
	v_{1x}\\
	v_{1y}\\
\end{array} \right)
= -\frac{1}{B_0}
\left( \begin{array}{c}
	\partial/\partial x\\
	\partial/\partial y\\
\end{array} \right)
\Big( \frac{\partial (B_0v_{1x})}{\partial x}+\frac{\partial (B_0v_{1y})}{\partial y}\Big)} \tag{15}
$$

##### **The "box" model**

In the "box" model, assume $\boldsymbol{B_0} = \boldsymbol{B_0}(x,y)$, hence the unperturbed field lines are all straight lines of equal length(say from $z = -z_{ion}$ to $z_{ion}$). <span style='color:pink'>If the ionospheric conductivity is very large ($\rightarrow \infin$). Then the $E$ (and $v_1$) are zero at ionosphere</span>

$\Rightarrow$ Oscillations are standing waves with natural frequencies and wavelengths: $k_n = \frac{\pi n}{2z_{ion}},n=1,2,3\cdots$

$\Rightarrow$ Let $\boldsymbol{v_1}=\sum^N_{n=1}\boldsymbol{v_{1n}}(x,y,t)exp(ik_nz)$      $\therefore \frac{\partial^2}{\partial z^2}\rightarrow -k_n^2$

<img src="F:\Work_process\geophysics\Alex_simulation\notes\figure\image-20201019195117736.png" alt="20201019195117736" style="zoom:80%;" />


If an external driver is applied at a specific frequency $\omega$, then resonance occurs at locations where $\omega^2 = k^2_nv^2_A(x,y)=\omega^2_n(x,y) \Rightarrow FLRs$

You used these equations in your 2D MHD wave model(with $n=\pm 1$, expressed in terms of  $\boldsymbol{E}$ instead of $\boldsymbol{v_1}$ in the following JGR papers: *Degeling et al. 2011, 2013 and 2014*

Actually,  we can express these as a single PDE for $B_{1z}$ for the case of continuously driven waves at frequency $\omega$:

Firstly, note that: $\boldsymbol{v_1}=\frac{\partial \boldsymbol{\xi}}{\partial t}$, the $\boldsymbol{\xi}$ represents the field line displacement

Then equation (12) - (14) give:
$$
\begin{aligned}
&B_{1z} = -\Big(\frac{\partial (B_0 \xi_x)}{\partial x} + \frac{\partial (B_0 \xi_y)}{\partial y} \Big)   \tag{16}\\
& \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^\textcolor[rgb]{1,0,0}{2}}{\partial t^2}\Big)(B_0 \xi_x)
= + \frac{\partial}{\partial x} B_{1z}    \tag{17} \\
& \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^\textcolor[rgb]{1,0,0}{2}}{\partial t^2}\Big)(B_0 \xi_y)
= + \frac{\partial}{\partial y} B_{1z}    \tag{18} \\
\end{aligned}
$$
Now apply the operator $\Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)$ to both sides of equations (16):
$$
\Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big) \boldsymbol{B_{1z}} = -\Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)\Big(\frac{\partial (B_0 \xi_x)}{\partial x} + \frac{\partial (B_0 \xi_y)}{\partial y} \Big)   \tag{19}
$$
For continuously driven waves of frequency $\omega_1$ let solutions for $B_{1z}$, $\xi_x$ and $\xi_y$ have the form:

<span style='color:pink'>(P.S. I don't know why the solutiona have this kind of form)</span>
$$
F(x,y,z,t) = f(x,y)cos(k_\parallel z)exp(-i\omega t)
$$
Then:
$$
\begin{aligned}
\Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big)\ F &=
\ \Big(\frac{\partial^2}{\partial z^2}-\frac{1}{v_A^2}\frac{\partial^2}{\partial t^2}\Big) \big(f(x,y)cos(k_\parallel z)exp(-i\omega t) \big) \\
 & =\ -(k_\parallel^2 - \frac{\omega^2}{v_A^2})\;F
\end{aligned}
$$
Let $k_\parallel^2 - \frac{\omega^2}{v_A^2} = K^2(x,y)$. Then the equation (19) becomes:
$$
\begin{aligned}
K^2 B_{1z} &= -\Big(K^2 \frac{\partial (B_0 \xi_x)}{\partial x} + K^2\frac{\partial (B_0 \xi_y)}{\partial y}\Big) \\
           &= -\Big( \frac{\partial }{\partial x}(K^2B_0 \xi_x) +
           \frac{\partial }{\partial y}(K^2B_0 \xi_y) -
           2K \Big( \frac{\partial K}{\partial x}B_0\xi_x+\frac{\partial K}{\partial y}B_0\xi_y\Big)\Big) \\
           &= -\Big( \frac{\partial }{\partial x}(K^2B_0 \xi_x) +
           \frac{\partial }{\partial y}(K^2B_0 \xi_y) -
           \frac{2}{K} \Big( \frac{\partial K}{\partial x}K^2B_0\xi_x+\frac{\partial K}{\partial y}K^2B_0\xi_y\Big)\Big) \\
\end{aligned}
$$
And equations (17) & (18) give:
$$
K^2B_0 \xi_x = - \frac{\partial}{\partial x} B_{1z} \tag{20}\\
$$
$$
K^2B_0 \xi_y = - \frac{\partial}{\partial y} B_{1z} \tag{21}
$$

Thus

$$
\boxed{
\textcolor{#3E9EBC}{
\Big(\frac{\partial^2}{\partial x^2} +\frac{\partial^2}{\partial y^2}-
\frac{2}{K}\big(\frac{\partial K}{\partial x}\frac{\partial}{\partial x}+\frac{\partial K}{\partial y}\frac{\partial}{\partial y}\big)}
-\textcolor{#3E9EBC}{K^2 \Big) B_{1z}= 0
}
}
\tag{22}
$$
This 2D elliptic PDE for $B_{1z}$ can be solved using the *Matlab PDE-toolbox*

*Note*: The PDE is singular where $K(x,y)=0$ (This is where FLRs occur!)

To remove the singularity, we add a small dissipative term to $\omega$, i.e. <span style='color:red'>$\omega \rightarrow \omega(1 + i \gamma)$</span> to mimic the effect of finite ionospheric conductivity in damping the wave.

As a first step, let's use a circular inner and outer boundary for the equatorial plane:

<img src="C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201020092516872.png" alt="image-20201020092516872" style="zoom:70%;" />

**Boundary condition:**

- **Inner b.c.** : $\boldsymbol{n} \cdot \nabla B_{1z} = 0$ where $\boldsymbol{n} = cos\phi\hat{\boldsymbol{x}}+sin\phi \hat{\boldsymbol{y}}$, $\phi = tan^{-1}(\frac{y_{in}}{x_{in}})$, $R_{in}=(x_{in}^2+y_{in}^2)^{\frac{1}{2}}$    <span style='color:blue'>(This is a "Neuman" b.c.)</span>

- **Outer b.c.**: Let
  $$
  B_{1z}(x_{out},y_{out})=\sum^M_{m=-M} A_m\ exp\big(i(m(\phi_{out}+\phi_{in})-\omega t) \big)
  $$
  where $\omega$, $A_m$ & $\phi_m$ are inputs. And $\phi_{out} = tan^{-1}(\frac{y_{out}}{x_{out}})$ with $R_{out}^2 = x_{out}^2+y_{out}^2$   <span style='color:blue'>(This is a "Diriclet" b.c.)</span>



#### Make a 2D model for MHD waves in box model using *matlab* *PDE toolbox*

Sorry for I can't finish the exercise for me about making a 2D model for MHD waves, using a "box" model magnetic field you mentioned in the e-mail.

 I have learned something about *PDE toolbox*, but there are still some problems that I have not solve.

- Partial Differential Equation Toolbox solves scalar equations of the form:

$$
m\frac{\partial^2 u}{\partial t^2} + d \frac{\partial u}{\partial t} - \nabla \cdot (c \nabla u) + au = f
$$

And I need to solve this equation:
$$
\Big(\frac{\partial^2}{\partial x^2} +\frac{\partial^2}{\partial y^2}-
\frac{2}{K}\big(\frac{\partial K}{\partial x}\frac{\partial}{\partial x}+\frac{\partial K}{\partial y}\frac{\partial}{\partial y}\big)
-
K^2 \Big) B_{1z}= 0
$$
<span style='color:pink'>I have no way to find the parameters $m$, $d$, $c$, $a$ and $f$.</span>

**Supplement**:
$$
\begin{aligned}
& u = B_{1z} \\
& m=d=0  \rightarrow  We\; will\; first\; solve\; the\; "elliptic"\; problem.  \\
& c=-1 \\
& a=-K^2=-k_\parallel + \frac{\omega^2}{v_A^2} \quad k_\parallel=\frac{\Pi}{L_{f.l.}} \;where \; L_{f.l.} \approx  10R_E  \quad and \quad v_A^2 = \frac{B_0^2(x,y)}{\mu_0 \rho(x,y)}\\
& f=\frac{2}{K}\big(\frac{\partial K}{\partial x}\frac{\partial u}{\partial x} + \frac{\partial K}{\partial y}\frac{\partial u}{\partial y} \big)
\end{aligned}
$$

#### Simplicity for the equation (22) further

Equation (16):
$$
B_{1z} = -\Big(\frac{\partial (B_0 \xi_x)}{\partial x} + \frac{\partial (B_0 \xi_y)}{\partial y} \Big)   \tag{16}\\
$$
Equation (20) and (21)
$$
K^2B_0 \xi_x = - \frac{\partial}{\partial x} B_{1z} \tag{20}\\
$$

$$
K^2B_0 \xi_y = - \frac{\partial}{\partial y} B_{1z} \tag{21}
$$

Then
$$
\Big(\frac{\partial}{\partial x}\big( \frac{1}{K^2} \frac{\partial}{\partial x}\big) + \frac{\partial}{\partial y}\big( \frac{1}{K^2} \frac{\partial}{\partial y}\big) - 1 \Big)B_{1z}=0  \tag{22}
$$
Let $B_{1z} = e^{i\lambda y}\quad \& \quad K^2 = K^2(x)$. Thus:
$$
\Big(\frac{\partial}{\partial y}\big( \frac{1}{K^2} \frac{\partial}{\partial y}\big) - \frac{K^2+\lambda}{K^2} \Big)B_z = 0
$$
The PDE toolbox solves equations of the form:
$$
m\frac{\partial^2 u}{\partial t^2} + d \frac{\partial u}{\partial t} - \nabla \cdot (c \nabla u) + au = f
$$
Hence for equation (22) we have
$$
a = -1, \quad f=0, \quad, m=0,\quad d=0, \quad c = -\frac{1}{K^2}
$$
Cheers,

Niu Zhe.

2020/10/20
