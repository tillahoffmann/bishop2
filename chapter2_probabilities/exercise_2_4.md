> Verify that the uniform distribution $p(x)=1/(d - c)$ is correctly normalized, and find expressions for its mean and variance.

The integral of the density is
$$
\int_c^d 1/(d - c) dx=\frac{\int_c^d dx}{d - c}=1.
$$

The mean is
$$\begin{aligned}
\mathbb E [x]&=\frac{1}{d - c}\int_c^d x dx\\
&=\frac{x^2\vert^{x=d}_{x=c}}{2(d - c)}\\
&=\frac{d^2-c^2}{2(d - c)}\\
&=\frac{(d+c)(d-c)}{2(d - c)}\\
&=\frac{d + c}{2}.
\end{aligned}$$

The second moment is
$$\begin{aligned}
\mathbb E [x^2]&=\frac{1}{d - c}\int_c^d x^2 dx\\
&=\frac{x^3\vert^{x=d}_{x=c}}{3(d - c)}\\
&=\frac{d^3-c^3}{3(d - c)}\\
&=\frac{(d - c) (c^2 + c d + d^2)}{3(d - c)}\\
&=\frac{c^2 + c d + d^2}{3}.
\end{aligned}$$

The variance is thus
$$\begin{aligned}
\mathrm{var} x&=\mathbb{E}[x^2]-(\mathbb{E}[x])^2\\
&=\frac{c^2 + c d + d^2}{3}-\left(\frac{d + c}{2}\right)^2\\
&=\frac{4c^2+4cd+4d^2-3d^2-6cd-3c^2}{12}\\
&=\frac{c^2-2cd+d^2}{12}\\
&=\frac{(d-c)^2}{12}.
\end{aligned}$$

Let's verify numerically.

```python
from matplotlib import pyplot as plt
import numpy as np

c = 3
d = 5

x = np.random.uniform(c, d, size=1_000_000)
print(f"mean: {x.mean():.3f}, {(c + d) / 2:.3f}")
print(f"2nd moment: {np.square(x).mean():.3f}, {(c ** 2 + d ** 2 + c * d) / 3:.3f}")
print(f"var: {x.var():.3f}, {(d - c) ** 2 / 12:.3f}")
```
