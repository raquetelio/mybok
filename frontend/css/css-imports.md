# CSS imports

https://developer.mozilla.org/en-US/docs/Web/CSS/@import

The @import CSS at-rule is used to import style rules from other valid stylesheets. An @import rule must be defined at the top of the stylesheet, before any other at-rule (except @charset and @layer) and style declarations, or it will be ignored.


## Example:

_./src/base.css_
```css
body {
padding: 0;
margin: 0;
height: 100vh;
display: flex;
flex-direction: column;
}
```

_./src/styles.css_
```css
@import url("base.css")
```