# SASS functions

https://sass-lang.com/documentation/at-rules/function/


Functions are defined using the @function at-rule, which is written @function <name>(<arguments...>) { ... }. A function’s name can be any Sass identifier that doesn’t begin with --. It can only contain universal statements, as well as the @return at-rule which indicates the value to use as the result of the function call. Functions are called using the normal CSS function syntax.


```scss
@function fibonacci($n) {
  $sequence: 0 1;
  @for $_ from 1 through $n {
    $new: nth($sequence, length($sequence)) + nth($sequence, length($sequence) - 1);
    $sequence: append($sequence, $new);
  }
  @return nth($sequence, length($sequence));
}

.sidebar {
  float: left;
  margin-left: fibonacci(4) * 1px;
}
```

```css
.sidebar {
  float: left;
  margin-left: 5px;
}
```