## SoME3: More on L'Hôpital's rule

This post is intended to be read after watching the 3B1B video [Limits, L'Hôpital's rule, and epsilon delta definitions | Chapter 7, Essence of calculus](https://youtu.be/kfF40MiS7zA) which introduces L'Hôpital's rule. Here is the example used in the video:

$$\lim_{x\to 1} \frac{\text{sin}(\pi x)}{x^2-1} = -\frac{\pi}{2}$$

which is an application of

$$\lim_{x\to a} \frac{f(x)}{g(x)} = \frac{f'(a)}{g'(a)}$$
when $f(a) = g(a) = 0$ and the right hand side makes sense.

There is an extended version of L'Hôpital's rule that will allow us to compute other limits. For instance, we will see that

$$\lim_{x\to 1} \frac{\text{cos}(\pi x)+1}{x^3-3x+2} = \lim_{x\to 1} \frac{-\pi\text{sin}(\pi x)}{3(x^2-1)} = \frac{-\pi}{3} \times \frac{-\pi}{2} = \frac{\pi^2}{6} $$

The extended version of L'Hôpital's rule is

$$\lim_{x\to a} \frac{f(x)}{g(x)} = \lim_{x\to a} \frac{f'(x)}{g'(x)}$$
when $f(a) = g(a) = 0$ and the right hand limit exists.

### One-sided limits
The video explained what the limit notation means: when we write $$\lim_{x\to a} r(x) = L$$ we mean that for every $\epsilon > 0$ there exists a $\delta > 0$ such that whenever $0 < |x - a| < \delta$, we have $|r(x) - L| < \epsilon$. The output $r(x)$ can be kept arbitrarily close to the limit value $L$ by restricting the input $x$ to be sufficiently close to $a$.

We are going to use a slightly modified version of limits that is only concerned with inputs greater than $a$. When we write $$\lim_{x\to a^{+}} r(x) = L$$ we mean that for every $\epsilon > 0$ there exists a $\delta > 0$ such that whenever $a < x < a+\delta$, we have $|r(x) - L| < \epsilon$. This is called the right-hand limit of $r(x)$ at $a$.

There is of course a corresponding notation for inputs less than $a$: $$lim_{x\to a^{-}} r(x) = L$$, the left-hand limit. Importantly, the ordinary limit equals $L$ exactly when both the right-hand limit equals $L$ and the left-hand limit equals $L$. Sometimes, the left-hand limit and right-hand limit both exist but have different values; this means the ordinary limit does not exist.

The approach we will take to L'Hôpital's rule will focus on establishing the right hand limit:

$$\lim_{x\to a^{+}} \frac{f(x)}{g(x)} = \lim_{x\to a^{+}} \frac{f'(x)}{g'(x)}$$

A completely symmetric 
