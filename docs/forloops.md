
# Table of Contents

1.  [Posts](#org9dd384c):@java:
    1.  [For Loops](#orgf02172a)
        1.  [Enter the `for` loop.](#orga4de43a)



<a id="org9dd384c"></a>

# Posts     :@java:


<a id="orgf02172a"></a>

## DONE For Loops

<p class="verse">
The purpose of this document is not to teach you `for` loops from scratch. It is intended as notes to help solidify your understanding from doing the Review Questions, attending lectures, and completing labs.<br />
</p>

A loop in Java is a way of repeating a sequence of commands without having to type it out multiple times. For example, if I wanted to print &ldquo;tick&rdquo; 5 times, I could do the following:

    System.out.println("tick");
    System.out.println("tick");
    System.out.println("tick");
    System.out.println("tick");
    System.out.println("tick");

Of course, I don&rsquo;t want to do that. What if I wanted to do it 100 times instead? Or 1000?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> Copy/pasting the line repeatedly would not be very fun at all. You might almost want to&#x2026; *write a program to do it for you!*


<a id="orga4de43a"></a>

### Enter the `for` loop.

    // Lets print "tick" 5 times!
    for (int i = 0; i < 5; i++) {
      System.out.println("tick");
    }

We immediately recognize `int i = 0;` as a way of defining a new integer variable with the value 0. `i < 5` is our *condition*, and `i++` tells us how we get from our starting state to our *condition*.

-   The loop variable &rsquo;governs&rsquo; our loop. In this case, our variable is `i`.
-   `initializer` sets the starting value for the loop variable. Here, our initializer is `int i = 0;`.
-   `condition` tells us whether we should continue executing the loop. We plan to stop at `i > 5` in this loop.
-   `update` tells us how the variable should change at the end of each *iteration*. We are increasing the value of `i` by `1` using `i++`.

Lets break this loop down a little bit.

    // We could use an integer that already exists, if we wanted to!
    int i = 0;
    for (; i < 5; i++) {
        System.out.println("tick");
    }

What if I want to go backwards?

    int i = 5;
    for (; i > 0; i--) {
        System.out.println("kcit");
    }

What if you have *oudenophobia*<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup> and really want to avoid using the number `0` in your code?

    // we don't have to start at 0!
    int i = 3214;
    for (; i < 3219; i++) {
        System.out.println("tick");
    }

Wait&#x2026; how does that work? 3219 has nothing to do with 5. Or does it?<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup> If you read the footnote at this point, you&rsquo;ll know that 3219-3214=5, which is vital information for relating the above `for` loop to the number 5.

Ok. So we are starting with some value for `i` and we are stopping when the *condition* is no longer true. In the cases we&rsquo;ve been looking at so far, the *condition*

So what if I wanted to do that 100 times now? Do I just repeat that for loop (*counts quietly for a second*) 20 times? No. Of course not. We just change the value that `i` is counting up to.

![img](./static/img/forloop1.png "A for loop, broken down. Credits: Prof Kazakova.")

<p class="verse">
Steps:<br />
0. Create an integer called `i` and set its value to `0`.<br />
1. Check if `i < limit`. If it is, continue to 2. If not, exit the loop.<br />
2. Execute the `body` of the loop. tick.<br />
3. update `i`. Here, we are adding 1 to i.<br />
1. check if `i < limit`. If it is, continue to 2. If not, exit the loop.<br />
</p>

Between the *initializer* and the *condition* we are defining a range of values for `i` to fall into. The *update* tells us how `i` will move through that range. One way to think about for loops is to draw a number line with the initial value of your loop variable, or the *start*, and the value implied by your condition, or the *finish*. You can then count how many times you would have to use the update function to get from the *start* to the *finish*. Relate that back to the counting exercises we did when we started clicker questions on for loops.


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> I am fully aware that a program that just says &ldquo;tick&rdquo; 1000 times is neither exciting to a user nor your goal as a programmer.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> *ouden* is Greek for nothing, or literally, *not one*.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> Very related to 5 in this context. 3219-3214=5.
