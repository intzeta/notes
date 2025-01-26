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

