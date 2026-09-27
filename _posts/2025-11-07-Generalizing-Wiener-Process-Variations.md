---
title: "Generalizing Wiener Process Variations: an attempt to correctly solve my Bachelor's final exam in Stochastic Calculus"
permalink: /posts/2025/11/generalizing-wiener-process-variations/
tags:
  - Semester 1 S2 - UNIPD M1 
date: 2025-11-07
---
<p align="justify">  
Most probability theory students know that when we work on partitions on the interval \([0,T]\), the Wiener process has unbounded absolute variation and finite quadratic variation given by \(T\). Now, we shall make a simple generalization which gave an unsurprising result of \(0\) for the \(n\)-th variation when \(n \ge 3\)!
</p>
<p align="justify">  
This exercise comes from my final exam on my Bachelor's course in Stochastic Calculus. Simply speaking, this was an elective course and one of the hardest class available in my school, that is Gadjah Mada University. The simple reason I wrote this article right now since I'm currently taking another similar course in the University of Padova, that is, Stochastic Analysis. As expected, the class is hard, lol. Another reason for that is I was wondering if my argument that I made during the exam was correct (sorry, I'm bad in probability stuffs).
</p>

<p align="justify">  
Last week, we discussed the first two variations in the Stochastic Analysis class, and I suddenly remembered that I had done the same thing before. So yeah, as I haven't tried to update anything on my page lately, let's just try to solve this simple problem. Thank you <a href="https://math.stackexchange.com/questions/92648/calculation-of-the-n-th-central-moment-of-the-normal-distribution-mathcaln">the internet</a> for providing me such a great identity that I can abuse in the future! Let us cook now!
</p>
# The Problem
<p align="justify">  
Let \(W(t)\) be a standard Wiener process. Compute
$$
\lim_{\|P\|\to 0} \sum_{k=0}^{m-1} (W(t_{k+1}) - W(t_k))^n,
$$
for \(n \ge 3\).
</p>
# Solution
<p align="justify">  
We shall assume that the partition \(P\) is taken over an interval \([0,T]\). For all such partition \(P\), given as
$$P = \{0=t_0 < t_1 < t_2< \ldots<t_m = T\},$$
define
$$S_P^n := \sum_{k=0}^{m-1}(W(t_{k+1})-W(t_k))^n.$$
We shall prove \(S_P^n \xrightarrow{L^2} 0\), that is
$$\text{E}[(S^n_P-0)^2] \to 0$$
as \(\|P\|\to 0\).

Since \(\text{E}[(S^n_P)^2] = \text{Var}(S^n_P) + \text{E}[S^n_P]^2\), it is sufficient to prove \(\text{Var}(S^n_P)\to 0\) and \(\text{E}[S^n_P]^2\to 0\) as \(\|P\|\to 0\).

For a random variable \(X\sim N(0,\sigma^2)\), one can show that
$$
\text{E}[X^n] = \begin{cases}
    0&, \ \text{\(n\) odd}\\
    (n-1)!!\cdot\sigma^n&, \ \text{\(n\) even}
\end{cases}
$$
by utilizing the Taylor expansion of the Moment Generating Function for X to get the desired result.

By the independent increment property of the standard Wiener process, we have
$$\text{Var}(S^n_P) = \sum_{k=0}^{m-1}\text{Var}((W(t_{k+1})-W(t_k))^n)$$
and by the linearity of expectations
$$\text{E}[S^n_P] = \sum_{k=0}^{m-1}\text{E}[(W(t_{k+1})-W(t_k))^n].$$
For any \(k\in\{0,1,2,\ldots,m-1\}\) we have \(W(t_{k+1})-W(t_k)\sim N(0,t_{k+1}-t_k)\). Therefore,
$$
\text{E}[(W(t_{k+1})-W(t_k))^n] = \begin{cases}
    0&, \ \text{\(n\) odd}\\
    (n-1)!!\cdot(t_{k+1}-t_k)^{\frac{n}{2}}&, \ \text{\(n\) even}\end{cases}
$$
and
$$
\text{E}[(W(t_{k+1})-W(t_k))^{2n}] =
    (2n-1)!!\cdot(t_{k+1}-t_k)^n.
$$
    We shall assume \(n\) is even, as the case of \(n\) odd is simpler. From these results, we also have
$$
\begin{aligned}
    \text{Var}((W(t_{k+1})-W(t_k))^n) &= \text{E}[(W(t_{k+1})-W(t_k))^{2n}] - \text{E}[(W(t_{k+1})-W(t_k))^n]^2\\
    &=[(2n-1)!!-((n-1)!!)^2]\cdot(t_{k+1}-t_k)^n.
\end{aligned}
$$
    As we don't need the exact value of \((2n-1)!!\) and \((n-1)!!\) in this computation, we write \(A = (n-1)!!\) and \(B = (2n-1)!!-((n-1)!!)^2\). Since, \(\|P\|=\max_{1\le k\le m-1} (t_{k+1}-t_k)\),
$$
0=t_0 < t_1 < t_2 < \ldots < t_m=T,
$$
    and \(A\), \(B > 0\) (by the fact \(n \ge 3\)), we have
$$
0\le\text{E}[S^n_P] = A\sum_{k=0}^{m-1}(t_{k+1}-t_k)^{\frac{n}{2}} \le A\cdot \|P\|^{\frac{n-2}{2}}\sum_{k=0}^{m-1}(t_{k+1}-t_k)=A\cdot\|P\|^{\frac{n-2}{2}}\cdot T
$$
    and
$$
\begin{aligned}
    0\le\text{Var}(S^n_P) = B\sum_{k=0}^{m-1}(t_{k+1}-t_k)^n \le B\|P\|^{n-1}\sum_{k=0}^{m-1}(t_{k+1}-t_k)=B\cdot\|P\|^{n-1}\cdot T.
\end{aligned}
$$
    Taking \(\|P\|\to 0\) implies \(\text{E}[S^n_P] = \text{Var}(S_P^n) = 0\) by the Squeeze Theorem. Hence
$$
\lim_{\|P\|\to 0}\text{E}[(S^n_P)^2] = 0 + 0 = 0.
$$
    Therefore, we have proved \(S_P^n \xrightarrow{L^2} 0\) and so
$$
\lim_{\|P\|\to 0}\sum_{k=0}^{m-1}(W(t_{k+1})-W(t_k))^n = 0
$$
    in \(L^2\) which also implies the limit becomes \(0\) in Probability.
</p>
## Slight remark
<p align="justify">  
A slight modification of this argument can be used to prove \(S_P^2\xrightarrow{L^2}T\), that is, by proving \(\lim_{\|P\|\to 0}\mathrm{E}[(S_P^2-T)^2] = 0\).
</p>

<script src="https://giscus.app/client.js"
        data-repo="orlandoferrari/orlandoferrari.github.io"
        data-repo-id="R_kgDOOY8AQA"
        data-category="Announcements"
        data-category-id="DIC_kwDOOY8AQM4CpDpE"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="dark_dimmed"
        data-lang="en"
        data-loading="lazy"
        crossorigin="anonymous"
        async>
</script>
