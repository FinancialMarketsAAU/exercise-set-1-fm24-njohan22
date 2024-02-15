# Exercise Set 1 for the Financial Markets Course

Commit with your solutions.

Excercise 1)

i)

Assume $x \succ x$. Then we have $x \succsim x$ but not $x \precsim x$. But this is impossible.

Assume $x \succ y$ and $y \succ z$. Then we have $x \succsim y$ but not $x \precsim y$ and $y \succsim z$ but not $y \precsim z$. Thus we must have $x \succ y \succ z$.

ii)

Assume $x \sim x$. Then we have $x \succsim x$ and $x \precsim x$ Which is true.

Assume $x \sim y$ and $y \sim z$. Then we have $x \succsim y$ and $x \precsim y$ and we also have $y \succsim z$ and $y \precsim z$. Thus we have $x \succsim y \succsim z$ and $x \precsim y \precsim z$. Thus we must have $x \sim z$

Assume $x \sim y$. Then we have $x \succsim y$ and $x \precsim y$. Thus we must also have $y \sim x$.

iii)

Assume $x \succ y \succsim z$. Then we have $x \succsim y$ and not $x \precsim y$. We also have $y \succsim z$ and $y \precsim z$. Thus we have $x \succsim z$ and not $x \precsim z$. Thus we have 
$x \succ z$

Exercise 2)

i)

Assume $(x_1,x_2) \succsim (y_1,y_2)$ and $(y_1,y_2) \succsim (z_1,z_2)$. Then we have 4 cases to consider.

The first condition for both relations. We know that $x_1 > y_1 > z_1$. Thus $(x_1,x_2) \succsim (z_1,z_2)$.

The second condition for both relation. we know that $x_1 = y_1 = z_1$ and $x_2 \geq y_2 \geq z_2$. Thus $(x_1,x_2) \succsim (z_1,z_2)$.

The first conditon is true for the first relation, and the second condition is true for the second relation. We know that $x_1 > y_1 = z_1$. Thus $(x_1,x_2) \succsim (z_1,z_2)$.

The second condition is true for the first relation, and the first condition is true for the second relation. We know that $x_1 = y_1 > z_1$ Thus $(x_1,x_2) \succsim (z_1,z_2)$.

ii)

$\forall n \in \mathbb{N}$ we have:
$$(x_1^n,x_2^n) \precsim (y_1,y_2)$$

But we also have:
$$lim_{n \rightarrow \infty}(x_1^n,x_2^n) \succsim (y_1,y_2)$$

Thus it is not continous.

Excercise 3)

i)

$$U(x+y) = \alpha_1(x_1 + y_1) + \alpha_2(x_2+y_2) =  \alpha_1 x_1 +  \alpha_1 y_1 +  \alpha_2 x_2 +  \alpha_2 y_2 = U(x) + U(y)$$

$$U(cx) = \alpha_1 cx_1 + \alpha_2 cx_2 = cU(x)$$

ii)
$$ln(U(x)) = \frac{ln(\alpha_1x_1^\rho + \alpha_2x_2^\rho)}{\rho}$$

Then we can use L'hospital when we let $\rho \rightarrow 0$ because in cobb-douglas $\alpha_1 + \alpha_2 = 1$.
$$\frac{\alpha_1x_1^\rho ln(x_1) + \alpha_2 x_2^\rho ln(x_2)}{\alpha_1x_1^\rho+\alpha_2x_2^\rho}$$

Letting $\rho \rightarrow 0$

$$\frac{\alpha_1 ln(x_1) + \alpha_2 ln(x_2)}{\alpha_1+\alpha_2}$$

Which means:
$$U(x) = e^{\frac{\alpha_1 ln(x_1) + \alpha_2 ln(x_2)}{\alpha_1+\alpha_2}} = x_1^{\alpha_1} x_2^{\alpha_2}$$

(Its actually the $\alpha_1 + \alpha_2$, root of $x_1^{\alpha_1} x_2^{\alpha_2}$, but $\alpha_1 + \alpha_2 = 1$ in cobb-douglas).

iii)

If $\alpha = 1$, $\rho = \frac{1}{2}$ and $U(x) = 1$ then
$$1 = (x_1^{\frac{1}{2}}+x_2^{\frac{1}{2}})^2$$

$$(1 -\sqrt{x})^2 = x_2$$

then the following code shows the lower countour set

using Plots

X = 0.1:0.005:0.35     

α = 1

f(x,k) =(1-sqrt(x))^2

y=[f(x,0.5) for x in X]

plot(X,y, fillrange = zeros(size(X,1),1), 

fillalpha = 0.3, label="{y∈R²:y≺x}")

plot!(X,y,line = :dash, color = :red, 

linewidth = 3, label="{y∈R²:y~x}")

iv)

when $\rho = \frac{1}{2}$, $\alpha_1 = \alpha_2 = 1$ and $U(x)= 1$, $U(x)= 2$ and $U(x)= 3$ we use the following julia code


using Plots

X = 0.1:0.05:1

K = 1:1:3

p = 1/2

f(x,k) =(k^p-x^p)^(1/p)

y=[f(x,k) for x in X, k in K]

plot(X, y, label=["K=1" "K=2" "K=3"])


v)
If we take
$$\lim_{\rho \to -\infty}U(x) = \lim_{\rho \to -\infty}(\alpha_1x_1^\rho + \alpha_2x_2^\rho)^\frac{1}{\rho}$$






