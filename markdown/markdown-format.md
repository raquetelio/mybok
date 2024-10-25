# Markdown format

- https://www.markdownguide.org/extended-syntax/ 
- https://markdownlivepreview.com/ 



## Scaping characters:

For italic text use backticks (``):
```
_this_is_italic_text_
_`this_is_italic_text`_
```

For tables use backward slash: (\):

```
(x|y) -> NOK
(x\|y) -> OK 
```

| Bracket | Description | 
| ------- | :----------: |
| (x\|y) | Find any of the alternatives specified |




## Syntax Highlighting
Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks before the fenced code block.

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
The rendered output looks like this:
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25

}
```