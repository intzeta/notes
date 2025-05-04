#Dowody 
###### Przypuszczenie 1.
Załóżmy, że $n \in \mathbb{Z}$, $n > 1$ i do tego $n$ nie jest liczba pierwszą. To wtedy $2^n - 1$ również nie jest liczbą pierwszą.

###### Udowodnienie przypuszczenia 1.
Ponieważ $n$ nie jest liczbą pierwszą, istnieją liczby całkowite dodatnie $a$ i $b$ takie, że $a < n$, $b < n$ i $n = ab$. 

Zatem niech $x = 2^b-1$ i $y = 1 + 2^b + 2^{2b} + \dots + 2^{\left(a - 1\right)b}$. Więc 
$$
\begin{align}
xy &= \left(2^b - 1\right) \cdot \left(1 + 2^b + 2^{2b} + \dots + 2^{\left(a - 1\right)b}\right) \\
   &= 2^b \cdot \left(1 + 2^b + 2^{2b} + \dots + 2^{\left(a - 1\right)b}\right) - \left(1 + 2^b + 2^{2b} + \dots + 2^{\left(a-1\right)b}\right) \\
   &= \left(2^b + 2^{2b} + 2^{3b} + \dots + 2^{ab}\right) - \left(1 + 2^b + 2^{2b} + \dots + 2^{\left(a-  1\right)b}\right) \\
   &= 2^{ab} - 1 \\
   &= 2^n - 1
\end{align}
$$