---
title: Chapter 3 — Proofs
---

## [How to Prove It, by Daniel J. Velleman](../)

{{< toc >}}

### Chapter 3 — Proofs

#### Chapter 3.1 — Proof Strategies
##### Notes

Proofs are like the logical arguments studied in [§1](../ch1): they consist of a set of _hypotheses_ leading to a _conclusion_. The goal of a proof is to prove the validity of a _theorem_, where the theorem is usually an answer to a mathematical question. Hypotheses and conclusions are usually general and non-specific, which is to say, they contain free variables. If we were to assign these variables values, in our attempt at proving a theorem for example, we would create an _instance_ of that theorem. 

Like an argument, a theorem is considered correct or valid if, in _every possible_ instance of the theorem where the hypotheses are true, the conclusion is also true. A way to disprove a theorem is thus obvious: we find a _counterexample_ to this rule; an instance where the hypotheses are true, but the conclusion is false. 

There exists no exact method for writing a proof, given the vastness of maths. It is a sort of art. There are, however, strategies and techniques for more easily solving proofs. One example of a technique would be drawing _inferences_ from the hypothesis; we _assume_ that the hypotheses are true and link (infer) from that a statement, which we can also assume as true. For instance, in any theorem of the form $P \rightarrow Q$, we can take $P$ as a hypothesis and assume its truth; from there, we attempt to show how $P$ being true means $Q$ must be true as well.

Note that taking something as a hypothesis, assuming its truth, does not mean it _is_ true (_asserting_ its truth). Care must be taken in this regard. To help in this process, we can divide a theorem into two parts: _givens_ and _goals_. The givens are statements and propositions assumed to be true, and the goal is the statement that we must prove in order to validate our theorem. 

For statements of the form $P \rightarrow Q$, you may remember the idea of a contrapositive: the statement can also be expressed as $\neg Q \rightarrow \neg P$. We can use this in our method as well; we assume that Q is false, and prove that P is false as well.

##### Exercises
1. ...
   1. Hypotheses: $n > 1$, and $n$ is composite. Conclusion: $2^n-1$ is composite. When $n=6$, the hypotheses are both true, and thus we can conclude that $2^6 - 1$ is composite, and so it is ($63$). However, this is just one instance of the theorem, and can not be taken as proof of anything.
   2. The hypotheses are both true, so we can conclude that $2^{15} - 1$ is composite. Indeed, it is so.
   3. In this case, $n = 11$, the second hypothesis is not true, since $11$ is prime. Therefore, the theorem is pointless and a vacuous truth, though the conclusion _is_ true.
2. ...
   1. Hypotheses: $b^2 > 4ac$. Conclusion: $ax^2 + bx + c = 0$ has two solutions.
   2. Because we are solving _for_ x in the quadratic equation, so giving it a value would go against the whole point.
   3. The hypothesis ($25 > 24$) is true, so we can conclude that $2x^2 - 5x + 3 = 0$ has two solutions. Indeed, the conclusion ($x = 3/2$ and $x = 1$) is true.
   4. The hypothesis ($16 > 24$) is false, so the instance is a vacuous truth and pointless.
3. ...
   1. Hypotheses: $n > 2$ and $n$ is composite. Conclusion: $2n+13$ is composite. 
   2. When $n = 9$, both hypotheses are true, and we can conclude that $2n+13$ is composite. However, $2(9)+13=31$ and $31$ is a prime number. Therefore, this theorem is incorrect.
4. **Theorem:** if $0 < a < b$, then $b^2 > a^2$.
   1. Proof:
      1. We know that $b > a$.
      2. We can multiply positive number $a$ with both sides to get the inequality: $ab > a^2$.
      3. We can multiply positive number $b$ with both sides to get the inequality: $b^2 > ab$.
      4. If $ab > a^2$, and $b^2 > ab$, then $a^2 < b^2$.
      5. **QED**
5. **Theorem:** if $a < b < 0$, then $a^2 > b^2$.
   1. Proof:
      1. We know that $a < b$.
      2. Multiplying both sides by negative number $a$ gives us: $a^2 > ab$.
      3. Multiplying both sides by negative number $b$ gives us: $ab > b^2$.
      4. If $ab > b^2$ and $a^2 > ab$, then $a^2 > b^2$.
      5. **QED**
6. **Theorem:** if $0 < a < b$, then $\frac{1}{b} < \frac{1}{a}$.
   1. Proof:
      1. We know that $\frac{1}{b} < \frac{1}{a}$.
      2. Multiplying both sides by $\frac{1}{ab}$ gives us: $\frac{a}{ab} < \frac{b}{ab}$.
      3. We can simplify these fractions to get: $\frac{1}{b} < \frac{1}{a}$.
      4. **QED**
7. **Theorem:** if $a^3 > a$, then $a^5 > a$.
   1. Proof:
      1. We know that $a^3 > a$.
      2. We can multiply both sides with positive number $a^2$ to get: $a^5 > a^3$.
      3. If $a^3 > a$ and $a^5 > a^3$, then $a^5 > a$.
      4. **QED**

#### Chapter 3.2 — Proofs Involving Negations and Conditionals
##### Notes

Try and convert a negative statement $\neg P$ into a positive statement before working on it. If you can not achieve this, then attempt to prove it by *contradiction* — assume $P$ is true, and then try and prove some theorem that is false with it.