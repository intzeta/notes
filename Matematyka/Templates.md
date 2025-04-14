$\big[\begin{smallmatrix} \ x \ \\ \ y \ \end{smallmatrix}\big]$

$\begin{bmatrix} \ x \ \\ \ y \ \end{bmatrix}$


```tikz

\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[xmin=-5,xmax=5,ymin=-5,ymax=5,axis lines=middle, xtick={-10,...,10},ytick={-10,...,10}, xlabel=$x$, ylabel=$y$]
    \addplot[samples=250, black] {x^2};
    \node[anchor=west, black] at (axis cs:0,0) {$$};
\end{axis}
\end{tikzpicture}
\end{document}
```
