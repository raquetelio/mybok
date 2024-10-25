# CSS

Cascading Style Sheets (CSS) is a simple mechanism for adding style (e.g., fonts, colors, spacing) to Web documents.

CSS = Cascading Style Sheets
[W3C (World Wide Web Consortium)](https://www.w3.org/) standard

CSS rule: Properties with their values grouped by a selector.

## Versions
- CSS1: 1996
- CSS2: 1998
- CSS3: 2011 -> Modularized. Each module evolves independently.

[W3C specifications](https://www.w3.org/Style/CSS/#specs)


## CSS Reference

https://developer.mozilla.org/en-US/docs/Web/CSS/Reference 


:es:

## Selectores
Siven para hacer target sobre los elementos HTML.

selector1, selector2,... {
    propiedad: valor;
}

**Shorthand**: Agrupa propiedades/valor en 1 string. 
```
border: 1px solid black;


border-width: 1px;
bordery-style: solid;
border-color: black;
```


## CSS links
### External CSS

```html
<!DOCTYPE html>
<head>
  <link rel="stylesheet" href="styles.css"/>  
</head>
<body>
    <p>Hello world<p>
</body>
</html>
```


### Internal CSS

```html
<!DOCTYPE html>
<head>
  <style>
        p{
            color:red;
        }
  </style> 
</head>
<body>
    <p>Hello world<p>
</body>
</html>
```

### Inline CSS

```html
<!DOCTYPE html>
<head>
</head>
<body>
    <p style="color:red;">Hello world<p>
</body>
</html>
```

## CSS Elements

- ### CSS Selectors
    [CSS Selectors](css-selectors.md)

- ### CSS Values
    [CSS Values](css-values.md)

- ### CSS Cascade
    [CSS Cascade](css-cascade.md)

- ### CSS Inheritance
    [CSS Inheritance](css-inheritance.md)

## CSS Box Model
[CSS Box Model](css-box-model.md)

## CSS Position
[CSS Position](css-position.md)

## CSS Stack level: z-index
[CSS Stack level: z-index](css-stack-level-z-index.md)

## CSS Flexbox
[CSS Flexbox](css-flexbox.md)

## CSS Grid
[CSS Grid](css-grid.md)


## CSS Gap
[CSS Gap](css-gap.md)


## References

Browser support tables for modern web technologies: 
https://caniuse.com/ 