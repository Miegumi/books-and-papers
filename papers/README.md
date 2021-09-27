[TOC]
# paper写作思路

### 1. relaxed lasso + cox model
### 2. relaxed adaptive lasso
### 3. relaxed adaptive lasso + cox model


## 一、已读论文总结

### 1. Knight K, Fu W.(2000) - Asymptotics for Lasso-type estimators

- 在适当的条件下，我们证明了当参数的真值为0时，可以以正概率将回归参数的估计值收缩到0。
- $Z_{n}$是凸函数且满足条件C是非奇异的，当
  $\lambda_{n}=o(n)$时桥估计量$\hat{\boldsymbol{\beta}}_{n}$具有相合性。
- 当γ≥1，C是非奇异的且满足$\lambda_{n} / \sqrt{n} \rightarrow \lambda_{0} \geq 0$时，参数具有$\sqrt{n}$相合性，即$\sqrt{n}\left(\hat{\boldsymbol{\beta}}_{n}-\boldsymbol{\beta}\right) \rightarrow_{d} \operatorname{argmin}(V)$。
- 通过“局部渐近”来检验真参数很小但非零时的小样本行为，即在有限样本中，即使存在“大”参数，“小”参数也可以被精确地估计为0。
- 当γ<1时，我们可以无渐近偏差地以通常的速度估计非零回归参数，同时以正概率将零回归参数的估计缩小到0。



### 2. Peng Z,  Yu B(2006)- On Model Selection Consistency of Lasso

![Lasso一致性](https://user-images.githubusercontent.com/88085038/132467105-01e970de-1f04-4ab2-b0db-298caa8110bb.jpg)

### 3. Hastie T,Tibshirani R, Tibshirani R J(2017)-Extended Comparisons of Best Subset Selection, Forward Stepwise Selection, and the Lasso

- 最佳子集选择和lasso都没有明确适用的模型，最佳子集选择通常在高信噪比(SNR)条件下表现得更好，lasso在低信噪比下表现得更好；

- 最佳子集选择和正向逐步选择在整个过程中表现非常相似；

- 宽松lasso总体是最好的，在低信噪比下的表现与lasso差不多。

### 4. Wang X and Leng C(2016)-High-dimensional Ordinary Least-squares Projection for Screening Variables

- 计算估计量$\hat{\beta}=X^{T}\left(X X^{T}\right)^{-1} Y$为对角占优矩阵，从而 $\left|\hat{\beta}_{j}\right|$ 能尽可能保留 $\left|\beta_{\mathrm{j}}\right|$ 的大小顺序。证明Holp具有确定的筛选性质，在没有强相关性假设的情况下给出了一致的变量选择，并且计算效率高。

