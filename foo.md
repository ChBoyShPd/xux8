---
abstract: |

# LaTeX Variables
papersize: letter
documentclass: article
fontsize: 10pt
linestretch: 1
header-includes: |
  \usepackage{amssymb}
  \usepackage{amsmath}
  \usepackage{mathtools}
  \DeclarePairedDelimiter{\ceil}{\lceil}{\rceil}
  \DeclarePairedDelimiter{\floor}{\lfloor}{\rfloor}
  \usepackage[margin=0.1in]{geometry}
---

NAMEHERE | FOCS Exam 2 Crib Sheet | 2019-04-03

1.1:

**propositions**: declarative sentence 
**operators**: $\land$ = and, $\lor$ = or, $\oplus$ = xor, $\to$ = implication, $\leftrightarrow$ = bidirectional 
**implies**: if $p$ then $q$, $p$ implies $q$, if $p$, $q$, $p$ only if $q$, $p$ is sufficient for $q$, a sufficient condition for $q$ is $p$, $q$ if $p$, $q$ whenever $p$, $q$ when $p$, $q$ is necessary for $p$, a necessary condition for $p$ is $q$, $q$ follows from $p$, $q$ unless $\neg p$. 
**ncci**: converse $\equiv$ inverse, normal $\equiv$ contrapositive. 
**precedence**: $\neg$, $\land$/$\lor$, $\to$/$\leftrightarrow$.

1.4:

**predicates**: $P(x)$ where $x$ is a variable and $P$ is a statement involving a variable
**quantifiers**: $\forall$ = for all, $\exists$ = exists, $\exists!$ = exists exactly 1.
**negation**: $\neg \forall x P(x) \equiv \exists x \neg P(x)$ and vice versa

1.5:

Location of quantifiers matter. Read the predicate statements.

1.7/1.8:

Informal you can skip steps, formal you can't. Announce if you're not doing a direct proof.
**Exhaustive Proof/Proof by Cases**: Prove all cases.
**WLOG**: If there are equivalent cases you can remove them. Be extremely careful.
**Existence**:
Constructive = find element. Nonconstructive: prove that there is an element but don't find it.
**Uniqueness**:
Prove that for all elements besides the one that is true, the predicate is false.
**Multiple strats**: Forward/Backward/Adapting Existing Proofs/Counterexamples

4.1/4.3:

**division**: $a \mid b$ = a is factor/divisor for b, b is multiple of a. $a \nmid b$ means not divisible. $a \div d = q$, $a \mod d = r$, a = dividend, d = divisor, q = quotient, r = remainder.
**mod expon**: using mod arith, split into $(ab) \mod x = (a \mod x)(b \mod x) \mod x$ (mult = mult, add = add), use to break into binary, then build up ($a \mod x$, $a^2 \mod x$, $a^4 \mod x$, etc.)
**ftoa**: all integers greater than 1 are prime or the product of primes.

4.2:

converting binary to octal to decimal to hex, etc. ez

2.1:

**sets to know**: $\mathbb{N} = {0, 1, 2, 3, \dots}$ 
$\mathbb{Z} = {\dots, -3, -2, -1, 0, 1, 2, 3, \dots}$
$\mathbb{Z^+} = {1, 2, 3, \dots}$
$\mathbb{R} =$ real numbers
$\mathbb{R^+} =$ positive real numbers
$\mathbb{C} =$ complex numbers
$\mathbb{Q} =$ rational numbers
$\mathbb{I} =$ irrational numbers.
$U$ = everything.
$\emptyset$ = nothing.
**notation**:
Interval notation [] inclusive () exclusive. Set builder $\{x~|~x\}$
**set equality**: same elements = equal sets
**subsets**: A subset B if A contains everything in B, proper if A $\neq$ B.
**cardinality**: number of distinct elements
**size**: finite/infinite (countable/uncountable)
**power set**: set of all subsets: cardinality of 2^(n) where there are n elements of the original set.
**cartesian product**: set of tuples/combinations of all elements in A with all in B (with all in C, etc)
**quantifiers** restricting domain of $U$

2.2:

**functions**:
$A \cup B$: union, everything in A and B
$A \cap B$: intersection, everything in both A and B but not in only A or only B
$A \setminus B$: difference, everything in A but not B
$\overline{A}$: complement, everything not in A
$\bigcup_{i=1}^{n} A_i = A_1 \cup A_2 \cup \dots \cup A_n$
$\bigcap_{i=1}^{n} A_i = A_1 \cap A_2 \cap \dots \cap A_n$
$A \oplus B$: union - intersection
**inclusion/exclusion principle**: A B C = A + B + C - A and B - B and C - C and A + A B C

2.3/2.5 functions/cardinality:

**functions**: maps from A to B.
$f~:~A \to B$
A is domain
B is codomain
$f(a) = b$
a is preimage of b, b is image of a (both under f)
**range** of $f$ is the set of all images of points in $A$ under $f$, denoted $f(A)$
**injection**:
all elements of $A$ are mapped to a unique element of $B$.
**surjection**:
all elements of $B$ are mapped to an element of $A$. 
**bijection**: inj+surj, implies that the domain and codomain are the same size.
**inverse func**: can map back to A from B with a func.
**floor/ceil**: denoted $\floor{x} and \ceil{x}$
**composition**: function from A to C, f = A to B, g = B to C, f(g(x)) or $f \circ g$
**cardinality**: $|A| = |B|$ iff there is a bijection from $A$ to $B$.
If there is an injection from $A$ to $B$ then $|A| \leq |B|$.
**countable/uncountable**: countable has cardinality of $\aleph_{0}$.

2.4 sequences/recurrence relations:

**sequence** ordered list of events, unique elements, function from a subset of integers to set $S$.
**arithmetic progression** is sequence of form $s_n = a + nd$ where $n = 0, 1, 2, \dots$, and the initial term $a$ and the common difference $d$ are real numbers.
**geometric progession** is a sequence of form $t_n = ar^n$ where $n = 0, 1, 2, \dots$, and the initial term $a$ and the common ratio $r$ are real numbers.
**recurrence relation** for the sequence ${a_n}$ is an equation that expresses $a_n$ in terms of one or more of the previous terms of the sequence.
**initial conditions** for a sequence specify the terms that precede the first term where the recurrence relation takes effect.
**solving the recurrence relation** = finding a formula for the $n^{\text{th}}$ term of a recurrence relation. this is closed formula.

5.1 weak induction:

**basis step**: show $p(x)$ is true where $x$ is the base case.
**inductive step**: show $p(k) \to p(k+1)$ is true for all positive integers $k$.
**inductive hypothesis/I.H.** = $p(k)$.
**points**: don't assume $p(k)$ is true for all positive integers, prove that if $p(k)$ is true then $p(k+1)$ is true.

5.2 strong induction:

**basis step**: show $p(x)$ is true for all $x$ where $x$ are the base cases.
**inductive step**: assume $p(x)$ up to $p(k)$, show that this implies $p(k+1)$ (where the lowest $x \leq j \leq k$ and $k \geq$ the highest $x$ if there are multiple $x$).

5.3 recursive definitions/structural induction:
**recursive/inductive definition of function**: specify the function at the base values, define rule for finding the function's value based on previous values. Example: $f(0) = 1$, $f(n) = n \times f(n-1)$ for $f(n) = n!$
**recursive definition of set**: define initial collection of elements, define rules for forming new elements of the set from other elements. Example: $3 \in S$, if $x \in S$ and $y \in S$ then $x + y \in S$ will give the set of all multiples of 3.
**alphabet**: set of symbols denoted by $\Sigma$.
**string** is a finite sequence of symbols from $\Sigma$.
**$\Sigma*$** is the set of all strings over $\Sigma$.
**$\lambda$** is the emptyset, and $\Sigma*$ is defined by $\lambda \in \Sigma*$ followed by if $w \in \Sigma*$ and $x \in \Sigma$ then $wx \in \Sigma*$.
**graph** is a set of vertices $V$ and a set of edges $E$.
**path** between vertices $i$ and $j$ is a sequence of edges that connect $i$ and $j$.
**connected graph** is a graph in which there is a path between every pair of vertices
**nodes** are another term for vertices.
**trees** are connected graphs with only a single path between any pair of vertices
**rooted tree** is a special type of tree, it contains a distinguished vertex called the **root**
**recursive definition**: Basis: A single vertex $r$ is a rooted tree, recursive: suppose that disjoint rooted trees exist, and the graph formed by connecting the root of each disjoint rooted trees to a new point $r$ is a rooted tree.
**full binary tree** is a rooted tree where each vertex has either 0/2 children (regular binary tree can have one child) - single vertex $r$ is a full binary tree, if $T_1$ and $T_2$ are disjoint FBTs, there is a FBT denoted $T_1 \cdot T_2$ consisting of a root $r$ w/edges connecting to the roots of $T_1$ and $T_2$. # nodes for $T = T_1 \cdot T_2$ = $1 + N(T_1) + N(T_2)$, $N(T) = 1$ then $T$ is single node, height is $H(T) = 0$ then $T$ is a single node, $T = T_1 \cdot T_2$ where $T_1$/$T_2$ are FBTs, $H(T) = \text{max}(H(T_1), H(T_2)) + 1$
**structural induction**: show result holds for structure specified in basis step of recursive definition. show that if statement is true for each structure used to construct the new structure, then it is true for the new stucture.

5.4:

algorithms are recursive if it solve a problem by reducing it to an instance of the same problem with smaller input. example:
```python
procedure mystery(n: nonnegative integer)
    if n = 0 then return 1
    else return n + mystery(n-1)
```

6.1-6.2 counting/pidgeonhole principle:
**product rule** if a procedure is 2 tasks and there are $x$ ways to do first task and $y$ ways to do second task there are $xy$ ways to do the procedure
**sum rule** if there are either $x$ ways to do something or $y$ ways to do something then there are $x+y$ ways to do something.
**subtraction rule** if a task can be done either in one of $x$ or one of $y$ ways, then the total number of ways is $x + y - (\text{overlap between }x\text{ and }y)$
**division rule** if there are $n$ ways to carr out a task, for for any way $w$ there are $(d-1)$ ways that are identical to $w$, then there are $n \div d$ ways to do the task.
**pidgeonhole principle**: if $k$ is positive integer and $k+1$ objects are placed into $k$ boxes then at least one box has 2 or more objects.
**generalized PHP**: if $N$ objects are placed into $k$ boxes, then there is at least one box containing at least $\ceil{\frac{N}{k}}$ objects.

6.3-6.5 permutations/combinations:
**permutations** order is important.
**combinations** order isn't important.
**$r$-permutations** is a partial permutation of $S$.
**$P(n,r)$ no repeats**: $\frac{n!}{(n-r)!}$.
**$C(n,r)$ no repeats**: $\frac{n!}{(n-r!)!r!}$.
**binomial theorem**: $(x+y)^n = \sum_{j=0}^{n} \binom nj x^{n-j}y^{j}$.
**pascal's identity**: $\binom {n+1}k = \binom n{k-1} + \binom nk$.
**$P(n,r)$ repeats**: $n^r$.
**$C(n,r)$ repeats**: $\frac{(n+r-1)!}{((n+r-1)-r)!r!}$.
**permutations with indistinguishale objects**: $\frac{n!}{n_1! n_2! \dots n_k!}$.

7.1 discrete probability:
**experiment** is a procedure that yields one of a given set of possible outcomes.
**sample spaace** is the set of possible outcomes.
**event** is subset of the sample space.
**probability of event** is $p(E) = \frac{|E|}{|S|}$ where $E$ is event and $S$ is sample space
**probability of complement** is $p(\overline{E}) = 1 - p(E)$.
**probability of unions** is $p(E_1 \cup E_2) = p(E_1) + p(E_2) - p(E_1 \cap E_2)$

7.2 probability theory:
**probability distribution**: $0 \leq p(s) \leq 1$ for each $s \in S$, and $\sum_{s \in S} p(s) = 1$. for each outcome $s \in S$.
**uniform distribution**: duh
**probility of event** equal to the sum of probabilities of the outcomes in the event
**complement and union rules** still apply
**conditional probability**: $p(E|F) = \frac{p(E \cap F)}{p(F)}$
**multiplication rule**: $p(A \cap B) = p(A|B) \times p(B)$

7.3 bayes theorem:
**law of total probability**: $p(B) = p(B|A_1)p(A_1) + \dots + p(B|A_k)p(A_k) = \sum_{i=1}^{k} p(B|A_i)p(A_i)$
**"probability"** = frequency
**Bayesian Probability** is a measure of a state of knowledge that quantifies uncertainty.
**theorem**: $p(A|B) = \frac{p(B|A)p(A)}{p(B)} = \frac{p(B|A)p(A)}{p(B|A)p(A) + p(B|\overline{A})p(\overline{A})}$
