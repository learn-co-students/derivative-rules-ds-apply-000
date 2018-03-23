
# Rules for calculating derivative 

### Learning Objectives

* Understand the rules for taking the derivative of each term
* Understand how to take the derivative of a function 

### Introduction 

From previous lessons, you know that the derivative is the instantaneous rate of change of a function.  We said that the derivative of a function at a certain point is just the slope of the function at that point.  And to calculate that slope of the function at a given point, we make $\Delta x$ value smaller and smaller to approach a change of zero, and see what our $ \Delta f/\Delta x $ converges upon.

For example, we saw the following table: 

| $ \Delta x $        | $ \Delta f/\Delta x $|
| ------------- |:-------------:|
| .1      | -171,000      |
| .01 | -179,100     |
| .001 | -179,910      |
| .0001 | -179,991      |


This convergance around one number is called the **limit **.  And we can describe what we see in the above table as the expression: 


 $$ f'(x) = \lim_{\Delta x\to0} \frac{\Delta f}{\Delta x} = -180,000  $$.

We read this as the limit of $\Delta f / \Delta x $ -- that is the number $\Delta f / \Delta x $ approaches -- as  $ \Delta x $ approaches zero is -180,000.  So, in general our definition of the derivative is:

$$ f'(x) = \lim_{\Delta x\to0} \frac{\Delta f}{\Delta x}  = \lim_{h\to0} \frac{f(x + h) - f(x)}{h} $$

### Our rules for calculating the derivative

So far, we have calculated the derivative by changing our delta as reflected in the table above, and seeing the convergance.  However, mathematicians have given us shortcuts to calculate the derivative, and that is what we'll learn about here.  

##### The power rule

The first rule for us to learn is the power rule.  The power rule states is expressed as the following.  Given the following:

$$f(x) = x^r $$

Then, the derivative, $f'(x)$ is: 
$$ f'(x) = r*x^{r-1} $$

This says that if a variable, $x$, is raised to a exponent $r$, then the derivative of that function is the exponent $r$ multiplied by the variable, with the variable raised to one minus the original exponent.  Let's start by trying this with our original function for calculating the derivative, $f(x) = 3*x $.

Remember that we originally calculated the derivative with our formula: 

$$ f'(x) = \lim_{h\to0} \frac{f(x + h) - f(x)}{h} $$

$$ f'(4) = \lim_{h\to0} \frac{f(4 + h) - f(4)}{h} = 3 $$

$$ f'(8) = \lim_{h\to0} \frac{f(8 + h) - f(8)}{h} = 3 $$

We saw that our rate of change of the function $f(x) = 3x $ was always 3.

![](./derivative-3x.png)

Now let's see how this works with our power rule: 

$$f(x) = 3*x = 3*x^{1} $$

Now applying our rule that for a function with 

$$f(x) = x^r $$ 

$$ f'(x) = r*x^{r-1} $$ 

we see that in this case $r = 1$.  So applying our power rule we have: 

$$f'(x) = r*3*x^{r-1} = 1*3*x^{1-1} = 3*x^{0} = 3 $$

Great!  This is aligns with what our graph shows, as well as our calculation using the original definition of the derivative, $\lim_{\Delta x\to0} \frac{\Delta y}{\Delta x}$ .

### Another example

Now, let's apply the power rule with another example to make sure that we have the hang of it. 

$$f(x) = x^2 $$

$$f'(x) = 2*x^{2-1} = 2*x^1 = 2*x $$

Think about what our calculation for $f'(x)$ is saying about our function.  It says, for our function $f(x) = x^2$, a small change in $x$ produces an increase in $f(x) $ equal to 2 times the $ x $ value.  Ok, now let's try to use our power rule to calculate $f'(x)$ at specific values of $x$.  

Our rule says that $ f'(x) = 2*x $, so when 

$ x = 2$ then $f'(2) = 2*2 = 4 $


And when $ x = 10 $, then $ f'(10) = 2*10 = 20$. 

We won't prove the power rule here.  But hopefully you can see that it does seem to fit our graph of the function $f(x) = x^2$.  Let's take a look.

![](./derivative-x2.png)

It seems reasonable that the slope of the line tangent to a curve is $2*x$.  So our power rule for derivatives looks good.

##### The constant factor rule

Believe it or not, we've already made use of the constant factor rule.  The constant factor addresses how to take the derivative of a function multiplied by a constant. 

So in the above example, we our function of $f(x) = 3*x$.  Now, the derivative of that function

$$f'(x) = 3 * \frac{\Delta f}{\Delta x} $$

Applying the power rule, we know that $ \frac{\Delta f}{\Delta x}x^1 = x^{1-1} = 1 $, so we have: 

$$f'(x) = 3 * \frac{\Delta f}{\Delta x}x = 3*1 = 3$$

In the general case, we can say, consider the function $a*f(x)$ where $a$ is a constant (that is, is a number and not a variable).  Then $$\frac{\Delta f}{\Delta x}(a*f(x)) = a * \frac{\Delta f}{\Delta x}*f(x) $$  

Now, don't let the fancy equations above confuse you.  The rule simply says if a variable is multiplied by a constant (i.e. a number), then to take the derivative of that term, apply the power rule to the variable and multiply the variable by that same constant.

So given the function: 

$$f(x) = 2x^2 $$
$$f'(x) = 2*\frac{\Delta f}{\Delta x} x^{2} = 2*2*x^{2-1} = 4x^1 = 4x $$

That's the constant factor rule in action.

##### The addition rule

So far all of our functions have only had one term.  Remember that a term is a constant or variable that is separated by a plus or minus sign.  So the function, $f(x)$ below has three terms:
    
$ f(x) = 4x^3 - x^2 + 3x $

Ok, so to take a derivative of a function that has multiple terms, simply take the derivative of each of the terms individually.  So for the function above, $ f'(x) = 12x^2 - 2x + 3  $.  Do you see what we did there, we simply applied our previous rules to each of the terms individually and continued to add or subtract the terms accordingly.

### The chain rule

Ok, now let's talk about the chain rule.  Imagine that we would like to take the derivative of the following function:

$$f(x) = (3 + x^2 + 2x )^2 $$ 

Doing something like that can be pretting tricky right off the bat.  Lucky for us, we can use the chain rule.  The chain rule is essentially a trick that can be applied when our functions get complicated.  The first step is using functional composition to break our function down. Ok, let's do it.

$$g(x) = (3 + x^2 + 2x)$$
$$f(g(x)) = g(x)^2$$

So now note that $f(x) = f(g(x))$.  So our new question is to find the derivative of that latter function, $f'(g(x))$.  Sounds impossible, you say?

The chain rule allows us to answer just this question.  Remember, taking a derivative means changing a variable $x$ a little, and seeing the change in the output.  The chain rule allows us to solve the problem of seeing the change in output when our function does not **directly** depend on that changing variable, but depends on **a function ** that depends on a variable.  

So here $f(g(x) $ does not directly depend on $x$.  Instead it depends on the fucntion $g(x)$ which depends on $x$.  Ok, enough talk let's see the rule.

 $f'(g(x)) = \frac{\Delta f}{\Delta g}f(g)*\frac{\Delta f}{\Delta x}g(x)$.  Yes it's a mouthful, but it's not so bad in practice.

### Applying the chain rule

Let's apply our chain rule step by step to the function by taking the derivative $f'(x) $ where:

$$g(x) = (3 + x^2 + 2x)$$
$$f(g(x)) = g(x)^2$$

Remember our chain rule is: $f'(g(x)) = \frac{\Delta f}{\Delta g}f(g)*\frac{\Delta f}{\Delta x}g(x)$

* First we take the derivative $\frac{\Delta g}{\Delta x}g(x) = g'(x) = 2x + 2$.
* Then, we take the derivative $\frac{\Delta f}{\Delta g}f(g(x))$ where $f(g(x)) = (g(x))^2 $.

This is how we evaluate that second derivative.  $\frac{\Delta f}{\Delta g}f(g(x)) = 2 * (g(x))^1 =  2 * g(x)$ 

The reason why is because to take that second derivative $\frac{\Delta f}{\Delta g}f(g(x))$, means how does the output of $f(g(x))$ change as we nudge **the function** $g(x)$.  This means that we can just treat the entire function $g(x)$ as a variable, and use our power rule.  

Ok, now we have solved our two derivatives.  Let's plug these derivatives back into our chain rule of $f'(g(x)) = \frac{\Delta f}{\Delta g}f(g)*\frac{\Delta f}{\Delta x}g(x)$.

Doing so we have $$f'(g(x)) = 2*g(x)*(2x + 2) = 2*(3 + x^2 + 2x)*(2x + 2) $$

Leaving our equation there is fine.  We've done enough math for one lesson.  Hopefully, you see how using the chain rule allows us to break a complicated function up into two, and simply apply the rule to calculate the derivative.   

### Summary

In this section we saw a different way for calculating the derivative.  The derivative of a function at a given point is still the instantaneous rate of change of that function at that point. Now we have three rules that allow us to calculate our derivative.  The most tricky of these is the power rule, which says that if $f(x) = x^r$, then $ f'(x) = r * b^{r-1} $.

Using our derivative rules, we can now calculate the derivative across the entire function.  So the derivative of $f(x) = 3x $ is always 3, and the derivative of $f(x) = x^2 $ is $f(x) = 2x $.  Then to evaluate our derivative at a specific value of $x$ we simply plug that value of $x$ into our derivative, so when $f'(x) = 2x$, then $f'(2) = 2*2$.  

Finally we saw how the chain rule allows us to break a complicated function up into two, and simply apply the rule of $f'(g(x)) = \frac{\Delta f}{\Delta g}f(g)*\frac{\Delta f}{\Delta x}g(x)$.


```python

```
