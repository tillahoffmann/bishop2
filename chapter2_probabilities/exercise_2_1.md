> In the cancer screening example, we used a prior probability of cancer of $p(C = 1) = 0.01$. In reality, the prevalence of cancer is generally very much lower. Consider a situation in which $p(C = 1) = 0.001$, and recompute the probability of having cancer given a positive test $p(C = 1\mid T = 1)$. Intuitively, the result can appear surprising to many people since the test seems to have high accuracy and yet a positive test still leads to a low probability of having cancer.

From equations (2.14–2.17), we have
$$
\begin{aligned}
p(T=1\mid C=1)&=0.9\\
p(T=0\mid C=1)&=0.1\\
p(T=1\mid C=0)&=0.03\\
p(T=0\mid C=0)&=0.97.
\end{aligned}
$$
Using Bayes rule, we have
$$
\begin{aligned}
p(C = 1\mid T = 1)&=\frac{p(T=1\mid C=1)p(C=1)}{p(T=1)}\\
&=\frac{p(T=1\mid C=1)p(C=1)}{p(T=1\mid C=0)p(C=0)+p(T=1\mid C=1)p(C=1)}\\
&=\frac{0.9 \times 0.001}{0.03\times 0.999 + 0.9 \times 0.001}\\
&\approx 0.029.
\end{aligned}
$$
