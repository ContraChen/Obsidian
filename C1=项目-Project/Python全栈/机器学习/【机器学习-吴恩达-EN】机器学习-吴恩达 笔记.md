## Machine learning-Andrew Ng
#area/cs #src/p/吴恩达  #end
## 1 Introduction

### 1-1 Welcome
**machine learning**

- Grow out of work in AI
- New capability for computer

**Examples**

- Database mining

- Applications can't program by hand

- Self-customizing programs 

- Understanding human learning (brain,real AI)

### 1-2 What is machine learning
**Definition**

Arthur Samuel (1959)

Tom Mitchell (1998)

​	T task

​	P performance measure

​	E experience

**Machine learning algorithms**

- Supervised learning

- Unsupervised learning

  **others :**

  ​	Reinforcement learning

  ​	recommender learning

  **Also talk about:**

  ​	Practical advice for applying learning algorithms

### 1-3 Supervised learning

​	"right answers" given

**Regression Problem** predict continuous valued output

**Classification Problem** Discrete valued output

### 1-4 Unsupervised learning

 **Clustering algorithm** 聚类算法

**Cocktail party problem** 鸡尾酒会问题

Octave 软件

```octave
[W,s,v]=svd((repmat(sum(x.*x,1),size(x,1),1).*x)*x');	//svd是奇异值分解函数
```



## 2 Linear regression with one variable

### 2-1 Model representation

**Training set**

**m** = Number of training examples

**x's** = "input" variable/features

**y's** = "output" variable/"target" variable

**(x,y)** = one training example

**Hypothesis** 假设函数
$$
h_\theta (x)=\theta_0+\theta_1 x
$$
![](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210728151820956.png)

### 2-2 Cost Function

Goal: **minimize** 
$$
\frac{1}{2m}\sum_{1}^{m}(h_\theta(x^{(i)}-y^{(i)})^2
$$
> 除以m是使得误差平均到每个样本，除以2是一个微积分技巧，用于消除计算偏导数时出现的2。

**Cost Function**(Square error function )
$$
J(\theta_0,\theta_1)=\frac{1}{2m}\sum_{i=1}^{m}(h_\theta(x^{(i)}-y^{(i)})^2
$$

### 2-3  Cost Function Intuition I

**Simplified**

$\theta_0=0$

### 2-4 Cost Function Intuition II

**Contour plot/figure** 等高线图

### 2-5 Gradient descent

**Outline**

- Start with some $\theta_0,\theta_1$

- Keep changing  $\theta_0,\theta_1$ to reduce  $J(\theta_0,\theta_1)$ 

  until we hopefully end up with a minimum

**Gradient descent algorithm**

repeat until convergence{

$\theta_j := \theta_j-\alpha\frac{\partial}{\partial\theta_j}J(\theta_0,\theta_1)$​ 	（for j=0 and j=1）

}

$\alpha$​ learning rate

**Correct ：Simultaneous update**

$\textcolor{blue}{temp0：}$$\theta_0 : \theta_0-\alpha\frac{\partial}{\partial\theta_0}J(\theta_0,\theta_1)$​​

$\textcolor{blue}{temp1：}$ $\theta_1 : \theta_1-\alpha\frac{\partial}{\partial\theta_1}J(\theta_0,\theta_1)$

$\theta_0:$=$\textcolor{blue}{temp0}$

$\theta_1$ :=$\textcolor{blue}{temp1}$

### 2-6 Gradient descent Intuition

**Learning rate $\alpha$**

if $\alpha$ is too small,gradient descent can be slow

if $\alpha$ is too large,gradient descent can overshoot the minimum .It may fail to  converge,or even diverge

**learning rate $\alpha$​​ fixed**

As we approach a local minimum, gradient descent will automatically take smaller steps. So, no need to decrease $\alpha$ over time

### 2-7 Gradient descent for linear regression

 **Gradient decent algorithm**

repeat until convergence{
$$
\begin{cases}\theta_0 := \theta_0-\alpha\frac{1}{m}\sum_{i=1}^{m}{(h_\theta(x^{(i)}-y^{(i)})}
 \\\theta_1 := \theta_1-\alpha\frac{1}{m}\sum_{i=1}^{m}{(h_\theta(x^{(i)}-y^{(i)})}.x^{(i)}

\end{cases}
$$
}

update $\theta_0$ and $\theta_1$​ simultaneously

convex function 凸函数

**”Batch“ Gradient Descent**

Batch ": Each step of gradient descent uses all the training examples



## 3 Linear Algebra review（optional）

(线性代数还不错的可以不用学习这一部分)

### 3-1 Matrices and Vectors

**Matrix**: Rectangular array of numbers

**Dimension of matrix**: number of rows x number of columns	(m x n)

**Matrix Elements**(entries of matrix)

**Vector**: An n x 1 matrix

1-indexed

refer A/B/C/X a,b,x,y

### 3-2 Addition and scalar multiplication

**Matrix Addition**

**Matrix Scalar Multiplication**

**Combination of Operands**

### 3-3 Matrix-vector multiplication

【m x n】【n x 1】=【m x 1】

**neat trick**: prediction = data-matrix x parameters

### 3-4 Matrix-matrix multiplication

【m x n】【n x o】=【m x o】

**neat trick**:prediction = data-matrix x parameters-matrix 

### 3-5 Matrix  multiplication properties

$A \times B \neq B  \times A$

$A \times B \times C = A \times (B \times C)=(A \times B) \times C$

 **Identity Matrix**

Denote $I$ (or $I_{n\times n}$​) 

$A·I=I·A=A$

### 3-6 Inverse and Transpose

0 don‘t have inverse

**Matrix Inverse**

 	$A^{-1}: A^{-1}A=I$

**Matrix Transpose**

​	$A^T$​ : $B=A^T$  $B_{ij}=A_{ji}$​



## 4 Linear Regression with multiple variables

### 4-1 Multiple features

**Multiple features** (variables)

​	Notation:

​		$n$​ = number of features
​		$x^{(i)}$​=input(features) of $i^{th}$​ training example.
​		$x_j^{(i)}$​=value of feature in $i^{th}$​​ training example.

**Hypothesis**

​	$h_\theta(x)=\theta_0+\theta_1x_1+\theta_2x_2+···+\theta_nx_n$

​	define $x_0$=1

​		$x=\begin{bmatrix}x_0\\x_1\\x_2\\\vdots\\x_n\end{bmatrix}$				$\theta=\begin{bmatrix}\theta_0\\\theta_1\\\theta_2\\\vdots\\\theta_n\end{bmatrix}$	

​		$h_\theta (x)=\theta^Tx$

### 4-2 Gradient descent for multiple variable

**Cost function**
$$
J(\theta)=J(\theta_0,\theta_1,\cdots,\theta_n)=\frac{1}{2m}\sum_{i=1}^{m}(h_\theta(x^{(i)}-y^{(i)})^2
$$
**Gradient descent**

​		$ \theta_j := \theta_j-\alpha\frac{\partial}{\partial\theta_j}J(\theta)$​​ 

​		**Previously(n=1):**

​		Repeat{
$$
\begin{cases}\theta_0 := \theta_0-\alpha\frac{1}{m}\sum_{i=1}^{m}{(h_\theta(x^{(i)}-y^{(i)})}
 \\\theta_1 := \theta_1-\alpha\frac{1}{m}\sum_{i=1}^{m}{(h_\theta(x^{(i)}-y^{(i)})}.x^{(i)}

\end{cases}
$$
​		}

​		**New algorithm(n$\ge1$​)**

​		Repeat{
$$
\theta_j := \theta_j-\alpha\frac{1}{m}\sum_{i=1}^{m}{(h_\theta(x^{(i)}-y^{(i)})x^{i}_j}
$$
​		}

### 4-3 Gradient descent in practice I: Feature Scaling

**Feature Scaling** 特征缩放

​	Ideal ：make sure  features are on a similar scale

​	Get every feature into approximately a $0\le x_i \le 1$​  ($x_0=1$) range​​

**Mean normalization**

​	Replace $x_i$ with $x_i-\mu_i$ to make features have approximately zero mean (Do not apply to $x_0=1$)
$$
x_i\longleftarrow \frac{x_i-\mu_i}{s_i}
\\
$$
​	$x_i$: feature number

​	$\mu_i$:average value

​	$s_i$: range(max-min)

### 4-4 Gradient descent in practice I: Learning rate

**Gradient descent**

​	$\theta_j := \theta_j-\alpha\frac{\partial}{\partial\theta_j}J(\theta)$

 - Debugging: make sure gradient descent is working correctly

 - How to choose learning rate $\alpha$ 

   **Convergence test:**

   ​	Declare convergence if $J(\theta)$​​ decreases by less than $10^{-3}$​​​ ($\epsilon$​​)in one iteration

**Summary**

For sufficiently small $\alpha$, $J(\theta)$​should decrease on every iteration.
But if Q is too small, gradient descent can be slow to converge

**To choose $\alpha$,try**

​	steps of ten

​	···,0.001,0.003,0.01,0.03,···

### 4-5 Features and polynomial regression

housing price prediction

**Polynomial regression**

$h_\theta(x)=\theta_0+\theta_1x_1+\theta_2x_2+\theta_3x_3$

$\longrightarrow$$h_\theta(x)=\theta_0+\theta_1(size)+\theta_2(size)^2+\theta_3(size)^3$​

**Choice of features**

$h_\theta(x)=\theta_0+\theta_1x_1+\theta_2\sqrt{size}$

### 4-6 Normal equation

**Intuition: ($\theta\in R$​) **($\theta\in R^{n+1}$)
$$
\theta=(X^TX)^{-1}X^Ty
$$

```octave
pinv(x'*x)*x'*y		%octave
```



m **examples** ($(x^{(1)},y^{(1)}),\cdots,(x^{(m)},y^{(m)})$​​),n **features**

$x^{(i)}=\begin{bmatrix} x_0^{(i)}\\ x_1^{(i)}\\x_2^{(i)}\\\vdots\\x_n^{(i)}\end{bmatrix}$​​               X=$\begin{bmatrix}\cdots & （x^{(1)})^T & \cdots \\ \cdots & （x^{(2)})^T & \cdots \\&\vdots&\\\cdots & （x^{(m)})^T & \cdots  \end{bmatrix}$​​

$y=\begin{bmatrix}y^{(1)}\\y^{(2)}\\\vdots\\y^{(m)}\end{bmatrix}$

| Gradient Descent O(n)           | Normal Equation O($n^3$)      |
| ------------------------------- | ----------------------------- |
| Need to choose $\alpha$         | No need to choose $\alpha$    |
| Needs many iterations           | Don't need to iterate         |
| Works well even when n is large | Need to compute $(X^TX)^{-1}$ |
|                                 | Slow if n is very large       |

### 4-7 Normal equation and non-invertibility(optional)

singular or degenerate matrices

**What if  $X^TX$ is non-invertible ? **

 - Redundant features (linear dependent)

   e.g. $x_1$=size in $feet^2$​

   ​		$x_2$=size in $m^2$​

 - Too many features(e.g. m$\le$n)

   -Delete some features,or use regulariztion

### **Octave Tutorial

**Working on and submitting programming exercises** 



## 5 Octave Tutorial

*（Octave也可以用MATLAB学习，个人决定使用Python进行学习实现,5-6建议无论学习什么语言都可以看一看）*

### 5-1  Basic operations

### 5-2 Moving data around

### 5-3 Computing on data

### 5-4  Plotting data

### 5-5 for,while,if statements,and function

### 5-6  Vectorization

**Vectorization example**
$$
h_\theta(x)=\sum_{j=0}^n \theta_jx_j=\theta^Tx
$$
​								**Matlab**

```matlab
%% Unvectorized implementation
prediction = 0.0;
for j =1:n+1
	prediction=prediction + theta(j) * x(j)
end
```

```matlab
%% Vectorized implementation
prediction = theta' * x
```

​								**C++**

```C++
// Unvectorized implementation
double prediction =0.0;
for (int j=0;j<n;j++)
    	prediction += theta[j] * x[j];
```

```C++
// Vectorized implementation
double prediction = theta.transpose() * x;
```

**Gradient descent**





## 6 Logistic Regression

### 6-1 Classification

 **Classification**

​	$y \in \{0,1\}\ \ \ \ \ \ \ \ \ \ \ \ \begin{matrix} 0:"Negative Class"\\1:"Positive Class" \end{matrix}$

​		$h_\theta(x)$ can be >1 or <0

**Logistic Regression**: $0 \le h_\theta(x) \le 1$

### 6-2 Hypothesis Representation

**Logistic Regression Model**

​	Want  $0 \le h_\theta(x) \le 1$

​	**Sigmoid function**/**Logistic function**

​						$h_\theta(x)=g(\theta^Tx)$		$g(z)=\frac{1}{1+e^{-z}}$
$$
h_\theta(x)=\frac{1}{1+e^{-\theta^Tx}}
$$
**Interpretation of Hypothesis Output**

$h_\theta(x)$=estimated probability that y=1 on input​

probability that y= 1, given x, parameterized by $\theta$ 

### 6-3 Decision boundary

$$
h_\theta(x)=g(\theta^Tx)=\frac{1}{1+e^{-\theta^Tx}}=P(y=1|x;\theta)
$$

predict "y=1" if  $\theta^Tx\geq 0$	($h_\theta(x)\geq 0.5$)

predict "y=0" if  $\theta^Tx\leq 0$	($h_\theta(x)\leq 0.5$)

**Decision Boundary**

**Non-linear decision boundaries**

${ h _ {\theta} ( x ) = g ( \theta _ { 0 } + \theta _ { 1 } x _ { 1 } + \theta _ { 2 } x _ { 2 } }  { + \theta _ { 3 } x ^ { 2 } + \theta _ { 4 } x _ { 2 } ^ { 2 } })$​

### 6-4 Cost function

​	**Training set:**

​	$\{ ( x ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( x ^ { ( 2 ) } , y ^ { ( 2 ) } ) , \cdots , ( x ^ { ( m ) } , y ^ { ( m ) } ) \}$

​	**m example**	

​	$$x \in \left[ \begin{array}  { l  }  { x _ { 0 } } \\ { x _ { 1 } } \\ { x _ { n } } \end{array} \right] \quad x _ { 0 } = 1 , y \in \{ 0 , 1 \}$$

​	$$h _ { \theta } ( x ) = \frac { 1 } { 1 + e ^ { - \theta Tx }  }$$

**Cost function**

​	**Linear regression**

​		$$J ( \theta ) = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } \frac { 1 } { 2 } ( h _ { 0 } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 }= \frac { 1 } { m } \sum _ { i = 1 } ^ { m }cost(h_\theta(x^{(i)}),y{(i)})$$​

non-convex $\longrightarrow$​ convex

**Logistic regression function**

$$\operatorname { Cost } ( h _ { \theta } ( x ) , y ) = \{ \begin{array}  { l l  }  { - \log ( h _ { \theta } ( x ) ) } & {  y = 1 } \\ { - \log ( 1 - h _ { \theta } ( x ) ) } & {  y = 0 } \end{array}$$​

Cost =0 if y= 1, $h_\theta(x)$=1But as $h_\theta(x)$→0,Cost→$\infty $​

Captures intuition that if $h_\theta(x)$​=0 (predict P(y=1lx;0)=0), but y=1,well penalize learning algorithm by a very large cost.

### 6-5 Simplified cost function and gradient descent

**Logistic regression cost function**

$J ( \theta ) = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } \operatorname { Cost } ( h _ { \theta } ( x ^ { ( i ) } ) , y ^ { ( i ) } )$​​

$$\operatorname { Cost } ( h _ { o } ( x ) , y ) = \{ \begin{array}  { l l  }  { - \log ( h _ { \theta } ( x ) ) } & {  y = 1 } \\ { - \log ( 1 - h _ { \theta } ( x ) ) } & {  y = 0 } \end{array}$$​

$$Note： y =0\ or\ 1\ always$$​

$\downarrow$

$$J(\theta)= - \frac { 1 } { m } [ \sum _ { i = 1 } ^ { m } y ^ { ( i ) } \log h _ { b } ( x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) \log ( 1 - h _ { g } ( x ^ { ( i ) } ) ) ]$$

​	**To fit parameters ${\theta}$**

​		$$min_\theta J ( \theta )$$

​	**To make a prediction given new x:**

​		Output $$h _ { \theta } ( x ) = \frac { 1 } { 1 + e ^ { - \theta Tx } }$$​

**Gradient Descent**

​	Repeat{

​			$\theta _ { j } : = \theta _ { j } - \alpha \frac { \theta } { \partial \theta _ { j } }J ( \theta )=\theta _ { j } - \alpha \sum _ { i = 1 }^{m} ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) x _ { j } ^ { ( i ) }$​​​

​	}

Algorithm looks identical to linear regression !

But $h_\theta(x)$​ different 

### 6-6 Advanced optimization

**Optimization algorithm**

​	Cost function $J(\theta)$.Want $min_\theta J(\theta)$

​	Given $\theta$, we have code that can compute

Optimization algorithms

-Gradient descent
-Conjugate gradient
-BFGS
-L-BFGS

Advantages:

- No need to manually pick $\alpha$
- Often faster than gradient descent

Disadvantages:

	- More complex

```matlab
function [jVal,gradient]=costFunction(theta)
	jVal=(theta(1)-5)^2+...
		(theta(2)-5)^2;
	gradient=zero(2,1);
	gradient(1)=2*(theta(1)-5);
	gradient(2)=2*(theta(2)-5);
```

```matlab
options =optimset('GradObj','on','MaxIter','100');
initialTheta =zeros(2,1);
[optTheta,functionVal,exitFlag]...=Fminunc(@costFuncion,initiaTheta,options);
```

note: theta 0 is actually written theta 1 in octave

### 6-7 Multi-class classification : One-vs-all

**Multiclass classification**

​	*example :*Email foldering/tagging: Work, Friends, Family, Hobby

$$h _ { \theta } ^ { ( i ) } ( x ) = P ( y = i | x ; \theta ) \quad ( i = 1 , 2 , 3 \cdots)$$​​

**One-vs-all**
Train a logistic regression classifier $h_\theta^{i}(x)$ for each class $i$​ to predict the probability that $y=i$

On a new input to make a prediction, pick the class i that maximizes

$\operatorname {max}_i h _ { \theta } ^ { ( i ) } ( x )$



## 7 Regularization

### 7-1 The problem of overfitting

underfitting——high bias

Just right

overfitting——high variance 高方差

**Overfitting**: If we have too many features, the learned hypothesis may fit the training set very well, but fail to generalize to new examples

**Addressing overfitting**：

Options:
1. *Reduce number of features*
2. *Regularization*
  - Keep all the features, but reduce magnitude/values of parameters 0
  - Works well when we have a lot of features, each of which contributes a bit to predicting y

### 7-2 Cost function

**Intuition**

if $\theta _ { 0 } + \theta _ { 1 } x + \theta _ { 2 } x ^ { 2 }$ fitting，and $\theta _ { 0 } + \theta _ { 1 } x + \theta _ { 2 } x ^ { 2 } + \theta_3 x ^ { 3 } + \theta_4 x ^ { 4 }$ overfitting

$\longrightarrow$Suppose we penalize and make $\theta_3,\theta_4$​ really small,close to 0

**Regularization**

Small values for parameters $\theta_0,\theta_1,\cdots,\theta_n$​

- Simpler"hypothesis
- Less prone to overfitting

Housing:

- Features: $x_1,x_2,\cdots,x_{100}$​
- Parameters: $\theta_0,\theta_1,\theta_2,\cdots,\theta_{100}$​

$$J ( \theta ) = \frac { 1 } { 2 m } [ \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 } + \lambda \sum _ { j = 1 } ^ { n } \theta _ { j } ^ { 2 } ]$$​

(**$\lambda$​**​ regularization parameter)

In regularized linear regression, we choose $\theta$​ to minimize $J(\theta)$

What if $\lambda$ is set to an extremely large value (perhaps for too large for our problem, say $\lambda=10^{10}$)?

### 7-3 Regularization linear regression

**Regularization linear regression**

$$J ( \theta ) = \frac { 1 } { 2 m } [ \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 } + \lambda \sum _ { j = 1 } ^ { n } \theta _ { j } ^ { 2 } ]$$

$$\theta _ { j } : = \theta _ { j } ( 1 - \alpha \frac { 1 } { m } ) - \alpha \frac { 1 } { m } \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) x _ { j } ^ { ( i ) }$$

**Normal equation**

$$X = \left[ \begin{array}  { l  }  { ( x ^ { ( 1 ) } ) ^ { T } }\\\vdots \\ { ( x ^ { ( m ) } ) ^ { T } } \end{array} \right]$$​			$$y = \left[ \begin{array}  { l  }  { y ^ { ( 1 ) } } \\ { \vdots } \\ { y ^ { ( m ) } } \end{array} \right]$$​

**Non-invertibility(optional/advanced)**

Suppose m$\le$n	(m: examples,n: features)

$$\theta = ( X ^ { T } X ) ^ { - 1 } X ^ { T } y$$

if $\lambda>0$​,

$$\theta = ( X ^ { T } X + \lambda(\begin{bmatrix} 0 \\ &1 \\ &&1 \\ &&&\ddots \\&&&&1\end{bmatrix}) ^ { - 1 } X ^ { T } y$$​​​​​​​

### 7-4 Regularized logistic regression

**Gradient descent**

Repeat{

​		$$\theta _ { 0 } : = \theta _ { 0 } - \alpha \frac { 1 } { m } \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) x _ { 0 } ^ { ( i ) }$$​

​		$$\theta _ { j } : = \theta _ { j } ( 1 - \alpha \frac { 1 } { m } ) - \alpha \frac { 1 } { m } \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) x _ { j } ^ { ( i ) }$$

​	}

**Advanced optimization**

```matlab
function [jVal,gradient] = costFunction(theta)
	jVal = [code to compute J(θ)];
	gradient(1)= [code to compute ∂J(θ)/∂(θ_0) ] 
	gradient(2)= [code to compute ∂J(θ)/∂(θ_1) ]
	gradient(3)= [code to compute ∂J(θ)/∂(θ_2) ]
	...
	gradient(n+1)= [code to compute ∂J(θ)/∂(θ_n) ]
	
```



## 8 Neural Networks： Representation

### 8-1 Non-linear hypotheses

**Non-linear Classification** 0、1

### 8-2 Neurons and the brain

**Neurons Networks**

***Origins***: Algorithms that try to mimic the brain.

Was very widely used in 80s and early 90s;popularity diminished in late 90s
	***Recent resurgence***: State-of-the-art technique for many applications

**The "one learning algorithm" hypothsis**

	neuro-rewiring experiments

**Sensor representation in brain**

### 8-3 Model representation I

**Neuron in brain**

**Neuron model: logistic unit**

	sigmoid (logistic) activation function.

**Neural Network**

input layer

hidden layer

output  layer

$a_i^{(j)}=$"activation" of unit i in layer j

$\Theta^{(j)=}$matrix of weight controlling function mapping from layer j to layer j+1

$\begin{matrix}\\a_1^{(2)}=g(\Theta_{10}^{(1)}x_0+\Theta_{11}^{(1)}x_1+\Theta_{12}^{(1)}x_2+\Theta_{13}^{(1)}x_3)\\a_2^{(2)}=g(\Theta_{20}^{(1)}x_0+\Theta_{21}^{(1)}x_1+\Theta_{22}^{(1)}x_2+\Theta_{23}^{(1)}x_3)\\a_3^{(2)}=g(\Theta_{30}^{(1)}x_0+\Theta_{31}^{(1)}x_1+\Theta_{32}^{(1)}x_2+\Theta_{33}^{(1)}x_3)\\h_{\Theta(x)=a_1^{(3)}=g(\Theta_{10}^{(2)}a_0^{(2)}+\Theta_{11}^{(2)})a_1^{(2)}+\Theta_{12}^{(2)}a_2^{(2)}+\Theta_{13}^{2}a_3^{(2)}}\end{matrix}$

If network has $s_j$ units in layer$j, s_j+1$ units in layer j+ 1, then $\Theta^{(j)}$ will be of dimension $s_{j+1}\times(s_j+1)$

### 8-4 Model representation II

**Forward propagation: Vectorized implementation**

$x =\begin{bmatrix}x_0 \\ x_1 \\ x_2\\x_3\end{bmatrix}$		$z ^ { ( 2 ) } = \left[ \begin{array}  { l  }  { z _ { 1 } ^ { ( 2 ) } } \\ { z _ { 2 } ^ { ( 2 ) } } \\ { z _ { 3 } ^ { ( 2 ) } } \end{array} \right]$

$z ^ { ( 2 ) } = \Theta ^ { ( 1 ) } x$

$a ^ { ( 2 ) } = g ( z ^ { ( 2 ) } )$

**Add** $a_0^{(2)}=1$

$z^{(3)}=\Theta^{(2)}a^{(2)}$

$h_\Theta(x)=a^{(3)}=g(z^{(3)})$

**Neural Network learning its own features**

**Other network architectures**

### 8-5 Example and intuitions I

**XOR/XNOR**

**AND**

**Or**

### 8-6 Example and intuitions II

**Negation**

**Putting it together:**

**AND/NOT AND NOT/OR**$\longrightarrow$**$x_1$ XNOR $x_2$**

*(Similar to the combination of multiple logic circuits)*

Handwritten digit classfication

### 8-7 Multi-class classification

**Multiple output units : One-vs-all**

**Want** $h_\Theta(x)\approx \begin{bmatrix}1\\0\\0\\0\end{bmatrix}$, $h_\Theta(x)\approx \begin{bmatrix}0\\1\\0\\0\end{bmatrix}$, $h_\Theta(x)\approx \begin{bmatrix}0\\0\\1\\0\end{bmatrix}$,$etc$

**Training set:**$(x^{(1)},y^{(1)}),(x^{(2)},y^{(2)}),\cdots,(x^{(m)},y^{(m)})$

$y^{(i)}$ one of	$\begin{bmatrix}1\\0\\0\\0\end{bmatrix}$，$\begin{bmatrix}0\\1\\0\\0\end{bmatrix}$，$\begin{bmatrix}0\\0\\1\\0\end{bmatrix}$，$\begin{bmatrix}0\\0\\0\\1\end{bmatrix}$



## 9 Neural Network : Learning

### 9-1 Cost function

**Neural Network(classification)**

$(x^{(1)},y^{(1)}),(x^{(2)},y^{(2)}),\cdots,(x^{(m)},y^{(m)})$

$L$ = total no. of layers in network

$s_l$ = no. of unit (not counting bias unit) in layer $l$

**Compare between Binary | Multi-class(K classes) classification** 

*Binary classification*

​	$y=0\; or\; 1$​​

​	1 out put unit

*Multi-class classification(K classes)*

​	$y\in\mathbb{R{\LARGE } } ^K$

​	K output unit

**Cost function**

​	Logistic regression:

​		$$J ( \Theta ) = - \frac { 1 } { m } [ \sum _ { i = 1 } ^ { m } y ^ { ( i ) } \log h _ { \Theta } ( x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) \log ( 1 - h _ { 0 } ( x ^ { ( i ) } ) ) ] + \frac { \lambda } { 2 m } \sum _ { j = 1 } ^ { n } \Theta^2_j$$​​​

​	Neural network:

​		$$h _ { \Theta } ( x ) \in R ^ { K } \quad ( h _ { \Theta } ( x ) ) _ { i } = i ^ { t h } \quad output$$​

​		$$J ( \Theta ) = - \frac { 1 } { m } [ \sum _ { i = 11 } ^ { m } \sum _ { k = 1 } ^ { K } y _ { k } ^ { (i) } \log ( h _ { k } ( x ^ { ( i ) } ) ) _ { k } + ( 1 - y _ { k } ^ { (i) } \log( 1 - ( h _ { \Theta } ( x ^ { ( i ) } ) _k)]+ \frac { \lambda } { 2 m } \sum _ { l = 1 } ^ { L - 1 } \sum _ { i = 1 } ^ { s_l } \sum _ { j = 1 } ^ { s_l + 1 } ( \Theta _ { ji } ^ { ( l ) } ) ^ { 2 }$$​​​​

### 9-2 Backpropagation algorithm

反向传播算法

**Gradient computation**

​	$min_\Theta J(\Theta)$

​	**Need code to compute:**

 - $J(\Theta)$
 - ${\frac{\partial}{\partial\Theta^{(l)}_{ij}}J(\Theta)}{\LARGE}$​​

Given one training example (x,y):

​	Forward propagation:

$\begin{array}{l}{a^{(1)}=x}\\z^{(2)}=\Theta^{(1)}a^{(1)}\\a^{(2)}=g(z^{(2)})\quad(add\; a_0^{(2)})\\z^{(3)}=\Theta^{(2)}a^{(2)}\\a^{(3)}=g(z^{(3)})\quad(add\; a_0^{(3)})\\z^{(4)}=\Theta^{(3)}a^{(3)}\\a^{(4)}=h_\Theta(x)=g(z^{(4)})\end{array}$

**Gradient computation: Backpropagation algorithm**

Intuition: $\delta_j^{(l)}=$"error" of node $j$ in layer $l$

**For each out put unit (layer L=4)**

 $$\delta _ { j } ^ { ( 4 ) } = a _ { j } ^ { ( 4 ) } - y _ { j }$$​

$$\left. \begin{array}  { l  }  { \delta ^{( 3 )} = ( \Theta ^ { ( 3 ) } ) ^ { T } \delta^{( 4 )} .* g ^ { \prime } ( z ^ { ( 3 ) } ) } \\ { \delta ^ { ( 2 ) } = ( \Theta ^ { ( 2 ) } ) ^ { T } \delta ^ {( 3 )} .* g ^ { \prime } ( z ^ { ( 2 ) } ) } \end{array} \right.$$​​​​​

($no \qquad \delta^{(1)}$​​​)

**Backpropagation algorithm**

*Training set: **$(x^{(1)},y^{(1)}),(x^{(2)},y^{(2)}),\cdots,(x^{(m)},y^{(m)})$​**​*

*Set: **$\bigtriangleup_{ij}^{(l)}=0\quad(for\;all\;l,i,j)$​​​***

**$\bigtriangleup_{ij}^{(l)}$​​​​** used to compute **${\frac{\partial}{\partial\Theta^{(l)}_{ij}}J(\Theta)}{\LARGE}$​​​​​**

*For **$i=1$​​ to $m$**:*

​	*Set **$a^{(1)}=x^{(i)}$​​***

​	*Perform forward propagation to compute **$a^{(l)}$**​​​ for **$l=2,3,\cdots,L$​​**​*

​	*Using **$y^{(i)}$**​​​,compute **$\delta( L ) = a ^ { ( L ) } - y ^ { ( i ) }$​​​***

​	*Compute **$\delta{( L - 1 )} , \delta ^{( L - 2 )} , \cdots , \delta^{( 2 )}$​​​***

​	***$$\bigtriangleup _ { i j } ^ { ( i ) } : = \bigtriangleup _ { i j } ^ { ( l ) }+a_j^{(l)}\delta_i^{(l+1)}$$​​​***

***$$\left. \begin{array}  { l  }  { D _ { ij } ^ { ( l ) } : = \frac { 1 } { m } \bigtriangleup _ { i j } ^ { ( l ) } + \lambda \Theta _ { i j } ^ { ( t ) }  \quad if\;j \neq 0 } \\ { D _ { i j } ^ { ( l ) } : = \frac { 1 } { m } \bigtriangleup_{ij}^{(l)} \quad if \; j=0} \end{array} \right.$$​​​***

$$\frac { \partial } { \partial \Theta _ { i j}^{(l)} } J ( \Theta ) = D _ { i j } ^ { ( l ) }$$​​​​

### 9-3 Backpropagation intuition

**Forward propagation**

$x_1^{(i)},x_2^{(i)},\dots\xRightarrow{z^{(2)}=\Theta^{(1)}a^{(1)}+\cdots}z_1,z_2,\cdots\xRightarrow{a^{(2)}=g(z^{(2)})}a_1,a_2,\cdots \Rightarrow \cdots$

**​​​What is backpropagation doing?**
$$
J ( \theta ) = - \frac { 1 } { m } [ \sum _ { i = 1 } ^ { m } y ^ { (i) } \log ( h _ { \Theta } {( x ^ { ( i ) })} )   + ( 1 - y ^ { (i) }) \log( 1 - ( h _ { \Theta } {( x ^ { ( i ) } )} )]+ \frac { \lambda } { 2 m } \sum _ { l = 1 } ^ { L - 1 } \sum _ { i = 1 } ^ { s_l } \sum _ { j = 1 } ^ { s_l + 1 } ( \Theta _ { ji } ^ { ( l ) } ) ^ { 2 }
$$
Focusing on a single example $x^{(i)},y^{(i)}$, the case of 1 output unit,and ignoring regularization ($\lambda=0$)

$$\operatorname {cost} ( i ) = y ^ { ( i ) } \log h _ { \Theta } ( x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) \log h_\Theta ( x ^ { ( i ) } )$$​​

(Thinking of $$\operatorname {cost} ( i ) \approx ( h _ { \Theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 }$$​​)

I.e. how well is the network doing on example i?

**Backpropagation**

$\delta_j^{(l)}=$"error" of cost for $a_j^{(l)}\quad(unit\;j\;in\; layer \;l).$

$Formally,\delta_j^{(l)}=\frac{\partial}{\partial z_j^{(l)}}cost(i)\quad (for \;j\ge0),where\\\operatorname {cost} ( i ) = y ^ { ( i ) } \log h _ { \Theta } ( x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) \log h_\Theta ( x ^ { ( i ) } )$​​

### 9-4 Implementation note: Unrolling parameters

**Advanced optimization**

```matlab
function [jval,gradient] =costFunction(theta)
...
optTheta = fminunc(@costFunction,initialTheta,options)
```

Neural Network(L=4):

​	$\Theta^{(1)},\Theta^{(2)},\Theta^{(3)}-$​matrices(Theta1,Theta2,Theta3)

​	$D^{(1)},D^{(2)},D^{(3)}-$matrices(D1,D2,D3)

"unroll" into vectors

**Example**

$$\begin{array}  { l  }  { s _ { 1 } = 10 , s _ { 2 } = 10 , s _ { 3 } = 1 } \\ { \Theta ^ { ( 1 ) } \in \mathbb{R} ^ { 10 \times 11 } , \Theta ^ { ( 2 ) } \in \mathbb{R} ^ { 10 \times 11 } , \Theta ^ { ( 3 ) } \in \mathbb{R} ^ { 1 \times 11 } } \\ { D ^ { ( 1 ) } \in \mathbb{R} ^ { 10 \times 11 } , D ^ { ( 2 ) } \in \mathbb{R} ^ { 10 \times 11 } , D ^ { ( 3 ) } \in \mathbb{R} ^ { 1 \times 11 } }\end{array}$$​​​

```matlab
thetaVec =[Theta1(:);Theta2(:);Theta3(:)];
Dvec =[D1(:),D2(:),D3(:)];

Theta1=reshape(thetaVec(1:110),10,11)
Theta2=reshape(thetaVec(111,220),10,11)
Theta1=reshape(thetaVec(221:231),1 ,11)
```

**Learning Algorithm**

Have initial parameters $\Theta^{(1)},\Theta^{(2)},\Theta^{(3)}$​

Unroll to get $\color{Blue}initialTheta$​ to pass to 

```matlab
fminunc(@costFunction,initialTheta,options)
```

```matlab
function[jval,gradientVec] = costFunction(thetaVec)
```

From $\color{Blue}thetaVec$​, get $\Theta^{(1)},\Theta^{(2)},\Theta^{(3)}$​

Use forward prop/back prop to compute $D^{(1)},D^{(2)},D^{(3)}$ and $J(\theta)$

Unroll $D^{(1)},D^{(2)},D^{(3)}$ to get $\color{Blue}gradientVec$

### 9-5 Gradient checking

**Numerical estimation of gradient**

$\frac{d}{d\theta}J(\theta)\approx\frac{J(\theta+\epsilon)-J(\theta-\epsilon)}{2\epsilon}$​

Implement

```matlab
gradApprox = (J(theta+EPSILON)-J(theta-EPSILON))/(2*EPSILON)
```

**Parameter vector $\theta$**

$\theta\in\mathbb{R}^n$	(E.g. $\theta$ is "unrolled" version of $\Theta^{(1)},\Theta^{(2)},\Theta^{(3)}$

$\theta=\theta_1,\theta_2,\theta_3,\cdots,\theta_n$

$$\begin{array}{l}
  & \\\frac{ \partial } { \partial \theta _ { 1 } } J ( \theta ) \approx \frac { J ( \theta _ { 1 } + \epsilon ,\theta_ { 2 } , \theta _ { 3 } \cdots , \theta _ { n } ) - J ( \theta _ { 1 } - \epsilon , \theta _ { 2 } , \theta _ { 3 } \cdots , \theta _ { n } ) } { 2 \epsilon }
  & \\\frac{ \partial } { \partial \theta _ { 1 } } J ( \theta ) \approx \frac { J ( \theta _ { 1 } ,\theta_ { 2 } + \epsilon, \theta _ { 3 } \cdots , \theta _ { n } ) - J ( \theta _ { 1 }  , \theta _ { 2 }- \epsilon , \theta _ { 3 } \cdots , \theta _ { n } ) } { 2 \epsilon }
  & \\\vdots
  & \\\frac{ \partial } { \partial \theta _ { 1 } } J ( \theta ) \approx \frac { J ( \theta _ { 1 }  ,\theta_ { 2 } , \theta _ { 3 }\cdots , \theta _ { n } + \epsilon ) - J ( \theta _ { 1 }  , \theta _ { 2 } , \theta _ { 3 } \cdots , \theta _ { n } - \epsilon) } { 2 \epsilon }
\end{array}$$

```matlab
for i=1:n,
	thetaPlus=theta;
	thetaPlus(i)=thetaPlus(i)+EPSILON;
	thetaMinus=theta;
	thetaMinus(i)=thetaMinus(i)-EPSILON;
	gradApprox(i)=(J(thetaPlus)-J(thetaMinus))/(2*EPSILON);
end;
```

Check that $\color{Blue}{gradApprox\approx Dvec}$​

**Implementation Note:**

- Implement backprop to compute  $\color{Blue}Dvec$(unrolled $D^{(1)},D^{(2)},D^{(3)},$)
- Implement numerical gradient check to compute $\color{Blue}gradApprox$
- Make sure they give similar values
- Turn off gradient checking Using backprop code for learning

**Important:**

- Be sure to disable your gradient checking code before training your classifier. If you run numerical gradient computation on every iteration of gradient descent(or in the inner loop of $\color{Blue}costFunction(\cdots)$​​​) your code will be very slow.

### 9-6 Random initialization

**Initial value of $\Theta$**

For gradient descent and advanced optimization method, need initial value for $\Theta$

```matlab
optTheta = fminunc(@costFunction,initialTheta,options)
```

Consider gradient descent

Set $\color{Blue}initialTheta = zeros(n,1)$​?	$\Huge\color{red}\times$​

**Zero initialization**

$\Theta_{ij}^{(l)}=0\;for \; all \;i,j,l.$

After each update, parameters corresponding to inputs going into each of two hidden units are identical

**Random** each $\Theta_{ij}^{(l)}$​ to a random value in $[-\epsilon,\epsilon]$​($i.e.\quad -\epsilon \le \Theta_{ij}^{(l)}\le\epsilon$​)

$E.g.$

```matlab
Theta1 = rand(10,11)*(2*INIT_EPSILON)-INIT_EPSILON;
Theta2 = rand(1,11)*(2*INIT_EPSILON)-INIT_EPSILON;
```

### 9-7 Putting it together

**Training a neural network**

Pick a network architecture( connectivity pattern between neurons)

- No of input units: Dimension of features $x^{(i)}$

- No output units: Number of classes

  $y^{(1)}=\begin{bmatrix}1\\0\\0\\0\\0\end{bmatrix},y^{(2)}=\begin{bmatrix}0\\1\\0\\0\\0\end{bmatrix},\cdots$​

- Reasonable default: 1 hidden layer, or if >1 hidden layer, have same no of hidden units in every layer(usually the more the better

> 1. Randomly initialize weights
> 2. Implement forward propagation to get $h_\Theta(x^{(i)})$ for any $x^{(i)}$ 
> 3. Implement code to compute cost function, $J(\Theta)$
> 4. Implement backprop to compute partial derivatives $$\frac { \partial } { \partial \Theta _ { j k }^{(l)} } J ( \Theta )$$​​

for i=1:m

​	Perform forward propagation and backpropagation using example $(x^{(i)},y^{(i)})$​
​	( Get activations $a^{(l)}$​ and delta terms $\delta^{(l)}\;for\;l=2,\cdots,L$​

> 5. Use gradient checking to compare $$\frac { \partial } { \partial \Theta _ { j k }^{(l)} } J ( \Theta )$$​ computed using backpropagation vs. using numerical estimate of gradient of $J(\Theta)$​.
> Then disable gradient checking code.
> 6. Use gradient descent or advanced optimization method withbackpropagation to try to minimize $J(\Theta)$​ as a function ofparameters $\Theta$​​

### 9-8 Autonomous driving example



## 10 Advice for applying machine learning

### 10-1 Deciding what to try next

**Debugging a learning algorithm**

Suppose you have implemented regularized linear regression to predict housing prices.

$$J ( \theta ) = \frac { 1 } { 2 m } [ \sum _ { i = 1 } ^ { m } ( h _ { 0 } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 } + \lambda\sum _ { j = 1 } ^ { m } \theta _ { j } ^ { 2 } ]$$

However, when you test your hypothesis on a new set of houses, you find that it makes unacceptably large errors in its predictions. What should you try next?

- Get more training examples
- Try smaller sets if features
- Try getting additional features
- Try adding polynomial features

- Try decreasing $\lambda$
- Try increasing $\lambda$

**Machine learning diagnostic:**

Diagnostic: A test that you can run to gain insight what is/isn' t working with a learning algorithm, and gain guidance as to how best to improve its performance.

Diagnostics can take time to implement, but doing so can be a very good use of your time.

### 10-2 Evaluating a hypothesis

**Evaluating your hypothesis**

Fails to generalize to new examples not in training set

**Training/testing procedure for linear regression**

- Learn parameter $\theta$ from training data(minimizing training error ($J(\theta)$))
- Compute test set error :$J_{test}(\theta)$

classification problem:

- Learn parameter $\theta$ from training data
- Compute test set error:

​	$$J _ {test} ( \theta ) = - \frac { 1 } { m _ { test} } \sum _ { i = 1 } ^ { m _ { t e s t } } y^{(i)}_{test}\log h_{\theta}(x_{test}^{(i)}) + ( 1 - y _ { t e s t }) ^ { ( i ) }logh_{\theta}(x_{test}^{(i)})$$



- Miscalssification error (0/1 miscalssification error):

![image-20210903145317714](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210903145317714.png)

### 10-3 Model selection and training/validation/test sets

**Overfitting example**

Once parameters $\theta_0,\theta_1,\cdots,\theta_n$ were fit to some set of data (training set), the error of the parameters as measured on that data(the training error $J(\theta)$ is likely to be lower than the actual generalization error.

**Model selection**

parameter **d**=degree of  polynomial

How well does the model generalize? Report test set error $J_{test}(\theta^{(d)})$

Problem: $J_{test}(\theta^{(d)})$ is likely to be an optimistic estimate of generalization error l.e. our extra parameter(d = degree of polynomial)is fit to test set.

**Evaluating your hypothesis**

Training set 60%

cross validation	20%

test set 20%

**Training/validation/test error**

Training error:

$$J _ { t r a i n } ( \theta ) = \frac { 1 } { 2 m } \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 }$$

Cross validation error:

$$J _ { c v } ( \theta ) = \frac { 1 } { 2 m _ { c v } } \sum _ { i = 1 } ^ { m _ { v } } ( h _ { \theta } ( x _ { c v } ^ { ( i )}  ) - y _ { c v } ^ { ( i ) } ) ^ { 2 }$$

Test error:

$$J _ { t e s t } ( \theta ) = \frac { 1 } { 2 m_{ t e s t} } \sum _ { i = 1 } ^ { m _ { t e s t } } ( h _ { \theta } ( x _ { t e s t }^{(i)} ) - y _ { t e s t } ^ { ( i ) } ) ^ { 2 }$$

Estimate generalization error for test set $J_{test}(\theta^{(4)})$

### 10-4 Diagnosing bias vs. variance

**Bias/variance** 偏差/方差

Training error:

Crossing validation error:

**Diagnosing bias vs variance**
Suppose your learning algorithm is performing less well than you were hoping. $(J_{cv}(\theta)\;or\;J_{test}(\theta) \; is \;high)$ Is it a bias problem or a variance problem?

**Bias (underfit)**:$J_{train}(\theta)$ will be high;$J_{cv}(\theta)\approx J_{train}(\theta)$

**Variance(Overfit)**:$J_{train}(\theta)$ will be low;$J_{cv}(\theta)>> J_{train}(\theta)$

### 10-5 Regularization and bias/variance

**Linear regression with regularization**

Model:

$$h _ { \theta } ( x ) = \theta _ { 0 } + \theta _ { 1 } x + \theta _ { 2 } x ^ { 2 } + \theta _ { 3 } x ^ { 3 } + \theta _ { 4 } x ^ { 4 }$$

$$J ( \theta ) = \frac { 1 } { 2 m } [ \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 } + \lambda \sum _ { j = 1 } ^ { n } \theta _ { j } ^ { 2 } ]$$

High bias——Large $\lambda$

Just right——intermediate $\lambda$

High variance——small $\lambda$

**Choosing the regularization parameter $\lambda$**

​	the smallest $J_{cv}(\theta^{(i)})$ error

**Bias/variance as a function of the regularization parameter $\lambda$**

![image-20210903155215221](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210903155215221.png)

### 10-6 Learning curves

**Learning curves**

$J_{train}(\theta)$

$J_{cv}(\theta)$

**High bias**: more and more close

If a learning algorithm is suffering from high bias, getting more training data will not (by itself) help much

**High variance**: large gap

If a learning algorithm is suffering from high variance, getting more training data is likely to help

### 10-7 Deciding what to try next (revisited)

**Debugging a learning algorithm:**

- Get more training examples $\longrightarrow$fixed high variance
- Try smaller sets if features$\longrightarrow$fixed high variance
- Try getting additional features$\longrightarrow$fixed high bias
- Try adding polynomial features$\longrightarrow$$\longrightarrow$fixed high bias
- Try decreasing $\lambda$$\longrightarrow$fixed high bias
- Try increasing $\lambda$$\longrightarrow$fixed high variance

**Neural networks and overfitting**

![image-20210903162402023](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210903162402023.png)



## 11 Machine learning system design

### 11-1 Prioritizing what to work on: Spam classification example

**Building a spam classifier**

Supervised learning.  x=features of email. y=spam(1) or not spam(0).
Features x: Choose 100 words indicative of spam/not spam

$x_j=\begin{cases}1\text{ if word j appear in email}\\0\text{ otherwise}\end{cases}$

Note: In practice, take most frequently occurring n words(10,000 to 50,000 in training set, rather than manually pick 100 words.

**How to spend your time to make it have low error?**

- collect lots of data
  - E.g. "honeypot" project
- Develop sophisticated features based on email routing information(from email header)

- Develop sophisticated features for message body, e.g. should discount"and discounts"be treated as the same word? How about" deal"and"Dealer"? Features about punctuation?
- Develop sophisticated algorithm to detect misspellings(e.g. mortgage, medlcine, watches.)

### 11-2 Error analysis

**Recommended approach**

- Start with a simple algorithm that you can implement quickly Implement it and test it on your cross-validation data
- Plot learning curves to decide if more data, more features, etc.are likely to help
- Error analysis: Manually examine the examples(in cross validation set)that your algorithm made errors on. See if you spot any systematic trend in what type of examples it is making errors on

**example:**

$m_{cv}=500$ examples in cross validation set
Algorithm misclassifies 100 emails
Manually examine the 100 errors, and categorize them based on:
	(i) What type of email it is
	(ii)What cues (features)you think would have helped the algorithm classify them correctly

Deliberate misspellings: ( morgage medicine, etc.)
Unusual email routing: 
Unusual (spamming) punctuation:

**The importance of numerical evaluation**
Should discount/discounts/discounted/discounting be treated as the same word?
Can use"stemming"software (E.g."Porter stemmer")

Error analysis may not be helpful for deciding if this is likely to improve performance. Only solution is to try it and see if it works

Need numerical evaluation(e.g, cross validation error)of algorithms performance with and without stemming

### 11-3 Error metrics for skewed classes

**Cancer classification example**
Train logistic regression model $h_{\theta}(x)$.(y=1 if cancer, y=0 otherwise）
Find that you got 1% error on test set.
(99% correct diagnoses

**Precision/Recall**
y= 1 in presence of rare class that we want to detect

![image-20210904151636583](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210904151636583.png)

precision 查准率

Of all patients where we predicted y=1, what fraction actually has cancer?

True pos / (True pos+False pos) 

Recall 召回率

Of all patients that actually have cancer, what fraction did we correctly detect as having cancer?

True pos/(True pos + False pos)

### 11-4 Trading off precision and recall

**Trading off precision and recall**

$\begin{array}{l}\text{Logistic regression: } 0\le h_\theta(x)\le 1\\\text{Predict 1 if } h_\theta(x)\ge0.5\\\text{Predict 0 if } h_\theta(x)<0.5\end{array}$

$precision=\frac{true\;positives}{no.\;of \;predicted\;positive}$

$recall=\frac{true\;positives}{no.\;of \;actual\;positive}$

- Suppose we want to predict y=1 (cancer) only if very confident.$\longrightarrow$Higher precision,lower recall

- Suppose we want to avoid missing too many cases of cancer(avoid false negatives).$\longrightarrow$Higher recall,lower precision

- more generally: predict  1 if $h_{\theta}(x)\ge threshold$

**$F_1$ Score (F score)**

How to compare/recall numbers?

Average: $\frac{P+R}{2}$ 	$\color{red}false$ when R=1 predict y=1 all the time

$F_1$ Score: $2\frac{PR}{P+R}$	$\color{red}true$

### 11-5 Data for machine learning

**Designing a high accuracy learning system**

E.g. Classify between confusable words: {to,too,two}, {then, than}
For breakfast I ate____eggs
Algorithms

- Perceptron(Logistic regression)
- Winnow
- Memory-based
- Naive Bayes

> It's not who has the best algorithm that wins.
> It's who has the most data

**Large data rationale**

Assume feature $$x\in R ^ { n + 1 }$$ has sufficient information topredict y accurately

Example: For breakfast I ate____eggs.
Counterexample: Predict housing price from only size(feet)and no other features 

Useful test: Given the input x,can a human expertconfidently predict y ?

Use a learning algorithm with many parameters (e.g. logistic regression/linear regression with many features; neural network with many hidden units)$\longrightarrow J_{train}(\theta)$ will be small
Use a very large training set (unlikely to overfit)$\longrightarrow J_{test}(\theta)$ will be small



## 12 Support Vector Machines

### 12-1 Optimization objective

**Alternative view of logistic regression** 

$$h _ { \theta } ( x ) = \frac { 1 } { 1 + e ^ { - \theta ^ { T } x } }$$

If $y=1$,we want $h_{\theta}(x)\approx1, \theta^Tx\gg0$

If $y=0$,we want $h_{\theta}(x)\approx0, \theta^Tx\ll0$

​	**Cost of example:**$$- ( y \log h _ { \theta } ( x ) + ( 1 - y ) \log ( 1 - h _ { \theta } ( x ) ) )$$$$= - y \log \frac { 1 } { 1 + e ^ { - \theta ^ { r } x } } - ( 1 - y ) \log ( 1 - \frac { 1 } { 1 + e ^ { - \theta ^ { r } x } } )$$

**Support vector machine**

Logistic regression:
$$
min_\theta\frac { 1 } { m } [ \sum _ { i = 1 } ^ { m } y ^ { ( i ) }( -\log h _ { \theta } ( x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) (-\log ( 1 - h _ { \theta } ( x ^ { ( i ) } ) ) ] + \frac { \lambda } { 2 m } \sum _ { j = 1 } ^ { n } \theta^2_j
$$
support vector machine:
![image-20210906160856352](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906160856352.png)

$$min _ { \theta} C \sum _ { i = 1 } ^ { m }[ y ^ { ( i ) } {cost} _ { 1 } ( \theta ^ { T } x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) {cost} _ { 0 } ( \theta ^ { T } x ^ { ( i ) } ) ] + \frac { 1 } { 2 } \sum _ { i = 1 } ^ { n}\theta_j^2$$

**SVM hypothesis**
$$
min _ { \theta} C \sum _ { i = 1 } ^ { m }[ y ^ { ( i ) } {cost} _ { 1 } ( \theta ^ { T } x ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) {cost} _ { 0 } ( \theta ^ { T } x ^ { ( i ) } ) ] + \frac { 1 } { 2 } \sum _ { i = 1 } ^ { n}\theta_j^2
$$
Hypothesis:

$h_\theta(x)=\begin{cases}1\quad if\;\theta^Tx\ge0\\0\quad otherwise\end{cases}$

### 12-2 Large Margin Intuition

**Support Vector Machine**

if $y=1$,we want $\theta^Tx\ge1\quad(\text{not just $\ge$ 0})$

![image-20210906162105877](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906162105877.png)

if $y=0$,we want $\theta^Tx\le-1\quad(\text{not just $<$ 0})$

![image-20210906162121332](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906162121332.png)

**SVM Decision Boundary**

**SVM Decision Boundary: Linearly separable case**

![image-20210906162830504](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906162830504.png)

**Large margin classifier in presence of outliers**

![image-20210906163410368](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906163410368.png)

### 12-3 The mathematics behind large margin classification (optional)

**Vector Inner Product** 向量内积

![image-20210906164043687](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906164043687.png)

**SVM Decision Boundary**

![image-20210906164505354](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906164505354.png)

![image-20210906165218669](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906165218669.png)

### 12-4 Kernels I

核函数

**Non-linear Decision Boundary**

predict y=1 if $${ \theta _ { 0 } + \theta _ { 1 } x _ { 1 } + \theta _ { 2 } x _ { 2 } + \theta _ { 3 } x _ { 1 } x _ { 2 } } { + \theta _ { 4 } x _ { 1 } ^ { 2 } + \theta _ { 5 } x _ { 2 } ^ { 2 } + \cdots \geq 0 }$$

$h_\theta(x)=\begin{cases}1\quad if\;{ \theta _ { 0 } + \theta _ { 1 } x _ { 1 } + \theta _ { 2 } x _ { 2 } + \theta _ { 3 } x _ { 1 } x _ { 2 } } {  + \cdots \geq 0 }\\0\quad otherwise\end{cases}$

Given x,compute new feature depending on proximity to landmarks $l^{(1)},l^{(2)},l^{(3)}$

**Kernels and Similarity**

$f_1=similarity(x,l^{(1)})=exp(-\frac{||x-l^{(1)}||^2}{2\sigma^2})=\operatorname { exp } ( - \frac { \sum _ { j = 1 } ^ { n } ( x _ { j } - l _j^{ ( 1 ) } ) ^ { 2 } } { 2 \sigma ^ { 2 } } )$

$If \; x\approx l^{(1)}:$$f_1\approx 1$

$If \;x\; if \; far \; from\;l^{(1)}:$$f_1\approx 0$

![image-20210906171414865](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906171414865.png)

###  12-5 Kernels II

**Choosing the landmarks**

**SVM with Kernels**

Given $$( x ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( x ^ { ( 2 ) } , y ^ { ( 2 ) } ) , \cdots , ( x ^ { ( m ) } , y ^ { ( m ) } )$$

choose $$l ^ { ( 1 ) } = x ^ { ( 1 ) } , l ^ { ( 2 ) } = x ^ { ( 2 ) } , \cdots , l ^ { ( m ) } = x ^ { ( m ) }$$

Given example x:	

​			$\begin{array}{l}f_1=similarity(x,l^{(1)})\\f_2=similarity(x,l^{(2)})\\\cdots\end{array}$

For training example $(x^{(i)},y^{(i)})\longrightarrow f^{(i)}$

---

Hypothesis: Given x,compute features $f\in \mathbb{R}^{m+1}$

Predict "y=1" if $\theta^T f\ge 0$

Training:$min _ { \theta} C \sum _ { i = 1 } ^ { m }[ y ^ { ( i ) } {cost} _ { 1 } ( \theta ^ { T } f ^ { ( i ) } ) + ( 1 - y ^ { ( i ) } ) {cost} _ { 0 } ( \theta ^ { T } f ^ { ( i ) } ) ] + \frac { 1 } { 2 } \sum _ { i = 1 } ^ { n}\theta_j^2$

**SVM parameters:**

$C(=\frac{1}{\lambda})$.	

Large C: Lower bias, high variance.(small $\lambda$)
Small C: Higher bias, low variance.($large\;\lambda$)

$\sigma^2$

Large $\sigma^2$: Features $f_i$; vary more smoothly. Higher bias, lower variance.

Small $\sigma^2$: Features $f_i$; vary less smoothly. Lower bias, Higher variance.

### 12-6 Using an SVM

Use SVM software package (e.g. liblinear,  libsvm, ..) to solve for parameters $\theta$

Need to specify:

Choice of parameter C

Choice of kernel (similarity function):

​	E.g.	No kernel ("linear kernel") 

$\theta _ { 0 } + \theta _ { 1 } x _ { 1 } + \theta _ { 2 } x _ { 2 } + \theta _ { 3 }  + \cdots \ge 0 \longrightarrow n\;large,m\;small$

​			  predict:"y=1" if $\theta^Tx\ge0$

​	Gaussian kernel:

$f_i=exp(-\frac{||x-l^{(i)}||^2}{2\sigma^2}),where\;l^{(i)}=x^{(i)}$

​				Need to choose $\sigma^2$

**Kernel (similarity) functions:**

```octave
function f= kernel(x1,x2)
	f=exp((-abs(x1-x2)^2)/(2*(sigma^2)))
return
```

Note: Do perform feature scaling before using the Gaussian kernel

=[](#4-3 Gradient descent in practice I: Feature Scaling)

**Other choices of kernel** 

Note: Not all similarity functions similarity(x, l) make valid kernels (Need to satisfy technical condition called"mercer's Theorem"to make sure SVM packages' optimizations run correctly, and do not diverge)

Many of-the-shelf kernels avaliable:

	- Polynomial kernel:$k(x,l)=(x^Tl)^2,(x^Tl+1)^3,(x^Tl+5)^4$
	- More esoteric: String kernel, chi-square kernel, histogram intersection kernel

**Multi-class classification**

![image-20210906183431232](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210906183431232.png)

**Logistic regression vs. SVMS**

m=number of features($x\in \mathbb{R}^{n+1}$), m =number of training examples
If n is large(relative to m)
	Use logistic regression, or SVM without a kernel ("linear kernel")

If n is small, m is intermediate:
	Use SVM with Gaussian kernel

If m is small, m is large:
	Create/add more features, then use logistic regression or SVM without a kernel

Neural network likely to work well for most of these settings, but may be slower to train



## 13 Clustering

### 13-1 Unsupervised learning introduction

**Supervised learning**

![image-20210908144714085](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210908144714085.png)

Training set: $$\{ ( x ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( x ^ { ( 2 ) } , y ^ { ( 2 ) } ) , ( x ^ { ( 3 ) } , y ^ { ( 3 ) } ) , \cdots , ( x ^ { ( m ) } , y ^ { ( m ) } ) \}$$

**Unsupervised learning:**

![image-20210908144909284](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210908144909284.png)

Training set: $$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , x ^ { ( 3 ) } , \cdots , x ^ { ( m ) } \}$$

**Applications of clustering**

Market segmentation

Social network analysis

Organize computing clusters

Astronomical data analysis

### 13-2 K-means algorithm

step1：cluster assignment 簇分配

step2：move centroid 移动聚类中心

**K-means algorithm**

Input:

- K(number of cluster)
- Training set:  $$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , x ^ { ( 3 ) } , \cdots , x ^ { ( m ) } \}$$

$$x ^ { ( i ) } \in \mathbb{R} ^ { n }\quad\text{drop $x_0=1$ convention}$$

---

Randomly initialize K cluster centroids $\mu_1,\mu_2,\cdots,\mu_K\in\mathbb{R}^n$

Repeat{

​	for $i=1$ to m

​		$c^{(i)}$:=index (from 1 to K) of cluster centroid closet to $x^{(i)}$

​	for $k=1$ to K

​		$\mu_k$:=average(mean) of points assigned to cluster k

}

**K-means for non-separated clusters**

### 13-3 Optimization objective

**K-means optimization objective**

$c^{(i)}$= index of cluster (1, 2, ...,K) to which example $x^{(i)}$ is currently assigned
$\mu_k$= cluster centroid $k\;(\mu_k\in\mathbb{R}^n)$

$\mu_{c^{(i)}}$= cluster centroid of cluster to which example $x^{(i)}$ has been assigned

Optimization objective:
$$
J(c^{(1)},\cdots,c^{(m)},\mu_1,\cdots,\mu_K)=\frac{1}{m}\sum_{i=1}^{m}||x^{(i)}-\mu_{c^{(i)}}||^2
$$

$$
\underset{\mu_1,\cdots,\mu_K}{\underset{c^{(i)},\cdots,c^{(m)}}{\min}}J(c^{(1)},\cdots,c^{(m)},\mu_1,\cdots,\mu_K)
$$

### 13-4 Random initialization

**Random initialization**

Should have K < m
Randomly pick K training examples
Set $\mu_1,\cdots,\mu_k$ equal to these K examples

**Local optima**	**Random initialization**

K=2-10,if large not necessary

For i= 1 to 100 {
		Randomly initialize K-means
		Run K-means. Get $c^{(1)},\cdots,c^{(m)},\mu_1,\cdots,\mu_k$
		Compute cost function( distortion )

​			$J(c^{(1)},\cdots,c^{(m)},\mu_1,\cdots,\mu_K)$

}

Pick clustering that gave lowest cost $J(c^{(1)},\cdots,c^{(m)},\mu_1,\cdots,\mu_K)$

### 13-5 Choosing the number of cluster

by hand better

**What is the right value of K?** No right answer

**Choosing the value of K** 

Elbow method: 

Sometimes, you're running K-means to get clusters to use for some later/downstream purpose. Evaluate K-means based on a metric for how well it performs for that later purpose.



## 14 Dimensionality Reduction

### 14-1 Motivation I:Data Compression

**Data Compression**

Reduce data from 2D to 1D:project line $x_1,x_2\longrightarrow z_1$

Reduce data from 3D to 2D:project plane $x_1,x_2,x_3\longrightarrow z_1,z_2$

### 14-2 Motivation I:Data Visualization

**Data Visualization**

### 14-3 Principal Component Analysis problem formulation

PCA 主成分分析

**Principal Component Analysis (PCA) problem formulation**

Reduce from 2-dimension to 1-dimension: Find a direction (a vector $u^{(i)}\in \mathbb{R}^n$) onto which to project the data so as to minimize the projection error

Reduce from n-dimension to k-dimension: Find k vectors $u^{(1)},u^{(2)},\cdots,u^{(k)}$ onto which to project the data, so as to minimize the projection error.

**PCA is not linear regression**

linear regression: distance y x$\longrightarrow$y

PCA: distance  $x_1,x_2,\cdots$

### 14-4 Principal Component Analysis algorithm

**Data preprocessing**

Training set: $x^{(i)},x^{(2)},\cdots,x^{(m)}$

Preprocessing (feature scaling/mean normalization):

​	$\mu_j=\frac{1}{m}\sum^m_{i=1}x_j^{(i)}$

​	Replace each $x_j^{(i)}$ with $x_j-\mu_j$.

 If different features on different scales(e.g.,$x_1$=size of house,$x_2$ =number of bedrooms), scale features to have comparable range of values.

**Principal Component Analysis (PCA) algorithm**

Reduce data from n-dimensions to k-dimensions
Compute "covariance matrix"
$\sum=\frac{1}{m}\sum^{n}_{i=1}(x^{(i)})(x^{(i)})^T$
Compute "eigenvectors"of matrix $\sum$:

```octave
[U,S,V]=svd(Sigma); %or eig(sigma)
```

Sigma: $n\times n$ matrix

From [U,S,V]=svd(Sigma),we get:

$U_{reduce}$ ：$U=[u^{(1)},u^{(2)},u^{(3)},\cdots,u^{(n)}]\in\mathbb{R}^{n\times n}$

![image-20210909163833748](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210909163833748.png)

---

After mean normalization(ensure every feature has zero mean )and optionally feature scaling:

$Sigma=\frac{1}{m}\sum^{n}_{i=1}(x^{(i)})(x^{(i)})^T$

$[U,S,V]=svd(Sigma);$

$Ureduce=U(:,1:k);$

$z=Ureduce'*x$

### 14-5 Choosing the number of principal components

**Choosing k (number of principal components)**

![image-20210909165215813](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210909165215813.png)

![image-20210909165621053](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210909165621053.png)

![image-20210909165814013](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210909165814013.png)

### 14-6 Reconstruction from compressed representation

**Reconstruction from compressed representation**

$z=U_{reduce}^Tx\quad x_{approx}=U_{reduce}.z$

### 14-7 Advice for applying PCA

**Supervise learning speedup**

$$( x ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( x ^ { ( 2 ) } , y ^ { ( 2 ) } ) , \cdots , ( x ^ { ( m ) } , y ^ { ( m ) } )$$

Extract inputs:

​	Unlabeled dataset: $$x ^ { ( 1 ) } , x ^ { ( 2 ) } , \cdots , x ^ { ( m ) }\in\mathbb{R}^{10000}\longrightarrow z ^ { ( 1 ) } , z ^ { ( 2 ) } , \cdots , z ^ { ( m ) }\in\mathbb{R}^{1000}$$

​	New training set:

$$( z ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( z ^ { ( 2 ) } , y ^ { ( 2 ) } ) , \cdots , ( z ^ { ( m ) } , y ^ { ( m ) } )$$

Note: Mapping $x^{(i)}\rightarrow z^{(i)}$ should be defined by running PCA only on the training set. This mapping can be applied as well to the examples $x_{cv}^{(i)}$ and $x_{test}^{(i)}$ in the cross validation and test sets.

**Application of PCA**

- Compression
  - Reduce memory/disk needed to store data
  - Speed up learning algorithm
- Visualization

**Bad use of PCA: To prevent overfitting**

Use :$z^{(i)}$ instead of $x^{(i)}$ to reduce the number of features to $k<n$
Thus, fewer features, less likely to overfit

 $\color{red}\large{\times}$

This might work OK, but isnt a good way to address overfitting. Use regularization instead

$$\underset{\theta}{min} \frac { 1 } { 2 m } \sum _ { i = 1 } ^ { m } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } )^2+ \frac { \lambda } { 2 m } \sum _ { j = 1 } ^ { n } \theta _ { j } ^ { 2 }$$

**PCA is sometimes used where it shouldn't be**

Design of ML system:

- Get training set $$\{ ( x ^ { ( 1 ) } , y ^ { ( 1 ) } ) , ( x ^ { ( 2 ) } , y ^ { ( 2 ) } ) , \cdots , ( x ^ { ( m ) } , y ^ { ( m ) } ) \}$$

- Run PCA to reduce $x^{(i)}$ in dimension to get $z^{(i)}$
- Train logistic regression on $$\{ ( z ^ { ( 1 ) } , y ^ { ( 1 ) } ) , \cdots , ( z ^ { ( m ) } , y ^ { ( m ) } ) \}$$

- Test on test set:Map $x_{test}^{(i)}$ to $z_{test}^{(i)}$.Run $h_\theta(z)$ on $\{(z_{test}^{(1)},y_{test}^{(1)},\cdots,(z_{test}^{(m)},y_{test}^{(m)})\}$

How about doing the whole thing without using PCA?

Before implementing PCA, first try running whatever you want to do with the original /raw data $x^{(i)}$. Only if that doesn't do what you want, then implement PCA and consider using $z^{(i)}$



## 15 Anomaly detection

### 15-1 Problem motivation

**Anomaly detection example**

Aircraft engine features:

​	$x_1$=heat generated

​	$x_2$=vibration intensity

​	$\cdots$

Dataset: $$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , \cdots , x ^ { ( m ) } \}$$

New engine :$x_{test}$

![image-20210910151524616](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910151524616.png)

**Density estimation**

Dataset:$$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , \cdots , x ^ { ( m ) } \}$$
Is $x_{test}\quad anomalous?$

---

**Example**

Fraud detection:
	$x^{(i)}$= features of user i's activities
	Model p(x) from data
	Identify unusual users by checking which have $p(x)<\epsilon$

Manufacturing

Monitoring computers in a data center

​	$x^{(i)}$= features of machine i
​	$x_1$ =memory use , $x_2$=number of disk accesses/sec
​	$x_3$ =CPU load , $x_4$ =CPU load/network traffic

### 15-2 Gaussian distribution

**Gaussian (Normal) distribution**

​	Say $x\in\mathbb{R}$. If $x$ is a distribution Gaussian with mean $\mu$,variance $\sigma^{2}$

​			 $x\sim N(\mu,\sigma^2)$

​			$p(x;\mu,\sigma^2)=\frac{1}{\sqrt{2\pi}\sigma}e^{(-\frac{(x-\mu)^2}{2\sigma^2})}$

​			σ larger，image wider

**Parameter estimation**

Dataset:$$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , \cdots , x ^ { ( m ) } \}$$ 	$x^{(i)}\in \mathbb{R}$

### 15-3 Algorithm

**Density estimation**

Training set: $x^{(1)},\cdots,x^{(m)}$

Each example is $x\in \mathbb{R}^n$

**Anomaly detection algorithm**

1. Choose features $x_i$ that you think might be indicative of
    anomalous examples.

2. Fit parameters 

   $\mu_1,\cdots,\mu_n,\sigma_1^2,\cdots,\sigma_n^2$

   $$\mu _ { j } = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } x _ { j } ^ { ( i ) }$$

   $$\sigma _ { j } ^ { 2 } = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } ( x _ { i } ^ { ( i ) } - \mu _ { j } ) ^ { 2 }$$

3. Given new example x, compute p(x):

  $$p ( x ) = \prod _ { j = 1 } ^ { n } p ( x _ { j } ; u _ { j } , \sigma _ { j } ^ { 2 } ) = \prod _ { j=1 } ^ { n } \frac { 1 } { \sqrt { 2 \pi } \sigma _ { j } } e x p ( - \frac { ( x _ { j } - u _ { j } ) ^ { 2 } } { 2 \sigma _ { j } } )$$

  Anomaly if $p(x)<\epsilon$

**Anomaly detection example**

![image-20210910163307727](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910163307727.png)

### 15-4 Developing and evaluating an anomaly detection system

**The importance of real-number evaluation**

When developing a learning algorithm(choosing features, etc. ), making decisions is much easier if we have a way of evaluating our learning algorithm

Assume we have some labeled data of anomalous and non anomalous examples. (y=0 if normal, y=1 if anomalous

Training set: $x^{(1)},x^{(2)},\cdots,x^{(m)}$(assume normal examples/not anomalous)

Cross validation set :$$( x_{cv} ^ { ( 1 ) } , y_{cv} ^ { ( 1 ) } ) , \cdots , ( x_{cv} ^ { ( m _ { c v } ) } , y_{cv} ^ { ( m _ { c v } ) } )$$

Test set :$$( x_{test} ^ { ( 1 ) } , y_{test} ^ { ( 1 ) } ) , \cdots , ( x_{test} ^ { ( m _ { test } ) } , y_{test} ^ { ( m _ { test } ) } )$$

**Aircraft engines motivation example**

10000 good (normal) engines

20 flawed engines (anomalous)

>  Training set : 6000 good engines
>
> CV: 2000 good engines(y=0),10 anomalous (y=1)
>
> Test: 2000 good engines(y=0),10 anomalous(y=1)

or Alternative

**Algorithm evaluation**

Fit model $p(x)$ on training set $\{x^{(1)},\cdots,x^{(m)}\}$

On a cross validation/test example predict
$$
y=\begin{cases}1\quad if\;p(x)<\epsilon\;(anomaly)\\0\quad if\;p(x)\ge\epsilon\;(normal) \end{cases}
$$
Possible evaluation metrics:

- True positive, false positive, false negative, true negative
- Precision/Recall
- $F_1$ -score

Can also use cross validation set to choose parameter $\epsilon$

### 15-5 Anomaly detection vs. supervised learning

![image-20210910171310916](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910171310916.png)

![image-20210910171512210](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910171512210.png)

### 15-6 Choosing what features to use

**Non-gaussian features**

make the data look a bit more Gaussian

**Error analysis for anomaly detection**

Want   $p(x)$ large for normal examples $x$
			$p(x)$ small for anomalous examples a
Most common problem:
			$p(x)$ is comparable (say, both large) for normal
and anomalous examples

**Monitoring computers in a data center **

Choose features that might take on unusually large or small values in the event of an anomaly
$x_1$= memory use of computer
$x_1$=number of disk accesses/sec
$x_1$=CPU load
$x_1$=network traffic

### 15-7 Multivariate Gaussian distribution

**Motivating example: Monitoring machines in a data center**

**Multivariate Gaussian (Normal) distribution**

$x\in\mathbb{R}^n$.Don't model $p(x_1),p(x_2),\cdots,etc.$separately.
Model $p(x)$ all in one go.
Parameters:$\mu\in\mathbb{R}^n,\Sigma\in\mathbb{R}^{n\times n}\;(covariance\;matrix)$ 

![image-20210910180140801](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910180140801.png)

**Multivariate Gaussian (Normal) examples**

![image-20210910181718845](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910181718845.png)

### 15-8 Anomaly detection using the multivariate Gaussian distribution

**Multivariate Gaussian (Normal)distribution**

Parameters $\mu,\Sigma$

$$p ( x ; \mu , \Sigma ) = \frac { 1 } { ( 2 \pi ) ^ { \frac { n } { 2 } } | \Sigma  ^ { \frac { 1 } { 2 } } |}e^{(- \frac { 1 } { 2 } ( x - \mu ) ^ { T } \Sigma ^ { - 1 } ( x - \mu ))}$$

Parameter fitting:

Given training set $$\{ x ^ { ( 1 ) } , x ^ { ( 2 ) } , \cdots , x ^ { ( m ) } \}$$

$$u = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } x ^ { ( i ) }$$

$$\Sigma=\frac{1}{m} \sum _ { i = 1 } ^ { m } ( x ^ { ( i ) } - \mu ) ( x ^ { ( i ) } - \mu ) ^ { T }$$

**Anomaly detection with the multivariate Gaussian**

1. Fit model $p(x)$ by setting

   $$u = \frac { 1 } { m } \sum _ { i = 1 } ^ { m } x ^ { ( i ) }$$

   $$\Sigma=\frac{1}{m} \sum _ { i = 1 } ^ { m } ( x ^ { ( i ) } - \mu ) ( x ^ { ( i ) } - \mu ) ^ { T }$$

2. Given a new example x,compute

   $$p ( x ; \mu , \Sigma ) = \frac { 1 } { ( 2 \pi ) ^ { \frac { n } { 2 } } | \Sigma  ^ { \frac { 1 } { 2 } } |}e^{(- \frac { 1 } { 2 } ( x - \mu ) ^ { T } \Sigma ^ { - 1 } ( x - \mu ))}$$
   Flag an anomaly if $p(x)<\epsilon$

**Relationship to original model**

Original model:$$p ( x ) = p ( x _ { 1 } ; \mu _ { 1 } , \sigma _ { 1 } ^ { 2 } ) \times p ( x _ { 2 } ; \mu _ { 2 } , \sigma _ { 2 } ^ { 2 } ) \times \cdots \times p ( x _ { n } ; \mu _ { n } , \sigma_n^2 )$$

Corresponds to multivariate Gaussian

$$p ( x ; \mu , \Sigma ) = \frac { 1 } { ( 2 \pi ) ^ { \frac { n } { 2 } } | \Sigma|^{ \frac { 1 } { 2 } } } e x p ( - \frac { 1 } { 2 } ( x - \mu ) ^ { T } \Sigma ^ { - 1 } ( x - \mu ) )$$

where

![image-20210910183926221](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210910183926221.png)



## 16 Recommender System

### 16-1 Problem formulation

**Example : predicting movie rating**

User rates movies using one to five stars

![image-20210911152136387](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911152136387.png)

### 16-2 Content-based recommendations

**content-based recommender systems**

![image-20210911153052919](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911153052919.png)

**Problem formulation**

$r(i,j)=$1 if user j has movie i	(0,otherwise)

$y^{(i,j)}$ =rating by user j on movie i (if defined)

$\theta^{(j)}$=parameter vector for user j

$x^{(j)}$=feature vector for movie i

For user j,movie i,predicted rating:$(\theta^{(j)})^T(x^{(i)})$

$m^{(j)}=$no. of movie rated by user j

To learn $\theta^{(j)}$:

$\underset{\theta^{(j)}}{min}\frac{1}{2m^{(j)}}\underset{i:r(i,j)=1}{\sum}((\theta^{(j)})^T(x^{(i)})-y^{(i,j)})^2+\frac{\lambda}{2m^{(j)}}\sum^{n}_{k=1}(\theta_K^{(j)})^2$	$\theta^{(j)}\in\mathbb{R}^{n+1}$

**Optimization objective:**

To learn $\theta^{(j)}$(parameter for user j):

$$\underset{\theta^{(j)}}{min}\frac{1}{2}\underset{i:r(i,j)=1}{\sum} ( ( \theta ^ { ( j ) } ) ^ { T } x ^ { ( i ) } - y ^ { ( i , j ) } ) ^ { 2 } + \frac { \lambda } { 2 } \sum _ { k = 1 } ^ { n } ( \theta _ { k } ^ { ( j ) } ) ^ { 2 }$$

To learn $\theta^{(1)},\theta^{(2)},\cdots,\theta^{(n_u)}:$

![image-20210911154604916](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911154604916.png)

![image-20210911155110999](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911155110999.png)

### 16-3 Collaborative filtering

协同过滤

![image-20210911160248402](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911160248402.png)

### 16-4 Collaborative filtering algorithm

**Collaborative filtering optimization objective**

![image-20210911161521652](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911161521652.png)

**Collaborative filtering algorithm**

1. Initialize $x^{(1)},\cdots,x^{(n_m)},\theta^{(1)},\cdots,\theta^{(n_u)}$ to small random values.

2. Minimize $J(x^{(1)},\cdots,x^{(n_m)},\theta^{(1)},\cdots,\theta^{(n_u)})$ using gradient descent (or an advanced optimization algorithm).E.g. for every $j=1,\cdots,n_u,i=1,\cdots,n_m$:

   ($\color{red}\text{no loger $x_0,\theta_0$}$)

   ![image-20210911162732075](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911162732075.png)

3. For a user with parameters θ and a movie with (learned)
   features x , predict a star rating of $\theta^Tx$.

### 16-5 Vectorization: Low rank matrix factorization

低秩矩阵分解

**Collaborative filtering**$\longrightarrow$**Low rank matrix factorization**

![image-20210911164929347](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911164929347.png)

**Find related movies**

For each product i,we learn a feature vector $x^{(i)}\in\mathbb{R}^n$

find smallest $||x^{(i)}-x^{(j)}||$

### 16-6 Implementational detail : Mean normalization

**User who have not rated any movie**

![image-20210911165452572](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911165452572.png)

**Mean Normalization**

![image-20210911165950061](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210911165950061.png)

## 17 Large scale machine learning

### 17-1 Learning with large datasets

**Machine learning and data**

Classify between confusable words. E.g., (to, two, too), (then, than)

>  It's not who has the best algorithm that wins It's who has the most data

**Learning with large datasets**

![image-20210912095552787](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912095552787.png)

### 17-2 Stochastic gradient descent

**Learning regression with gradient descent**

![image-20210912095945162](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912095945162.png)

![image-20210912100716193](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912100716193.png)

**Stochastic gradient descent**

1. Randomly shuffle (reorder) training example

2. Repeat{

   ​	for $i:=1,\cdots,m${

   ​		$\theta_j=\theta_j-\alpha(h_\theta(x^{(i)})-y^{(i)})x_j^{(i)}$

   ​					(for every $j=0,\cdots,n$)

   ​	}

   }

   

### 17-3 Mini-batch gradient descent

**Mini-batch gradient descent**
Batch gradient descent: Use all m examples in each iteration
Stochastic gradient descent: Use 1 example in each iteration
Mini-batch gradient descent: Use b examples in each iteration

example：

Say $b=10,m=1000$
Repeat{
	for $i=1,11,21,31,\cdots,991${
		$\theta_j:=\theta_j-\alpha\frac{1}{10}\sum_{k=1}^{i+9}(h_\theta(x^{(i)})-y^{(i)})x_j^{(i)}$
				（for every j=0，...,n）
	}
}

### 17-4 Stochastic gradient descent converence

**Checking for convergence**

*Batch gradient descent:*

​	Plot $J_{train}(\theta)$ as a function of number of iterations of gradient decent.
​		$J_{train}(\theta)=\frac{1}{2m}(h_\theta(x^{(i)})-y^{(i)})^2$

*Stochastic gradient descent:*

​	$cost( \theta , ( x ^ { ( i ) } , y ^ { ( i ) } ) ) = \frac { 1 } { 2 } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) ^ { 2 }$

​	During learning, compute $cost(\theta,(x^{(i)},y^{(i)})^2$ before updating $\theta$ using $(x^{(i)},y^{(i)})$
​	Every 1000 iterations(say), plot $cost(\theta,(x^{(i)},y^{(i)})^2$ averaged over the last 1000 examples processed by algorithm

Learning rate a is typically held constant Can slowly decrease $\alpha$ over time if we want $\theta$ to converge. (E.g. $\alpha=\frac{const1}{iterationNumber+const2}$)

### 17-5 Online learning

**Online learning**
Shipping service website where user comes, specifies origin and destination, you offer to ship their package for some asking price, and users sometimes choose to use your shipping service (y=1) sometimes not (y=0).

Features $x$ capture properties of user, of origin/destination and asking price. We want to learn $p(y=1|x;\theta)$ to optimize price.

![image-20210912110031783](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912110031783.png)

**Other online learning example:**
Product search (learning to search)
	User searches for "Android phone 1080p camera"
	Have 100 phones in store Will return 10 results.

$x$=features of phone, how many words in user query match name of phone, how many words in query match description of phone, etc.
$y=1$ if user clicks on link. $y=0$ otherwise
Learn $p(y=1|x;\theta)$
Use to show user the 10 phones they're most likely to click on.

Other examples: Choosing special offers to show user; customized selection of news articles; product recommendation

### 17-6 Map-reduce and data parallelism

减少映射和数据并行

**Map-reduce**

Batch gradient descent： $$\theta _ { j }  : = \theta _ { j } - \alpha \frac { 1 } { 400 } \sum _ { i = 1 } ^ { 400 } ( h _ { \theta } ( x ^ { ( i ) } ) - y ^ { ( i ) } ) x _ { j } ^ { ( i ) }$$

​	![image-20210912112242220](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912112242220.png)

**Map-reduce and summation over the training set**
Many learning algorithms can be expressed as computing sums of functions over the training set

![image-20210912113555011](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912113555011.png)

**Multi-core machines**



## 18 Application example photo OCR

### 18-1 Problem description and pipeline

**The photo  OCR problem**

1.Text detection

2.Character segmentation

3.Character classification (recognition)

4.*Spelling correction

**Photo OCR pipeline**

![image-20210912154056239](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912154056239.png)

### 18-2 Sliding windows

**Text detection** | **Pedestrian detection**

**Supervised learning for pedestrian detection**

![image-20210912154751535](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912154751535.png)

Sliding window detection

**Text detection**

![image-20210912155324319](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912155324319.png)

**1D Sliding window for character segmentation**

![image-20210912160211406](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912160211406.png)

### 18-3 Getting lots of data: Artificial data synthesis

**Character recognition**

**Artificial data synthesis for photo OCR**

![image-20210912191351430](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912191351430.png)

**Synthesizing data by introducing distortions**

![image-20210912192152507](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912192152507.png)

**Discussion on getting more data**

1. Make sure you have a low bias classifier before expending the effort(Plot learning curves). E.g. keep increasing the number of features/number of hidden units in neural network until you have a low bias classifier
2. How much work would it be to get 10x as much data as we currently have?

  - Artificial data synthesis

  - Collect/label it yourself
  - Crowd source"(E.g. Amazon Mechanical Turk)

### 18-4 Ceiling analysis What part of the pipeline to work on next

**Estimating the errors due to each component(ceiling analysis**

What part of the pipeline should you spend the most time trying to improve?

**Another ceiling analysis example**
Face recognition from images (Artificial example

![image-20210912194850809](https://gitee.com/contrachen/img-load/raw/master/typora_md/image-20210912194850809.png)

## 19 Conclusion-Summary and Thank you

**Summary: Main topics**
Supervised Learning
-Linear regression, logistic regression, neural networks, SVMS
Unsupervised Learning
-K-means, PCA, Anomaly detection
Special applications/special topics
-Recommender systems, large scale machine learning
Advice on building a machine learning system
-Bias/variance, regularization; deciding what to work on next: evaluation of learning algorithms, learning curves, error analysis, ceiling analysis
