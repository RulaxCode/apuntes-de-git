 Curso git desde cero
Sistema de control de versiones para el mantenimiento eficiente y confiable de archivos.t

## Zonas de Git

1. Directorio de trabajo
2. Área de preparación
3. Directorio Git


## Flujo de trabajo básico en Git

1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiendo a tu área de preparación
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.


## Configurando Git por primera vez

```
git config --global user.name "jhon wick"
git config --global user.email john@correo.com
git config --global core.editor nano
git config --list

```

## Configuracion SSH en Windows

1. Creamos unna carpeta llamada `Llaves-ssh` en el disco `C` para evitar problemas de ruta.

2. Ejecutamos el comando `ssh-keygen -t rsa -C "mi-correo@ejemplo.com"`
El correo debe ser el mismo con el que nos registramos en Github para evitar posibles problemas. 
Dejamos el passphrase vacío y  damos enter. 
Cuando nos pida la ruta `/c/llaves-ssh/gibhub_rsa`

3. Iniciamos ssh-agent en background ejecutamos el comando `eval "$(ssh-agent -s)"`.

4. Agregamos la llave ssh generada a ssh-agent ejecutando el comando `ssh-add /c/llaves-ssh/github_rsa`.

5. Usar el comando `cat /c/llaves-ssh/gibhub_rsa.pub`.
Con este comando vemos el contenido del archivo, copiamos todo el texto que nos muestra.

6. Ir a las configuraciones de nuestro perfil de github y agregar una nueva llave ssh con el contenido  que hemos copiado de `github_rsa.pub`.

Deesde ahora podemos hacer pull y push sin que github nos este pidiendo los datos de acceso.

