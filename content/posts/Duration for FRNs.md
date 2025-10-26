+++
title = 'Duration for FRNs'
date = 2025-10-26
draft = false
math = true
+++
## Introduction

This is **bold** text, and this is *emphasized* text.

Assuming a bond with notional $1$ that pays annually, the price at next coupon $P$ is 

$$
\begin{align*}
P &= \sum_{t=1}^{n} \frac{C_t}{(1+r)^t} + \frac{1}{(1+r)^n} \\
  &= \sum_{t=1}^{n} \frac{I + QM}{(1 + I + DM)^t} + \frac{1}{(1+I+DM)^n} \quad \text{(assuming a flat curve, where $I =$Assumed Index)} \\
  &= \sum_{t=1}^{n} \frac{y}{(1+y)^t} + \frac{1}{(1+y)^n} 
     \quad \text{(assuming the credit spread remains constant, let $QM = DM$ and $y = I + QM$)} \\
  &= 1
\end{align*}
$$

If the number of years to the next coupon is $t$, the current price $P_0$ will be

$$
P_0 = \frac{1+IN+QM}{1+(IN+DM)t} \quad \text{(where $IN =$Index to Next Pay)}
$$

We can see this is a zero-coupon bond with maturity $t$, Macaulay duration $t$, and modified duration \frac{t}{1 + (IN + DM)t}

For floaters with a forward-looking reset index, note that $IN$ is fixed at the previous coupon date, we can get the modified duration by differentiating $P_0$ with respect to $DM$:

$$
M_{Dur} = \frac{dP_0}{dDM} = \frac{t}{1 + (IN + DM)t}
$$
