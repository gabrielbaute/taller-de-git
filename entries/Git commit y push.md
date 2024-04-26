# Agregar y enviar archivos: add, commit y push

Una vez configurada nuestra cuenta de Github y el sistema local de Git, podemos comenzar a usarlo. Para ello podemos dirigirnos a cualquier proyecto que tengamos (o bien crear uno), y proceder como de costumbre hasta ahora:

```
git init
```

Esto inicializará git en nuestro proyecto, produciendo también una carpeta .git que almacenará toda la información del proyecto mientras lo estamos trackeando. De esta manera, si escribimos:

```
git status
```

Nos mostrará el estatus actual de todos los archivos en nuestro proyecto, nos dirá:

* Qué archivos están siendo trackeados y cuáles no (con una letra `U`, indicándonos que no se está registrando nada sobre ellos).
* De los archivos trackeados, cuáles han sido mnodificados (empleando para ello la letra `M`, de "modified").

## El comando `add`

Este comando nos permite agregar a la lista el archivo que hayamos indicado. Esto significa que hemos decidido "trackear" o "rastrear" el archivo o directorio. Así, podemos escribir:

```
git add nombre-del-archivo
```

Sin embargo, si contamos con demasiados archivos, no es nada eficiente escribir el comando por cada uno de los archivos o ficheros que tengamos, por ello empleamos:

```
git add .
```

Lo que automáticamente agregará a todos los archivos del directorio donde nos encontremos a la lista de archivos trackeados de o hacia la rama `origin/main`. Para saber si un archivo o fichero ha sigo incorporado, lo notaremos al ver que junto a su nombre su estatus cambió de `U` a `A`, de "added", agregado.

## El comando `commit`

El `commit` es como realizar una fotografía, es el punto en el que queremos guardar el proyecto como una "versión", incluso como un punto de restauración. Para ello, deberemos haber tenido listos los archivos con el comando `git add`. La sintaxis sería:

```
git commit -m "comentario entre comillas"
```

El término `commit` se refiere a la acción que vamos a realizar, realizaremos un commit. El `-m` indica un comentario. Debemos agregar un comentario, puesto que los commit registran puntos a los que podemos volver en el tiempo, po9r lo que es útil identificar en el comentario lo que distingue esa etapa del código. Estos comentarios serán visibles en el historial de Github, por lo que también notificarás a los demás colaboradores qué has cambiado en el código.

## El comando `git push`

Con este comando, podemos enviar los cmabios a los que ya hemos hecho un commit hacia un repositorio remoto, como el de github. Habitualmente hacemos:

```
git push -u origin main
```

Este comando ya ha sido explicado en [secciones anteriores](./Vincular%20un%20repositorio%20remoto). También en dicha sección se explicó que, habiendo empleado este comando la primera vez, en las siguientes ocasiones sólo es necesario emplear:

```
git push
```