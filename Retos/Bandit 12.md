# Bandit 12
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Primero se crea una carpeta tempotal donde trabajar, esto se hace en /tmp con #mkdir
` mkdir /tmp/Datos `

Despues  extraer los datos del hexdump en una carpeta temporal, para esto se usa #xxd con el argumento -r, que indica revert, y se hace una redirección de la salida.
` xxd -r datos.txt > /tmp/Datos/datos `

Seguidamente hay que navegar hasta la carpeta con #cd y despues para saber que tipo de fichero se ha creado se puede usar el comando #file, en este caso es un dichero de gzip, entonces se le pone la extension de gzip para evitar problemas con el #mv
` mv datos datos.gz `

Para descomprimir este fichero se usa #gzip, con el argumento -d
`gzip -d datos.gz`

El fichero que queda es de bzip2, para descomprimirlo se usa #bzip2 con el argumento -d que indica descompresión, además si se quiere conservar el originar el puede poner el argumento -k
`bzip2 datos`

De este sale otro archivo gzip, por lo que se trata de repetir de nuevo la parte de gzip, despues de esto se obtiene un fichero tar.

Para descomprimir este fichero se usa #tar con los argumentos -x para extraer y -f para especificar un fichero
`tar -xf datos`

Despues de unas pocas descompresiones más sale el fichero con la contraseña, para ir viendo que tipo de fichero es el que sale en cada descompresión, de forma que se pueda saber que herramienta usar, se usa el comando #file.
