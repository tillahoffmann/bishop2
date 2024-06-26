> Consider a variable $y$ given by the sum of two independent random variables $y = u + v$ where $u \sim p_u(u)$ and $v\sim p_v(v)$. Show that the distribution $p_y(y)$ is given by
> $$ p_y(y)=\int p_u(u) p_v(y - u) du. $$

By the sum rule,
$$
p_y(y)=\int p_u(u) p_v(v) \delta(u + v - y) du dv,
$$
where $\delta$ is the Dirac delta function. Integrating over $v$ has zero mass everywhere except $v=y-u$, yielding the desired expression.
