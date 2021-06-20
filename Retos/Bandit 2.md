# Bandit 2
En este caso el problema es que existe espacios en el nombre del fichero en el que se encuentra la contraseña, como los espacios son carácteres especiales que se usan como separadores causan un error, para salucionarlo tan solo es necesario escapar los espacios con el caracter  de contrabarra \\.
Quedaría de la forma: ``` cat spaces\ in\ this \filename```
