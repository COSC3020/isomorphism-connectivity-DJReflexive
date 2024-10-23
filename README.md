# Isomorphism

Prove that if two graphs $A$ and $B$ are isomorphic they do *not* have to
be completely connected. I have started with the formal definition of
isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.



# My Proof

Assume that A and B are disconnected graphs of equal sizes.

$A = (V_A , E_A)$ and $B = (V_B , E_B)$

We need to show that there exists a bijection where $f: V_A \to V_B$ such that $(v, u) \in E_A$ iff $(f(u), f(v)) \in E_B$.

### Let's look at an example:

Assume graph A has edges\
$( (A, B), (B, C), (C, A) ) \in E_A$ and $( (D, E), (E, D) ) \in E_A$

Assume graph B has edges \
$( (X, Y), (Y, Z), (Z, X) ) \in E_B$ and $( (W, V), (V, W) ) \in E_B$

We can then map the following vertexes from $f: V_A \to V_B$:\
$f(A) \to X$\
$f(B) \to Y$\
$f(C) \to Z$\
$f(D) \to W$\
$f(E) \to V$

Therefore mapping the edges would resemble:\
$f(A, B) \to (X, Y)$\
$f(B, C) \to (Y, Z)$\
$f(C, A) \to (Z, X)$\
$f(D, E) \to (W, V)$\
$f(E, D) \to (V, W)$

This means we can state there is a bijection (every edge from A can be mapped to B) therefore graphs A and B are isomorphic.


### Let's look at a counter-example:

We're going to assume a very similar example, but lets say that one of the edges $(B, C)$ in graph A no longer exists, but graph B remains unchanged.

Assume graph A has edges\
$( (A, B), (C, A) ) \in E_A$ and $( (D, E), (E, D) ) \in E_A$

Assume graph B has edges \
$( (X, Y), (Y, Z), (Z, X) ) \in E_B$ and $( (W, V), (V, W) ) \in E_B$

We can then map the following vertexes from $f: V_A \to V_B$:\
$f(A) \to X$\
$f(B) \to Y$\
$f(C) \to Z$\
$f(D) \to W$\
$f(E) \to V$

Therefore mapping the edges would resemble:\
$f(A, B) \to (X, Y)$\
$f(C, A) \to (Z, X)$\
$f(D, E) \to (W, V)$\
$f(E, D) \to (V, W)$

However, the edge $(Y, Z)$ still exists in graph B and there is nothing mapping to it. This means the two graphs are not onto, and therefore does not have a bijection. In this example, the graphs A and B are **not** isomorphic.


# Sources

- TA Ali: For the idea to add a counter example where the two graphs are not isomorphic and show how those two graphs do not show a bijection. He also reviewed all of this assignment to see if things looked good and made sense.

# Plagiarism Acknowledgement

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.