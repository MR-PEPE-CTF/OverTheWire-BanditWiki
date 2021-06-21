# Bandit 6
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

Para encontrar el fichero en este caso, usando el #find,  como no se sabe donde esta hay que buscar desde la raiz, representada por el simbolo /
``` find / -user bandit7 -group bandit6 -size 33c ```

Donde -user indica el usuario, -group el grupo y -size el tamaño.
Tambien se puede usar uns redicción para abrir directamente el fichero encontrado, de la forma:
``` find / -user bandit7 -group bandit6 -size 33c | xargs cat```

El resultado es:
![[bandit6.jpg]]
