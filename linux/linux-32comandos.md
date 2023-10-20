# Lista de Comandos Linux básicos más importantes

[1. pwd](#cl1)

[30. echo](#cl30)

[31. zip](#cl31)

[32. vi](#cl32)

<span id="cl1"></span>

## 1. Comando pwd
El comando pwd significa “directorio de trabajo de impresión” y es un comando de Linux simple pero útil. Este comando se usa para mostrar el nombre de su directorio actual, lo que puede ser útil al navegar por el sistema de archivos.

Ejemplos:
```bash
pwd
/home/usuario
```
Este es un ejemplo de la consola Terminal que puedes usar en el panel de control cPanel de Dongee.

<span id="cl2"></span>
## 2. __Comando cd__

El comando cd de Linux se usa para cambiar el directorio de trabajo actual de un usuario. Se puede usar para subir un nivel en el sistema de archivos, o se le puede dar un directorio como argumento para cambiar el directorio de trabajo.

Ejemplos:

cd

(para ir al home por defecto del usuario)

cd ..

(para devolverse o salir desde la carpeta en la que estás posicionado)

cd carpeta

cd carpeta

(para ingresar a un folder)

cd /home/usuario/public_html

(para saltar entre directorios)

<!-- 🔥 Promo para lectores
Plan de Hosting (60%) Solo lectores.

Plan especial para desarrolladores ideal para practicar comandos shell, instalar frameworks populares y comenzar tu carrera de desarrollador.
Adquirir plan Dongee 60% Off -->
<span id="cl3"></span>

## 3. Comando ls

El comando ls es una utilidad de línea de comandos que enumera el contenido de un directorio.

Se utiliza para enumerar archivos y directorios en sistemas operativos Unix y similares a Unix, incluido Linux.

El comando ls se puede utilizar con los siguientes parámetros:

* -l (lista en formato largo)

* -a (enumera todos los archivos, incluidos los ocultos)

* -t (ordenar por hora de última modificación)

* -S (ordenar por tamaño de archivo)

Ejemplos:

ls -la

(muy usado debido a que complementa dos flags completos)

ls -l

ls -lR

(Ver la lista completa de archivos dentro de carpetas)

Puedes por ejemplo usar este último combinado con el comando pipe | para filtrar por ejemplo:

ls -lR |grep configuration.php

<span id="cl4"></span>

## 4. Comando cat

Cat, aunque es un comando simple en su nivel más básico, es uno de los comandos de Linux más utilizados en el sistema. Significa “concatenar” y se usa para mostrar lo que hay dentro de un archivo de texto. Solo puede usar el comando cat si conoce el nombre y la extensión del archivo que desea mostrar.

Ejemplos:
```bash
cat archivo.txt
```
(lee simplemente el archivo)cat < archivo
```bash
cat < archivo
```

(crea un nuevo archivo)

```bash
cat archivo1 archivo2 < archivo3
```

(Une dos archivos  el archivo1 y archivo2 y los envía al archivo3)

<span id="cl5"></span>

## 5. Comando cp

El comando ‘cp’ es una utilidad de línea de comandos que copia archivos. Es uno de los comandos más útiles del sistema Linux y puede copiar archivos o directorios a otro directorio. El comando cp se puede usar con los comandos ‘cp’ o ‘mv’ para mover archivos.

Ejemplos:

```bash
cp foto.jpg public_html/imagenes/
```

(copia la imagen dentro de la carpeta imagenes)

```bash
cp foto.jpg public_html/imagenes/
```

copia la imagen y si encuentra otra con el mismo nombre la reemplaza, el back slash o “\” se usa para que el comando que se ejecuta, corra de manera forzada, sin preguntas. Debes tener cuidado con este carácter.

<span id="cl6"></span>

## 6. Comando mv

El comando mv es un comando de Linux que se usa para mover y renombrar archivos y directorios.

Ejemplos:

mv foto.jpg nombrecambiado.jpg

Renombrando una imágen

mv foto.jpg carpeta/imagenes2/

Mover una imagen

<span id="cl7"></span>

## 7. __Comando mkdir__

El comando mkdir es un comando muy importante que se usa para crear directorios y subdirectorios que son una parte integral del sistema operativo Linux. Este comando solo se puede ejecutar desde la terminal y no necesita ningún argumento cuando se usa. Todo lo que necesita hacer es escribir mkdir en la terminal e inmediatamente se creará un directorio para usted.

Ejemplos:

mkdir /home/imagenes

crea una carpeta dentro de otra llamada

mkdir -pv /home/imagenes/otracarpeta/otracarpeta/yotramas

Crea una carpeta dentro de otra recursivamente

8. __Comando rmdir__

La idea detrás de este comando específico es eliminar un directorio vacío y su contenido del sistema de archivos. Para hacerlo, deberá ingresar lo siguiente:

Ejemplo:

rmdir carpeta

9. __Comando rm__

El comando rm se usa en sistemas Linux para eliminar archivos y directorios. El comando se puede personalizar con una variedad de opciones, como el indicador -r, que elimina recursivamente los archivos de un directorio determinado.

Ejemplos:%rm imagen.jpg%rm -r carpeta

rm imagen.jpg

rm -r carpeta

Borra la carpeta completamente con todo adentro

rm -fr

aquí se usa el flag f que es forzar, es decir adiós archivos sin preguntar nada 😲

10. __Comando touch__

El comando touch se usa a menudo para cambiar la marca de tiempo en un archivo. El comando touch también se puede utilizar para otros fines, el más usado es para crear un archivo vacío.

Ejemplos:

touch archivo.txt

Crea un archivo vacío llamado archivo.txt. Por ejemplo podrías crear un archivo llamado index.html para cuando acabas de crear tu hosting y aún no tienes el diseño listo, con esto haces más segura tu cuenta ya que los rastreadores y bots no podrán ver que tienes dentro de tu carpeta de archivos.

touch -t yyyymmddhhmm archivo.txt

Toma el archivo y pone la fecha en el formato año, mes, día, hora y minuto.

11. __Comando locate__

El comando de localización locate es un comando que se utiliza para buscar archivos en la computadora, la red o Internet. Este comando se puede usar en sistemas operativos similares a Unix, como Linux y Mac OS X.

El comando de localización tiene muchas opciones diferentes que se pueden usar para encontrar el archivo deseado. Por ejemplo, la opción -i buscará todos los archivos en una base de datos de índice en lugar de buscar en todos los directorios del sistema. La opción -r buscará en todos los directorios recursivamente.

El comando de localización también se puede usar para buscar texto dentro de un archivo usando expresiones regulares. Esto se hace agregando un indicador -i regexp y luego especificando lo que está tratando de encontrar con la sintaxis de regexp.

Para linux debes primero instalar mlocate ejemplo:

yum install mlocate
updatedb

Con esto ya se indexará el sistema operativo con & lo que le dices al sistema es que corra en background.

Ejemplo:

locate archivo.txt

Encuentra todos los archivos archivo.txt que estan en tu computadora.

12. __Comando grep__

grep es un comando UNIX que filtra la salida de un comando desde la entrada estándar. Se utiliza para encontrar patrones en un archivo o en el sistema.

Ejemplo:

grep texto archivo.txt

en este ejemplo grep busca en el archivo.txt todo lo que tenga la palabra “texto”

grep -i texto archivo.txt

grep busca la palabra “texto” no importa si está escrita en mayúsculas o minúsculas.

cat archivo.txt | grep textofiltro

este es uno de los usos más comunes, primero se le pasa el comando cat que lee el archivo.txt y luego extrae todas las líneas que tengan el texto “textofiltro”.

cat archivo.txt | grep -c textofiltro

en este ejemplo usa -c para contar el número de líneas que contienen la palabra textofiltro.

13. __Comando dig__

El comando dig de Linux se puede usar para consultar los registros DNS del dominio ingresando el siguiente comando: “dig domain.com”.

Ejemplo:

dig apple.com

14. __Comando df__

El comando df enumera el espacio utilizado y disponible en todos los sistemas de archivos montados. La primera columna enumera los diferentes tipos de sistemas de archivos, mientras que la segunda columna muestra cuánto espacio está disponible y la tercera columna muestra cuánto espacio está en uso.

Ejemplo:

df

df -h

el mismo comando anterior pero más legible para humanos.

15. __Comando du__

El comando du es un comando común de Unix que imprime el uso del disco de un directorio (o árbol de directorios) y el espacio total que ocupan en el disco. A menudo se usa para identificar cuánto espacio queda en las particiones de montaje.

Ejemplo:

du -sch

es un comando que listara el peso de donde estas parado

du -sch *

el mismo anterior pero mostrando el paso de cada carpeta donde estás parado.

16. __Comando head__

palabras claves: comando linux, head comando linux, ejemplos de comando head

Head es un comando de Linux que muestra las primeras líneas de un archivo.

Ejemplo:

head archivo.txt

imprimirá las primeras líneas del archivo

17. __Comando tail__

El comando tail es un comando de Unix y Linux que muestra las últimas líneas de un archivo en la salida estándar. Es lo opuesto a head, pero se puede usar en cualquier archivo sin importar el formato.
Ejemplo:

tail -f archivo.txt

imprimirá las últimas líneas del archivo, muy útil para por ejemplo ver los errores de tu archivo error_log en tu wordpress. tail -f /home/usuario/public_html/error_log con esto podrás depurar tu sitio para el error 500 fácilmente.

18. __Comando diff__

El comando diff permite al usuario encontrar las diferencias entre dos archivos. Esto puede ser muy útil para identificar cambios en el código.

Ejemplo:

diff archivo1.txt archivo2.txt

diff toma los dos archivos e imprime las diferencias entre los dos archivos.

19. __Comando tar__

El comando tar es una poderosa utilidad para archivar y extraer archivos. Puede usarlo para crear archivos, extraer o enumerar el contenido de los archivos.

Ejemplo:

tar cf archivo.tar carpeta

En este ejemplo tar toma todo el contenido de la carpeta “carpeta” y genera un archivo que puedes descargar.

tar -zcvf archivo.tar.gz carpeta

En este caso tar coma la carpeta “carpeta”, la mete en un “tar” y al mismo tiempo la comprime. Un comando super útil para comprimir todo tu sitio por ejemplo ubicado en public_html.

tar -xzvf archivo.tar.gz

Se descomprime el archivo archivo.tar.gz y dejará al final dos archivos, el archivo.

tar.gz y la carpeta “carpeta”

20. __Comando chmod__

El comando chmod se usa para cambiar los permisos de un archivo. Los permisos están representados por letras, y cada letra representa un tipo diferente de acceso.

El comando chmod se puede usar para cambiar el permiso de cualquier usuario o grupo en el archivo. El permiso para todos los demás usuarios no se cambiará.

Ejemplo:

chmod 755 archivo.jpg

aquí añadimos permisos 755 los más usados por seguridad. Establecerá el permiso para que todos los usuarios lean y ejecuten, pero no escriban

chmod 777 archivo.jpg

Esto establecerá el permiso para que todos los usuarios lean, escriban y ejecuten. No recomendado.

chmod -R 755 public_html

Se usa -R para hacerlo de manera recursiva en todos los archivos de la carpeta public_html.
21. __Comando chown

El comando tar es una poderosa utilidad para archivar y extraer archivos. Puede usarlo para crear archivos, extraer o enumerar el contenido de los archivos.
Ejemplo:
-R: esta opción cambia recursivamente la propiedad de todos los archivos y directorios en un árbol de directorios con raíz en el directorio.
-U usuario: Esta opción cambia de dueño a usuario, pero solo para este archivo o directorio.
-L: esta opción enumera todos los archivos afectados por este comando, así como sus nuevos propietarios.
-v: esta opción genera una salida detallada sobre lo que está sucediendo.

chown usuario:grupo archivo.html

chown -R usuario:grupo carpeta

aquí cambiaría a toda la carpeta los permisos del propietario.
22. __Comando ps

El comando ps es un comando de Linux que se utiliza para listar los procesos que se ejecutan en el sistema.

El comando ps toma un comodín o varios comodines como entrada y enumera todos los procesos que coinciden con esas especificaciones. También puede tomar argumentos como -a y -e para mostrar todos los procesos o solo aquellos que han finalizado respectivamente.

Ejemplo:

ps -a

Muestra los procesos que se están ejecutando en el momento. Funciona también en mac.

ps -aux

Muestra los procesos que se están ejecutando con mucho más detalle. Recuerda que puedes filtrar.

aquí usamos pipe grep para filtrar sólo procesos que tengan la palabra “palabra”.

23. __Comando kill__

El comando `kill` es una utilidad de línea de comandos de Unix que se utiliza para finalizar procesos. Se puede utilizar para eliminar procesos en ejecución, enviar señales a procesos en ejecución o finalizar todos los procesos asociados con un usuario determinado. Es muy útil cuando una aplicación se bloquea y no se cierra sola.
Ejemplo:

kill -9 12345

aquí matamos un proceso que se quedo pegado. El número del proceso se puede obtener con el comando anterior ps. Recuerda que no puedes matar algunos procesos como el de la base de datos ya que se pueden corromper los índices y perderías tus datos.

24. __Comando ping__

El comando ping es una respuesta a la necesidad de una forma simple pero efectiva de determinar si un dispositivo está en línea o no. Ping puede hacer esto enviando una solicitud de eco al dispositivo de destino y esperando una respuesta de eco.
Ejemplo:

ping google.com

viendo si google esta activo 😀 lo más común es que si no responde al ping es porque tu no tienes internet.

ping 8.8.8.8

probando una ip de un servidor popular de DNS

25. __Comando wget__

wget es una maravillosa herramienta de línea de comandos que se puede usar para descargar archivos de Internet. Tiene algunas características realmente ingeniosas, como la descarga recursiva, la configuración del agente de usuario, etc.
Ejemplo:

wget https://www.midominio.com/copiaderespaldo.tar.gz

aquí descargaremos un archivo tar.gz con nuestra copia y posteriormente podríamos usar tar -xzvf copiaderespaldo.tar.gz para descomprimirla y desentarrarla.

wget -b https://www.midominio.com/copiaderespaldo.tar.gz

wget es una navaja suiza, puedes por ejemplo bajar un archivo en segundo plano, y posteriormente verificar cualquier registro de la operación con el comando tail -f wget-log

wget -c https://www.midominio.com/copiaderespaldo.tar.gz

Si experimenta un corte de energía o pierde su conexión a Internet, su descarga puede interrumpirse. Esto puede suceder al descargar archivos grandes como videos, así que para continuar con la descarga, use la función -c.
26. __Comando uname__

El comando uname es una utilidad del sistema Linux que muestra información sobre el sistema, como el nombre del kernel, el nombre del host, el sistema operativo, la fecha de lanzamiento y la versión.
Ejemplo:

uname

27. __Comando top__

El comando superior es una aplicación de terminal que le permite ver las tareas más intensivas de la CPU que se ejecutan en su sistema. Fue diseñado para ser un visor de procesos interactivo.
Ejemplo:

top

## 28. __Comando history__

El comando de historial o history se utiliza para mostrar al usuario lo que ha hecho en el sistema. Puede enumerar el contenido del directorio, iniciar programas y más.
Ejemplo:

history

lista los comandos anteriormente digitados

history -c

elimina el histórico para evitar que sea usado en contra tuya 🙂

## 29. __Comando man__

Man es una utilidad de línea de comandos que proporciona páginas de manual completas de las herramientas de Unix. Se puede usar junto con otras herramientas y scripts para permitir que el usuario busque información sobre comandos y datos del sistema relacionados.

Ejemplo:

man wget

Puedes ver todo el manual del comando wget, son textos realmente extensos y bien completos.

<span id="cl30"></span>
## 30. __Comando echo__

Echo es una utilidad de línea de comandos que proporciona páginas de manual completas de las herramientas de Unix. Se puede usar junto con otras herramientas y scripts para permitir que el usuario busque información sobre comandos y datos del sistema relacionados.

Ejemplo:

```bash
echo Esto es un ejemplo

echo ‘Esto es un ejemplo’

echo ‘Esto es un ejemplo’ < archivo.txt
```

Aquí imprime la frase “Esto es un ejemplo” y la manda al archivo archivo.txt

<span id="cl31"></span>
## 31. __Comando zip o comando unzip__

El comando zip es un comando de Linux que comprime archivos. Este comando se puede utilizar para crear, extraer, listar y actualizar archivos zip.
Ejemplo:

zip -r archivocomprimido.zip directorio

En este ejemplo se comprime todo lo que contiene el directorio que se menciona.

zip archivocomprimido.zip archivo1 archivo2 archivo3

En este ejemplo se adiciona en el archivo comprimido.zip los archivos 1 2 y 3 esto con el fin de elegir manualmente lo que se adiciona dentro del archivo comprimido.

unzip archivocomprimido.zip

Se descomprime un archivo comprimido con carpetas y subcarpetas que contenga.

<span id="cl32"></span>
## 32. Comando vi

VI es el editor de modo texto de Linux. Es tal vez uno de los comandos más potentes en la cantidad de opciones que logra hacer. Por ejemplo, puedes abrir un archivo de código, buscar un texto, reemplazarlo o sobreescribirlo. Para muchos es ciencia espacial, pero en realidad si lo aprendes a usar estas un paso más adelante que otros administradores. Por el momento solo te enseñaremos a crear un “hello world” creando un archivo, salvando y saliendo de él.

Ejemplo:

```bash
vi archivo.txt
```

para ingresar y crear un archivo en blanco llamado archivo.txt
Ya adentro puedes pulsar la S para insertar
Escribe un “hello world”
Escribe :wq para salir
Bonus: Otros Comandos Avanzados que deberías conocer (comando ssh, sh, curl, wacht con trucos avanzados)


