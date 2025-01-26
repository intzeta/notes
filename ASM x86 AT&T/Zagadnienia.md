## Dyrektywa .globl

**.global, .globl** - Oznacza, że asembler nie powinien usuwać tego symbolu po zakończeniu procesu assemblera, ponieważ linker będzie go potrzebować. Np. łączenie pliku C i ASM w celu optymalizacji pliku wykonywalnego.

**\_start** - Jest specjalnym symbolem który zawsze musi być oznaczony za pomocą **.globl**, ponieważ oznacza on lokalizację rozpoczęcia programu

## Stack

**Stack** znajduje się na najwyższych adresach pamięci i rośnie w dół. Na stos można dodać element za pomocą instrukcji `pushl`, albo można usunąć za pomocą `popl`. Rejestr `%esp` zawsze będzie wskazywał na samą górę stosu (czyli na samym dole pamięci stosu).

Jeżeli byśmy chcieli uzyskać wartość z góry stosu, ale jej nie usuwać można użyć adresowania pośredniego ([[Instrukcje w ASM x86#Metody dostępu do danych - ** CPU - Procesor Metody dostępu do danych Dostęp do danych **|Metody dostępu do danych]]).

```
movl (%esp), %eax
```

Do rejestru `%eax` trafi wartość znajdująca się na samej górze stosu. Natomiast jeżeli byśmy chcieli przetrzymać wskaźnik użyjemy adresowanie rejestrowego.

```
movl %esp, %eax
```

Jeżeli byśmy chcieli uzyskać wartość poniżej góry stosu, użyjemy adresowania z bazowym wskaźnikiem (Base Pointer). Do rejestru `%esp` zostanie dodane 4:

```
movl 4(%esp), %eax
```

## Funkcje

Przed wykonaniem funkcji, program wprowadza wszystkie parametry funkcji w odwrotnej kolejności. Następnie instrukcją `call` wskazuje, którą funkcję ma wykonać.
Następnie umieszcza `return address` na stos, i zmienia rejestr `%eip` aby wskazywał na początek funkcji.

```
Parametr n
...
Parametr 2
Paramatr 1
Return Address (%esp)
```

Potem trzeba zapisać rejestr wskaźnika bazowego `%ebp` za pomocą `pushl %ebp`. Używany jest do dostępu do parametrów i zmiennych lokalnych funkcji. Następnie wskaźnik `%esp` jest kopiowany do `%ebp` za pomocą `movl %esp, %ebp`. Przez co, `%ebp` staje się stałym odniesieniem do ramki stosu (stack frame). `%ebp` pozwala zawsze uzyskać dostęp do parametrów funkcji, zmiennych lokalnych i adresu powrotu (return address).

```
Parametr n
...
Parametr 2
Paramatr 1
Return Address
%ebp (%esp) i (%ebp)
```

Następnie funkcje rezerwuje miejsce na stosie dla zmiennych lokalnych. Wykonuje się to poprzez przemieszczenie wskaźnika stosu. Na przykład jeżeli potrzebujemy dwóch zmiennych lokalnych 4 bajtowych, zrobimy to za pomocą instrukcji: 

```
subl $8, %esp
```

```
Parametr n         n * 4 + 4(%ebp)
...
Parametr 2         12(%ebp)
Paramatr 1         8(%ebp)
Return Address     4(%ebp)
%ebp (%ebp)
Zmienna lokalna 1 -4(%ebp)
Zmienna lokalna 2 -8(%ebp) i %esp
```

Rejestr `%ebp` został specjalnie zrobiony w tym celu.


```
movl %ebp, %esp
popl %ebp
ret
```