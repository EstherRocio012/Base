# IISSI-2 IS: Examen de laboratorio

## ENUNCIADO
Una vez se ha puesto en marcha la primera versión de DeliverUS, los inversores han solicitado la inclusión de una nueva funcionalidad que consiste en ofrecer a los propietarios la posibilidad de promocionar sus restaurantes. Cada propietario sólo podrá promocionar uno de sus restaurantes.

Un propietario podrá promocionar un restaurante de dos maneras distintas:

En el formulario de creación de restaurante. Por defecto, se seleccionará la opción de no promocionado. Si el propietario indica que el nuevo restaurante debe estar promocionado, pero ya existían restaurantes promocionados del mismo propietario, al pulsar el botón Save se mostrará un error y no se creará el restaurante.

En la pantalla de "Mis restaurantes", mediante un botón mostrado junto a cada restaurante, que permitirá mediante su pulsación promocionar el restaurante en cuestión. Si el propietario pulsa el botón para promocionar un nuevo restaurante y ya existían otros restaurantes promocionados del mismo dueño, se procederá a promocionar el restaurante indicado y se marcará como "no promocionado" el restaurante que lo fuese anteriormente. La aplicación debe pedir confirmación al propietario cuando se pulse el botón; utilice para ello el componente suministrado ConfirmationModal, similar al componente DeleteModal utilizado en clase.

Además, los restaurantes promocionados aparecerán siempre al principio de los listados de restaurantes que se le presentan tanto a los propietarios como a los clientes. Además de presentarse al principio, los restaurantes promocionados deben destacarse visualmente, por lo que aparecerá una etiqueta de texto ¡En promoción! con el color principal de la marca.

Ejercicio 1 Realice todos los cambios necesarios en el proyecto de backend para implementar el nuevo requisito.

Ejercicio 2 Realice todos los cambios necesarios en el proyecto de frontend para implementar el nuevo requisito.

## Proyecto base suministrado

Este repositorio incluye el backend completo (carpeta `DeliverUS-Backend`) y el frontend de `owner` (carpeta `DeliverUS-Frontend-Owner`). Servirá como base para realizar el examen de laboratorio de la asignatura.

## Preparación del entorno

### a) Windows

* Abra un terminal y ejecute el comando `npm run install:all:win`.

### b) Linux/MacOS

* Abra un terminal y ejecute el comando `npm run install:all:bash`.

## Ejecución

### Backend

* Para **rehacer las migraciones y seeders**, abra un terminal y ejecute el comando

    ```Bash
    npm run migrate:backend
    ```

* Para **ejecutarlo**, abra un terminal y ejecute el comando

    ```Bash
    npm run start:backend
    ```

### Frontend

* Para **ejecutar la aplicación frontend de `owner`**, abra un nuevo terminal y ejecute el comando

    ```Bash
    npm run start:frontend:owner
    ```

## Depuración

* Para **depurar el backend**, asegúrese de que **NO** existe una instancia en ejecución, pulse en el botón `Run and Debug` de la barra lateral, seleccione `Debug Backend` en la lista desplegable, y pulse el botón de *Play*.

* Para **depurar el frontend**, asegúrese de que **EXISTE** una instancia en ejecución del frontend que desee depurar, pulse en el botón `Run and Debug` de la barra lateral, seleccione `Debug Frontend` en la lista desplegable, y pulse el botón de *Play*.


## Test

* Para comprobar el correcto funcionamiento de backend puede ejecutar el conjunto de tests incluido a tal efecto. Para ello ejecute el siguiente comando:

    ```Bash
    npm run test:backend
    ```
**Advertencia: Los tests no pueden ser modificados.**

## Problemas con los puertos

En ocasiones, los procesos de backend o frontend, con o sin depuración, pueden quedarse bloqueados sin liberar los puertos utilizados, impidiendo que puedan ejecutarse otros procesos. Se recomienda cerrar y volver a iniciar VSC para cerrar dichos procesos.


## Procedimiento de entrega

1. Borrar las carpetas **node_modules** de backend y frontend y **.expo** del frontend.
1. Crear un ZIP que incluya todo el proyecto. **Importante: Comprueba que el ZIP no es el mismo que te has descargado e incluye tu solución**
1. Avisa al profesor antes de entregar.
1. Cuando el profesor te dé el visto bueno, puedes subir el ZIP a la plataforma de Enseñanza Virtual. **Es muy importante esperar a que la plataforma te muestre un enlace al ZIP antes de pulsar el botón de enviar**. Se recomienda descargar ese ZIP para comprobar lo que se ha subido. Un vez realizada la comprobación, puedes enviar el examen.
  
Si no se siguen estos pasos de manera escrupulosa, cabe la posibilidad de que no se entregue nada o que el ZIP contenga cualquier cosa. 
