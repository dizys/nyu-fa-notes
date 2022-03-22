---
description: >-
  Outline of Algorithmics
---

# Recurrences

Separable form for recurrence relation:

$$T(n) = G(n, T(n_1), ..., T(n_k))$$

where $$G(x_0, x_1, ..., x_k)$$ is a function in $$k+1$$ variables and each
$$n_i (i=1,...,k)$$ is a function of $$n$$ that is strictly less than $$n$$.

**Fibonacci sequence** is defined by the recurrence relation:

$$F(n) = F(n-1) + F(n-2)$$

For this, we have $$k=2, n_1=n-1, n_2=n-2$$

$$G(n, x, y) = x + y$$

**Merge sort** complexity:

$$T(n) = n + 2T(n/2)$$

For this, we have $$k=1, n_1=n/2$$

$$G(n, x) = n + 2x$$

## Rote Method

{% hint style="info" %}

Related homework questions: h2-Q7

{% endhint %}

### EGVS method

4 stages: **E**xpand, **G**uess, **V**erify and **S**top-and-Sum.

**Example:**

$$T(n) = 2T(n/2) + n$$

1. Expand:

   $$
   \begin{align*}
   T(n) &= 2T(n/2) + n \\
   &= 2 (2 T(n/4) + (n/2)) + n \\
   &= 4 T(n/4) + 2n \\
   &= 4 (2T(n/8) + (n/4)) + 2n \\
   &= 8T(n/8) + 3n \\
   &= \dots
   \end{align*}
   $$

2. Guess:

   $$ T(n) = 2^i T({n\over{2^i}}) + i n$$

3. Verify: (use natural induction)

   Base case: $$T(n)_{i=1} = 2T(n/2) + n$$ holds

   Inductive step: Assume $$T(n)_{i=k}$$ holds, the goal is to prove
   $$T(n)_{i=k+1}$$ also holds.

   $$
   \begin{align*}
   T(n) &= 2^k T({n\over{2^k}}) + k n \\
   &= 2^k (2 T({n\over{2^{k+1}}}) + {n\over{2^k}}) + k n \\
   &= 2^{k+1} T(n/2^{k+1}) + （k+1) n
   \end{align*}
   $$

   Therefore, this proves $$T(n)_{i=k+1}$$ also holds.

   Combining the base case and the inductive step we verified that $$ T(n) = 2^i
   T({n\over{2^i}}) + i n$$.

4. Stop:

   We can pick $$i = \lfloor {lg n} \rfloor$$ for stopping, then
   $$0 < {n\over{2^i}} \le 2$$.

   By DIC, choose $$T(n) = 0$$ for all $$n \le 2$$.

   Therefore, for $$n > 1$$,

   $$T(n) = \lfloor {lg n} \rfloor n$$

### Basic Sums



## Master Theorem

## Summation Techniques

### Growth Types

### Summation Rules by Growth Type

## Transformation Techniques

## Real Induction

## Multi-term Master Recurrences

$$


$$

$$


$$

$$
$$

$$
$$
