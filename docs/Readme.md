# Alex Zarazua
## Práctica GitHub Pages
* ÍNDICE
* QUÉ ES Y PARA QUÉ SIRVE GIT
* QUÉ ES LA METODOLOGÍA GIT FLOW
* PORQUE LA HEMOS UTILIZADO
* QUE ES GITHUB PAGES
* LA PRÁCTICA



### ¿QUÉ ES GIT,Y PARA QUÉ SIRVE?
 * Git es un sistema de control de versiones, el cual nos puede servir para trabajar en equipo de una manera mucho más simple,cómoda y óptima cuando estamos desarrollando una aplicación o software
* Además de que vamos a poder controlar todos los cambios que se hacen en nuestra aplicación y en nuestro código teniendo acceso al control absoluto de todo lo que pasa en el código, pudiendo volver atrás en el tiempo, pudiendo abrir diferentes ramas de desarrollo, etc.
* De forma que si tenemos dos o tres personas trabajando en ciertas funcionalidades del proyecto,nosotros podemos estar trabajando en nuestra parte del código. Cuando acabamos de desarrollar nuestro código, utilizamos Git para mezclar los cambios con los otros compañeros,de forma que el código se mezcla de manera perfecta sin generar ningún tipo de fallo y de forma rápida.
 * También nos va a proporcionar un listado de los cambios(commits) y podemos volver atrás en el tiempo a cualquiera de esos cambios o commits.

### ¿QUÉ ÉS LA METODOLOGÍA GIT FLOW?
 - Es un flujo de trabajo aplicado a un repositorio Git. Vincent Driessen fue el encargado de popularizarlo, definiendo un modelo estricto de ramificación diseñado en torno a los lanzamientos del proyecto. Es ideal para proyectos que lleven una planificación de entregas iterativas. 
-  Permite la paralelización del desarrollo mediante ramas independientes para la preparación, mantenimiento y publicación de versiones del proyecto, además de que soporta la reparación de errores en cualquier momento.

### ¿POR QUÉ LA HEMOS UTILIZADO ?
 - En este proyecto hemos utilizado la herramienta git flow, ya que podemos desarrollar el proyecto en paralelo , 
 de tal manera que cada uno de los integrantes de este proyecto puede ir desarrollando su parte sin que le moleste las funcionalidades de los demás compañeros.

### La Práctica
El primer paso para esta práctica , es crear tres carpetas para simular los tres usuarios que intervendrán en los siguientes ejercicios.
<img src="../CapturasDocumentacion/creacion_carpetas_simulacion_users.png" alt="creacion_carpetas_simulacion_users" height="auto" with="200">

En segundo lugar,creamos el repositorio en GitHub y posteriormente hacemos un Git clone en cada una de las carpetas que hemos creado anteriormente para simular los distintos usuarios que colaboran en el mismo proyecto.
<img src="../CapturasDocumentacion/creando_repositorio_enGit.png" alt="creando_repositorio_enGit" height="auto" with="200">
<img src="../CapturasDocumentacion/gitClone_user-1.png" alt="gitClone_user-1" height="auto" with="200">
<img src="../CapturasDocumentacion/gitClone_usuarios-2-3.png" alt="gitClone_usuarios-2-3.png" height="auto" with="200">

Seguidamente creamos la estructura inicial en el usuario1 con una features para sus funcionalidades, además de la rama develop.
<img src="../CapturasDocumentacion/inicializacion_estructura-inicial-user1.png" alt="inicializacion_estructura-inicial-user1.png" height="auto" with="200">

Creamos la página inicial desde el usuario1
<img src="../CapturasDocumentacion/index-usuario1.png" alt="index-usuario1.png" height="auto" with="200">

Modificamos el Index.html para que quede com nos indican
<img src="../CapturasDocumentacion/index-pagina-princial.png" alt="index-pagina-princial.png" height="auto" with="200">

Subimos los cambios de la página inicial a la feature del usuario1.
<img src="../CapturasDocumentacion/subimos-cambios-rama-funcionalidad.png" alt="subimos-cambios-rama-funcionalidad.png" height="auto" with="200">

Creamos la develop y la funcionalidad en la carpeta del usuario 2
<img src="../CapturasDocumentacion/feature-funcionalidad-user-2.png" alt="feature-funcionalidad-user-2.png" height="auto" with="200">
<img src="../CapturasDocumentacion/develo-in-user2.png" alt="develo-in-user2.png" height="auto" with="200">


Nos posicionamos en la feature/funcionalidad_user2, donde realizaremos el git pull --rebase origin  feature/Funcionalidad_USER1 
<img src="../CapturasDocumentacion/git%20pull-feature-user1-in-user2.png" alt="git%20pull-feature-user1-in-user2.png" height="auto" with="200">


Creamos el siguiente html llamado modificar_contenido_html.html desde la nueva feature del usuario2 y realizamos la subida a la feature
Vemos los cambios gracias al git status

<img src="../CapturasDocumentacion/ver-cambios-user2-feature.png" alt="ver-cambios-user2-feature.png" height="auto" with="200">

Añadimos solamente los archivos en los cuales hemos realizado los cambios, como son el index y el nuevo fichero html.

<img src="../CapturasDocumentacion/git-add-commit-push-cambios-user2.png" alt="git-add-commit-push-cambios-user2.png" height="auto" with="200">

Seguidamente creamos una nueva feature ya que este usuario tiene que implementar una nueva funcionalidad, crear un nuevo archivo html dedicado a la página de atributos html.

<img src="../CapturasDocumentacion/rama-feature-atributos.png" alt="rama-feature-atributos.png" height="auto" with="200">

Con el comando git checkout -b feature/atributosHtml1 develop creamos la feature y nos posicionamos ya en ella,realizamos un git branch para comprobar que efectivamente estamos posicionados en esta.
Ahora es el turno de crear y modificar el nuevo archivo html.
La página quedaría de tal manera : 

<img src="../CapturasDocumentacion/modificar-atributos-html.png" alt="modificar-atributos-html.png" height="auto" with="200">

Comprobamos que efectivamente hemos realizado cambios tanto como en el atributos.html como en el index, realizamos el  git add para estos dos archivos, seguido del commit y el push a esta feature.

<img src="../CapturasDocumentacion/comporbacion-atributos-html.png" alt="comporbacion-atributos-html.png" height="auto" with="200">
<img src="../CapturasDocumentacion/git-add-commit-push-modif-atributos-user2.png" alt="git-add-commit-push-modif-atributos-user2.png" height="auto" with="200">


Una vez terminadas las funcionalidades de cada usuario , procedemos a realizar git merge para pasarlo a la rama master del proyecto.
Empezando por el usuario 1, lo primero que debemos hacer es posicionarnos en la rama master y desde esta hacer un git merge develop.

<img src="../CapturasDocumentacion/git-checkout-master-user1.png" alt="git-checkout-master-user1.png" height="auto" with="200">

<img src="../CapturasDocumentacion/git-merge-user1.png" alt="git-merge-user1.png" height="auto" with="200">

Ahora le toca al usuario 2
Nos posicionamos en master y comprobamos que cambios hay.

<img src="../CapturasDocumentacion/posicion-branch-status-user2.png" alt="posicion-branch-status-user2.png" height="auto" with="200">

Y realizamos el merge de develop de la feature de atributos
<img src="../CapturasDocumentacion/git-merge-feature-funcionalidad-puhs.png" alt="git-merge-feature-funcionalidad-puhs.png" height="auto" with="200"> 

Y de la feature/Fucionalidades_user2 que hace referencia al archivo de modificaciones contenido html,más el git push a la rama master
<img src="../CapturasDocumentacion/git-merge-feature-funcionalidad-puhs.png" alt="git-merge-feature-funcionalidad-puhs.png" height="auto" with="200"> 

Y de esta manera tendremos los cambios de los dos usuarios en la rama master.
Creamos la feature para el usuario 3 que se encargará de los cambios en el CSS.
<img src="../CapturasDocumentacion/creando-feature-estilos-user3.png" alt="creando-feature-estilos-user3.png" height="auto" with="200"> 

Creamos el archivo modificar_estilos_css y lo modificamos tal que asi.
<img src="../CapturasDocumentacion/estilos_css_html.png" alt="estilos_css_html.png" height="auto" with="200"> 

Añadiendo es este un código básico de js que lo que hace es una vez pulses el botón te cambia el tamaño del texto.
Como ya hemos creado la feature y modificado el archivo con el git add, más el commit y push subimos los cambios a la rama.

<img src="../CapturasDocumentacion/git-add-commit-push-user3.png" alt="git-add-commit-push-user3.png" height="auto" with="200"> 

Y creamos una nueva release que contendrá todas las features y con la etiqueta v1.2.3


<img src="../CapturasDocumentacion/merger-a-develop-y-creacion-release.png" alt="merger-a-develop-y-creacion-release.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/merge-de-la-release-y-tags.png" alt="merge-de-la-release-y-tags.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/subida-release-y-tags.png" alt="subida-release-y-tags.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/show-tag-creada.png" alt="show-tag-creada.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/push-tag.png" alt="push-tag.png" height="auto" with="200"> 

Actualizamos los datos en la carpeta del usuario 1 con el git pull
<img src="../CapturasDocumentacion/actualizando-datos-user1-antes-del-hotif.png" alt="actualizando-datos-user1-antes-del-hotif.png" height="auto" with="200"> 

Seguidamente procedemos a crear el hotfix en dicho usuario
<img src="../CapturasDocumentacion/creando-hotfix.png" alt="creando-hotfix.png" height="auto" with="200"> 

<img src="../CapturasDocumentacion/actualizando-hotfix.png" alt="actualizando-hotfix.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/modificacion-parael-hotfix.png" alt="modificacion-parael-hotfix.png" height="auto" with="200"> 

<img src="../CapturasDocumentacion/git--add--commit-hotfix.png" alt="git--add--commit-hotfix.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/git-push-hotfix.png" alt="git-push-hotfix.png" height="auto" with="200"> 

<img src="../CapturasDocumentacion/git-checkout-master-merge.png" alt="git-checkout-master-merge.png" height="auto" with="200"> 

Lo que podemos visualizar en las anteriores carpetas , es en primer lugar como menciono anteriormente, la creación del hotfix.
En segundo lugar, con el git branch comprobamos que estamos situados en el hotfix y actualizamos los datos.
Seguidamente realizamos el git add y el git commit -m para la posterior subida a remoto.
Lo subimos a remoto con el git push.
Para finalizar, con el git checkout master nos cambiamos a la rama master para actualizarla y subir los cambios al repositorio remoto con el git push origin master.

En esta segunda parte de la práctica les explicaré  paso por paso , cómo hacer un GitHub Pages en vuestro repositorio de GitHub.

El primer paso , obviamente es tener un repositorio github, que está explicado al principio de dicha práctica, no hace falta que al nombre le pongamos un nombre que acabe en .io ya que lo podremos activar teniendo el nombre que nosotros queramos.

Una vez tenemos el repositorio creado, nos dirigimos a los settings/ajustes y encontraremos un apartado de gh pages.

<img src="../CapturasDocumentacion/settings-github.png" alt="settings-github.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/githubpages-settings.png" alt="githubpages-settings.png" height="auto" with="200"> 

Lo siguientes que debemos hacer es seleccionar la rama la cual más adelante podremos acceder desde el enlace que nos proporcionará en mi caso, pondré la master.


<img src="../CapturasDocumentacion/github-pages-master.png" alt="github-pages-master.png" height="auto" with="200"> 

Y guardamos la configuración pulsando en Save.
Como podemos comprobar, la página cargará y ya nos mostrará nuestro enlace de github pages.


<img src="../CapturasDocumentacion/github-pages-guardado.png" alt="github-pages-guardado.png" height="auto" with="200"> 

De esta manera ya podremos acceder mediante la url de gh pages a los archivos de nuestra rama master.

Si por el contrario lo que queremos es tener por una parte el código en la rama master y que cuando accedemos al enlace que no muestre la documentación del proyecto, lo que tenemos que hacer es crear una rama llamada gh-pages y aqui es donde subiremos la documentación, por lo que cuando entremos en nuestra github pages nos mostrará dicha documentación.
Por lo tanto, procedemos a crear la rama y subir la documentación.

<img src="../CapturasDocumentacion/creamos-rama-pages.png" alt="creamos-rama-pages.png" height="auto" with="200">

<img src="../CapturasDocumentacion/rama-gh-pages-.png" alt="rama-gh-pages-.png" height="auto" with="200"> 

<img src="../CapturasDocumentacion/ative-gh-pages.png" alt="ative-gh-pages.png" height="auto" with="200"> 

Tenemos la rama de pages con un index.html que más adelante lo cambiaremos por un .md para poderle poner un tema a nuestra página y que la documentación se vea más elegante.
Nos dirigimos a los ajustes del repositorio y al apartado de GitHub Pages donde veremos la opción elegir un tema.

<img src="../CapturasDocumentacion/theme-gh-pages.png" alt="theme-gh-pages.png" height="auto" with="200"> 
<img src="../CapturasDocumentacion/opciones-themas.png" alt="opciones-themas.png" height="auto" with="200"> 

































### Support or Contact
PROYECTO PRÁCTICA GITHUB PAGES , GIT FLOW ALEX ZARAZUA
