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


<https://www.atlassian.com/es/git/tutorials/comparing-workflows/gitflow-workflow>

------------------------------------------------------------------------------------------------------------------


### GitFlow: 
Es flujo de trabajo para la gestión de ramas en git, ordena qué tipo de ramas se deben configurar y cómo fusionarlas.

Éste flujo de trabajo utiliza dos ramas para registrar el historial del proyecto:
* Main: almacena el historial de publicación oficial.
* Develop: sirve como rama de integración para las funciones

Instalar GitFlow en el sistema:
- [x] brew install git-flow

**Inicializar el proyecto:**
- [x] git flow init (crear ramas para ti)

**A continuación, otros desarrolladores deberían clonar el repositorio central y crear/actualizar la rama develop:**
- [x] git checkout develop
- [x] git pull origin develop

**Crear la ramas feature que utiliza la rama develop como rama primaria:**
NOTA: Las ramas feature suelen crearse a partir de la última rama develop.
- [x] git flow feature start feature/nombreFeature

SIN gitFlow:
- [ ] git checkout develop
- [ ] git checkout -b feature_branch

 **Cuando una función está terminada, se vuelve a fusionar a develop:**
- [x] git add .
- [x] git commit -m "commit message"
- [x] git checkout develop
- [x] git pull origin develop
- [x] git flow feature finish feature/nombreFeature
- [x] git push origin develop

**Creación de rama realease:**
- [x] debes bifurcar una rama release a partir de develop
- [x] Cuando está lista para el lanzamiento, la rama release se fusiona en main y se etiqueta con un número de versión. Además, debería volver a fusionarse en develop, ya que esta podría haber progresado desde que se iniciara la publicación.
- [x] Se puede crear una nueva rama release: git flow release start 0.1.0
- [x] Finalizar rama realease: git flow release finish '0.1.0'
