**Undirected Graph (Graf Nieskierowany)** - Graf nie posiadający określonego kierunku pomiędzy wierzchołkami.

Niech $G$ będzie grafem (nieskierowanym) składającym się z dwóch zbiorów: $V$ oraz $E$, przy czym $V$ jest niepustym zbiorem, którego elementy nazywane są wierzchołkami, a $E$ jest rodziną dwuelementowych podzbiorów zbioru wierzchołków $V$, zwanych krawędziami: $E \subseteq \{\{u,v\} \mid u, v \in V\}$. Zbiory $V$, $E$ nie muszą być skończone.

![[Pasted image 20250626122509.png | 600]]
**Directed Graph - Digraf (Graf Skierowany)** - Graf w którym krawędzie mają kierunek, np. $(u, v)$ to krawędź z $u$ do $v$.

Niech $G$ będzie grafem (skierowanym) składającym się z dwóch zbiorów: $V$ i $A$, przy czym $V$ jest niepustym zbiorem, którego elementy nazywane są wierzchołkami, a $A$ jest rodziną par uporządkowanych elementów zbioru $V$, zwanych krawędziami. Kolejność wierzchołków w parze wyznacza kierunek krawędzi. W przypadku pary $(u, v)$, krawędź zaczyna się na wierzchołku $u$ a kończy na wierzchołku $v$. 
![[Pasted image 20250626123440.png | 600]]
**Graph with Weight (Grafy z wagami)** - Graf któremu wierzchołka lub krawędzią można przepisać etykiety, służące do przechowywania dodatkowej informacji. Na przykład odległość między wierzchołkami.

Jeżeli jest to graf z wagami na krawędziach najczęściej dodaje się dodatkowy element do pary - $(u, v, w)$, gdzie $w$ oznacza wartość wagi.