# ISC4221C Discrete Algorithms for Science Applications (Fall 2023) Lab 8

**Your report should be a self-contained markdown file with a description of your answers and the code copied inside of it.**

## Problem 1 (10 pts): Random Samples of a Triangle
If α, β, γ are nonnegative and sum to 1, and A, B, C are the vertices of a triangle, then the point p = αA + βB + γC is in the triangle. The following proposed algorithms for randomly sampling a triangle each come up with values for the coefficients that define p.

### Algorithm 1
Choose three random values r1, r2, and r3. Set:
- $α = r1 / (r1 + r2 + r3)$
- $β = r2 / (r1 + r2 + r3)$
- $γ = r3 / (r1 + r2 + r3)$

### Algorithm 2
Choose two random values r1 and r2; but if $r1 + r2 > 1$ then replace r1 by $1 - r1$ and r2 by $1 - r2$. Set:
- $α = 1 - r1 - r2$
- $β = r1$
- $γ = r2$

### Algorithm 3
Choose two random values r1 and r2. Set:
- $α = 1 - \sqrt{r1}$
- $β = √r1 * \sqrt{r2}$
- $γ = √r1 * (1 - \sqrt{r2})$

Write a program which accepts the vertices of a triangle and a point count N, computes N random points in the triangle according to each of the 3 algorithms, and makes a separate plot of the sample points for each algorithm.

Test your code with $N=1000$ points on the triangle {(4,0), (3,4), (0,1)}.

Turn in your three plots. One algorithm behaves differently from the other two; please comment on this difference and describe what you see.

## Problem 2 (10 pts): Triangle Quadrature

Let T be the triangle whose vertices {A,B,C} are {(0,1), (3,0), (2,5)}. The integral of a function f(x, y) over the triangle can be approximated by evaluating the function at N points selected uniformly at random from T, averaging these values, and multiplying by the area of T.

Estimate the integral of the function $f(x) = x^2$ over T using N = 10, then 100, then 1000, then 10000, then 100000 and:
1. Algorithm 1;
2. Algorithm 2;
3. Algorithm 3.

Turn in your 15 computed estimates for the integral and make any comments you can think of about the fact that the exact integral is 46.25.

## Problem 3 (10 pts): Triangle Properties

Let T be the triangle whose vertices {A,B,C} are {(0,1), (3,0), (2,5)}. Compute the following quantities:
1. the angles at vertices A, B, and C;
2. the area;
3. the centroid;
4. the distance from the point (7, 24, 0) to T.

Turn in your numbered answers to these questions.