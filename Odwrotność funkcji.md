Jest to funkcja która "odwraca funkcję".

Niech $f : X \rightarrow Y$, to wtedy $f^{-1} : Y \rightarrow X$ oznacza odwrotność funkcji $f$.
$$
\begin{align}
	f(x) &= y \\
	f^{-1}(y) &= x
\end{align}
$$
Funkcja $g$ to odwrotność funkcji $f$ jeżeli:
$$
\begin{align}
	g(f(x)) &= x \quad \forall x \in D_f \\
	f(g(x)) &= x \quad \forall x \in D_g
\end{align}
$$
Warto zaznaczyć, że dla każdego $x$ musi być inna wartość $y$, np. $f(x)=2x^2-9$ nie posiada odwrotność bo dla każdej wartości $y \neq 9$, $f^{-1}$ przyjmuje 2 wartości dla $y$.
$