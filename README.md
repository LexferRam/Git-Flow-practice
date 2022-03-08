### Flujo de trabajo con gitflow 😀


1. git flow init 
2. git flow feature start nombreFeature
3. git add .
4. git commit -m "commit message"
5. git checkout develop
6. git pull origin develop
7. git flow feature finish nombreFeature
8. git push origin develop


##### El flujo general de Gitflow es el siguiente

1. Se crea una rama develop a partir de main.
2. Se crea una rama release a partir de la develop.
3. Se crean ramas feature a partir de la develop.
4. Cuando se termina una rama feature, se fusiona en la rama develop.
5. Cuando la rama release está lista, se fusiona en las ramas develop y main.
6. Si se detecta un problema en main, se crea una rama hotfix a partir de main.
6. Una vez terminada la rama hotfix, esta se fusiona tanto en develop como en main.
   

##### Guardar cambios en la GNU nano:

1. [ctrl] + [X]
2. pulsar [S]
3. Escribir mensaje y pulsar [Enter]
