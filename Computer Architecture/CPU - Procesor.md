Procesor odczytuje instrukcję z pamięci pojedynczo i wykonuje je, znane jest to jako cykl pobierania-wykonywania (fetch-execute cycle). Procesor zawiera następujące elementy, aby to osiągnąć:

- **Licznik programu**  - Informuje komputer, skąd pobrać następną instrukcję. Przechowuje on adres pamięci następnej instrukcji, która ma zostać wykonana.
  
- **Dekoder instrukcji**  - Ustala, co oznacza instrukcja z licznika programu. Obejmuje to, jaki proces musi zostać wykonany (dodawanie, mnożenie, przenoszenie danych etc.) i jakie lokalizacje pamięci będą zaangażowane w ten proces.
  
- **Szyna danych**  - Połączenie między procesorem a zewnętrzną pamięcią procesora.
  
- **Rejestry ogólnego przeznaczenia**  - Specjalne obszary pamięci w procesorze, gdzie wykonywane są podstawowe operacje, takie jak dodawania lub porównania. Istnieją dwa rodzaje rejestrów: ogólnego przeznaczenia i specjalnego użycia. Ze względu na ich małą ilość, większość informacji przechowywana jest w pamięci głównej, wprowadzana do rejestru w celu przetworzenia, a następnie umieszczana z powrotem do pamięci po zakończeniu przetwarzania.
  
- **Jednostka arytmetyczna i logiczna (ALU)**  - Wykonuje operacje arytmetyczne i logiczne na danych pobranych i zdekodowanych przez procesor. Wyniki są umieszczane na szynie danych i wysyłane do odpowiedniej pamięci lub rejestrów zgodnie z instrukcją.
