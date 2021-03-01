

# What's limit?

## The Basic Idea

(The history of limit?)

As we know,calculus wouldn't exist without the concept of limits.



Although it's tricky to define a limit properly, an intuitive understanding of limit will be enough to tackle differentiation and integration.



Here are a function ${f}$ and a point on the x-axis, which we'll call ${a}$. Let's think about this weird question: **what does ${f(x)}$ look like when ${x}$ is really really close to ${a}$, but not equal to ${a}$ ?** 



Here's an example showing this question:
$$
f(x)=
\begin{cases} 
x-1,\ \ x \ne 2\\ 
3\ \ \ \ \ \ \ , \ \  x=2
\end{cases}
$$

(the graph of this function)



$\lim\limits_{x\to 2}f(x)$ is irrelevant to the value of $f(2)$. It's only the values of $f(x)$ where $x$ is **close to** 2, not actually **at** 2, which matter. So, $\lim\limits_{x\to 2}f(x)=1$, even though $f(2)=3$.



Note: $\lim\limits_{x\to 2}f(x)$ isn't actually a function of $x$ .The equation $\lim\limits_{x\to 2}f(x)=1$ means that $f(x)$ is close to 1 when $x$ is close to 2. We could actually replace $x$ by any other letter and this would still be true. For example, we can also write $\lim\limits_{q\to 2}f(q)=1$, $\lim\limits_{b\to 2}f(b)=1$, $\lim\limits_{z\to 2}f(z)=1$,and even $\lim\limits_{\alpha\to 2}f(\alpha)=1$, and so on until we run out letters and symbols. 



The variable $x$ is just a *dummy variable*, which is a temporary label for some quantity that is (in this case) getting very close to $2$. Also, when we work out the value of the limit, the answer cannot include the dummy variable.

## Left-Hand and Right-Hand Limits

Let's describe the behavior of $h(x)$ near $x=3$ :

![image-20210228150034691](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228150034691.png)

What happens when we approach $x=3$ from the left? Imagine that we climb the "hill" from the far left of this picture, then when our horizontal position is close to 3, our height is close to 1. Everything to the right of $x=3$ (the other part of the function), including $x=3$ (a sheer drop and a weird litter ledge floating in space above us), is irrelevant. So, *the left-hand limit* of $h(x)$ at $x=3$ is equal to $1$.



On the other hand, if we walking leftward from the right-hand side of the picture, we will see that the *right-hand limit* of $h(x)$ at $x=3$ is equal to $-2$. Now everything to the left of $x=3$, including $x=3$ itself, is irrelevant.



We can summarize our findings from above by writing:

$\lim\limits_{x\to3^{-}}h(x)=1$ The little minus sign after the $3$ means that the limit is a left-hand limit. The reason of writing the subscript is that this limit only involves values of $x$ less than $3$.

$\lim\limits_{x\to3^+}h(x)=-2$  The litter plus sign after the $3$ means that the limit is a right-hand limit. So we only need to consider what happens when we add a little bit onto $3$.

(So,why illustrate limits like this?  Why does the subscript + means left-hand limit?)

Note: write the minus or plus sign **after** the $3$, not before it! $\lim\limits_{x\to-3}h(x)$ refers to the regular two-sided limit of $h(x)$ at $x=-3$.

# The Existence of Limits

Limits don't always exist. The regular two-sided limit an $x=a$ exists when **both** left-hand and right-hand limits at $x=a$ exist **and are equal to each other**! In other words, all three limit—two-sided, left-hand, and right-hand—are the same. In other words, $\lim\limits_{x\to a^-}f(x)=L$    **and**    $\lim\limits_{x\to a^+}f(x)=L$  is the same thing as   $\lim\limits_{x\to a}f(x)=L$ .

If the left-hand and right-hand limits are not equal, then the two-sided limit does not exist. We'd write $\lim\limits_{x \to a}f(x)$ does not exist, or just write $\lim\limits_{x\to a}f(x)$ DNE. 

The case in the function h mentioned above is an good example—$\lim\limits_{x \to3}h(x)$ DNE, since $\lim\limits_{x\to3^-}h(x)=1$ and $\lim\limits_{x\to3^+}h(x)=-2$.



Here is a more dramatic example, which involves infinity. Consider the graph of $f(x)=1/x$ :

![image-20210228173657199](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228173657199.png)

When $x$ is positive and close to $0$, $f(x)$ gets larger and larger (larger than anything we can imagine).We say that the limit is infinity, and write
$$
\lim\limits_{x\to0^+}\frac{1}{x}=\infty
$$
Similarly, the left-hand limit here is $-\infty$, since $f(x)$ gets arbitrarily more and more negative as $x$ slides upward to $0$. That is,
$$
\lim\limits_{x\to0^-}\frac{1}{x}=-\infty
$$
The two-sided limit certainly doesn't exist, since the left-hand and right-hand limits are different.



On the other hand, consider the graph of the function $g$ defined by $g(x)=1/x^2$:

![image-20210228175029131](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228175029131.png)

Both the left-hand and right-hand limits at $x=0$ are $\infty$ ,so $\lim\limits_{x\to0}1/x^2=\infty$ as well.

By the way, we now have a formal definition of the term "vertical asymptote":

> "$f$ has a vertical asymptote at $x=a$" means that at least one of $\lim\limits_{x\to a^+}f(x)$ and $\lim\limits_{x\to a^-}f(x)$ is equal to $\infty$ or $-\infty$ .

It's possible that even a left-hand or right-hand limit fails to exist. Let's meet the funky function $g$ defined by $g(x)=sin(1/x)$.  Since $sin(x)$ has zeros at the values $x=\pi,2\pi,3\pi,\cdots$, then $sin(1/x)$ will have zeros when $\pi,2\pi,3\pi,\cdots$, which means that  $1/x=\frac{1}{\pi},\frac{1}{2\pi}\frac{1}{3\pi},\cdots$ These numbers are the x-intercepts of $sin(1/x)$. On the number line, this is what they look like:

![image-20210228181833575](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228181833575.png)

As we see, they are really bunch up as we get close to $0$. Just as $sin(x)$, $sin(1/x)$ goes up to $1$ or down to $-1$ between every x-intercept:

![image-20210228182644156](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228182644156.png)

It oscillates infinitely often between $1$ and $-1$, faster and faster as we move from the right toward $x=0$.There is no vertical asymptote, but there's still no limit—the function doesn't tend toward any one number as $x$ goes to $0$ from the right. So, we say that $\lim\limits_{x\to0^+}sin(1/x)$ DNE.

## Limits at $\infty$ and $-\infty$ 

We've concentrated on the behavior of a function near a point $x=a$. There is one more type of limit —$\lim\limits_{x\to \infty}f(x)=L$ which means that $f(x)$ gets really close, and stays close, to the value L when $x$ is large. This limit indicates that the graph of $f$ has a right-hand horizontal asymptote. 



Similarly, $\lim\limits_{x\to -\infty}f(x)=L$ means that $f(x)$ gets extremely close, and stays close, to L when $x$ gets more and more negative (or more precisely, -$x$ gets larger and larger). This of course corresponds to the graph of $y=f(x)$ having a left-hand horizontal asymptote. 



Here is the formal definition of the term "horizontal asymptote":

> "$f$ has a right-hand horizontal asymptote at $y=L$" means that $\lim\limits_{x\to \infty}f(X)=L$.
>
> "$f$ has a left-hand horizontal asymptote at $y=M$" means that $\lim\limits_{x\to -\infty}f(X)=M$. 



Of course, something like $y=x^2$ doesn't have any horizontal asymptotes, since $\lim\limits_{x\to \infty}x^2=\infty$

Alternatively, the limit may not even exist. For example, $sin(x)$ just oscillating back and forth between $1$ and $-1$ when x gets larger and larger. There's no horizontal asymptote, nor does the function wander off to $\infty$ or $-\infty$; the best way we can do is to say that $\lim\limits_{x\to \infty}sin(x)$ DNE.

Let's return to the function $f$ given by $f(x)=sin(1/x)$. 

![image-20210228195356491](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228195356491.png)

$f$ is an odd function, because $f(-x)=sin(\frac{1}{-x})=sin(-\frac{1}{x})=-sin(\frac{1}{x})=-f(x)$. Since $sin(0)=0$, it should be true that $sin(1/x)$ is very close to 0 (1/x is very close to 0 when x is large). 

## Large numbers and small numbers

As far as we know, 1,000,000,000,000 is a large number. But how about -1,000,000,000,000? Perhaps controversially, we should think of this as a large negative number rather than a small number. An example of a small number would be 0,0000000001, while -0.0000000001 is  a small negative number. To the contrary, we're not going to think of $0$ itself is being small: it's just $0$. So we have a informal definition of large numbers and small numbers:

> A number is *large* if its absolute value is a really big number.
>
> A number is *small* if it is really close to $0$ but not actually equal to $0$

But what do "really big" and "really close to $0$" mean precisely? Well, consider the limit equation $\lim\limits_{x\to \infty}f(x)=L$, which means that when $x$ is a large enough number, the value of $f(x)$ is almost L. But how large is "large enough" ? It depends on how close to L we want $f(x)$ to be. Look at the following picture:

![image-20210228202030948](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228202030948.png)

 $f(10)$ is nowhere near L, while $f(x)$ is pretty close to L when $x$ is at least $100$, so any number above $100$ would be large. 

And then look at the next picture:

![image-20210228202311379](C:\Users\86133\AppData\Roaming\Typora\typora-user-images\image-20210228202311379.png)

In this picture, $f(100)$ is far away from $L$, so now $100$ isn't large enough. We need to go up to about $200$ in this case.



After all, the term "large" has to be taken in context, relative to some function or limit. So we can't just pick number like 1,000,000,000,000 and say that it's always large, because a function might wander around until 5,000,000,000,000 before it starts getting close to its horizontal asymptote. 

A number can't really be near $\infty$ in the literal sense, and this term only makes sense in the context of limit as $x\to \infty$. To be honest, 1,000,000,000,000 is too smaller than $10^{10}$, and $10^{10}$ is too smaller than $10^{100}$.

All mentioned above also apply to limits as $x\to -\infty$. And similarly, the term "small" (near $0$) is also depend on the context of some function or limit.



