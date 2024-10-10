# IISSI-2 IS: Examen de laboratorio

## ENUNCIADO
After the initial launch of DeliverUS, investors have requested a new feature that allows owners to pin their restaurants. Each owner can pin as many restaurants as they wish.

An owner can pin restaurants in two different ways:

In the restaurant creation form. By default, it will not be pinned, but the owner can choose to pin it. To do this, a Switch should be provided that works with a property called pinned. If the Switch is checked, the restaurant should be created as pinned. The backend expects the pinned property to be a boolean and optional. If the property is not present, it should be created as not pinned.

On the "My Restaurants" screen, through an icon that will act as a button and will be displayed next to each restaurant. By clicking it, the restaurant will be pinned or unpinned. The application should ask for confirmation from the owner when the button is pressed: use the provided ConfirmationModal component, similar to the DeleteModal component used in class. The system will inform the user if the restaurant has been pinned or unpinned.

Finally, pinned restaurants will always appear at the top of the restaurant lists presented to their owner and will be ordered by the date they were pinned (oldest first), followed by the non-pinned ones.

Task 1
Make all the necessary changes in the backend project to implement the new requirement. The backend tests expect the route to be: PATCH /restaurants/:restaurantId/togglePin and that restaurants have a new property called pinnedAt.

Remember that you can run the tests with:

npm run test:backend
Task 2
Make all the necessary changes in the frontend project to implement the new requirement.

You can render the proposed pin icon with

<MaterialCommunityIcons
    name={item.pinnedAt ? 'pin' : 'pin-outline'}
    color={GlobalStyles.brandSecondaryTap}
    size={24}
/>
Scoring
Task 1 Scoring
RF1. Ability to create a pinned or unpinned restaurant. (2 points)
RF2. Ability to set an existing restaurant as pinned or unpinned. (2 points)
RF3. List restaurants in the described order: first the pinned restaurants ordered by pin date (the oldest pinned restaurants must come first), and then the unpinned restaurants. (1 point)
Task 2 Scoring
RF1. Ability to create a pinned or unpinned restaurant. (1 point)
RF2. Ability to set an existing restaurant as pinned or unpinned.
RF2.1. Ability to set an existing restaurant as pinned, with confirmation and feedback about the successful pinning. (1,5 points)
RF2.2. Ability to set an existing restaurant as unpinned, with confirmation and feedback about the successful unpinning. (1,5 points)
Global. Visual correctness: icons, layout, modals etc. (1 point)
All actions/screens/etc. that cannot be human-checked (as a final user would do) due to any errors, may not be considered for scoring.

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
