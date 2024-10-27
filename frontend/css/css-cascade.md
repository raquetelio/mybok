# CSS Cascade

Factors:
- Importance: ```!important```
- Specificity.
- Order (from top to down)

## Origin types
https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade#origin_types


User agent < User CSS < Author CSS


## Specificity

https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#specificity 

Specificity is the algorithm that the browser uses to decide which property value is applied to an element. If multiple style blocks have different selectors that configure the same property with different values and target the same element, specificity decides the property value that gets applied to the element. Specificity is basically a measure of how specific a selector's selection will be:


Specificity calculator:
https://specificity.keegan.st/



Prevalencia en base a pesos.
A mayor especificidad-> mayor peso.
Niveles de pesos:
A: nº estilos aplicados meidante style. Si existe: 1
B: nº apariciones de 1 id en 1 selector.
C: nº apariciones de 1 clase, pseudoclase o atributo.
D: nº apariciones de 1 elemento o pseudoelemento.
