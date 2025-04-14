Wektor to uporządkowana para liczb. Jeżeli wektor nie ma początku, to jest on wektorem swobodnym, oznaczony jako $\vec{v}$. Jeżeli natomiast wektor ma początek, to jest on wektorem zaczepionym, oznaczony jako $\vec{AB}$. 

Niech będą dane punkty $A = \left(x_1,y_1\right)$ i $B = \left(x_2, y_2\right)$, to współrzędne wektora $\vec{AB}$ określa wzór:$$\vec{AB} = \begin{bmatrix} \ x_2 - x_1 \ \\ \ y_2 - y_1 \ \end{bmatrix}$$Wektory mają również przedstawienie geometryczne na układzie współrzędnych, przykłady dla wektorów $\big[\begin{smallmatrix} \ 3 \ \\ \ 2 \ \end{smallmatrix}\big]$ i $\big[\begin{smallmatrix} \ -1.5 \ \\ \ -2.5 \ \end{smallmatrix}\big]$:

```tikz

\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[xmin=-4,xmax=4,ymin=-3,ymax=3,axis lines=middle, xtick={-1.5,3},ytick={-2.5,2}, xlabel=$x$, ylabel=$y$]
    \addplot[samples=250, ultra thick, red, ->] coordinates {
	    (0,0)
	    (3,2)
    };
    \addplot[samples=250, ultra thick, blue, ->] coordinates {
	    (0,0)
	    (-1.5,-2.5)
    };
    \node[anchor=west, black] at (axis cs:0,0) {$$};
\end{axis}
\end{tikzpicture}
\end{document}
```

Długość wektora $\vec{v}$ i $\vec{AB}$ można zapisać następująco:$$
\begin{align}
\left|\vec{v}\right| &= \sqrt{w^2_x + w^2_y} \\
\left|\vec{AB}\right| &= \sqrt{\left(x_2-x_1\right)^2+\left(y_2-y_1\right)^2}
\end{align}$$
Sumę, różnicę i iloczyn $\vec{v} = \big[\begin{smallmatrix} \ v_x \ \\ \ v_y \ \end{smallmatrix}\big]$ i $\vec{u} = \big[\begin{smallmatrix} \ u_x \ \\ \ u_y \ \end{smallmatrix}\big]$, wyraża się następującymi wzorami:$$
\begin{align}
\vec{v} + \vec{u} &= 
	\begin{bmatrix}
		\ v_x + u_x \ \\ \ v_y + u_y \ 
	\end{bmatrix}\\
\vec{v} - \vec{u} &= 
	\begin{bmatrix}
		\ v_x - u_x \ \\ \ v_y - u_y \ 
	\end{bmatrix} \\
\vec{v} \cdot s &= 
	\begin{bmatrix}
		\ v_x \cdot s \ \\ \ v_y \cdot s \ 
	\end{bmatrix}, \, s \in \mathbb{R}
\end{align}
$$