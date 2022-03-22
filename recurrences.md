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

Other kinds of sums are often reduces to the following forms.

#### Arithmetic Sums

$$S^k_n := \sum^n_{i=1}{i^k}$$

Solution: $$S^k_n = \Theta(n^{k+1})$$

#### Geometric Sums

When $$x \ne 1$$,

$$S_n(x) := \sum^{n-1}_{i=0}{x^i}$$

Solution: $$S_\infty = {{x^n - 1}\over{x - 1}}$$

#### Infinite Geometric Series

When $$\lvert{x}\rvert < 1$$,

$$S_{\infty}(x) := \sum^{\infty}_{i=0}{x^i}$$

Solution: $$S_{\infty}={1\over{1 - x}}$$

#### Harmonic Series

$$H_n := 1 + {1\over{2}} + {1\over{3}} + \dots + {1\over{n}}$$

Solution: $$H_n = ln(n) + g(n)$$ where $$0 < g(n) < 1$$.

## Summation Techniques

### Growth Types

{% hint style="info" %}

Related homework questions: h3-Q1

{% endhint %}

#### Polynomial Type

A real function $$f$$ is **polynomial-type** if $$f$$ is non-decreasing (ev.)
and there is some $$C > 1$$ such that:

$$f(x) \le C f(x/2)\ (ev.)$$

#### Increasing Exponential Type

$$f$$ increases exponentially if there exists real numbers $$C > 1$$ and
$$k > 0$$ such that:

$$f(x) \ge C f(x - k)\ (ev.)$$

#### Decreasing Exponential Type

$$f$$ decreases exponentially if there exists real numbers $$C > 1$$ and
$$k > 0$$ such that:

$$f(x) \le f(x - k) / C\ (ev.)$$

#### Lemma 8: Closed Properties

(a) **Polynomial-type** functions are closed under addition, multiplication, and
raising to any positive power $$a > 0$$.

(b) **Exponential-type** functions $$f$$ are closed under addition,
multiplication, and raising to any power $$a$$. In case $$a > 0$$, the function
$$f^a$$ will not change its subtype (increasing or decreasing). In case
$$a < 0$$, the function $$f^a$$ will change its subtype.

(c) If $$f$$ is polynomial-type and $$lg f$$ is non-decreasing then $$lg f$$ is
also polynomial-type. If $$f$$ is exponential-type and $$a > 1$$ then so is
$$a ^ f$$.

### Summation Rules by Growth Type

{% hint style="info" %}

Related homework questions: h3-Q2

{% endhint %}

## Transformation Techniques

## Master Theorem

## Multi-term Master Recurrences

## Real Induction
