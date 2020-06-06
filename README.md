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




## Inicializar un realease 
Esta función se realiza cuando se ha terminado un sprint, cuando se tiene el codigo listo para entregar a producción
en esta rama se suele hacer pruebas de QA y al inicializarse toma la ultima version de la rama develop

### En consola 

 ``` git flow realease start <nombre de version > ```
 
![startReleaseConsola](img/releaseconsola.png)

### Git Kraken
![startRelease](img/releasekraken.png)
![startRelease2](img/releasekraken2.png)