---
layout: page
title: Python Notional Machine
hidden: true
---

## Environment diagrams are lovable things, too!

I love environment diagrams and you should too!

At the heart of CS 61A is the idea of computational thinking. And at the core of computational thinking is a strong understanding of computation and how computers compute. It might seem tedious at first, but once you get the hang of them, environment diagrams will become your greatest companion not only on the diagramming questions but also in code-writing and in understanding how computation works in general. Practically-speaking, a lot of programming errors become much easier to spot once you've thoroughly trained yourself in the science of environment diagrams and can think through the pathways of execution.

[If you're still not pleased, Albert Wu has many more words for you.](http://albertwu.org/cs61a/notes/environments.html#preface-a-defense)

## Python reads from left to right

Seems pretty straightforward, right? That makes sense if our calls only look like `add(1, 2)`. But things get messy when we start combining multiple terms.

    add(mul(5, sub(2, 1)), 3)

So how does python read this? We go left to right, sure, but what about all the complicated calls in the argument?

Recall the three rules of evaluating an expression:
1. Evaluate operator.
2. Evaluate operands.
3. Apply the operator on the operands.

We first evaluate the **operator**, `add`, which we know to be a built-in function that can add together two numbers.

    ___
    add(mul(5, sub(2, 1)), 3)

Great, so it won’t error out immediately when we call it. The first opening parentheses signals to python that the arguments (**operands**) are coming up next. So what’s the first argument that python sees if it’s reading from left to right?

        _________________
    add(mul(5, sub(2, 1)), 3)

The entire first argument to `add` is *another* function call. We'd really, really like to just evaluate the `add` and be done with things, but we can't do that until all of the arguments have been evaluated in terms of **final values** like numbers or strings.

We first have to figure out what that call to `mul` does. For all python knows, our call to `mul` might not return a number: return `None`, do any number of weird things to the environment, or even error out and crash the program!

Fortunately, in this simple example, we know `mul` is the built-in function that multiplies numbers, so it is a valid operator for its arguments. Now let’s consider the arguments to `mul`.

            ____________
    add(mul(5, sub(2, 1)), 3)

The first argument is the integer 5, a **final value**. This is good!

The second argument is another function call. This is just like the case with `add` earlier but this time, we can't proceed with `mul` because we don’t know what this new call to `sub` does!

               _________
    add(mul(5, sub(2, 1)), 3)

Our operator, `sub`, is a function! And the operands, 2 and 1, are just integers so they’re both final values! Finally, something we can compute!

But before we get any further, let’s recap: this whole time, `add` has been waiting for `mul` to compute which has, in turn, been waiting for `sub` to compute! We haven’t even made any function calls yet because we've been waiting on the "evaluate operands" step for each of the function calls. The first function we actually call is `sub` because its arguments only consist of final values that we can work with. Let’s compute!

The first function call will be `sub(2, 1)` which returns 1. This is a **final value**, so we can plug it back into the `mul` call what was waiting for us.

The second function call will be `mul(5, 1)`. Now that we know all of `mul`’s arguments are final values, we can now compute the call to `mul`, returning 5. Then, we can plug this 5 back into the call to `add` which was waiting for the just-computed `mul`.

The third function call will be `add(5, 3)`. We just figured out that the `mul` call returned the final value, 5, so we now need to evaluate the remaining arguments. Luckily, the second argument is just the number 3, also a final value, so we don't need to perform any additional computation. Adding these two values together gives us 8, the result of the original computation.

We read python from left to right, evaluating operators first before evaluating operands. But sometimes, we may need to do a lot of other computations in order to figure out what the operators and operands really are. In this example, we had to perform several function calls in order to figure out what `add`’s first **operand** was. But in other examples, we may need to do a lot of work to evaluate the **operator**. This is particularly prevalent when *currying* with higher-order functions.

## Interpreting higher-order function calls

Let’s say we’re trying to evaluate the following code.

    def make_adder(n):
	    """Returns a function that adds N."""
	    def hof(x):
		    return n + x
	    return hof
	make_adder(mul(1, 2))(3)

What’s our first move after defining the `make_adder` function in the global frame? We learned above that python evaluates from left to right, operators first then operands, so let’s see how far that gets us!

    __________
    make_adder(mul(1, 2))(3)

The first thing we do is take a look at the operator: `make_adder` is a higher-order function that we’ve defined above. It takes in some number and returns a one-parameter function, `hof`, that does the actual work of adding both numbers together.

Next, we see an open parentheses which signals to us that the arguments will be coming up.

               _________
    make_adder(mul(1, 2))(3)

Like we demonstrated earlier, this function call to `mul(1, 2)` is not a **final value**. We must evaluate this function call before proceeding. The first function call to `mul` gives us 2 in return which is the final value we were looking for. Plugging back into `make_adder`, we can imagine the original call looks something like `make_adder(2)(3)`.

At this point, we've completely evaluated all of `make_adder`'s operands. As the second operation, we can call `make_adder(2)` which returns the higher-order function, `hof` whose parent is the `make_adder` frame. But we have not done anything with this function just yet.

To help illustrate where we’re at after calling the frame, you can think of the original call as now looking like `hof(3)`. Evaluating this as we would normally, we can open a frame for `hof` and call it with 3 as the argument. The body of `hof` tells us to add `n + x` which returns 5 in this case, the answer to the original computation.

It might seem like an awful lot of work to do such a simple computation, but it’s important that we practice all of these steps. With higher-order functions, the first function call to `make_adder(n)` should return a function which will become the new **operator** to some other argument, `x`. We’ll still have to perform the same steps of inspecting `make_adder` and its arguments before opening the `make_adder` frame, but there’s an added layer of complexity as `make_adder`’s `hof` is the **operator** for another set of arguments.
