# CSS Inheritance

```
        <html>
          |
        <body>
          |
   |------|-------|       
 <h1>    <p>    <div>
                  |
                  ------------|
                             <p>

```


https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#controlling_inheritance


CSS provides five special universal property values for controlling inheritance. Every CSS property accepts these values.

## inherit
Sets the property value applied to a selected element to be the same as that of its parent element. Effectively, this "turns on inheritance".

## initial
Sets the property value applied to a selected element to the initial value of that property.

## revert
Resets the property value applied to a selected element to the browser's default styling rather than the defaults applied to that property. This value acts like unset in many cases.

## revert-layer
Resets the property value applied to a selected element to the value established in a previous cascade layer.

## unset
Resets the property to its natural value, which means that if the property is naturally inherited it acts like inherit, otherwise it acts like initial.

Note: See [Origin types](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade#origin_types) for more information on each of these and how they work.

We can look at a list of links and explore how universal values work. The live example below allows you to play with the CSS and see what happens when you make changes. Playing with code really is the best way to better understand HTML and CSS.


## Example

```
div {
    font-size: initial;
}
```