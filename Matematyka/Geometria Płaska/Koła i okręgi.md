W zależności od położenia koła i prostej, wyznacza się $3$ rodzaje położenia:

**Rozłączne** występują wtedy gdy odległość między prostą a środkiem okręgu jest większa od promienia, czyli $d > r$.

```tikz
\begin{document}
\begin{tikzpicture}
	\def\radius{1.0}
	\def\ABangle{-15.0}
	\def\CDangle{15.0}
	\def\Ax{-1.0}
	\def\Ay{\radius}
	\def\Bx{4.0}
	\def\By{\radius}
	
	\def\Cx{-1.0}
	\def\Cy{-\radius}
	\def\Dx{4.0}
	\def\Dy{-\radius}

	% Środek koła
	\coordinate (O) at (0,0);

	% Dwie proste |AB| i |CD| od koła obrócone o dany kąt ABangle, CDangle.
	\coordinate (A) at ({\Ax * cos(\ABangle) - \Ay * sin(\ABangle)}, {\Ax * sin(\ABangle) + \Ay * cos(\ABangle)});
	\coordinate (B) at ({\Bx * cos(\ABangle) - \By * sin(\ABangle)}, {\Bx * sin(\ABangle) + \By * cos(\ABangle)});
	\coordinate (C) at ({\Cx * cos(\CDangle) - \Cy * sin(\CDangle)}, {\Cx * sin(\CDangle) + \Cy * cos(\CDangle)});
	\coordinate (D) at ({\Dx * cos(\CDangle) - \Dy * sin(\CDangle)}, {\Dx * sin(\CDangle) + \Dy * cos(\CDangle)});

	% Promienie, długości stycznych
	\coordinate (E) at ({-\radius * sin(\ABangle)}, {\radius * cos(\ABangle)});
	\coordinate (F) at ({\radius * sin(\CDangle)}, {-\radius * cos(\CDangle)});

	\draw[black, thick] (O) circle (\radius);
	\filldraw[black, thick] (O) circle (0.02);
	\draw[black, thick] (A) -- (B);
	\draw[black, thick] (C) -- (D);

	\draw[black, thick] (E) circle (0.02);
	\draw[black, thick] (F) circle (0.02);

	\draw[black, thick] (O) -- (E);
	\draw[black, thick] (O) -- (F);
\end{tikzpicture}
\end{document}
```
