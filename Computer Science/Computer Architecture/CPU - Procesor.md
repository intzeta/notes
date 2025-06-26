**Procesor** - odczytuje instrukcję z pamięci pojedynczo i wykonuje je, znane jest to jako cykl pobierania-wykonywania (fetch-execute cycle). Procesor zawiera następujące elementy, aby to osiągnąć:

- **Licznik programu**  - Informuje komputer, skąd pobrać następną instrukcję. Przechowuje on adres pamięci następnej instrukcji, która ma zostać wykonana.
  
- **Dekoder instrukcji**  - Ustala, co oznacza instrukcja z licznika programu. Obejmuje to, jaki proces musi zostać wykonany (dodawanie, mnożenie, przenoszenie danych etc.) i jakie lokalizacje pamięci będą zaangażowane w ten proces.
  
- **Szyna danych**  - Połączenie między procesorem a zewnętrzną pamięcią procesora.
  
- **Rejestry ogólnego przeznaczenia**  - Specjalne obszary pamięci w procesorze, gdzie wykonywane są podstawowe operacje, takie jak dodawania lub porównania. Istnieją dwa rodzaje rejestrów: ogólnego przeznaczenia i specjalnego użycia. Ze względu na ich małą ilość, większość informacji przechowywana jest w pamięci głównej, wprowadzana do rejestru w celu przetworzenia, a następnie umieszczana z powrotem do pamięci po zakończeniu przetwarzania.
  
- **Jednostka arytmetyczna i logiczna (ALU)**  - Wykonuje operacje arytmetyczne i logiczne na danych pobranych i zdekodowanych przez procesor. Wyniki są umieszczane na szynie danych i wysyłane do odpowiedniej pamięci lub rejestrów zgodnie z instrukcją.

### Metody dostępu do danych

Procesor ma wiele sposobów na dostęp do danych, znane jako tryby adresowania. Procesor posiada następujące tryby dostępu do danych:

- **Tryb natychmiastowy** - Dane są wbudowane w instrukcję. Na przykład: zainicjowanie wartości rejestru wartością 0 poprzez umieszczenie 0 w instrukcji, zamiast podawania adresu (Immediate mode).
  
- **Adresowanie rejestrowe** - Wskazuje rejestr, a nie lokalizację w pamięci, do odczytania danych (Register addressing mode).
  
- **Adresowanie bezpośrednie** - Posiada bezpośredni adres pamięci z danymi (Direct addressing mode).
  
- **Adresowanie indeksowe** - Łączy podstawowy adres pamięci z przesunięciem zapisanym w rejestrze indeksowym. Można użyć też mnożnika indeksu, aby np. odczytywać co 4 bajty (Indexed addressing mode).
  
- **Adresowanie pośrednie** - Rejestr posiada wskaźnik do adresu pamięci z danymi (Indirect addressing mode).
  
- **Adresowanie z bazowym wskaźnikiem** -Łączy wartość w rejestrze (Base Pointer addressing mode).

