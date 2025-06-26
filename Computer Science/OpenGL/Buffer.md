Pozwala na szybki i efektywny odczyt danych w GPU.

```
GLuint buffer;
glGenBuffers(GLsizei n, GLuint *buffer);
glBindBuffer(GLenum target, GLuint buffer);
glBufferData(GLenum target, GLsizeiptr, const void *, GLenum usage);
```

gdzie:
- `GLsizei` - To ilość bufforów (W tym przypadku ile chcemy wygenerować) 
- `GLsizeiptr` - Ilość bajtów

Na początku dostaje on własne ID, potem jest on tworzony i na końcu kopiowane są do niego dane.

`GLenum usage`:
- `GL_STREAM_DRAW` - Dane są ustawione tylko raz i używane maksymalnie kilka razy
- `GL_STATIC_DRAW` - Dane są ustawiane tylko raz, ale używane są wiele razy
- `GL_DYNAMIC_DRAW` - Dane się zmieniają i używane są kilka razy

Jakoż iż, shader pozwala nam definiować dane wejściowe w postaci atrybutów. Trzeba określić jak OpenGL powinno interpretować dane przed renderowaniem (przykład dla $\triangle$):

```
vec3 vertices[] = {
  {-0.8f, -0.4f, 0.0f},
  {0.0f, 0.8f, 0.0f},
  {0.8f, -0.4f, 0.0f},
};

/* Jak OpenGL powinnien intepretować buffer wierzchołków */
glVertexAttribPointer(0, 3, GL_FLOAT, GL_FALSE, 3 * sizeof(float), (void*)0);
glEnableVertexAttribArray(0);
```

Dla funkcji `glVertexAttribPointer`:
- Pozycja atrybutu (Pozycja była zdefiniowana w shaderze). 
- Rozmiar atrybutu (vec3 czyli 3 wartości)
- Typ danych
- Czy dane są znormalizowane
- Rozmiar pomiędzy atrybutami (Stride).
- Offset gdzie zaczynają się dane

Dla `glEnableVertexAttribArray`:
- Pozycja atrybutu (Pozycja była zdefiniowana w shaderze)

![[vertex_attributes.png]]