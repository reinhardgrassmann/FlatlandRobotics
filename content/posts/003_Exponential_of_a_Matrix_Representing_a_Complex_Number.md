---
title: "Exponential of a Matrix Representing a Complex Number"
date: 2025-09-05T18:21:08-04:00
description: An exploration into the complex number representations
categories: ["Mathematics"]
tags: ["complex numbers", "orientation", "trigonometric", "matrix exponential"]
toc: true
math: true
draft: false
---

In this blog post, we will briefly look into complex numbers and their representations in $\mathbb{C}$, $\mathbb{R}^2$, and $\mathbb{R}^{2 \times 2}$.
Afterward, we will take a look at what is arguably the _"greatest equation ever"_ and the _"most beautiful theorem in mathematics"_.
It is nothing other than Euler's identity, _i.e.,_

$$
e^{i\pi} + 1 = 0,
$$

which can be seen as a special case of Euler's formula, _i.e.,_

$$
e^{i \theta} = \cos\left(\theta\right) + i \sin\left(\theta\right).
\tag{1}
$$

A straightforward question arises:
_What does Euler's formula look like for these representations?_


## Prerequisites: Power Series with Real Numbers

Let's recap a few power series.
The two considered trigonometric power series are

$$
\sin\left(x\right) 
= x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \frac{x^9}{9!} - \cdots 
= \sum^{\infty}_{n=0} \frac{(-1)^n}{(2n+1)!} x^{2n+1}
\tag{2}
$$

and

$$
\cos\left(x\right) 
= 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \frac{x^8}{8!} - \cdots 
= \sum^{\infty}_{n=0} \frac{(-1)^n}{(2n)!} x^{2n}.
\tag{3}
$$

Another important one is the power series of the exponential function, _i.e._,

$$
e^x 
= 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \frac{x^5}{5!} + \frac{x^6}{6!} + \cdots 
= \sum_{n=0}^{\infty} \frac{x^n}{n!}. 
\tag{4}
$$

Comparing the pattern in Eq. (4) and the result of adding Eq. (2) and Eq. (3), we can imagine that the exponential function is related to the trigonometric function.
To fix and account for the alternating signs with a "$++--$" pattern, we can use the imaginary unit $i$. 
Voil&agrave;, we kinda prove Eq. (1).
This is enough to get an intuition on the origin of Eq. (1), see [this wikipedia article](https://en.wikipedia.org/wiki/Euler%27s_formula#Using_power_series) on a proof using power series.


## Complex Numbers and a Subset of their Representations 

In this part, I provide a brief overview of their representations.
I will not state all of them, and I will also be lazy and reuse the same variable name for a complex number $z$.

The Cartesian form of a complex number $z$ is

$$
z = a + ib 
\quad\in\mathbb{C},
\tag{5}
$$

where $i$ is the imaginary unit, and $a$ and $b$ are real numbers.
For the imaginary unit, we know that its square is negative, _i.e._, $i^2 = -1$.
With this representation, the scaling with a real number, addition with other complex numbers, and the multiplication with other complex numbers are possible.
One might argue that scaling with a real number is a special case of complex multiplication.
That's right.
However, to distinguish scaling from complex multiplication will be crucial for the next representation.

We can embed complex numbers in a vector space $\mathbb{R}^2$.
This would look like

$$
z = 
\begin{bmatrix}
    a\\\\
    b
\end{bmatrix}
\quad\in\mathbb{R}^2
\tag{6}
$$

For this representation, scaling with a scalar (or real number) and vector addition are well-defined.
After all, we are dealing with a vector space.
However, multiplication of two vectors are not really defined, but this is a different story for another blog post.
For now, sorry, we cannot do this.

What a vector representation cannot do, a matrix representation can.
In fact, the whole shebang; scaling, adding, and multiplying.
The matrix

$$
z = 
\begin{bmatrix}
    a & -b \\\\
    b & a
\end{bmatrix}
\quad\in\mathbb{R}^{2 \times 2}
\tag{7}
$$

is the matrix representation of a complex number.
Let's bring Eq. (7) to the test.
After some sort of reversing the addition and scaling in Eq. (7), we can find the following decomposition.

$$
z = 
a
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}+
b
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}
.
\tag{8}
$$

We see two matrices.
The one associated with $b$ behaves like the complex unit $i$, _i.e.,_ its square is a negative identity matrix.


## Exponential Representations

Now, the scene is set.
Let us derive each exponential.


### Cartesian Representation


Back to the straightforward question:
_What does Euler's formula Eq. (1) look like for Eq. (4)?_
Instead of using Eq. (4), we apply the product rule for exponentiation.

$$
e^{a + ib} = e^a e^{ib} = e^{a}\left(\cos\left(b\right) + i \sin\left(b\right)\right) = e^{a}\cos\left(b\right) + i e^{a}\sin\left(b\right).
\tag{9}
$$

That was easy.
So, $b$ is like an angle and $a$ relates to a scaling.

### Vector Representation

Unfortunately, this is not possible.
Extending the power series of the exponential function as stated in Eq. (4) would require to define multiplication for vectors.
Also, fat or tall matrices cannot be considered$-$only squared matrices.


### Matrix Representation

Speaking of squared matrices, the matrix representation of $z$ is a squared matrix.
It is common to extend the expression in Eq. (4) and hope that the power series converges.
We expect something analogous to Eq. (9), but with matrices.
So, let's do it.

In the following, I will use $\exp\left(X\right)$ instead of $e^X$.
It's easier to read.

#### A Trick to Consider


First of all, I would like to use a similar trick, _i.e.,_ $\exp\left(a + b\right) = \exp\left(a\right)\exp\left(b\right)$.
This trick can only be used if $ab = ba$, which is true for real numbers.
It is also true for complex numbers, since $ib = bi$, which implies $aib = iba$.
However, in general, matrix multiplication is not commutative, _i.e.,_ $AB \not= BA$.
Luckily, the matrix $A$ associated with the component $a$ of $z$ in Eq. (8) is an identity matrix.
Therefore, we can use the trick.
Using this trick leads to

$$
\exp\left(
a
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} +
b
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}
\right) =
\exp\left(
a
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}
\right)
\exp\left(
b
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}
\right).
$$

This is a win.
Don't assume you can do the trick again to simplify further.
This would be a big lose because you cannot just separate the scaling factor from the matrix in a similar fashion, _i.e._,

$$
\exp\left(
a
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}
\right) \not=
\exp\left(
a
\right)
\exp\left(
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}
\right).
$$


#### The Simple Part

Anyway, now, we can separately deal with the exponential function.
Using the fact that the identity matrix is the same identity matrix after repeated multiplication with itself, the pattern is quite simple and allows us to separate the matrix from the infinite sum.
the first one results in 

$$
\exp\left(
\begin{bmatrix}
    a & 0 \\\\
    0 & a
\end{bmatrix}
\right) = 
\sum_{n=0}^{\infty} \frac{1}{n!}
\begin{bmatrix}
    a & 0 \\\\
    0 & a
\end{bmatrix}^n  = 
\left(\sum_{n=0}^{\infty} \frac{a^n}{n!}\right)
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}  =
\exp\left(a\right)
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} .
$$


#### The Hard Part

The second one is harder because the pattern is not that simple but at least there is a pattern. 
Let's take a look.
The zero-power, _i.e._,

$$
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}^0  =
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix},
$$

and the first-power, _i.e._,

$$
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}^1  =
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix},
$$

are obvious.
They are the identity matrix and the matrix itself, respectively.
The second-power, _i.e._,

$$
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}^2  =
\begin{bmatrix}
    -1 & 0 \\\\
    0 & -1
\end{bmatrix} = -
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}
$$

is a negative identity matrix as mentioned before.
Next we have

$$
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}^3  =
\begin{bmatrix}
    0 & 1 \\\\
    -1 & 0
\end{bmatrix} = -
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}
$$

and

$$
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix}^4  =
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}
$$

resulting in a nice and familiar patter.
This behavior should remind us of $i^2 = -1$, $i^3 = -i$, and $i^4 = 1$.
If we include $i^0 = 1$ and $i^1 = i$, this pattern is the "$++--$" pattern mentioned in the beginning, where I provided some intuition on relation between Eq. (1) and Eq. (4) in a hand-wavy way.
So, we might find some hidden trigonometric functions.

Writing down the power series like

$$
\exp\left(
\begin{bmatrix}
    0 & -b \\\\
    b & 0
\end{bmatrix}
\right) = 
\sum_{n=0}^{\infty} \frac{1}{n!}
\begin{bmatrix}
    0 & -b \\\\
    b & 0
\end{bmatrix}^n  =
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} +
\frac{b}{1!}
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix} - 
\frac{b^2}{2!}
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} -
\frac{b^3}{3!}
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix} +
\frac{b^4}{4!}
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} + 
\frac{b^5}{5!}
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix} -
\frac{b^6}{6!}
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix} - 
\cdots
$$

allows us to rearrange the infinite series.
By grouping the matrices leads to

$$
\exp\left(
\begin{bmatrix}
    0 & -b \\\\
    b & 0
\end{bmatrix}
\right) = 
\left(
1 - \frac{b^2}{2!} + \frac{b^4}{4!} - \frac{b^6}{6!} + \cdots
\right)
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}  +
\left(
b - \frac{b^3}{3!} + \frac{b^5}{5!} - \frac{b^7}{7!} + \cdots
\right)
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix},
$$

where the coefficients should remind us of Eq. (2) and Eq. (3) confirming our intuition.
After substitution, the result is

$$
\exp\left(
\begin{bmatrix}
    0 & -b \\\\
    b & 0
\end{bmatrix}
\right) = 
\cos\left(b\right) 
\begin{bmatrix}
    1 & 0 \\\\
    0 & 1
\end{bmatrix}  +
\sin\left(b\right) 
\begin{bmatrix}
    0 & -1 \\\\
    1 & 0
\end{bmatrix} =
\begin{bmatrix}
    \cos\left(b\right)  & -\sin\left(b\right)  \\\\
    \sin\left(b\right)  & \cos\left(b\right) 
\end{bmatrix}.
$$

This is a rotation matrix.
The one for $SO(2)$.
It makes total sense, as complex numbers can rotate a point in a plane.


#### Both Parts together


To answer the straightforward question:
_What does Euler's formula Eq. (1) look like for Eq. (6)?_
It is a scaled rotation matrix, _i.e._,

$$
\exp\left(
\begin{bmatrix}
    a & -b \\\\
    b & a
\end{bmatrix} 
\right) =
\exp\left(a\right)
\begin{bmatrix}
    \cos\left(b\right)  & -\sin\left(b\right)  \\\\
    \sin\left(b\right)  & \cos\left(b\right) 
\end{bmatrix}.
\tag{10}
$$


## Takeaways

In this post, I ask a more exploratory question.
While many of the different representations simply represent the same thing, we can explore their pros and cons.
Sometimes we find interesting connections, and we can strengthen our intuition. 
Also, it is a good chance to revisit some concepts.

But is exploration useful?
(i) At some point you will encounter Lee groups and rotation matrices.
The exponential of a matrix is one big part of all those stories.
Especially, when introducing the exponential coordinates of rotations and the rotation matrix based on them, this can be overwhelming.
To avoid this, we can obviously toy around with $SO(2)$ instead of $SO(3)$.
I hope this post helps you in understanding the derivation for the $SO(3)$ case.
(ii) Matrix exponentials are incredibly useful for state transition because they are related to differentiation of systems of equations.
For example, to describe a system in control theory.
(iii) I also hope that I could include some cliffhangers, _e.g._, what does multiplication between vectors mean? or what is a complex number equivalent to a rotation in $SO(3)$?





---
**Sidenote:**

I use [$\KaTeX$](https://katex.org/) to create wonderful looking equations.
Unfortunately, not all $\LaTeX$ functions/commands are possible.
Available and supported ones are listed in this online reference of [supported $\TeX$ functions](https://katex.org/docs/supported.html).

Use double-double backslash for matrix environment.
```math
$$
\begin{bmatrix}
    a & b \\\\
    c & d
\end{bmatrix}
$$
```
It's a weird quirk of $\KaTeX$.


**Edit:**

Updated on Sep. 12, 2025: Just reformating and refactoring.