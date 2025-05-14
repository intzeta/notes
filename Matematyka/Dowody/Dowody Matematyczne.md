#Dowody 
#### Przypuszczenie 1.
Załóżmy, że $n \in \mathbb{Z}$, $n > 1$ i do tego $n$ nie jest liczba pierwszą. To wtedy $2^n - 1$ również nie jest liczbą pierwszą.
#### Udowodnienie przypuszczenia 1.
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

---

#### Przypuszczenie 2.
Niech $a$, $b$ i $c$ to liczby całkowite oraz $x$, $y$ i $z$ to liczby rzeczywiste różnymi od $0$, które spełniają poniższe równania: $$\frac{xy}{x + y} = a \quad \text{i} \quad \frac{xz}{x+z} = b \quad \text{i} \quad \frac{yz}{y + z} = c$$
To wtedy $x$ jest liczbą wymierną.
#### Udowodnienie przypuszczenia 2.
Rozłóżmy podane wyrażenia na formy łatwiejsze. $$
\begin{align*}
	\frac{xy}{x + y} = a \Rightarrow \frac{x + y}{xy} = \frac{1}{a} \Rightarrow \frac{1}{x} + \frac{1}{y} = \frac{1}{a} \\
	\frac{xz}{x + z} = b \Rightarrow \frac{x + z}{xz} = \frac{1}{b} \Rightarrow \frac{1}{x} + \frac{1}{z} = \frac{1}{b} \\
	\frac{yz}{y + z} = c \Rightarrow \frac{y + z}{yz} = \frac{1}{c} \Rightarrow \frac{1}{y} + \frac{1}{z} = \frac{1}{c} \\
\end{align*}
$$
Po przekształceniu podanych wyrażeń, możemy znaleźć wartość $x$.
$$
\begin{align}
	\frac{2}{x} + \frac{2}{y} + \frac{2}{z} &= \frac{1}{a} + \frac{1}{b} + \frac{1}{c} \\
	\frac{2}{x} &= \frac{1}{a} + \frac{1}{b} + \frac{1}{c} - \frac{2}{y} - \frac{2}{z} \\
	\frac{2}{x} &= \frac{1}{a} + \frac{1}{b} + \frac{1}{c} - \frac{2}{c} \\
	\frac{2}{x} &= \frac{1}{a} + \frac{1}{b} - \frac{1}{c} \\
	2 &= x \cdot \left(\frac{1}{a} + \frac{1}{b} - \frac{1}{c}\right) \\
	x &= \frac{2}{\frac{1}{a} + \frac{1}{b} - \frac{1}{c}} \\
	x &= \frac{2}{\frac{bc + ac - ab}{abc}} \hspace{4em}
\end{align}
$$
Jako, że liczby $a, b, c \in \mathbb{Z}$, to $x$ jest liczbą wymierną co wynika z definicji liczb wymiernych. $\blacksquare$

---

