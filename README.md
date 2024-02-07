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



