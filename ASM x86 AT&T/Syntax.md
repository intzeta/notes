## Dyrektywa .globl

**.global, .globl** - Oznacza, że asembler nie powinien usuwać tego symbolu po zakończeniu procesu assemblera, ponieważ linker będzie go potrzebować. Np. łączenie pliku C i ASM w celu optymalizacji pliku wykonywalnego.

**\_start** - Jest specjalnym symbolem który zawsze musi być oznaczony za pomocą **.globl**, ponieważ oznacza on lokalizację rozpoczęcia programu

