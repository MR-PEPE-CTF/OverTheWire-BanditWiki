The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

Para resolver este apartado se puede visualizar el documento ordenandolo, porque según esta nota del man de #uniq no detecta las lineas repetidas si no son adyacentes.
*Note:  'uniq'  does not detect repeated lines unless they are adjacent.  You may want to sort the input first, or use 'sort -u' without 'uniq'*

Despues mediante una tubería pasar el resultado al comando #uniq con el argumento -u, que muestra solo las lineas únicas, quedando de la forma:
``` sort data.txt | uniq -u```
