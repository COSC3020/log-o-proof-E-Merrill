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
Let $T(n) = log_2n$ and $f(n) = log_5n$  
If $T(n) \in O(f(n))$ then (the growth of $T(n)$) $\leq$ (the growth of $f(n)$)  
The growth of a function can be found from its first derivative.  
$\frac{d}{dn} T(n) = \frac{d}{dn} log_2n$    $\frac{d}{dn} f(n) = \frac{d}{dn} log_5n$  
$T'(n) = \frac{1}{ln(2)} * \frac{1}{n}    f'(n) = \frac{1}{ln(5)} * \frac{1}{n}$  
$\frac{1}{ln(2)}$  and  $\frac{d}{ln(5)}$  are both just constants, which have no bearing on the asymptotic complexity of a function/algorithm.  
Thus, ignoring the constant yields:  
$T'(n) = \frac{1}{n}    f'(n) = \frac{1}{n}$  
These two function are the same, meaning that their parent functions, $T(n)$ and $f(n)$ grow at the same rate (the same end behavior.)  
This means that there must be a nonzero, positive constant **c** such that $T(n) \leq c * f(n)$  
This satisfies the definition for $T(n) \in O(f(n))$:  
$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$  


I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
