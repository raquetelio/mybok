# Emmet in VS Code
Source: https://code.visualstudio.com/docs/editor/emmet.

Support for Emmet snippets and expansion is built right into Visual Studio Code, no extension required. Emmet 2.0 has support for the majority of the Emmet Actions including expanding Emmet abbreviations and snippets.



## How to expand Emmet abbreviations and snippets
Emmet abbreviation and snippet expansions are enabled by default in html, haml, pug, slim, jsx, xml, xsl, css, scss, sass, less and stylus files, as well as any language that inherits from any of the above like handlebars and php.

![Emmet in suggestion/auto-completion list](https://code.visualstudio.com/assets/docs/editor/emmet/emmet.gif)

When you start typing an Emmet abbreviation, you will see the abbreviation displayed in the suggestion list. If you have the suggestion documentation fly-out open, you will see a preview of the expansion as you type. If you are in a stylesheet file, the expanded abbreviation shows up in the suggestion list sorted among the other CSS suggestions.




## Using Tab for Emmet expansions
If you want to use the Tab key for expanding the Emmet abbreviations, add the following setting:

```
"emmet.triggerExpansionOnTab": true
```

This setting allows using the Tab key for indentation when text is not an Emmet abbreviation.


## Emmet when quickSuggestions are disabled
If you have disabled the editor.quickSuggestions setting, you won't see suggestions as you type. You can still trigger suggestions manually by pressing Ctrl+Space and see the preview
