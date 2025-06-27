```tikz
\usepackage{pgfplots, tikz}
\usetikzlibrary{angles, quotes, calc}
\begin{document}
\begin{tikzpicture}
	\coordinate (A) at (0, 0);
	\coordinate (B) at (6, 0);
	\coordinate (C) at (6, 4);

	\draw[black, very thick]
		(A) -- node[pos = 0.5, below] {$a$}
		(B) -- node[pos = 0.5, right] {$b$}
		(C) -- node[pos = 0.5, above left] {$c$}
		cycle;
	
	\draw[black, thick]
		pic["$\theta$", draw=black, angle radius = 10mm, angle eccentricity=0.75] {angle=B--A--C};

	\draw (B) -- ++(-0.3, 0) -- ++(0, 0.3) -- ++(0.3, 0);
  
\end{tikzpicture}
\end{document}
```

Na rysunku powyżej został przedstawiony $\triangle$ prostokątny. Opiszemy funkcje trygonometryczne:
$$

\begin{align}
	\sin \theta &= \frac{b}{c} \\
	\cos \theta &= \frac{a}{c} \\
	\tg \theta &= \frac{b}{a} \\
	\ctg \theta &= \frac{a}{b} \\
\end{align}
$$
Z następujących wzorów i definicji można wywnioskować:
$$
\begin{align}
	\sin^2 \theta + \cos^2 \theta = 1 \\
	\tg \theta \cdot \ctg \theta = 1 \\
	\tg \theta = \frac{\sin \theta}{\cos \theta} \\
	\ctg \theta = \frac{\cos \theta}{\sin \theta}
\end{align}
$$
Z wykresu funkcji sinus i cosinus, można odczytać że:
$$
\begin{align}
	\sin\left(90^\circ - \theta \right) &= \cos \theta \\
	\cos\left(90^\circ - \theta \right) &= \sin \theta \\
	\tg\left(90^\circ - \theta \right) &= \ctg \theta \\
	\ctg\left(90^\circ - \theta \right) &= \tg \theta \\
\end{align}
$$

---

#Trygonometria