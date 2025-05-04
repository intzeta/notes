#### Przesunięcie przez wektor

Przesunięcie wykresu funkcji najłatwiej jest zapisać za pomocą wektora, np. $\vec{v} = \big[\begin{smallmatrix} \ 1\ \\ \ 5 \ \end{smallmatrix}\big]$. Wektor ten oznacza przesunięcie funkcji o 1 jednostkę w prawo i 5 do góry. Na wykresie poniżej przedstawiono przykładowe przesunięcie funkcji:

```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[xmin=-3.5,xmax=3.5,ymin=-0.5,ymax=11.5,axis lines=middle, xtick={-4,-3,...,4},ytick={0,5,10}, xlabel=$x$, ylabel=$y$]
    \addplot[samples=250, dashed, black] {x^2};
    \node[anchor=west, black] at (axis cs:-2.6,8.5) {$y = x^2$};
    \addplot[samples=250, ultra thick, red] {(x-1)^2 + 5};
    \node[anchor=west, black] at (axis cs:0,8.5) {$y = (x-1)^2 + 3$};
\end{axis}
\end{tikzpicture}
\end{document}
```
Ogólny wzór przesunięcia funkcji przez wektor $\vec{v} = \big[\begin{smallmatrix} \ p \ \\ \ q \ \end{smallmatrix}\big]$ to:
$$g(x) = f(x - p) + q$$
#### Przekształcenie symetralne względem OX

Dana jest funkcja $y = f(x)$, odbicie symetralnym tej funkcji względem osi OX jest funkcja $y = -f(x)$.

```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[xmin = -0.5, xmax = 6.5, ymin = -3.5, ymax = 3.5, axis lines = middle, xlabel=$x$, ylabel=$y$, xtick={-10, ..., 10}, ytick={-10, ..., 10}]

\addplot[samples = 250, ultra thick, red, domain = 0:6.5] {sqrt(x)};
\node[black] at (axis cs:3.0,2.5) {$y = \sqrt{x}$};
\addplot[samples = 250, ultra thick, blue, domain = 0:6.5] {-sqrt(x)};
\node[black] at (axis cs:3.0,-2.5) {$y = -\sqrt{x}$};
	
\end{axis}
\end{tikzpicture}
\end{document}
```

#### Przekształcenie symetralne względem OY

Dane jest funkcja $y = f(x)$, odbicie symetralne tej funkcji względem osi OY jest funkcja $y = f(-x)$.

```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[xmin = -3.5, xmax = 3.5, ymin = -1.5, ymax = 3.5, xtick = {-4, ..., 4}, ytick = {0, ..., 4}, xlabel = $x$, ylabel = $y$, axis lines=middle]

\addplot[samples = 250, domain=-4:4, ultra thick, red] {(x-1)^2};
\node[black] at (axis cs:-2,-1) {$y = \left(-x-1\right)^2$};
\addplot[samples = 250, domain=-4:4, ultra thick, blue] {(-x-1)^2};
\node[black] at (axis cs:2,-1) {$y = \left(x-1\right)^2$};
	
\end{axis}
\end{tikzpicture}
\end{document}
```
#Funkcje 