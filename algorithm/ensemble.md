# Ensemble learning

### Overview
* [wikipedia/Category:Ensemble_learning](https://en.wikipedia.org/wiki/Category:Ensemble_learning)
* [wikipedia/Boosting](https://en.wikipedia.org/wiki/Boosting_(machine_learning)

### Boosting
* [wikipedia/Gradient boosting](
  https://en.wikipedia.org/wiki/Gradient_boosting)
* AdaBoost
* GBDT

### Parallel Methods
* Bagging
* Random Forest: Random Forest

### Stacking Methods / Blending
* Stacked generalization （by D. Wolpert）
* 将分类器的结果作为下一层分类器的输入，将分类器堆叠起来，提升性能
* 刚刚搞的 Deep Forest 可以算是在这类方法上的升级

#### Paper
> 以下paper都是 二十年之内 机器学习领域经典，引用少则上千多则几万，必读经典； 如果不知道，好像很难说是在 ML圈内混的 -by 空芃

##### Sequential Methods/ Boosting
> 记住一个人 R Schapire， 还有一段未解的纷争

* AdaBoost ：
  * A desicion-theoretic generalization of on-line learning and an application to boosting (by Y Freund, R Schapire)
    > * AdaBoost是求证一个理论问题的副产品，即：弱可学习性和强可学习性的等价性， AdaBoost是一个构造性证明
    > * R Schapire靠此文获得 理论计算机科学最高奖 Gödel 奖
  * Boosting the margin: A new explanation for the effectiveness of voting methods （by Schapire、Freund、Barlett、 et al.）
    > * AdaBoost在实践中取得了优异的性能，但是其理论性质未知
    > * Schapire等人认为， boosting就是在最大化margin，并给出了泛化性证明
  * Additive logistic regression: a statistical view of boosting (With discussion and a rejoinder by the authors) (by FHT)
    > * 统计学界对它为啥work一直不理解，并且认为margin的解释是一个不靠谱的东西
    > * 统计的几个大牛FHT（这几个人是统计界的巨牛，还是要知道一下的）提出了一套理论解释， 认为Boosting就是在Fit一个加性模型
    > * 但是很多人也不是很买这个账，后面有一堆的discussion， 有兴趣的话，大家可以看一下
  * Boosting的理论工作，仍然是一个open的问题，基本上都是这两派代表
  * [应用] Rapid Object Detection using a Boosted Cascade of Simple Features： AdaBoost最强大的一个应用是 Viola_Jones的face detecter，直接造就了 CV 领域的近二十年来最大的 breakthrough， 把实验室玩的 detection 搞到了实时，可工业化生产

* GBM / GBDT :
  > 记住一个人 JH Friedman，不错，就是 FHT里面的F

  * Greedy function approximation: a gradient boosting machine
  * 从梯度下降角度看 Boosting的过程， 认为boosting就是在用梯度下降fit一个函数
  * 是一个强大的框架，可以加速不同的loss， 在工业界用的极多


##### Parallel Methods
> 记住一个人 Leo Breiman（一个具有神奇经历的人，统计界巨牛，一趟非洲之旅改变了人生观，将生命的最后几年投入machine learning，产生了几个极其有影响力的神级工作）

* Bagging ： Bagging Predictors
  > 巨简单的 ensemble 方法，对样本做一个 有放回的取样，然后再 vote，效果很好

* Random Forest: Random Forest
  > 可以认为是 Bagging + Random Tree， 在现实使用中具有极好的性能，同时使用方便

> Bagging和RF的理论分析很难做； bagging在regression有一些 bias - variance 分解的说明， 在分类情况下，还是open的问题

##### Stacking Methods / Blending
> 记住一个人 D. Wolpert ，这个人还是要知道一下的， No Free Lunch 定理

  * Stacked generalization （by D. Wolpert）
  * 将分类器的结果作为下一层分类器的输入，将分类器堆叠起来，提升性能
  * 刚刚搞的 Deep Forest 可以算是在这类方法上的升级
