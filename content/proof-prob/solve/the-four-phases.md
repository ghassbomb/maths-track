---
title: The Four Phases
---

## [How to Solve It, by G. Polya](../)

### The Four Phases

As you attempt a problem, you develop your (orginally incomplete) understanding of the question given. This is a continuous process, even when you are close to the end. It can be grouped into four phases:

The first is *understanding the problem* --- figuring out what is required of us. To this end, you should be able to restate the problem fluently, and understand the unknowns, the data, and the condition. You should draw out any figures, if applicable. If not given, you should introduce suitable notation. 

**Example**: A rectangular garden has a length that is 5 meters more than twice its width. If the area of the garden is 60 square meters, find the dimensions of the garden.

1. What are the unknowns? The dimensions of the garden, which we can notate with $l$ (length) and $w$ (width).
2. What is the data? That $l = 2w + 5$, and the area, $A$, of the garden is $60 ~m^2$.
3. What is the condition?  That $l = 2w + 5$ and $l \cdot w = 60$, since this links all our data and unknowns together.

Now that we understand how the various 'items' are connected, we *make a plan*. This involves recalling similar problems we have solved before, especially ones with similar unknowns. If that doesn't click, you can try restating the problem --- generalizing it, specializing it, analogizing it, removing parts of it, e.t.c. 

**Example**: Continuing with the same example:

1. Have you solved a similar problem before? Yes, I have. Algebraically, this problem resembles a *simultaneous equation*, where we have two unknowns and two equations linking them.
2. If not, try restating the problem. If you knew the width, could you solve this? What if it were a square instead of a rectangle?

The final working step is to carry out our plan. This is simple, so long as one does not lose sight of the solution --- something unlikely assuming he reasoned the solution himself.

**Example**: Continuing with the same example: we determined that our issue, though geometric in nature, can be resolved as a simultaneous equation. To this end:

1. We have two equations: the first, $l = 2w + 5$; and the second, $l \cdot w = 60$. 
2. One of our variables is already expressed in terms of the other in the first equation, so we can substitute it ($l$) into the second equation: $(2w + 5) \cdot w = 60$.
3. We can simplify this equation thus: $2w^2 + 5w - 60 = 0$.
4. Solving this quadratic equation, we get: $(w - 5)(2w + 12)$, or $w = 5$ and $w = -6$.
5. If we remember the context, we can only have one value of $w$. Furthermore, since this is a geometric problem, it can not be negative. Thus, our value of $w = 5$. 
6. Now, we substitute this into any of our original two equations to get the value of $l$. In this case, I'll substitute it into the second: $l \cdot 5 = 60$ and $l = 60/5 = 15$.
7. So, of our unknowns: $l = 15$, and $w = 5$.

There is still one phase left: *reviewing* our solution. This is an oft neglected part of problem-solving. In reviewing, we not only double-check for any errors we have made, but also understand the solution such that we may use it in solving *other* problems as well (see phase two). For instance, we could imagine cases where the same method could be applied to different problems. We could try some thought experiments: 'could we have solved this problem (correctly) with a different method?', 'is there a more concise way to explain our solution?', and so on.

**Example**: In the context of our example:

1. Is the solution correct? We can verify it by substituting our values for $l$ and $w$ into our conditions ($l = 2w + 5$ and $l \cdot w = 60$), and we will find that they are true.
2. Could we have solved this problem (correctly) with a different method? Is there a more concise way to explain our solution? An obvious answer to our first question is that we could have substituted the second equation into the first instead of the opposite operation. Furthermore, we could have done this in terms of $w$ instead of $l$.
3. What if we knew the length, and the relation of the length to the width, instead of the area? 

