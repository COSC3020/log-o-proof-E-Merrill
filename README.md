# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$
Applying the log base change formula to change both logarithms to a base of e:  
$log_{5} n = \frac{ln{n}}{ln 5} = \frac{1}{ln 5} * ln n$  

$log_{2} n = \frac{ln(n)}{ln 2} = \frac{1}{ln 2} * ln n$  
Both logarithms follow the formula of *constant* \cdot ln{n}.  
It follows that, for either of the two logarithms:  
$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$  
In more concrete words:   
$\frac{ln{n}}{ln 5} \in O(\frac{ln{n}}{ln 2})$  since  $\exists c, n_0: \frac{ln{n}}{ln 5} \leq c \cdot \frac{ln{n}}{ln 2} \forall n \geq n_0$  
This satisfies the defintion for a function/algorithm to be an element of big O.


I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
