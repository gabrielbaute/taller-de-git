# Inicio de sesión en Git

Para iniciar sesión en git, abrimos la terminal bash integrada y tipeamos:

```
$ git init
```
Este comando inicializará git y creara, en un primer momento, un repositorio vacío en el directorio en donde estemos ubicado. El término "git" nos indica que ingresaremos un comando de Git, mientras que "init" inicializa Git en ese directorio. Para iniciar sesión, debemos configurar git con un nombre de usuario y un correo:

```
$ git config --global user.name "username"
$ git config --global user.email "usermail@example.com"
```
El término "config" indica que vamos a ingresar una configuración de git. Dicha configuración se guardará en el archivo ".gitconfig" que se encuentra en el directorio raíz del usuario en el sistema operativo. En ese archivo podemos consultar las configuraciones que hemos hecho.

El término "--global" nos indica que es una configuración global, es decir que se establecerá para todo el equipo. Siempre que se realice un "commit" o un "push", se realizará con ese usuario y correo. Al hacerlo de esta manera, se simplifica el trabajo a unos pocos comandos. Sin embargo, si solo se quiere tener esa identidad en un repositorio o directorio en específico, se puede omitir el término "--global", con lo que las identidades quedarán establecidas solo en el directorio donde se inició la sesión.