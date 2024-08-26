# Solutions to Modern Quantum Chemistry

## Chapter 1 Mathematical Review

### 1.1

Based on the definition of matrix-vector multiplication, the conclusions are obvious.

###  1.2

Note that
$$
\begin{align*}
\mathbf{A}\mathbf{B} = \left(
\begin{matrix}
1&-1&0\\
-1&0&0\\
0&0&-1\\
\end{matrix}
\right) = \mathbf{B}\mathbf{A}
\end{align*}
$$
thus
$$
\left[\mathbf{A}, \mathbf{B}\right] = 0
$$
which implies that $\mathbf{A}$ and $\mathbf{B}$ are commutable.
$$
\left\{\mathbf{A}, \mathbf{B}\right\} = 2\mathbf{A}\mathbf{B}
$$

### 1.3

Since
$$
\left(\mathbf{AB}\right)_{ij} = \sum_k \mathbf{A}_{ik}\mathbf{B}_{kj}
$$
thus
$$
\left(\mathbf{AB}\right)^{\dagger}_{ji} &= \sum_k \mathbf{A}_{kj}\mathbf{B}_{ik} \\
&= \sum_k \mathbf{B}_{ik}^\star\mathbf{A}_{kj}^\star \\
&= \left(\mathbf{B}^{T\star}\mathbf{A}^{T\star}\right)_{ji} \\
&= \left(\mathbf{B}^{\dagger}\mathbf{A}^\dagger\right)_{ji}
$$


which implies
$$
\left(\mathbf{AB}\right)^{\dagger}= \mathbf{B}^{\dagger}\mathbf{A}^{\dagger}
$$


### 1.4

#### a

Assume $\mathbf{A}$ and $\mathbf{B}$ has dimensions $M\times N$and $N \times M$ ,
$$
\begin{align}
\mbox{tr}\mathbf{AB} &=\sum_i^M\left(\mathbf{AB}\right)_{ii} \\
&= \sum_i^M \left(\sum_j^N \mathbf{A}_{ij}\mathbf{B}_{ji}\right)_{ii}\\
&= \sum_j^N \left(\sum_i^M \mathbf{B}_{ji}\mathbf{A}_{ij}\right)_{jj}\\
&= \mbox{tr} \mathbf{BA}
\end{align}
$$

#### b

$$
\begin{align}
\mathbf{B}^{-1}\mathbf{A}^{-1}\mathbf{AB} &= \mathbf{B}^{-1}\mathbf{IB} \\
&= \mathbf{I} \\
&= \left(\mathbf{AB}\right)^{-1}\mathbf{AB}
\end{align}
$$

which implies
$$
\mathbf{AB}^{-1} = \mathbf{B}^{-1}\mathbf{A}^{-1}
$$


#### c

$$
\begin{align}
\mathbf{B} &= \mathbf{U}^{\dagger}\mathbf{AU} \\
\mathbf{UB} &= \mathbf{UU}^\dagger\mathbf{AU} = \mathbf{AU} \\
\mathbf{UBU}^\dagger &= \mathbf{AUU}^\dagger = \mathbf{A}
\end{align}
$$

#### d

$$
\begin{align}
\mathbf{C} &= \mathbf{C}^{\dagger} \\
&= \mathbf{AB} \\
\mathbf{C}^\dagger &= \left(\mathbf{AB}\right)^\dagger \\
&= \mathbf{B}^\dagger\mathbf{A}^\dagger \\
&= \mathbf{B}\mathbf{A} \\
\end{align}
$$

then
$$
\mathbf{AB} = \mathbf{BA}
$$
or
$$
\left[\mathbf{A}, \mathbf{B}\right] = 0
$$

#### e

$$
\begin{align*}
\left(\mathbf{A}^{-1}\right)^{\dagger} &= \left(\mathbf{A}^{-1}\right)^\dagger\mathbf{I} \\
&= \left(\mathbf{A}^{-1}\right)^{\dagger}\mathbf{AA}^{-1} \\
&= \left(\mathbf{A}^{-1}\right)^{\dagger}\mathbf{A}^\dagger A^{-1} \\
&= \left(\mathbf{AA}^{-1}\right)^{\dagger} A^{-1} \\
&= \mathbf{A}^{-1}
\end{align*}
$$

#### f


$$
\begin{align}
\left(
\begin{array}{c}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{array}
\right)\cdot
\left(
\begin{array}{c}
A_{22} & -A_{12} \\
-A_{21} & A_{11}
\end{array}
\right)
&=
\left(
\begin{array}{c}
A_{11}A_{22} -A_{12}A_{21} & -A_{11}A_{12} + A_{12}A_{11} \\
A_{21}A_{22} -A_{22}A_{21} & -A_{21}A_{12} + A_{22}A_{11} \\
\end{array}
\right) \\
&=
\left(
A_{11}A_{22} - A_{12}A_{21}
\right)\mathbf{I} \\
\end{align}
$$

### 1.5

Omitted.

### 1.6

#### 6

Denote $\hat{\mathbf{P}}_{ij}$ to be the operator that swaps row $i$ and $j$ in a determinant. If a determinant $|\mathbf{D}|$ has row $k$ and $l$ equal, then
$$
|\hat{\mathbf{P}}_{kl}\mathbf{D}| = |\mathbf{D}|
$$
Apply property 3 to $\mathbf{D}$:
$$
|\hat{\mathbf{P}}_{kl}\mathbf{D}| = -|\mathbf{D}|
$$
it is obvious that $\mathbf{D}=0$.

#### 7

$$
\begin{align*}
|\mathbf{A}^{-1}||\mathbf{A}| &= 1 \\
|\mathbf{A}|^{-1}|\mathbf{A}| &= 1 \\
\end{align*}
$$

#### 8

$$
\begin{align*}
|\mathbf{AA}^\dagger| &= |\mathbf{A}||\mathbf{A}^\dagger| \\
&= |\mathbf{A}||\mathbf{A}|^\star \\
&= 1
\end{align*}
$$

#### 9

$$
\begin{align*}
|\mathbf{O}| &= |\mathbf{U}^\dagger||\mathbf{U}||\mathbf{O}|\\
&= |\mathbf{U}^\dagger||\mathbf{O}||\mathbf{U}| \\
&= |\mathbf{U}^\dagger\mathbf{O}\mathbf{U}| \\
&= |\mathbf{\Omega}|
\end{align*}
$$

### 1.7

Assume $|\mathbf{A}|\neq 0$ , then $|\mathbf{A}^{-1}|\neq 0$ 
$$
\begin{align*}
\mathbf{A}\vec{c}&=\mathbf{0} \\
\mathbf{A}^{-1}\mathbf{A}\vec{c} &= \mathbf{0}\\
\vec{c} &= \mathbf{0}
\end{align*}
$$

### 1.8

$$
\begin{align*}
\mbox{tr}\mathbf{\Omega} &= \mbox{tr}\left(\mathbf{U}^\dagger\mathbf{OU}\right) \\
&= \mbox{tr}\left(\mathbf{UU}^\dagger\mathbf{O}\right) \\
&= \mbox{tr}\left(\mathbf{IO}\right) \\
&= \mbox{tr}\mathbf{O}
\end{align*}
$$

### 1.9

Note the $i$ -th column of the matrix $\mathbf{U}$ as $\mathbf{U}_i$,
$$
\begin{align*}
\mathbf{U}_i\mathbf{\omega} &= \left(\mathbf{c}^1\omega_1\ \mathbf{c}^2\omega_2\cdot\cdot\cdot\mathbf{c}^N\omega_N \right)
\end{align*}
$$
and
$$
\begin{align*}
\mathbf{OU} &= \left(\mathbf{Oc}^1\ \mathbf{Oc}^2\ \cdot\cdot\cdot\ \mathbf{Oc}^N\right)
\end{align*}
$$
The proposition is obvious by comparing the columns.

### 1.10

It can be seen that
$$
\frac{\omega-O_{11}}{O_{12}} = c = \frac{O_{21}}{\omega - O_{22}}
$$
or
$$
\omega^2-(O_{11}+O_{22})\omega+(O_{12}O_{21}-O_{11}O_{22}) = 0
$$
and the two roots of the equation are
$$
\begin{align*}
\omega = \frac{1}{2}\left[O_{11} + O_{22} \pm \sqrt{\left(O_{11}-O_{22}\right)^2-4O_{12}O_{21}}\right]
\end{align*}
$$
which is the same to Eq. (1.94)

### 1.11

Omitted.

### 1.12

#### a

$$
\begin{align*}
|\mathbf{A}^n| &= |\mathbf{U}\mathbf{A}\mathbf{U}^\dagger\mathbf{U}\mathbf{A}\mathbf{U}^\dagger\mathbf{U}\cdot\cdot\cdot\mathbf{A}\mathbf{U}^\dagger| \\
&= |\mathbf{U}^\dagger\mathbf{A}\mathbf{U}|^n \\
&= |\mathbf{a}|^n \\
&= \prod _i^N a_i^n
\end{align*}
$$

#### b

$$
\begin{align*}
\mbox{tr}\mathbf{A}^n &= \mbox{tr}\left(\mathbf{UAU}^\dagger\right)^n \\
&= \mbox{tr}\mathbf{a}^n \\
&= \sum_i^N a_i^n
\end{align*}
$$

#### c

TBD

### 1.13

TBD

### 1.14


$$
\begin{align*}
v &= \int_{-\infty}^{\infty}\mbox{d}x\cdot a(x)\delta(x) \\
&= \lim_{\varepsilon\rightarrow 0}\int_{-\varepsilon}^{\varepsilon}\mbox{d}x\cdot a(x)\frac{1}{2\varepsilon} \\
\end{align*}
$$
Denote $a_{min}$ and $a_{max}$ the minimum and maximum value of $a$ in $\left[-\varepsilon, \varepsilon\right]$, 
$$
\begin{align*}
2\varepsilon a_{min}\leq \int_{-\varepsilon}^{\varepsilon}\mbox{d}x\cdot a(x) < 2\varepsilon a_{max}
\end{align*}
$$
or
$$
\begin{align*}
a(0) = \lim_{\varepsilon\rightarrow 0} a_{min} \leq v \leq \lim_{\varepsilon\rightarrow 0} a_{max} = a(0)
\end{align*}
$$

### 1.15

$$
\begin{align*}
\mathcal{O}|i\rangle &= \sum_j |j\rangle O_{ji} \\
\langle k|\mathcal{O}|i\rangle &= \delta(k - j)O_{ji} \\
\langle k|\mathcal{O}|i\rangle &= O_{ki} \\
O_{ji} &= \langle j | \mathcal{O} | i \rangle
\end{align*}
$$

### 1.16

$$
\begin{align*}
\mathcal{O}|\psi\rangle &= \omega|\psi\rangle \\
\mathcal{O}\sum_i|\phi_i\rangle\langle\phi_i|\psi\rangle &= \sum_i|\phi_i\rangle\langle\phi_i|\psi\rangle\omega \\
\mathcal{O}\sum_ic_i|\phi_i\rangle &=\sum_ic_i|\phi_i\rangle\omega \\
\langle\phi_j|\mathcal{O}|\phi_i\rangle\vec{c}&=\omega\vec{c} \\
\mathbf{O}\vec{c}&=\omega\vec{c}
\end{align*}
$$

### 1.17

#### a

$$
\begin{align*}
\langle i|\left(\int\mbox{d}x|x\rangle\langle x|\right)|j\rangle &= \int\mbox{d}x \left(\langle x | i \rangle\right)^\star \langle x | j \rangle \\
&= \int\mbox{d}x \psi_i^\star\psi_j
\end{align*}
$$

#### b

$$
\begin{align*}
\langle x | \sum_i|i\rangle\langle i|x'\rangle &= \sum_i \langle x | i \rangle \langle i | x'\rangle \\
&= \sum_i\psi_i(x)\psi_i^*(x') \\
\end{align*}
$$

#### c

TBD

### 1.18

Note that the trial function is a Gaussian basis. Normalization factor:
$$
\begin{align*}
\langle \tilde\Phi | \tilde\Phi \rangle &= \int_{-\infty}^{\infty}N^2\mathbf{e}^{-2ax^2}\mbox{d}x\\
&= \frac{N^2}{\sqrt{2a}}\int_{-\infty}^{\infty}\mathbf{e}^{-ax^2}\mbox{d}x \\
&= N^2\sqrt\frac{\pi}{2a}
\end{align*}
$$
It can be easily observed that $N$ will be canceled out:
$$
\begin{align*}
\Epsilon &\leq \frac{\langle \tilde\Phi|\hat{\mathbf{H}}|\tilde\Phi\rangle}{\langle \tilde\Phi | \tilde\Phi \rangle}\\
&= \sqrt{\frac{2a}{\pi}}\cdot \langle\mathbf{e}^{-ax^2}|\hat{\mathbf H}|\mathbf{e}^{-ax^2}\rangle \\
&=\sqrt\frac{2a}{\pi}\int_{-\infty}^{\infty}\left[-\frac{1}{2}\frac{\mbox{d}^2}{\mbox{d}x^2}\mathbf{e}^{-ax^2}- \delta(x)\right]\mathbf{e}^{-ax^2}\mbox{d}x\\
&=\sqrt\frac{2a}{\pi}\left[a\int_{-\infty}^\infty\mbox{d}x\ \mathbf{e}^{-2ax^2}(1-2ax^2)- 1\right]\\
&=\sqrt\frac{2a}{\pi}\left[a\left(\sqrt{\frac{\pi}{2a}}-\frac{1}{2}\sqrt{\frac{\pi}{2a}}\right)-1\right]\\
&=\frac{a}{2}-a^\frac{3}{2}\sqrt\frac{2}{\pi}
\end{align*}
$$
The minimum is
$$
\pi^{-1}
$$
when
$$
a=\frac{2}{\pi}
$$

#### 1.19

From 1.18, the norm of the trial basis is
$$
\langle\tilde\Psi|\tilde\Psi\rangle = N^2\sqrt\frac{\pi}{2a}
$$
And
$$
\nabla^2\equiv \frac{1}{r^2}\frac{\mbox{d}}{\mbox{d}r}\left(r^2\frac{\partial}{\partial r}\right)+\frac{1}{r^2\sin\theta}\left(\sin\theta\frac{\partial f}{\partial \theta}\right)+\frac{1}{r^2\sin^2\theta}\frac{\partial}{\partial\varphi}
$$

$$
\begin{align*}
\nabla^2|\tilde\Psi\rangle &= \frac{\mbox{d}}{r^2\mbox{d}r} \left( r^2 \frac{\mbox{d}|\tilde\Psi\rangle} {\mbox{d}r}\right) \\
&= \frac{\mbox{d}}{r^2\mbox{d}r}\left(-2aNr^3\cdot \mathbf{e}^{-ar^2}\right) \\
&= 2aN(-3+2ar^2)\mathbf{e}^{-ar^2}
\end{align*}
$$

$$
\begin{align*}
\langle \tilde\Psi |-\frac{1}{2}\nabla^2 | \tilde\Psi \rangle &= -\int_{0}^{\infty}\mbox{d}r\cdot aN^2(-3+2ar^2)\mathbf{e}^{-2ar^2}
\end{align*}
$$

