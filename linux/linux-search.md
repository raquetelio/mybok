# Linux search

_Source: https://stackoverflow.com/questions/16956810/find-all-files-containing-a-specific-text-string-on-linux_

## grep command

With recursive search (-r: recursive search )
```bash
grep -r "string to be searched" /path/to/dir
```

For current dir:
```bash
grep -r "string to be searched" .
```

n: line number will be shown for matches
```bash
 grep -rn "String to search" /path/to/directory/or/file
```

Recursive and case insensitive grep with line numbers:
```bash
grep -inr "Text" folder/to/be/searched/
```

Specific files
```bash
grep "class foo" **/*.c
```

## ripgrep
Larger projects or big files, you should use ripgrep

```bash
rg "class foo" .
```

## find

```bash
find / -type f -exec grep -l "text-to-find-here" {} \; 
```
Example:
```bash
find . -type f -exec grep -l "Apache License" {} \; 
```


for searching in all javascript files (*.js):
```bash
find . -name '*.js' -exec grep -i 'string to search for' {} \; -print
```
This will print the lines in the files where the text appears, but it does not print the file name.


```bash
find . -name "*.php" -execdir grep -nH --color=auto foo {} ';'
```