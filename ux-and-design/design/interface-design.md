# Interface design

:es:

Sistemas de espaciado de 8px
Ajustar diseño a 1 grid: Columnas/Modular/Implicit grid
Layout: Fluido-Responsive/Adaptativo/Fijo

Buscar equilibrio:
- Simetría (seriedad).
- Asimetría (destacar, dinamismo).
- Peso visual -> para balancear.

Flujos de lectura:
- Z -> simplicidad
- F -> mucho contenido


## Tipografía

Ver _https://m3.material.io/styles/typography/applying-type_

- Normalmente, 1. No más de dos tipografías distintas en una página web. (1 para títulos otra para texto).

- Peso Light -> reservar para títulos. No usarlos en body o textos pequeños.
- Labels: Medium o bold para destacar. 


### Líneas
Establecer longitud máxima de línea. Normalmente entre 50-70,75. 

### Google Material recomienda 40-60.

_Source: https://m2.material.io/design/typography/understanding-typography.html#readability_

Line lengths for body text are usually between 40 to 60 characters. In areas with wider line lengths, such as desktop, longer lines that contain up to 120 characters will need an increased line height from 20sp to 24sp.

![Google Material line length](https://lh3.googleusercontent.com/4o_swy1dMJTs5gPJQ0MyifUkNSlMM2f4lgf6aujDHp-4VA2PRIrtEUNwwk5dw9OrnpTRWAc4Msw3QADl89Pht4hngcUIxtwS_LWi8g=w1064-v0)
The ideal line length is 40-60 characters per line for English body text.


![Google Material line length - short lines](https://lh3.googleusercontent.com/hI8BRTwICe9A5UFV3E4bcA5VsDkY8mNRjf1S9tBw6F8sNjIuzrDYfuRE3YsdaX0ORltSY1fJ9FAClHaotbk5MJX0sPnDud0JH_xF=w1064-v0)
The ideal line length for short lines of English text is 20-40 characters per line.


## Line height

Line height, also known as leading, controls the amount of space between baselines in a block of text. A text’s line height is proportional to...

Line height, also known as leading, controls the amount of space between baselines in a block of text. A text’s line height is proportional to its type size.


## Alineación

Los textos centrados solo se ven bien si son cortos.
Cuando son largos -> seguir el patrón de lectura del idioma:
- A bandera izquierda.
- O a bandera derecha.



## Color y su semántica

Transmiten sensaciones (según cultura), son interactivos. Considerar daltonismo.
Escalas: HSLA & RGBA

HSL stands for hue, saturation, and lightness. HSLA color values are an extension of HSL with an Alpha channel (opacity).


Colores:
Usas 3 tonos de cada color (usar la luminosidad). Maximo 5 tonos por color, no más.

- Grises -> para el texto.
- Primarios - Botones, enlaces, branding.
- De acento - transmitir significado en la interfaz. Ej. errores
- Accesibles-> mejor + contraste y con fondo + claro y letra oscura.
- Regla a del 60/30/10

_Ver https://tailwindcolor.com/_


### 60/30/10 color rule
_https://saralynnbrennan.com/the-60-30-10-design-rule/#:~:text=It's%20a%20classic%20decor%20rule,10%25%20should%20be%20an%20accent._


It's a classic decor rule that helps create a color palette for a space. It states that 60% of the room should be a dominant color, 30% should be the secondary color or texture and the last 10% should be an accent.

_https://www.linkedin.com/pulse/60-30-10-rule-simple-formula-creating-balanced-ui-color-raghuvansh/_
![60-30-10 Rule](https://media.licdn.com/dms/image/v2/D4D12AQHmZXIzViiRuQ/article-cover_image-shrink_720_1280/article-cover_image-shrink_720_1280/0/1684470842206?e=1735171200&v=beta&t=9mze8HWknF45-jSgKcI5tlLhrNsllfjqeVyFinhQAfw)


## Iconografía e imágenes.

Preferiblemente svg (para escalar). png ya no se usa en iconos.
Siempre con texto, a menos que sea universal.
Considerar cómo van a escalar.


Imágenes:

Responsive.
Buena calidad. 
Subidas por el usuario -> dar un tamaño al layout independientemente del tamaño de la imagen subida por el usuario. 

## Patrones de diseño
[Interface design patterns](interface-design-patterns.md)