# NP Complete

## Polynomial Reducibility

When A is polynomial-reducible to B, we denote this relationship as:

$$A \leqslant^P B$$

To prove this relationship, we need:

- Construct an input $I_B$ for B according to input $I_A$ of A (be creative,
  your goal is the next bullet point). Get the result of B: $O_B$.
- Show that we can get the desired output $O_A$ from $O_B$.
