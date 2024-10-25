# CSS Elements

## CSS Selectors

### Simples

- Tag: ```p, h1```.
- Identifiers: ```#idElement```
- Classes: ```.myClass```, ```div.myClass```


### Complex

- PseudoClasses: ```a:visited```. BEHAVIOR, STATUS: ```hover, active, focus```.
- PseudoElements: ``` p::selection```. RELATIVE STATUS: ```selection, first-line, fist-letter, before, after```
- Atributes:
    ```html
       
        - [title]. EXISTS
        - [title="Email"]. EXISTS AND EQUAL TO
        - [title~="logo"]. EXISTS and has logo in the list of values.
        - [lang|="en"]. EXISTS and has an element with "en" or starts with "en".
        - [href^="https"]. EXISTS and starts with "https"
        - [href$=".pdf"]. EXISTS and ends with "pdf"
        - [href*="lemoncode"]. EXISTS and has "lemoncode" at any position.
    ```

### Multiple selectors

Separated by commas ",".

### Combinations

- Descendents: ```div p```.
- Childs: ```div>p```.
- Next-sibling combinator ```div+p```. (Adjacent sibling:)
- Subsequent-sibling combinator: ```div~p```.
