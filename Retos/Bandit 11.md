# Bandit 11
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

Primero hay que leer el documento mediante #cat y despues con #tr modificar la salida
``` cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' ```

Para convertir de la "a" a la "z", se empieza por las 13 primeras letras, es decir de la "a" a la "m", convirtiendalas en de la "n" a la "z" y después las 13 últimas,  es decir de la "n" a la "z", convirtiendalas en de la "a" a la "m". Esto también hay que hacerlo con las mayúsculas.