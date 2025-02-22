<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS_HTML" async></script>
# 问题背景

# 什么是$k$阶鞍点

给定一个在实希尔伯特空间$\mathcal{H}$上定义的二次Fréchet可微的能量泛函$E(\bm{x})$，其内积为$\langle ·,· \rangle$，我们令$\bm{F}(\bm{x})=−\nabla E(\bm{x})$表示其自然力，$\mathbb{G}(\bm{x}) =\nabla^2E(\bm{x})$表示其Hessian矩阵。

-   如果$\lVert \bm{F}(\bm{\hat{x}}) \rVert =0$，则称$\hat{x}\in\mathcal{H}$为$E(\bm{x})$的一个临界点。

-   一个不是局部极值的$E(\bm{x})$的临界点被称为$E(\bm{x})$的一个鞍点。特别的，有些时候我们也把局部极小值称为$0$阶鞍点，局部极大值称为$d$(系统维度)阶鞍点。

-   如果$\mathbb{G}(\bm{\hat{x}})$有一个有界逆，则称临界点$\bm{\hat{x}}$为非退化的。

-   根据Morse理论，非退化临界点$\bm{\hat{x}}$的指数（Morse指数）是使得$\mathbb{G}(\bm{\hat{x}})$为负定的最大子空间$\mathcal{K}$的维数。我们的目标是找到势能面上的指数为$k$的鞍点，简称为$k\textendash saddle$或$k$阶鞍点。

-   为简便起见，我们假设$\mathcal{H}$的维数为$d$，并将内积$\langle \bm{x},\bm{y} \rangle$写为$\bm{x}^T\bm{y}$。

下面先从特征值和特征向量的角度给一个鞍点阶数的直观理解，便于之后问题的开展。

我们注意到Hessian矩阵是实对称矩阵（用到前面的二次Fréchet可微），其正交相似于一个对角矩阵，即存在正交矩阵$\mathbb{T}$和对角矩阵$\mathbb{D}$使得$\mathbb{T}^{-1}\mathbb{G}(\bm{\hat{x}})\mathbb{T}=\mathbb{D}$。
事实上这个对角矩阵的对角线上各个元素即为该实对称矩阵的特征值$\hat{\lambda}_1,\hat{\lambda}_2,\ldots,\hat{\lambda}_d$，
且不妨$\hat{\lambda}_1\leq\hat{\lambda}_2\leq\ldots\leq\hat{\lambda}_d$，并设此时$\mathbb{T}$的列向量为$\bm{\hat{v}}_1,\bm{\hat{v}}_2,\ldots,\bm{\hat{v}}_d$。

可以证明，对于非退化临界点$\hat{x}$，若$\hat{\lambda}_1\leq\ldots\leq\hat{\lambda}_k<0<\hat{\lambda}_{k+1}\leq\ldots\leq\hat{\lambda}_d$,则$k$即为该鞍点的阶数。
一方面，$\mathbb{G}(\bm{\hat{x}})$在$\bm{\hat{v}}_1,\bm{\hat{v}}_2,\ldots,\bm{\hat{v}}_k$生成的子空间$\hat{\mathcal{V}}$上是负定的，故$\bm{\hat{x}}$至少为$k$阶；
另一方面，对于$\mathcal{H}$的任意一个$k+1$维子空间$\mathcal{K'}$，有$\bm{\hat{v}}_{k+1},\ldots,\bm{\hat{v}}_d$生成的子空间$\hat{\mathcal{V}}^{\perp}$与$\mathcal{K'}$交非零（否则$\mathcal{K'}$中添上$\bm{\hat{v}}_{k+1},\ldots,\bm{\hat{v}}_d$生成$d+1$维空间，矛盾！）。
取交集中一个非零元素
$$\bm{w}=\displaystyle \sum_{i=k+1}^{d} a_i\bm{\hat{v}}_i$$ 则有
$$\bm{w^T\mathbb{G}(\hat{x})w}=\displaystyle \sum_{i=k+1}^{d} a_i\bm{\hat{v}}_i^T\sum_{i=k+1}^{d} \hat{\lambda}_ia_i\bm{\hat{v}}_i
=\displaystyle \sum_{i=k+1}^{d} \hat{\lambda}_ia_i^2>0$$
故$G(\bm{\hat{x}})$在$\mathcal{K'}$上不是负定的，即$\hat{x}$的阶数为$k$。

