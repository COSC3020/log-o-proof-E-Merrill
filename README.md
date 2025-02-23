# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

To show that $O(log_{5} n)$ and $O(log_{2} n)$ are asymptoticallly equivalent, it must be shown that any arbitrary function, f(n), that belongs to O(log_{2} n) also belongs to O(log_{5} n).  
Applying the logarithm change of base formula to $log_{5} n$ nets:  
$log_{5}n = \frac{log_{2}n}{log_{2}5} = \frac{1}{log_{2}5} * \frac{log_{2}n}$
Assuming it is true that $f(n) \in O(log_{5}n)$, we can make the statement $f(n) \leq c * log_{5}n$, where c is some arbitrary, positive, nonzero constant.  
Inserting the equivalent expression for log_{5}n:  
$f(n) \leq c * \frac{1}{log_{2}5} * log_{2}n$  
Since $\frac{1}{log_{2}5}$ is just another postive constant, it can be put into another variable $c' = c * \frac{1}{log_{2}5}$  
This brings the expression to $f(n) \leq c' * log_{2}n$  which satisfies the definition for $f(n) \in O(log_{5}n)$  

**Showing the same thing, but with $log_{2}n$**  
Applying change of base formula to $log_{2}n$:  
$log_{2}n = \frac{log_{5}n}{log_{5}2} = \frac{1}{log_{5}2} * \frac{log_{5}n}$  
Assume $f(n) \in O(log_{2}n)$ and make the assertion $f(n) \leq c * log_{2}n$, where is an arbitrary, positive constant.  
Substituting an equivalent expression for $log_{2}n$:  
$f(n) \leq c * \frac{1}{log_{5}2} * log_{5}n$  
$\frac{1}{log_{5}2}$ is just another positive constant, it can be represented as $c'' = c * \frac{1}{log_{5}2}$  
The expression is now $f(n) \leq c'' * log_{5}n$, satisfying the defintion for $f(n) \in O(log_{2}n)$  

Through the log change of base formula, it has been shown that, asymptotically, $O(log_{5}n) = O(log_{2}n)$  



I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

Gage Hepworth gave me the idea/notion that I should use the log change of base formula for this proof.
