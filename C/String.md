`char word[32]` - Przykładowy string w `C`.

## Funkcje <string.h>

`char *strcpy(char *s, const char *ct)` - Kopiuje string `ct` do `s` (wraz z `'\0'`), zwraca `s`.
`char *strncpy(char *s, const char *ct, size_t n)` - Kopiuje maksymalnie `n` znaków z `ct` do `s`. Jeżeli `ct` ma mniej znaków niż `n` zostanie dodany `'\0'`, w przeciwnym wypadku **nie zostanie dodany**. Zwraca `s`.

`char *strcat(char *s, const char *ct)` - Doda `ct` do końca `s`, zwraca `s`.
`char *strncat(char *s, const char *ct, size_t n)` - Doda maksymalnie `n` znaków z `ct` do `s`, zostanie dodany `'\0'`, zwraca `s`.

`int strcmp(const char *cs, const char *ct)` - Porównuje `cs` i `ct` ze sobą. Zwraca 0 jeżeli `cs == ct`, > 0 jeżeli `cs > ct`, <0 jeżeli `cs < ct`.
`int strncmp(const char *cs, const char *ct, size_t n)` - Porównuje maksymalnie znaków z `cs` do `ct`. Zwraca 0 jeżeli `cs == ct`, > 0 jeżeli cs > ct, < 0 jeżeli `cs < ct`.

`char *strchr(const char *cs, int ch)` - Zwraca wskaźnik do pierwszego pojawienia się znaku `ch` w `cs`, lub NULL jeżeli w stringu `cs` nie ma `ch`.
`char *strchr(const char *cs, int ch)` - Zwraca wskaźnik do ostatniego pojawienia się znaku `ch` w `cs`, lub NULL jeżeli w stringu `cs` nie ma `ch`.

`size_t strlen(const char *s)` - Zwraca długość `s`.


`void *memcpy(void *s, const void *ct, size_t n)` - Kopiuje `n` znaków z `ct` do `s`, zwraca `s`.
`void *memset(void *s, int ch, size_t n)` - Wstawia `ch` do pierwszych `n` znaków w `s`, zwraca `s`.