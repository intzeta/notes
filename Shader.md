
```
GLuint shader = glCreateShader(GLenum type);
glShaderSource(GLuint shader, GLsizei count, const char *source, GLint *len);
glCompileShader(shader);
```


```
int success;
char infoLog[512];
glGetShaderiv(shader, GL_COMPILE_STATUS, &success);
if (!success){
	glGetShaderInfoLog(shader, 512, NULL, infoLog);
	printf("ERROR::SHADER::COMPILATION_FAILED\n%s\n", infoLog);
}

```
