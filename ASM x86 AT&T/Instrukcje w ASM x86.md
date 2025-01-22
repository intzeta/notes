- `movl $1, %eax` - Kopiuje wartość
- `int $0x80` - 
- `cmpl $0, %eax` - `%eflags` rejestr
## Instrukcje skoku warunkowego i niewarunkowego

- `je` (Jump if Equal) - Przejdź, jeżeli wartości są równe
- `jg` (Jump if Greater) - Przejdź, jeżeli wartość źródłowa jest większa niż pierwsza wartość źródłowa.
- `jge` (Jump if Greater or Equal) - Przejdź, jeżeli wartość źródłowa jest większa lub równa wartości docelowej.
- `jl` (Jump if Less) - Przejdź, jeżeli wartość źródłowa jest mniejsza niż pierwsza wartość źródłowa.
- `jle` (Jump if Less or Equal) - Przejdź, jeżeli wartość źródłowa jest mniejsza lub równa wartości docelowej.

- `jmp`- Przejdź bezwarunkowo.

Quick System Call Review: To recap - Operating System features are
accessed through system calls. These are invoked by setting up the
registers in a special way and issuing the instruction `int $0x80`. Linux
knows which system call we want to access by what we stored in the `%eax` register. Each system call has other requirements as to what needs to
be stored in the other registers. System call number 1 is the exit system
call, which requires the status code to be placed in `%ebx`.


## Metody dostępu do danych - **[[CPU - Procesor#Metody dostępu do danych|Dostęp do danych]]**

**Tryb natychmiastowy ($)** - Znak dolar przed np. `movl $1, %eax` jedynką oznacza, że chcemy użyć trybu natychmiastowego (**[[CPU - Procesor#Metody dostępu do danych|Dostęp do danych]]**). Bez znaku dolara użylibyśmy adresowania bezpośredniego, załadowując co kolwiek będące pod adresem 1.

**Adresowanie indeksowe** - `movl beginningAdress(, %indexRegister, wordSize), ...
Na przykład: `movl arr(, %edi, 4), %eax` - Zaczynając od pamięci `arr` + indeks z rejestru `%edi` * `wordSize` rozmiar w bajtach np. dla `.long` (4 bajty). Skonstruowana w taka sposób instrukcja użyje adresowanie indeksowego