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