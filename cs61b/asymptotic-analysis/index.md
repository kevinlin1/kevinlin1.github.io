---
layout: page
title: Asymptotic Analysis
---

### Algorithms

An _algorithm_ is a step-by-step procedure for solving a problem. An algorithm is an abstract notion, simply describing an approach for solving a problem. The code we write in this class, our programs, are implementations of algorithms.

For example, consider the problem of sorting a list of numbers. One algorithm we might use to solve this problem is called _bubble sort_. Bubble sort says to sort a list by repeatedly looping through the list and swapping adjacent items if they are out of order, until the entire sorting is complete.

Another algorithm we might use to solve this problem is called _insertion sort_. Insertion sort says to sort a list by looping through our list, taking out each item we find, and putting it into a new list in the correct order.

[VisuAlgo has developed a set of interactive visuals](http://visualgo.net/sorting) that can help us visualize these sorting algorithms. Spend a little time playing around with these demos to get an understanding of how much time it takes for bubble sort or insertion sort to completely sort a list.

Since each comparison and each swap takes time, we want to know which is the faster algorithm: bubble sort or insertion sort? And how fast can we make our Java programs that implement them? Much of our subsequent work in this course will involve estimating program efficiency and differentiating between fast algorithms and slow algorithms. This set of activities introduces an approach to making these estimates.

The problem with a timing a program, however, is that not all computers run a program at the same speed. And even on the same computer, a program's efficiency is very non-deterministic because other programs and processes are running at the same time. There are too many variables to take into account when we try to time the runtime of a program.

### Analyzing the runtime of a program

#### Counting Steps

An alternative approach is _step counting_. The number of times a given _step_, or instruction, in a program gets executed is independent of the computer on which the program is run. With counting steps, we can develop a more formal and deterministic method for describing the runtime of programs.

We define a single step as the execution of a single instruction or primitive function call. For example, the `+` operator which adds two numbers is considered a single step. We can see that `1 + 2 + 3` can be broken down into two steps where the first is `1 + 2` while the second takes that value and adds it to 3. From here, we can combine simple steps into larger and more complex _expressions_.

    (3 + 3 * 8) % 3

This expression takes 3 steps to complete, one for addition, one for multiplication, and one for modulus.

From expressions, we can construct _statements_. An assignment statement, for instance, combines an expression with one more step to assign the result of the expression to a variable. For example, in the code

    int a = 4 * 6;
    int b = 9 * (a - 24) / (9 - 7);

each assignment statement takes one additional step on top of however many steps it took to compute the right-hand side expressions. In this case, the first assignment to `a` takes one step to compute `4 * 6` and one more step to assign the result, 24, to the variable `a`. Try to calculate the number of steps it takes to assign to `b`.

Here are some basic rules about what we count as taking a single step to compute:

- Assignment and variable declaration statements

- `return` statements

- Conditional `if` statements

One important case to be aware of is that, while calling a function takes a single step to setup, the body of the function may require us to do much more than a single step of work.

#### Counting Conditionals

With a conditional statement like `if`, the total step count depends on the outcome of the test. For example, the program segment

    if (a > b) {
        temp = a;
        a = b;
        b = temp;
    }

can take four steps to execute: one for evaluating the conditional expression `a > b` and three steps for evaluating each line in the body of the condition. But this is only the case if `a > b`. If the condition is not true, then it only takes one step to check the conditional expression.

That leads us to consider two quantities: the _worst case count_, or the maximum number of steps a program can execute, and the _best case count_, or the minimum number of steps a program needs to execute. The worst case count for the program segment above is 4 and the best case count is 1.

#### Counting Loops

Consider the following program segment.

    for (int k = 0; k < N; k++) {
        sum = sum + 1;
    }

In terms of N, how many operations are executed in this loop? Remember that each of the actions in the for-loop header (the initialization, the test, and the increment) count as one step on its own.

It takes 1 step to execute the initialization, `int k = 0`. Then, to execute the loop, we have the following sequence of steps:

- Check the loop condition, `k < N`

- Add 1 to the `sum`

- Update the value of `sum` by assignment

- Increment the loop counter, `k`

In the very last loop, after we increment `k` such that `k` now equals N, when we check the loop condition again, we finally exit the loop. In the end, our total number of steps is __1 + 4N + 1__.

### Abbreviated Estimates

#### Estimation with _Proportional To_

Producing step count figures for even those simple program segments took a lot of work. Normally we don't need an exact count but rather just an estimate of how many steps will be executed.

The most commonly used estimate is that a program segment runs in time _proportional to_ a given expression, where that expression is in simplest possible terms. Here, _proportional to_ means _within a constant multiple of_.

Thus 2n + 3 is proportional to n since it's approximately 2 times n; and 3n<sup>5</sup> + 19n<sup>4</sup> + 35 is proportional to __n<sup>5</sup>__ since it's approximately 3 times n<sup>5</sup>. As n approaches infinity, the approximation better models the function's real runtime.

Basically, what we're doing here is discarding all but the most significant term of the estimate and also discarding any constant factor of that term.

#### Asymptotic Analysis with Big-Θ

A notation often used to provide even more concise estimates is _big-Theta_, represented by the symbol Θ. Say we have two functions `f(n)` and `g(n)` that take in non-negative integers and return real values. We could say 

> `f(n)` is in Θ(`g(n)`)

if and only if `f(n)` is proportional to `g(n)` as n approaches infinity.

Why do we say "in" Θ? You can think of Θ(`g(n)`) as a set of functions that all grow proportional to g. When we claim that f is in this set, we are claiming that f is a function that grows proportional to g.

There are analogous notations called _big-Oh_ (Ο) and _big-Omega_ (Ω), where big-Oh is used for upper-bounding and big-Omega is used for lower-bounding. If `f(n)` is in O(`g(n)`), it means f is in a set of functions that are upper-bounded by g. Likewise, if `f(n)` is in Ω(`g(n)`), it means f is in a set of functions that are lower-bounded by g.

#### Commonly-Occurring Orders of Growth

Here are some commonly-occurring estimates listed from no growth at all to fastest growth.

- __constant time__

- __linear time__ or _proportional to_ N

- __quadratic/polynomial time__ or _proportional to_ N<sup>2</sup>

- __exponential time__ or _proportional to_ k<sup>N</sup>

- __factorial time__ or _proportional to_ N!

#### Logarithmic Algorithms

We will shortly encounter algorithms that run in time proportional to `log N` for some suitably defined `N`. Recall from algebra that the base-10 logarithm of a value is the exponent to which 10 must be raised to produce the value. It is usually abbreviated as log<sub>10</sub>. Thus

- log<sub>10</sub> 1000 is 3 because 10<sup>3</sup> = 1000

- log<sub>10</sub> 90 is slightly less than 2 because 10<sup>2</sup> = 100

- log<sub>10</sub> 1 is 0 because 10 <sup>0</sup> = 1

In algorithms, we commonly deal with the base-2 logarithm, defined similarly.

- log<sub>2</sub> 1024 is 10 because 2<sup>10</sup> = 1024

- log<sub>2</sub> 9 is slightly more than 3 because 2<sup>3</sup> = 8

- log<sub>2</sub> 1 is 0 because 2<sup>0</sup> = 1

Another way to think of log is the following: log<sub>B</sub>N is the number of times N must be divided by B before it hits 1. For the purposes of determining orders of growth, however, the log base, B, actually doesn't make a difference because, by the change of base formula, we know that any logarithm of N is within a constant factor of any other logarithm of N. We usually express a logarithmic algorithm as simply `log N` as a result.

Algorithms for which the running time is logarithmic are those where processing discards a large proportion of values in each iterations. The binary search algorithm we encountered a few weeks back (in the "guess a number" game) is an example. In each iteration, the algorithm discards half the possible values for the searched-for number, repeatedly dividing the size of the problem by 2 until there is only one value left.

For example, say you started with a range of 1024 numbers in the number guessing game. Each time you would discard half of the numbers so that each round would have the following numbers under consideration:

| Round # | Numbers left |
|---------|--------------|
| 1       | 1024         |
| 2       | 512          |
| 3       | 256          |
| 4       | 128          |
| 5       | 64           |
| 6       | 32           |
| 7       | 16           |
| 8       | 8            |
| 9       | 4            |
| 10      | 2            |
| 11      | 1            |

We know from above that log<sub>2</sub>1024 = 10 which gives us an approximation of how many rounds it will take.

We will see further applications of logarithmic behavior when we work with trees in subsequent activities.

### Modeling runtime analysis

#### A Graphical Approach to Analyzing Iteration

We've thus far defined the language of asymptotic analysis and developed some simple methods based on counting the total number of steps. However, the kind of problems we want to solve are often too complex to think of just in terms of number iterations times however much work is done per iteration.

Consider the following function, `repeatedSum`.

    long repeatedSum(int[] values) {
        int N = values.length;
        long sum = 0;
	    for (int i = 0; i < N; i++) {
            for (int j = i; j < N; j++) {
                sum += values[j];
            }
        }
        return sum;
    }

In `repeatedSum`, we're given an array of `values` of length N. We want to take the repeated sum over the array as defined by the following sequence of `j`'s.

> 0, 1, 2, 3, ... , N-1
> 1, 2, 3, 4, ... , N-1
> 2, 3, 4, 5, ... , N-1

Notice that each time, the number of elements, or the iterations of `j`, being added is reduced by 1. While in the first iteration, we sum over all N elements, in the second iteration, we only sum over N-1 elements. This pattern continues until the outer loop, `i`, has incremented all the way to N.

One possible approach to this problem is to draw a bar graph to visualize how much work is being done for each iteration of `i`. We can represent this by plotting the values of `i` across the X-axis of the graph and the number of steps for each corresponding value of `i` across the Y-axis of the graph.

<amp-img width="960" height="720" layout="responsive" alt="Empty plot" src="empty_plot.png"></amp-img>

Now, let's plot the amount of work being done on the first iteration of `i` where `i = 0`. If we examine this iteration alone, we just need to measure the amount of work done by the `j` loop. In this case, the `j` loop does work proportional to N steps as the loop starts at 0, increments by 1, and only terminates when `j = N`.

How about the next iteration of `i`? The loop starts at 1 now instead of 0 but still terminates at N. In this case, the `j` loop is proportional to N-1 steps. The next loop, then, is proportional to N-2 steps.

<amp-img width="960" height="720" layout="responsive" alt="Partial linear plot" src="partial_linear_plot.png"></amp-img>

We can start to see a pattern forming. As `i` increases by 1, the amount of work done on each corresponding `j` loop decreases by 1. As `i` approaches N, the number of steps in the `j` loop approaches 0. In the final iteration, `i = N-1`, the `j` loop performs work proportional to 1 step.

<amp-img width="960" height="720" layout="responsive" alt="Extrapolated linear plot" src="extrapolated_linear_plot.png"></amp-img>

We've now roughly measured each loop proportional to some number of steps. Each independent bar represents the amount of work any one iteration of `i` will perform. The runtime of the entire function `repeatedSum` then is the sum of all the bars, or simply the area underneath the line.

<amp-img width="960" height="720" layout="responsive" alt="Complete linear plot" src="complete_linear_plot.png"></amp-img>

The problem is now reduced to finding the area of a triangle with a base of N and height of also N. Thus, the runtime of `repeatedSum` is in __Θ(N<sup>2</sup>)__.

We can verify this result mathematically by noticing that the sequence can be described by the following summation: 1 + 2 + 3 + ... + N = N * (N + 1) / 2 or roughly N<sup>2</sup>/2 which is in __Θ(N<sup>2</sup>)__.

#### Tree Recursion

Now that we've learned how to use a bar graph to represent the runtime of an iterative function, let's try the technique out on a recursive function, `mitosis`.

    int mitosis(int N) {
        if (N == 1) {
            return 1;
        }
        return mitosis(N / 2) + mitosis(N / 2);
    }

Let's start by trying to map each N over the x-axis like we did before and try to see how much work is done for each call to the function. The conditional contributes a constant amount of work to each call. But notice that in our return statement, we make two recursive calls to `mitosis`. How do we represent the runtime for these calls? We know that each call to `mitosis` does a constant amount of work evaluating the conditional base case but it's much more difficult to model exactly how much work each recursive call will do. While a bar graph is a very useful way of representing the runtime of iterative functions, it's not always the right tool for recursive functions.

Instead, let's try another strategy: drawing call trees. Like the graphical approach we used for iteration earlier, the _call tree_ will reduce the complexity of the problem and allow us to find the overall runtime of the program on large values of N by taking the tree recursion out of the problem. Consider the call tree for `fib` below.

    int fib(int N) {
        if (N <= 1) {
            return 1;
        }
        return fib(n - 1) + fib(n - 2);
    }

<amp-img width="960" height="720" layout="responsive" alt="Fibonacci tree" src="fib_tree.png"></amp-img>

At the _root_ of the tree, we make our first call to `fib(n)`. The recursive calls to `fib(n - 1)` and `fib(n - 2)` are modeled as the two _children_ of the root node. We say that this tree has a _branching factor_ of two as each node contains two children. It takes a constant number of instructions to evaluate the conditional, addition operator, and the return statement as denoted by the `1`.

We can see this pattern occurs for all nodes in the tree: each node performs the same constant number of operations if we don't consider recursive calls. If we can come up with a scheme to count all the nodes, then we can simply multiply by the constant number of operations to find the overall runtime of `fib`.

Remember that the number of nodes in a tree is calculated as the branching factor, _k_, raised to the height of the tree, _h_, or __k<sup>h</sup>__. Since the branching factor is 2 and the height is N, `fib` is in __O(2<sup>N</sup>)__. There's a small but significant difference between big-Oh and big-Θ in this problem as the runtime for `fib` is not exactly Θ(2<sup>N</sup>) as given by the tight bound, Θ, but rather only only upper-bounded by O(2<sup>N</sup>). Notice that the call tree is actually imbalanced as the left edge contains N nodes but the right edge contains only N/2 nodes. We describe this runtime as Θ(1.618<sup>N</sup>) which is within O(2<sup>N</sup>) but not within Θ(2<sup>N</sup>).

Now, back to `mitosis`. The problem is setup just like `fib` except instead of decrementing N by 1 or 2, we now divide N in half each time. Each node performs a constant amount of work but also makes two recursive calls to `mitosis(N / 2)`.

<amp-img width="960" height="720" layout="responsive" alt="N-time tree" src="n_tree.png"></amp-img>

Like before, we want to identify both the branching factor and the height of the tree. In this case, the branching factor is 2 like before. Recall that the series N, N/2, ... , 4, 2, 1 contains log<sub>2</sub> N elements since, if we start at N and break the problem down in half each time, it will take us approximately log<sub>2</sub> N steps to completely reduce down to 1.

Plugging into the formula, we get __2<sup>log<sub>2</sub>N</sup>__ nodes which simplifies to __N__. Therefore, N nodes performing a constant amount of work each will give us an overall runtime in __O(N)__.

### Conclusion

#### Summary

In this section, we learned about three different techniques for analyzing the runtime of program.

1. First, we tried to estimate the runtime efficiency of a program by __timing it__. But we found that the results weren't always the same between different computers or even running at different times.

2. Second, we developed the method of __counting steps__ as a deterministic way of calculating the algorithmic complexity of a program. This works well, but it can be challenging to get the exact instruction count. Oftentimes, we don't need exact constants or lower-order terms since, in the long-run, the size of the input, N, is the most significant factor in the runtime of a program.

3. Third, we learned how to __estimate__ the efficiency of an algorithm using proportionality and __orders of growth__.

    - Big-Ο describes an _upper bound_ for an algorithm's runtime.

    - Big-Ω describes a _lower bound_ for an algorithm's runtime.

    - Big-Θ describes a _tight bound_ for an algorithm's runtime.

In the final section, we applied what we learned about counting steps, estimation, and orders of growth to model algorithmic analysis for larger problems. Two techniques, _graphs_ and _call trees_, helped us break down challenging problems into smaller pieces that we could analyze individually.

#### Practical Tips

1. Before attempting to calculate a function's runtime, first try to understand what the function does.

2. Try some small sample inputs to get a better intuition of what the function's runtime is like. What is the function doing with the input? How does the runtime change as the input size increases? Can you spot any 'gotchas' in the code that might invalidate our findings for larger inputs?

3. Try to lower bound and upper bound the function runtime given what you know about how the function works. This is a good sanity check for your later observations.

4. If the function is recursive, draw a call tree to map out the recursive calls. This breaks the problem down into smaller parts that we can analyze individually. Once each part of the tree has been analyzed, we can then reassemble all the parts to determine the overall runtime of the function.

5. If the function has a complicated loop, draw a bar graph to map out how much work the body of the loop executes for each iteration.

#### Useful Formulas

- 1 + 2 + 3 + ... + N is in __Θ(N<sup>2</sup>)__

- There are __N__ terms in the sequence 1, 2, 3, ... , N while the sum of the terms is in __Θ(N<sup>2</sup>)__

- 1 + 2 + 4 + ... + N is in __Θ(N)__

- There are __log<sub>2</sub>(N)__ terms in the sequence 1, 2, 4, ... , N while the sum of the terms is in __Θ(N)__

- The number of nodes in a tree, N, is __k<sup>h</sup>__ where k is the _branching factor_ and h is the _height_ of the tree

- All logarithms are proportional to each other by the Change of Base formula.

It's worth spending a little time proving each of these to yourself with a visual model!
