# Limits and Derivatives Practice Problems

#### A. Are the following true or false? If true, explain why. If false, give a counter-example.

1. If $\displaystyle\lim_{x\to a} f(x)$ does not exist, then $f$ is undefined at the point $x=a$.
1. If $f$ and $g$ are continuous on their domains which contain $a$, then $\displaystyle\lim_{x\to a} f(x) + g(x) = f(a) + g(a).$
1. If a function is continuous at $a$, then $f'(a)$ exists.

#### B. Evaluate the following limits (or say that the limit DNE):

1. $\displaystyle\lim_{x\to 3}\frac{x^2-9}{x+3}$
1. $\displaystyle\lim_{x\to 3}\frac{x^2-9
   }{x-3}$
1. $\displaystyle\lim_{x\to \pi/2}\frac{\cot(x)}{\cos(x)}$
1. $\displaystyle\lim_{x\to 0}\frac{(\cos^2(x) - 1)(x+3)}{x}$

#### C. For each function $f$, find a value of $c$ so that $f$ is continuous on $\mathbb{R}$:

1. $f(x)=\begin{cases}2x & x \leq c \\ x^2+1 & x > c.\end{cases}$
1. $f(x)=\begin{cases}2x+c & x < 2 \\ x^2 + cx +1 & x \geq 2.\end{cases}$

#### D. For each $f$, find $f'$ using the limit definition of the derivative.

1. $f(x)=\sqrt{x+4}$
1. $f(x)=2x^2 + 3x$

#### E. For each $f$, find $f'$ and $f''$ using any method you want.

1. $f(x)=3x^3-\frac{4}{x^2}$
1. $f(x)=x\sin(x)$
1. $f(x)=\frac{x^2+3}{x-4}$
1. $f(x)=x^2\cos(x)+x\tan(x)$
1. $f(x)=\sin(x)\cos(x)e^x$

#### F. When are the following functions increasing/decreasing? When are they concave up/down?

1. $f(x)=2x^2+3x$
1. $f(x)=x^3+17x^2+2$

----

## Answers (in no particular order)

- $f'(x)=e^{x}(\cos^{2}(x)+\sin(x)\cos(x)-\sin^{2}(x))$, $f''(x)=f'(x)+e^{x}\left(-4\cos\left(x\right)\sin\left(x\right)+\cos^{2}\left(x\right)-\sin^{2}\left(x\right)\right)$
- 0
- $f'(x)=4x + 3$
- 6
- increasing: $x>\frac{-3}{4}$, decreasing: $x<\frac{-3}{4}$, concave up: all of $\R$, concave down: nowhere
- $f'(x)=\frac{1}{2}(x+4)^{-1/2}$
- False (e.g. $f(x)=\frac{x^2}{x}$ is not defined at 0, but $\lim_{x\to 0}f(x) = 0$)
- $f'(x)=\sin(x) + x\cos(x)$, $f''(x)=\cos(x) + \cos(x) -x\sin(x)$
- 1
- True (Since $f$ and $g$ are continuous, so is $f+g$. Then by the def. of continuity, $\lim_{x\to a} f(x)+g(x)=f(a) + g(a)$)
- $f'(x)=9x^2+8x^{-3}$, $f''(x)=18x-24x^{-4}$
- 0
- $-1$
- False ($f(x)=|x|$ is continuous at $0$, but $f'(0)$ DNE)
- $f'(x)=\frac{(2x)(x-4)-(x^2+3)}{(x-4)^2}$, $f''(x)=\frac{(2x-8)(x^2-8x+16)-(x^2-8x-3)(2x-8)}{(x^2-8x+16)^2}$
- 1
- increasing: $x>0$ or $x<\frac{-3}{4}$, decreasing: $\frac{-3}{4}<x<0$, concave up: $x>\frac{-17}{3}$, concave down: $x<\frac{-17}{3}$
- $f'(x)=2x\cos(x)-x^2\sin(x)+\tan(x)+x\sec^2(x)$, $f''(x)=\left(2-x^{2}\right)\cos\left(x\right)-4x\sin\left(x\right)+\sec^{2}\left(x\right)\left(2+2x\tan\left(x\right)\right)$

