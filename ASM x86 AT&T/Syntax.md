## Dyrektywa .globl

**.global, .globl** - Oznacza, że asembler nie powinien usuwać tego symbolu po assemblerze, ponieważ linker będzie go potrzebować. Np. łączenie pliku C i ASM w celu optymalizacji pliku wykonywalnego.

**\_start** - Jest specjalnym symbolem który zawsze musi być oznaczony za pomocą **.globl** ponieważ oznacza on lokalizację rozpoczęcia programu

labels
## Instrukcje itp.

`movl beginningAdress(, %indexRegister, wordSize), ...
Na przykład:
`movl arr(, %edi, 4), %eax` - Zaczynając od pamięci `arr` + indeks z rejestru `%edi` * `wordSize` rozmiar w bajtach np. dla `.long` (4 bajty).


