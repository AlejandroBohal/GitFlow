# GitFlow
Guia de uso  GitFlow

## Integrantes:
- Carlos Gomez
- Juan Rojas
- Santiago Rubiano
- Alejandro Bohorquez 
- Andrés Marcelo


## Que es GitFlow
GitFlow es un flujo de trabajo aplicado a un repositorio Git. Vincent Driessen fue el encargado de popularizarlo, definiendo un modelo estricto de ramificación diseñado en torno a los lanzamientos del proyecto. Es ideal para proyectos que lleven una planificación de entregas iterativas. Permite la paralelización del desarrollo mediante ramas independientes para la preparación, mantenimiento y publicación de versiones del proyecto así como soporta la reparación de errores en cualquier momento.

## Por qué deberíamos implementarlo?
* Aumenta la velocidad de entrega de código terminado al equipo de pruebas.
* Disminuyen los errores humanos en la mezcla de las ramas.
* Elimina la dependencia de funcionalidades al momento de entregar código para ser puesto en producción.


## ¿Cuándo se recomienda implementarlo?
 

* El equipo de trabajo está conformado por más de dos (2) personas.
* Se emplean metodologías ágiles.
* El proyecto tiene cambios frecuentes y se requiere actualizar el ambiente de producción garantizando continuidad en la operación.
* El proyecto tiene un nivel de complejidad considerable.
* Se desea tener un proceso de soporte a errores efectivo con actualizaciones rápidas.

## Esctructura GitFlow 

![Esctructura GitFlow](img/estructura.png) 

## Contenido de cada rama

Existen 4 diferentes tipos de ramas que GitFlow nos da. En cada una de ellas tendremos
diferentes contenidos para tener de manera mas organizada nuestro codigo. Las diferentes 
ramas son:
1. develop
2. feature
3. release
4. hotfix

![Image of GitFlow](https://cleventy.com/wp-content/uploads/2020/03/git-model-1.png)

## Inicializando un repositorio con GitFlow

Las ventajas de inicializar un repositorio con GitFlow es ordenar
el flujo de trabajo en ramas de la siguiente manera.

 git flow init 

![](https://i.ibb.co/G20hht9/Gitflow-1.png)

en GitKraken, clonamos el repositorio y editamos las preferencias.

![](https://i.ibb.co/BzZ0mYC/Gitflow-2.png)

y observamos un ejemplo de flujo de trabajo en GitKraken

![](https://i.ibb.co/qpf41gm/Gitflow-3.png)

 
# Comandos en GitFlow

### Inicializar un feature

En la terminal podemos utilizar el siguiente codigo para poder inicializar un feature

```
    git flow feature start NOMBREFEATURE
```

De igual manera mediante GitKraken podemos hacer lo mismo de la siguiente manera:

![Image of GitKraken1](https://cdn.discordapp.com/attachments/718609326071218189/718950450040274964/Screen_Shot_2020-06-06_at_5.04.31_PM.png)
![Image of GitKraken2](https://cdn.discordapp.com/attachments/718609326071218189/718950453324414976/Screen_Shot_2020-06-06_at_5.05.48_PM.png)

Y de esta manera quedarian nuestras ramas, en donde la rama morada, roja, naranja, amarilla y verde son features creadas
para poder tener las diferentes 
![Image of GitKraken3](https://cdn.discordapp.com/attachments/718609326071218189/718945365331673158/Screen_Shot_2020-06-06_at_4.52.06_PM.png)


## Publicar y finalizar Feature 

### Publicar

El comando en consola para hacer la publicación del feature

``` git flow feature publish MYFEATURE ```

![PublishFeature](img/PublicarFeatureConsola.PNG) 

En GitKraken es haciendo solamente un push de la rama que queremos

![PublishFeature2](img/PublicarFeatureGitKraken.PNG)

### Finalizar

El comando en consola para hacer la finalización del feature

``` git flow feature finish MYFEATURE ```

En GitKraken en el panel de la izquierda vemos la opcion de gitflow en la cual podemos finalizar de la rama que queremos

![FinishFeature2](img/FinalizarFeatureGitKraken.PNG)


## Inicializar un realease 
Esta función se realiza cuando se ha terminado un sprint, cuando se tiene el codigo listo para entregar a producción
en esta rama se suele hacer pruebas de QA y al inicializarse toma la ultima version de la rama develop

### En consola 

 ``` git flow release start <nombre de version > ```
 
![startReleaseConsola](img/releaseconsola.png)

### Git Kraken
![startRelease](img/releasekraken.png)
![startRelease2](img/releasekraken2.png)

### Finalizar un release

Es importante destacar que un release se finaliza cuando 
el proyecto está lo suficientemente avanzado para salir a producción,
o se encuentra listo para pruebas de integracion.

para finalizar un release utilizamos el comando de consola

 // Comando para finalizar release
 ``` git flow release finish "Nombre de version" ```
 
Ejemplo:  

![](https://i.ibb.co/x8Q3QFC/finish-Release.png)

Nos pedirá añadir  un comentario para el tag de la versión  

![](https://i.ibb.co/FH7NJBF/tag-Release.png)  


 // Finalmente, se publica la version  
 ``` git push origin --tags ```

Y git nos muestra un resumen de lo realizado.  

![](https://i.ibb.co/hghc3DJ/resumen.png)  


### Realizar un Hotfix  

En consola podemos realizar un hotfix con el siguiente comando:  

``` $ git flow hotfix start hotfix_branch  ```

Con GitKraken podemos inicializar un hotfix de la siguiente forma:  

![](https://cdn.discordapp.com/attachments/718609326071218189/718951834844266506/unknown.png)  

 

Se recomienda poner el nombre del hotfix con el versionamiento correspondiente. Ej: v1.1 - v0.1.1.  

Una vez ya esten los cambios realizados, debido a que Hotfix no posee un comando de publicación  
basta con realizar el commit y usar el comando:  

``` $ git flow hotfix finish ```  

Realizar la documentación de los cambios para el merge con develop y con master y hacer push.  

En GitKraken Basta con Finalizar el hotfix en el mismo panel donde se inició, si se desea borrar la rama hotfix, comentar los cambios y hacer push a Origin.
