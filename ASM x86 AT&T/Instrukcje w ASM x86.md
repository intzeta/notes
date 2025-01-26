- `movl source, destination` - Kopiuje wartość
- `int $0x80` - Wywołuje przerwanie systemowa (syscall)
- `cmpl $0, %eax` - `%eflags` rejestr
- `pushl %eax` - Umieszcza wartość z rejestru lub pamięci na stosie
- `popl %eax` - Pobiera wartość ze stosu, usuwa ją z niego i zapisuje wartość do rejestru lub pamięci
- 
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

#### Ogólna postać odwołań do adresów pamięci

`addressOrOffset(%baseOrOffset, %index, multiplier)`

**Gdzie:**
- `addressOrOffset`, `multiplier` - Constant
- `%baseOrOffset`, `%index` - Rejestry

Jeżeli nie ma jakiegoś elementu, jest zastąpiony jako 0.

**Tryb natychmiastowy ($)** - Znak dolar przed np. `movl $1, ...` jedynką oznacza, że chcemy użyć trybu natychmiastowego (**[[CPU - Procesor#Metody dostępu do danych|Dostęp do danych]]**). Bez znaku dolara użylibyśmy adresowania bezpośredniego, załadowując co kolwiek będące pod adresem 1.

**Adresowanie indeksowe** - `movl beginningAdress(, %index, wordSize), ...`
Na przykład: `movl arr(, %edi, 4), %eax` - Zaczynając od pamięci `arr` + indeks z rejestru `%edi` * `wordSize` rozmiar w bajtach np. dla `.long` (4 bajty). Skonstruowana w taka sposób instrukcja, bez `%baseOrOffset`, użyje adresowanie indeksowego.

**Adresowanie bezpośrednie** - Użycie tylko `addressOrOffset` spowoduje załadowanie wartości na podanym adresie. Na przykład:

```
.section .data
	y: .long 1
	
.section .text
	movl y, %eax
	...
```

Spowoduje załadowanie wartości `1` z adresu `y` do rejestru `%eax`.

**Adresowanie pośrednie** - Ładuję wartość z adresu wskazanego przez rejestr. Na przykład:

```
movl (%eax), %ebx
```

Jeżeli rejestr `%eax` posiadał by adres, moglibyśmy przenieść wartość spod tego adresu do rejestru `%ebx`.

**Adresowanie z bazowym wskaźnikiem** - 