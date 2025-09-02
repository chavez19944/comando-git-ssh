### Acceder con la terminal git bash
````
cd .ssh
ssh-keygen -t rsa -b 2048 -C "curso_github"
````
- asignar un nombre 
````
id_rsa_curso_github
````
- enter enter o poner un clave

### Mostrar el contenido del archivo pub
````
 cat id_rsa_curso_github.pub
````
### github

- copiar el contenido de id_rsa_curso_github.pub
- acceder a github
- en el perfil click en setting
- click en ssh ang GPG keys
-  click en new ssh key
- asignamos un titulo (id_key_curso_github)
- pegar el contenifo del archivo pub

### Cargar la clave

````
eval "$(ssh-agent -s)"
````
- ahora añade tu clave
````
ssh-add ~/.ssh/id_rsa_curso_github
````
### Verificamos
- finalmente volver a probar
````
ssh -T git@github.com
yes
````

