# CSS Custom properties (variables)

_https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties_

Custom properties (sometimes referred to as CSS variables or cascading variables) are entities defined by CSS authors that represent specific values to be reused throughout a document. They are set using the @property at-rule or by custom property syntax (e.g., --primary-color: blue;). Custom properties are accessed using the CSS var() function (e.g., color: var(--primary-color);).

## Example

```css
html {
    --back-color: darkorange;
}
```
Usage:
```css
main {
    background-color: var(--back-color);
}

footer {
    background-color: var(--back-color);
}


```