# Infix and Postfix
In mathematics, we write equations in `Infix` notation. The operators ($+$, $-$, $\cdot$, $\div$) come in the middle of the equation.</br>
E.g. $(67 + 2) \cdot (16 - 4)$

`Postfix` notation (Reverse Polish Notation) is an alternative way to write
equations to increase its readability for our computers. The operators come at
the end of the equation.</br>
E.g. If we were to write this `infix` equation $A+B$ in `postfix`, it would
look like this: $A B +$

### A few  examples
---
| Infix | Postfix |
| ----- | ------- |
| $(7+16)\cdot(12+5)$ | $7\;16+\;12\;5 + \cdot$ |
| $\frac{(3+7)\cdot(4+3)}{5}$ | $3\; 7+\;4\;3+\cdot\;5\;\div$ |

## Solving a Postfix Equation
An operator is applied to two operanders, as in two numbers or variables.
Let's take a look at this simple postfix equation $4\; 2\; 9+\cdot$</br>
The first operator that appears in this equation is "$+$". This applies to the 
two operanders directly to the left of the operator. So, we would firstly add
$2$ and $9$, resulting in $2+9=11$.</br>
The next operander is "$\cdot$". We can imagine an updated version of our equation:
$4\; 11\;\cdot$. Just as before, the operator is applied to the two operanders 
directly to the left of it, resulting in $4\cdot11=44$.

</br>

## Infix to Postfix Using \<stack>
We will base this on Frode's code in [eks_05_InfixTilPostfix.cpp](https://frh.folk.ntnu.no/algmet/eksempler/eks_05_InfixTilPostfix.cpp).

<em>Note: underscore ( _ ) symbolizes when the stack is blank/empty!</em>

Infix &emsp;&rarr; $(( A + B) \cdot ( C + D ))$</br>
Postfix &rarr; $A B + C D + \cdot$</br>
<b>Operator stack:</b></br>
&emsp;&emsp;&emsp;$+$</br>
_ $+$ _ $\cdot$ $\cdot$ $\cdot$ _

</br>

## Solving Postfix Equations Using \<stack>