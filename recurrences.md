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
