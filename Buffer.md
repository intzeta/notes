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
