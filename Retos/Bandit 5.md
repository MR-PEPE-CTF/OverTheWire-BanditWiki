# Bandit 5

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable

Despues de acceder al directorio **inhere** mediante el comando #cd se usa el #find para buscar el fichero que cumpla todos los requisistos.
En concreto se puede usar:
``` find . -readable -size 1033c ! -executable ```
Donde el punto representa el directorio actual, -readable los ficheros que son human-readable, -executable los ficheros ejecutables y ! niega el ultimo parámetro. Por otra parte -size indica el tamaño que tiene que tener el fichero, en este caso como indica la c detras del número en bytes.