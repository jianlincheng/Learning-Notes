# Interview Summary
## Machine learning
### Boosting
simple(weak) classifiers 

* logistic regreesion(simple feature)

add more features(second order polynomials,third order polynomials)
* shallow decision trees

go deeper 
* decision stumps

this weak classifiers are high bias and low variance which can not fit data very well

#### adaBoost
##### main thought about adaboost

Start same weight for all points

For t = 1 to T

* Learn weighted classification error
* Compute coefficient of classifier
* Recompute weights(more weight on data points where we made mistakes) 
* Normalize weights

Final model predict
### Bagging 
high variance & easily overfit

bootstrap sample:re-sample N examples from D uniformly with replacement-can also use arbitrary N instead of original dataset

For t = 1,2,...,T

* request size N data from bootstrapping
* obtain the model from data
* average the result


Simpler than boosting & easier to parallelize

Typically higher error than boosting for same numbers of trees
### Generative model vs Discriminative model
[On Discriminative vs. Generative classifiers: A comparison of logistic regression and naive Bayes](https://ai.stanford.edu/~ang/papers/nips01-discriminativegenerative.pdf)

生成模型是根据已知的样本用基于统计方法来估计整个样本空间的真实分布，判别模型就是根据已有的样本来生成一个“微缩”模型。
#### generative model
* Naive bayes
* Gaussian mixture model
* HMM(Hidden markov model)
* LDA(Latent Dirichlet allocation)

由数据学习联合概率分布，然后求条件概率分布作为预测模型。学习的是联合分布。
* 生成模型收敛速度比较快，即当样本数量较多时，生成模型能更快地收敛于真实模型
* 生成模型能够应付存在隐变量的情况，比如混合高斯模型就是含有隐变量的生成方法
* 联合分布是能提供更多的信息，但也需要更多的样本和更多计算，尤其是为了更准确估计类别条件分布，需要增加样本的数目，而且类别条件概率的许多信息是我们做分类用不到，因而如果我们只需要做分类任务，就浪费了计算资源

#### discriminative model
* SVM
* Nearest neighbor
* logistic regression
* Conditional random fields

由数据直接学习预测模型。
* 与生成模型缺点对应，首先是节省计算资源，另外，需要的样本数量也少于生成模型
* 准确率往往较生成模型高
* 由于直接学习预测条件概率，而不需要求解类别条件概率，所以允许我们对输入进行抽象（比如降维、构造等），从而能够简化学习问题
### AOC(area under curve)
The AUC value is equivalent to the probability that a randomly chosen positive example is ranked higher than a randomly chosen negative example.

which show how the number of correctly
classied positive examples varies with the number
of incorrectly classied negative examples
* ROC(receiver operating characteristic curve)

横坐标为false positive rate，纵坐标为true positive rate(recall)

consider four points (0,1),(1,0),(0,0),(1,1)

(0,1):完美分类器

(1,0):最差分类器

(1,1):都分类成了正样本

(0,0):都分类成了负样本

优点：
* cost-sensitive learning and learning in the presence of
unbalanced classes

[An introduction to ROC analysis](http://people.inf.elte.hu/kiss/12dwhdm/roc.pdf)
### Precision(Fraction of positive predictions that are actually positive)
High precision means positive predicitions actually likely to be positive
### Recall(Fraction of positive datapredicted to be positive)
High recall means positive data points are very likely to be discovered










 




































































































































































                
