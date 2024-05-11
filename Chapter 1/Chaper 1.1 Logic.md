---
id: "1.1"
tags:
  - Book
---

# Logic

- [Propositions](#propositions)
- [Bit Operations](#bit-operations)

## Propositions

Propositions
: A statement that is either true or false, but not both.

- $1+1=2$ (true)
- $2+2=4$ (false)

### NOT

> Let $p$ be a proposition. The statement "It is not the case
> that $p$" is another proposition, called **negation** of $p$.
> The negation of $p$ is denoted by $\lnot p$ (not $p$).
> If $p$ is true, then $\lnot p$ is false, vice versa

| $p$ | $\lnot p$ |
| --- | --------- |
| T   | F         |
| F   | T         |

### AND

> Let $p$ and $q$ be propositions
> Where "$p$ and $q$" is denoted by $p \land q$ is true if both $p$ and $q$ is true.
>
> $p\land q$ is the conjunction of two proposition

| $p$ | $q$ | $p\land q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | F          |

### OR

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\lor q$ is true if both $p$ and $q$ is false.
>
> $p\lor q$ is the disconjunction of two propositions

| $p$ | $q$ | $p\lor q$ |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | T         |
| F   | T   | T         |
| F   | F   | F         |

### XOR

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\oplus q$ is true if either $p$
> and $q$ is true.
>
> $p\oplus q$ is the exclusive of two propositions

| $p$ | $q$ | $p\oplus q$ |
| --- | --- | ----------- |
| T   | T   | F           |
| T   | F   | T           |
| F   | T   | T           |
| F   | F   | F           |

### Conditional

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\rightarrow q$ is
> true if $p$ is true and $q$ is false.
>
> $p\rightarrow q$ is the implication of two propositions

| $p$ | $q$ | $p\rightarrow q$ |
| --- | --- | ---------------- |
| T   | T   | T                |
| T   | F   | F                |
| F   | T   | T                |
| F   | F   | F                |

### Biconditional

> Let $p$ and $q$ be propositions.
> Where "$p$ and $q$" is denoted by $p\leftrightarrow q$ is true if
> both $p$ and $q$ have the same truth values.
>
> $p\leftrightarrow q$ is the biconditional of two propositions

| $p$ | $q$ | $p\leftrightarrow q$ |
| --- | --- | -------------------- |
| T   | T   | T                    |
| T   | F   | F                    |
| F   | T   | F                    |
| F   | F   | T                    |

## Bit-Operations

$\land$ (AND) $\lor$ (OR) $\oplus$ (XOR)

| $\land$ | 0   | 1   |
| ------- | --- | --- |
| 0       | 0   | 1   |
| 1       | 1   | 1   |

| $\lor$ | 0   | 1   |
| ------ | --- | --- |
| 0      | 0   | 0   |
| 1      | 0   | 1   |

| $\oplus$ | 0   | 1   |
| -------- | --- | --- |
| 0        | 0   | 1   |
| 1        | 1   | 0   |

> Comparing 2 bit to find the final bitwise using the tables.

|          | 0   | 1   | 1   | 0   | 1   |     | 1   | 0   | 1   | 1   | 0   |
| -------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|          | 1   | 1   | 0   | 0   | 0   |     | 1   | 1   | 1   | 0   | 1   |
| $\lor$   | 1   | 1   | 1   | 0   | 1   |     | 1   | 1   | 1   | 1   | 1   |
| $\land$  | 0   | 1   | 0   | 0   | 0   |     | 1   | 0   | 1   | 0   | 0   |
| $\oplus$ | 1   | 0   | 1   | 0   | 1   |     | 0   | 1   | 0   | 1   | 1   |
