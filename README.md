# GetNextLine
A function that allocates a line every time a next line is found until EOF :D

## ✅ usage
Include the header in your program
and then call like:
```c
char	*line;
int	fd = open("somerandomfile.txt", "r");

while (get_next_line(fd, &line) > 0) {
  printf("%s\n", line);
  free(line);
  }
```

### ❗ note
- get_next_line returns **the amount of bytes read** unless eof is reached in which case it returns **0** or an error occurred then **-1** is returned

### 💤 code
**prototype**
```c
int get_next_line(int fd, char **line);
```
