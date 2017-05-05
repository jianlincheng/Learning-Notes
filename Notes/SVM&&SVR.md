## SVM
### Primal Hard-Margin SVM
tolerate more noise & more roubust to overfitting

    robustness = fatness distance to closest point 

    find largest-margin separating hyperplane

    suppot vector machine(SVM):learn fattest hyperplanes(with help of support vectors)

### Dual Hard-Margin SVM(KKT conditions)
SVM "wihtout" d'

    no dependence only if avoiding naive computation

SVM with general QP(Quadratic programming) solver

another QP,better soloved with special solver(Kernel)
### Soft-Magin SVM && Dual Soft-Margin SVM
margin violation

    large C:want less margin violation

    small C:want large margin

d'+1+N variables & 2N constraints
### Kernel Rigde Regreesion
## [SVR primal](http://www.ics.uci.edu/~welling/classnotes/papers_class/SVregression.pdf)  
todo : L2-Regularized tube regression to get sparse β
## [SVR Dual](https://alex.smola.org/papers/2003/SmoSch03b.pdf)
## Kernel
Transfer + Inner Product 

kernel trick : plug in efficient kernel function to avoid dependence on d' 

kernel represents special similarity(Inner Product)


* Polynomial Kernel(small-Q only)

    Pros

        less restricted than linear

        strong physical control - 'knows' degree Q
    Cons
        
        numerical difficulty for large Q

        three parameters - more difficult to select
* Gaussian Kernel

    Pros
        
        more powerful than linear/poly

        bounded-less numerical difficulty than  poly

        one parameter only-easier to select than poly
    Cons
        
        mysterious-no w

        slower than linear

        too powerful?!(may be overfit)