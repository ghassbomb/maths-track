---
title: Chapter 2 — Quantificational Logic
---

## [How to Prove It, by Daniel J. Velleman](../)

{{< toc >}}

### Chapter 2 — Quantificational Logic

#### Chapter 2.1 — Quantifiers

##### Notes

Functional propositions such as $f(x)$ can be true for any number of $x$
within their universe of discourse $U$. But if we wish to express, or
'quantify', the number or range of values they are true for, we can use
the following quantifiers:

1.  If $f(x)$ is true for _every_ $x$ within $U$, then we can express
    this as: $\forall x f(x)$. Grammatically, this means something like
    'For all $x$, $f(x)$ (is true)'. Remember that this means the truth
    set of our function proposition is the same as its universe of
    discourse. Thus, we can also say that $f(x)$ is 'universally true'.

2.  If $f(x)$ is true for _at least_ one $x$ within $U$, then we can
    express this as: $\exists x f(x)$. Grammatically, this means
    something like 'There exists an $x$, such that $f(x)$'. This means
    the truth set of $f(x)$ is not empty, or null.

We say that quantifiers _bind_ a variable. For instance, take the
following quantified statement: $\forall x L(x, y)$ where $L(x,y)$ means
'$x$ likes $y$'. Here, $x$ is essentially irrelevant. Everyone
($\forall x$) is said to like $y$, so we only need to know which $y$
this statement is true for; which person or thing $y$ is liked by
everyone within the universe of discourse. $x$ is a bound variable,
whereas $y$ is a free variable. Interestingly, grammatically, we can
express this statement as: 'Everyone likes $y$'. If it was
$\exists x L(x, y)$ we would say 'Someone likes $y$'.

We can also use multiple quantifiers. For instance, if we were to say
'all students like someone':
$\forall x (S(x) \wedge \exists y L(x, y))$. Note that all variables are
bound in this statement; you can usually determine such features from
the grammatical form of the statement. Within '**all** students like
**some**one', all nouns are quantified. Thus, in logical form, if they
are quantified, they are bound.

Order of quantifiers is important. Let's go back to the statement
$\forall x L(x, y)$, 'There is a person $y$ whom everyone likes'. We can
rewrite the logic to fit the statement 'Everyone likes someone':
$\forall x \exists y L(x,y)$. What happens if we swap the two
quantifiers? If the statement is changed to
$\exists y \forall x L(x,y)$, it means 'Someone exists whom everyone
likes'. There is a subtle difference in these statements: in the first
statement, we mean that everyone has someone they like. In the second
statement, we mean that there exists a single person who is universally
liked by everyone.

##### Exercises

1.  1.  Where $F(x, y)$ means '$x$ has forgiven $y$', and $S(x)$ means
        '$x$ is a saint'.\
        $\forall x (\exists y F(x,y) \rightarrow S(x))$
    2.  Where $C(x)$ means '$x$ is in calculus class', $D(y)$ means '$y$
        is in discrete maths class', and $S(x,y)$ means '$x$ is smarter
        than $y$'.\
        $\neg \exists x (C(x) \wedge \forall y D(y) \rightarrow  S(x,y))$
    3.  Where $m$ means Mary, and $L(x, y)$ means '$x$ likes $y$'.\
        $\forall x (\neg (x = m) \rightarrow L(x, m))$
    4.  $S(x, y)$ means '$x$ saw a police officer $y$', $j$ means Jane,
        and $r$ means Roger.\
        $\exists y S(j, y) \wedge \exists y S(r, y)$
    5.  With the same meanings:\
        $\exists y (S(j, y) \wedge S(r, y))$

2.  1.  Every man who is not married to anyone is unhappy.
    2.  There exist parents with children $x$ who have aunts $z$.
3.  1.  True.
    2.  False.
    3.  False.
    4.  True.
    5.  True.
    6.  False.

#### Chapter 2.2 — Equivalences Involving Quantifiers

##### Notes

$\neg \exists xA(x)$, assuming $A(x)$ means '$x$ is annoying' and our
universe of discourse is every human, grammatically equates to 'There
exists no human who is annoying'. However, another way to express this
would be $\forall x \neg A(x)$, or 'Every human who exists is not
annoying'. Here, we're essentially flipping a negative statement to mean
the same as a positive statement.

We do this by flipping the other proposition in the statement like we
flipped the quantifiers. We can expand this rule further; assuming that
$\neg \exists x$ and $\forall x$ are opposites, then $\neg \forall x$
and $\exists x$ are also opposites. Thus, we can say that:

$$
\begin{aligned}
  \neg \exists x A(x) & = \forall x \neg A(x) \\
  \exists x \neg A(x) & = \neg \forall x A(x)
\end{aligned}$$ where $A(x)$ can be any function proposition. This is
one equivalence.

Another equivalence involves two *identical* quantifiers being used in
succession. We determined previously that two different quantifiers
affect meaning when swapped. For instance,
$\forall x \exists y (f(x, y)) \neq \exists y \forall x (f(x, y))$. The
same is not true of $\forall x \forall y (f(x, y))$ and
$\forall y \forall x (f(x, y))$. Assuming $f(x, y)$ means $x$ is friends
with $y$, these statements mean 'everybody ($x$) is friends with
everybody ($y$)', and 'everybody ($y$) is friends with everybody ($x$)';
thus, equivalent. The same holds true if it were:
$\exists y \exists x (f(x, y))$.

When writing quantifiers, you use the following form to denote universes
of discourse: $\forall x \in \mathbb{R} (x^2>0)$; which means 'Every
real number has a square greater than 0'. Yet another way to put it
would be 'All $x$ are real numbers, and (thus) $x^2$ is greater than
zero' which, in logical form, would be:
$\forall x (x \in \mathbb{R} \rightarrow x^2 \ge 0)$. The reason for the
conditional connective is simple: since the statement is universally
true for every element of the universe of discourse ($\mathbb{R}$), it
is a matter of course that 'if $x$ is an element of $\mathbb{R}$, then
it is true'. If it were that $\exists x \in \mathbb{R} (x^2>0)$, then
its equivalent would be $\exists x (x \in \mathbb{R} \wedge x^2 > 0)$.
We say that, as a quantifier bounds a variable, a universe of discourse
bounds the quantifier, making it a *bounded quantifier*.

Now, finally, let us discuss the expansion of quantified statements. Is
$\forall x (f(x) \wedge g(x)) = \forall x f(x) \wedge \forall x g(x)$?
Yes. It's merely the difference between '$x$ is always $f(x)$ and
$g(x)$' and '$x$ is always $f(x)$ and $x$ is always $g(x)$'. Is
$\exists x (f(x) \wedge g(x)) = \exists x f(x) \wedge \exists x g(x)$?
No. It's the difference between: 'some $x$ are $f(x)$ *and* $g(x)$' and
'some $x$ are $f(x)$ and some $x$ are $g(x)$'. This is false because we
mean to say that there exist some $x$ that satisfy both propositions
simultaneously, not that there exist some $x$ that satisfy one
proposition and some $x$ that satisfy the other.

##### Exercises

1.  1.  Where $M(x)$ means '$x$ is majoring in math', $F(x,y)$ means
        '$x$ and $y$ are friends', and $H(y)$ means '$y$ needs help with
        their homework'. 
        $$
        \begin{aligned}
          \neg \forall x[M(x) \rightarrow \exists y( F(x,y) \wedge H(y))] \\\\
          \exists x \neg[M(x) \rightarrow \exists y( F(x,y) \wedge H(y))] \\\\
          \exists x[M(x) \wedge \neg \exists y(F(x,y) \wedge H(y))] \\\\
          \exists x[M(x) \wedge  \forall y\neg(F(x,y) \wedge H(y))] \\\\
          \exists x[M(x) \wedge  \forall y(\neg F(x,y) \vee \neg H(y))]
        \end{aligned}
        $$

    2.  Where $R(x, y)$ means '$x$ has a roommate $y$' and $D(y, z)$
        means '$y$ dislikes $z$'. 
        $$
        \begin{aligned}
          \forall x \exists y (R(x,y) \wedge \forall z D(y, z)) \\\\
          \exists x \forall y \neg(R(x,y) \wedge \forall z D(y, z)) \\\\
          \exists x \forall y (\neg R(x,y) \vee \exists z \neg D(y, z)) \\\\
        \end{aligned}
        $$

#### Chapter 2.3 — More Operations on Sets

##### Notes

Previously, we used set-builder notation like this: $\\{n^2 \mid n \in \mathbb{N} \\}$ — this set contains every perfect square. With quantifiers, we can rephrase this as: $\\{ x \mid \exists n \in \mathbb{N} (x = n^2) \\}$. These two sets are the exact same, and we can thus say that: $x \in \\{n^2 \mid n \in \mathbb{N}\\}$ and $\exists n \in \mathbb{N} (x = n^2)$.

We can define an _indexed family of sets_, which is a number of related sets with which we use an index to distinguish between them. For instance, the indexed family of sets of Nobel Prize winners, where the index set $P$ contains the various Nobel Prizes ($p$) and the set $W_p$ contains the winners of the given Nobel Prize. For instance: $\text{Marie Curie} \in W_\text{Physics}$. We can define the family like this:

1. We create the _index set:_ $P = \\{p \mid p \text{ is a Nobel Prize}\\}$.
2. We use the index set to define our family of sets: $W_p = \\{w \mid w \text{ is a winner of the Nobel Prize } p\\}$.

In the same vein, but on a smaller scale, we can define set _families_, which consist of multiple sets. For instance, $X = \\{P, I\\}$ is the family of the two sets: $I$ ($1 - 100$) and $P$ ($1^2 - 100^2$). Note that elements of the set $P$ or $I$ are not elements of $X$; there are only two elements in $X$: $P$ and $I$. For instance, $1 \notin X$, even though $1 \in I$; $I \in X$ is true, however.

Let's say, however, that you _want_ the family set $X$ to contain the elements of $P$ and $I$; in that case, you would use $\bigcup X$. $\bigcup X$ is the union of the family $X$, and thus the set of elements of all the sets contained within the family ($I$, and $P$ in this case). We can express it as such: $X = \\{x \mid x \in I \vee x \in P\\}$. The intersection of a family, $\bigcap X$, would contain all the elements common to each of the sets in that family. In this case, it would be numbers like $1$ and $4$, that are both within the range $1-100$ and are perfect squares.

What if the family is indexed? The union of an indexed family of sets would function the exact same, though we have a special notation for it: $$\bigcap_{p \in P} W_p$$ Here, the union set would contain every Nobel Prize winner.