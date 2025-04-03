Stworzenie nowego shadera:

```
GLuint shader = glCreateShader(GLenum type);
glShaderSource(GLuint shader, GLsizei count, const char *source, GLint *len);
glCompileShader(shader);
```

Oraz sprawdzenie czy shader poprawnie się skompilował:

```
int success;
char infoLog[512];
glGetShaderiv(shader, GL_COMPILE_STATUS, &success);
if (!success){
	glGetShaderInfoLog(shader, 512, NULL, infoLog);
	fprintf(stderr, "error: %s\n", infoLog);
}

```

### Shader Program

Shader program to obiekt który połączy kilka shaderów w jedność.

```
GLuint shaderProgram = glCreateProgram();
glAttachShader(shaderProgram, GLuint shader);
...
glLinkProgram(shaderProgram);
...
glUseProgram(shaderProgram)
// Każdy shader i wywołanie rendorowania będzie używać tego programu jako obiekt
```


Po połączeniu ich w jedność, możemy je usunąć:

```
glDeleteShader(GLuint shader);
...
```
