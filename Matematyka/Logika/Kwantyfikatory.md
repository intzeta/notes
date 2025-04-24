### Kwantyfikator ogólny (Dla każdego)
Oznacza, że dla każdego obiektu, wartości, zmiennej itd. zachodzi dane wyrażenie, np: $\underset{x \ \in \ \mathbb{R}}{\forall}, \underset{x \ \in \ \mathbb{Z}}{\forall}, \underset{k \ \in \ \left\langle-2, \ 2\right\rangle}{\forall}, \underset{x \ \in \ \mathbb{R} \ \wedge \ x > 0}{\forall}$, etc.

Wyrażenia:$$\underset{x \ \in \ \mathbb{R}}{\forall}x^2\geq0 $$
### Kwantyfikator szczególny (Istnieje takie)
Oznacza, że istnieje przynajmniej jeden obiekt, wartość dla którego zachodzi dane wyrażenie, np: $\underset{x \ \in \ \mathbb{R}}{\exists},\underset{k \ \in \ \mathbb{Z}}{\exists}$, etc.

Wyrażenia:$$\underset{x \ \in \ \mathbb{R}}{\exists}x^2 - 4 =0 $$
### Łączność kwantyfikatorów
Można z łatwością zrozumieć dlaczego jest to prawdą, poniżej jest podany przykład wyprowadzania wzoru dla $\exists x \left(P(x) \vee Q(x)\right) = \exists x P(x) \vee \exists x Q(x)$ wiedząc że, $\forall x \left(P(x) \wedge Q(x)\right) = \forall x P(x) \wedge \forall x Q(x)$.
$$
\begin{align}
	\exists x \left(P(x) \vee Q(x)\right) &= \exists x P(x) \vee \exists x Q(x) \\ \\
	L &= \exists x\left(P(x) \vee Q(x)\right)\\
	  &= \neg\neg\exists x\left(P(x) \vee Q(x)\right)\\
	  &= \neg\forall x\left[\neg P(x) \wedge \neg Q(x)\right] \\
	  &= \neg\left[\forall x \neg P(x) \wedge \forall x\neg Q(x)\right] \\
	  &= \exists x P(x) \vee \exists x Q(x) \\ \\
	L &= R
\end{align}$$