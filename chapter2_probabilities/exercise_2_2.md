> Deterministic numbers satisfy the property of transitivity, so that if $x > y$ and $y > z$ then it follows that $x > z$. When we go to random numbers, however, this property need no longer apply. Figure 2.16 shows a set of four cubical dice that have been arranged in a cyclic order. Show that each of the four dice has a $2/3$ probability of rolling a higher number than the previous die in the cycle. Such dice are known as non-transitive dice, and the specific examples shown here are called Efron dice.
>
> ![An example of non-transitive cubical dice, in which each die has been ‘flattened’ to reveal the numbers on each of the faces. The dice have been arranged in a cycle, such that each die has a 2/3 probability of rolling a higher number than the previous die in the cycle.](./exercise_2_2.png)

Starting with the yellow die, all sides have the same value 3. For the blue die, four of six elements are larger than 3, satisfying the claim.

For the green die, the probability of rolling a higher number depends on the outcome of the roll of the blue die. With probability $1/3$, $blue=0$, and with probability $2/3$, $blue=4$. In the former case, the green die certainly has a larger value. In the latter, it has a larger value with probability $1/2$. Hence, the probability of observing a larger value is $1/3\times 1+2/3\times 1/2=1/3+1/3=2/3$, satisfying the claim.

The red die has a larger value of six with probability $1/3$ if the green die had a value of 5. If the green die had a value of 1, the red die certainly has a larger value. Hence, $1/3\times 1/2 + 1/2=1/6+3/6=4/6=2/3$.

Finally, the yellow die has a larger value than the red if and only if the red rolled a 2. This happens with probability $2/3$.
