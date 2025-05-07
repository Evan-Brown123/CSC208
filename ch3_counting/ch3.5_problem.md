## Problem

Using the digits 2 through 7, find the number of different 5-digit numbers such that:

1. Digits cannot be repeated and must be written in **increasing** order.  
   *(Increasing means strictly increasing. For example, the digits of 134 are increasing, but the digits of 133 are not.)*

2. Digits **can be repeated** and must be written in **non-decreasing** order.  
   *(Now the digits don’t need to be strictly increasing; 133 has digits non-decreasing.)*

---

## Solution

Let the digit set be:  
$\{2, 3, 4, 5, 6, 7\}$  
This gives us 6 possible digits to work with.

---

### Part 1: Strictly Increasing Digits (No Repeats)

I choose 5 **distinct** digits from 6 and arranging them in increasing order.  
There is only **one** way to arrange any set of distinct digits in increasing order.

So, the number of such numbers is:

$$
\binom{6}{5} = \frac{6!}{5!(6 - 5)!} 
= \frac{6!}{5! \cdot 1!} 
= \frac{6 \times 5 \times 4 \times 3 \times 2 \times 1}{(5 \times 4 \times 3 \times 2 \times 1)(1)} 
= \frac{720}{120} = 6
$$

---

### Part 2: Non-Decreasing Digits (Repeats Allowed)

I chose 5 digits from $\{2, 3, 4, 5, 6, 7\}$ **with repetition allowed** in **non-decreasing** order.

This is a "stars and bars" problem from the chapter: the number of multisets of size $r = 5$ from $n = 6$ elements.

This is the number of non-negative integer solutions to:

$$
x_2 + x_3 + x_4 + x_5 + x_6 + x_7 = 5
$$

The formula is:

$$
\binom{n + k - 1}{k - 1}
$$

where $n = 5$ (number of digits to choose), and $k = 6$ (distinct digits):

$$
\binom{5 + 6 - 1}{6 - 1} = \binom{10}{5}
= \frac{10!}{5! \cdot 5!}
= \frac{10 \times 9 \times 8 \times 7 \times 6}{5 \times 4 \times 3 \times 2 \times 1}
= \frac{30240}{120} = 252
$$

---

## Final Answers:

- **Strictly increasing (no repeats):** $\boxed{6}$
- **Non-decreasing (repeats allowed):** $\boxed{252}$
