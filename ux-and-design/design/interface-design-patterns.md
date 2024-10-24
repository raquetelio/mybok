# Interface design patterns

Designing Interfaces, 3rd Edition: https://www.oreilly.com/library/view/designing-interfaces-3rd/9781492051954/


Information Architecture for the World Wide Web, 3rd Edition https://www.oreilly.com/library/view/information-architecture-for/0596527349/


http://www.jjg.net/ia/ 


## The Elements of User Experience
http://www.jjg.net/elements/pdf/elements.pdf

![The Elements of User Experience](https://www.insight.com/en_US/content-and-resources/blog/focusing-on-the-foundations-of-user-experience/jcr:content/top-container-width/column_layout/-column-1/image.img.jpg/1571178345699.jpg)


## Patrones

### Arquitectura de la información

- Organización de datos.
- Patrones de búsqueda.
    - Búsqueda por texto libre + facetas (nº color, filtros) -> Amazon
    - Pre-filtrado. -> idealista (comprar, alquilar, ubicación)
- Patrones de navegación.
- Vocabularios controlados.
- Sistemas de etiquetados.
    - Enlaces, títulos de página y sección, índices, etiquetas de formularios, llamadas a la acción.


### Formularios

- Usar una columna en general. Usar 2 columnas solo si es necesario (Más carga).
- Ajustar al tamaño del dato (ej: CP).
- Si todo es obligatorio -> marcar solo el que es opcional. Si no: marcar obligatorios si son pocos.
- Agrupación -> leyes de la Gestalt. Secciones tituladas.
- Mostrar validación en línea mejor. A menos que sea i general de la página, que va arriba. El escaneo en vertical es + eficiente.
- Rotulado: etiqueta mejor arriba (menos carga cognitiva). 


    | Etiqueta |
    | -------- |
    | campo |
    ||

- Si hay pregunta que leer: alineado a la izquierda. El alineado a la derecha dificulta la lectura

    | |  |
    | -------- | ----- |
    | Pregunta: | respuesta |

- Usar etiquetas flotantes para ahorro de espacio vertical (etiquetas flotantes)

    |  | 
    | -------- | 
    | Título | 
    |  | 


- Usar máscaras para evitar errores. 
Pocas opciones en radio-button, checkbocks. Si son muchos => dropdown.

Contraseñas: 1º campo obligatorio recibe el foco.

Autorrellenar con los valores que ya están en las cookies.


### Ayuda

- puedes añadir placeholder, texto descriptivio, tooltip de i o i clickeable (para información no esencial)

### Validación y feedback

Mejor en línea.
Si error general => arriba. 


No dar i de la validación y feedback mientras se está escribiendo ni al salir del campo. Mejor al pulsar el botón activo se revisa todo y se puede hacer click en los errores.
Excepto si feedback tipo: contraseña debil fuerte.
IMP: botón siempre habilitado.

### Call to actions
Evitar: SUBMIT.

Mejor, describir tarea: CREATE ACCOUNT, SUBSCRIBE NOW, SEND MESSAGE,....

Al hacer click recibir feedback siempre: Success or Error.

En general no hacer autofocus, seguir la lógina de ordenación según aparecen.

### Mensajes de estado.

1ª heurística de Nielsen: visibilidad del estado del sistema.

Notificación: 
- evento razonable 
- con información adecuada 
- en tiempo razonable.

Antipatrón: falssa urgencia para forzar una acción (ej. anuncio)

En nuestra cultura el color tiene semática: 
- rojo: acción
- naranja/amarillo: aviso
. verde: todo OK.


### Acciones y comandos

#### Interfaz gráfica

Botones: 
- deben ser identificables (tamaño y forma destacado). 
- estilo depende d la acción.
- ubicación: al final de los elementos a los que aplique.

| Secundario | PRINCIPAL |
|-|-|
| izquierda | derecha |

Variants

_Source: https://carbondesignsystem.com/components/button/usage/_
Each button variant has a particular function and its design signals that function to the user. It is therefore very important that the different variants are implemented consistently across products, so that they message the correct actions.

![ button variant ](https://carbondesignsystem.com/static/c14e830dd29e73a0134e3abc018db11b/3cbba/button_usage_1.png)

| Variant |	Purpose | 
| ------- | ------- |
| Primary |	For the principal call to action on the page. Primary buttons should only appear once per screen (not including the application header, modal dialog, or side panel).
| Secondary	| For secondary actions on each page. Secondary buttons can only be used in conjunction with a primary button. As part of a pair, the secondary button’s function is to perform the negative action of the set, such as “Cancel” or “Back”. Do not use a secondary button in isolation and do not use a secondary button for a positive action.
| Tertiary	| For less prominent, and sometimes independent, actions. Tertiary buttons can be used in isolation or paired with a primary | button when there are multiple calls to action. Tertiary buttons can | also be used for sub-tasks on a page where a primary button for the | main and final action is present.
| Danger | 	For actions that could have destructive effects on the user’s data (for example, delete or remove). Danger button has three styles: primary, tertiary, and ghost.
| Ghost	 | For the least pronounced actions; often used in conjunction with a primary button. In a situation such as a progress flow, a ghost button may be paired with a primary and secondary button set, where the primary button is for forward action, the secondary button is for “Back”, and the ghost button is for “Cancel”.


Barras de menú.
Todas las acciones.
Organizadas de forma predictiva.
Suelend duplicar acciones que están en menús contextuales.

Menús contextuales y desplegables.
Barras de herramients y paneles de acciones.

Enlaces

- No poner: haz click aqui.
- Poner: Please find a _security questionary_

Si el enlace es corto: puedes dejar la URL.


Herramientas en Hover.
- Ayudan a no sobrecargar la interfaz, pero hay que dar piestas de que están ahí. 
No sirven para dispositivos móviles.


Acciones de teclado
- atajos, tabulador, comandos en terminal.

Drag&Drop.
- el elemento que recibie la accioón debe cambiar de estado y decir qué es la acción.


Affordance
- ayuda a saber que los elementos son interactivos. 


## Organización de la información

- lineal. 
```x-x-x```
- Tabular.
```
x-x-x
x-x-x
x-x-x
```

- Jerarquía - Grafos
- Red interconectada - grafos
- Listas.

Usar para infromación simple y consistente. Oculta detalles con navegación. Se usan para ser responsive una tabla.


``` 
clásica
----------
----------
----------
```

```
Pinterest
--- --- ---
--- --- ---
``` 

    - Cada elemento es independionte. 
    - No tiene filtros.
    - nº ade acciones limitado.


- Tablas.

Forma eficiente de mostrar información compleja.
datos: complejos, relacionads, información en bruto.


Si texto: alineación izquierda. Junto con su cabecera. Nunca al centro.
Si número: alineación derecha. Junto con su cabecera.

Fijar 1ª fila, columna, añadir filtrado en cabecera.

- Gráficas.

Tendencias en el tiempo, patrones o formas de datos, comparativas, datos salidas de la norma.

Patrones:
- data tips (hover)
- data spotlight (centrar en 1 elem al hacer click)
- dynamic queries (búsquedas)
- data brushing (mismos datos de forma distinta ej: mapa de calor + gráfica)