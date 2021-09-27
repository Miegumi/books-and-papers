[TOC]

## 一、已读论文总结

### 1.2021_Cross-validation what does it estimate and how well does it do it

- 使用非正则化OLS拟合线性模型时，普通的预测误差估计（交叉验证、bootstrap、Cp、数据分割）不适用于估计预测误差，它估计了来自同分布的其他数据集拟合模型的平均预测误差。
- 由于交叉验证得出的预测误差的标准置信区间可能远低于期望水平的覆盖率，因而引入嵌套的交叉验证（nested CV），证明嵌套CV具有一致的更好的覆盖率。
- 简单的数据分割不能给出有效的/渐进的置信区间。因此，如果想要预测误差的有效置信区间，建议数据拆分而不重新调整模型，或者嵌套CV。
- 摘录：Our primary result is that common estimates of prediction error—cross-validation, bootstrap,data splitting, and covariance penalties—cannot be viewed as estimates of the prediction error of the final model fit on the whole data. Rather, the estimate of prediction error is an estimate of the average prediction error of the final model across other hypothetical data sets from the same distribution.

### 2.2018_Principal component-guided sparse regression

  - 提出“Pclasso”方法适用于特征数p远大于观测值n的数据，该方法将Lasso(L1)稀疏惩罚与二次惩罚相结合，利用预测变量的相关性和分组结构来潜在地提高预测性能。如果特征被预先分配好组，PcLasso将每个分组的特征压缩到该组的主要特征，在这个过程中，它还进行了特征组的选择。

  - 摘录：We have proposed a new method for supervised learning that exploits the correlation and group structure of predictors to potentially improve prediction performance. We provide some theory for this method and illustrate it on a number of simulated and real data examples.

    

### 3.2016_Post-selection inference for l1-penalized likelihood models

   - 在回归模型选择后的推断问题上，本文将前人所得的高斯回归模型选择后的推断问题的结果推广到了lasso惩罚似然模型，包括Logistic回归模型和Cox风险比例模型等广义回归模型。
   - 本文在第二阶段估计时提出了创新，它与lasso后最大似然估计是渐进等价的，并且克服了二阶余数时遇到的一些问题。
   - lasso惩罚似然模型的选择后推断的估计量不需要MCMC抽样，并且可以在封闭环境下进行计算。其中估计量由在拟合套索后，在所选模型中进行的牛顿-拉夫森(或相当于Fisher评分)的单步计算构成。
   - 摘录：We applied lasso-penalized logistic regression, choos-
     ing the tuning parameter by cross-validation. The left panel shows the standard (naive) p-values and the post-selection p-values from our theory, for the predictors in the active set. Since the sample size is large compared to the number of predictors, the unadjusted and adjusted p-values are only substantially different for two of the predictors.

### 4.2016_High-dimensional regression adjustments in randomized experiments

   - 通过对具有高维协变量信息的随机试验中的处理效应估计问题的研究，证明了几乎任何风险一致的回归调整都可以用来获得平均处理效应的有效估计。
   - 本文提出了使用交叉估计的方法，从而可以简便地利用高维回归调整获得有限样本的无偏处理效应估计，并且可以将其引申到lasso，弹性网络，子集选择等回归模型估计的应用。
   - 在方法论创新方面，对原有的交叉验证方法进行了拓展，允许通过交叉验证进行自适应规范搜索，并使用了机器学习的方法（如随机森林或者神经网络）对非参数回归进行灵活地调整。
   - 摘录：However, the fact that model-free inference is possible in randomized controlled trials does not mean that it is always optimal: as argued by Fisher ,if we have access to auxiliary features that are related to our outcome of interest via a linear model, then controlling for these features using ordinary least squares will reduce the variance of the estimated average treatment effect without inducing any bias.

