Wartości dla współrzędnych **x, y, z** są przechowywane jako wartości od $-1$ do $1$

Każdy wierzchołek (vertex) przechowuje dane.
Dane te są przedstawiane używając atrybutów wierzchołka (Vertex Attributes), dane te mogą być jakiekolwiek jakie chcemy

Aby zarządzać pamięcią z naszymi danymi wierzchołków, używamy ***vertex buffer object*** (VBO). Który może przechować dużą ilość wierzchołków w pamięci GPU.

**Każdy obiekt w OpenGL posiada własne ID**.
**Do danego rodzaju buffora jest przypisany tylko jeden buffer.**
**Obiekty buffora pozwalają na szybki dostęp i przechowywanie danych w GPU.**