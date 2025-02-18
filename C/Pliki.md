## Informacje ogólne

`FILE *` - Obiekt posiadający informacje do kontroli strumienia

Standardowe strumienie:
- `stdin` - standard input
- `stdout` - standard output
- `stderr` - standard error

## Funkcje 

`FILE *fopen(const char *name, const char *mode)` - Otwiera plik, strumień. Metody otwarcia pliku to: "r", "w", "a" (Read, Write, Append). W razie błędu zwraca `NULL`, w innym przypadku wskaźnik do pliku.

`int fclose(FILE *fp)` - Odwrotność `fopen`, zwalnia wskaźnik `fp` i do tego czyści buffer.

`int getc(FILE *fp)` - Odczytuje znak z pliku, strumienia.

`int putc(int c, FILE *fp)` - Zapisuje znak do pliku, zwraca zapisany znak

`char *fgets(char *line, int maxline, FILE *fp)` - Odczytuje następną linie (wraz z `'\n'`) do tablicy char. Odczytuje maksymalnie `maxline - 1`, z powodu `'\0'`. Zwraca `char *line`, a dla błędów i `EOF` zwraca `NULL`.

To samo co `printf` i `scanf` tylko, że do strumienia, pliku: 
- `int fprintf(FILE *fp, char *format, ...)`
- `int fscanf(FILE *fp, char *format, ...)`

`int ferror(FILE *fp)` - Zwraca coś innego niż 0 jeżeli pojawił się problem z strumieniem, np. kiedy zapełni się dysk. (Bardzo rzadkie)

`int feof(FILE *fp)` - Zwraca coś innego niż 0 jeżeli pojawił się `EOF`.




