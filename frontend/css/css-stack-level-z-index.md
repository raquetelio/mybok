# CSS stack level: z-index

The z-index CSS property sets the z-order of a positioned element and its descendants or flex and grid items. Overlapping elements with a larger z-index cover those with a smaller one.

See [Try it](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index).

For a positioned box (that is, one with any position other than static), the z-index property specifies:

1. The stack level of the box in the current stacking context.
2. Whether the box establishes a local stacking context.


The z-index property is specified as either the keyword **auto or an `<integer>`**.

```
/* Keyword value */
z-index: auto;

/* <integer> values */
z-index: 0;
z-index: 3;
z-index: 289;
z-index: -1; /* Negative values to lower the priority */

/* Global values */
z-index: inherit;
z-index: initial;
z-index: revert;
z-index: revert-layer;
z-index: unset;
```


Source:

``` 
<!DOCTYPE html>
<head>
  <style>    
        .wrapper {
    position: relative;
    }
   .dashed-box {
    position: relative;
    z-index: 1;
    border: dashed;
    height: 8em;
    margin-bottom: 1em;
    margin-top: 2em;
    }
    .gold-box {
    position: absolute;
    z-index: 3; /* put .gold-box above .green-box and .dashed-box */
    background: gold;
    width: 80%;
    left: 60px;
    top: 3em;
    }
    .green-box {
    position: absolute;
    z-index: 2; /* put .green-box above .dashed-box */
    background: lightgreen;
    width: 20%;
    left: 65%;
    top: -25px;
    height: 7em;
    opacity: 0.9;
    }
  </style> 
</head>
<body>
   <div class="wrapper">
    <div class="dashed-box">Dashed box</div>
    <div class="gold-box">Gold box</div>
    <div class="green-box">Green box</div>
    </div>
</body>
</html>
```


Result:

<!DOCTYPE html>
<head>
  <style>    
       .wrapper {
        position: relative;
        }
        .dashed-box {
        position: relative;
        z-index: 1;
        border: dashed;
        height: 8em;
        margin-bottom: 1em;
        margin-top: 2em;
        }
        .gold-box {
        position: absolute;
        z-index: 3; /* put .gold-box above .green-box and .dashed-box */
        background: gold;
        width: 80%;
        left: 60px;
        top: 3em;
        }
        .green-box {
        position: absolute;
        z-index: 2; /* put .green-box above .dashed-box */
        background: lightgreen;
        width: 20%;
        left: 65%;
        top: -25px;
        height: 7em;
        opacity: 0.9;
        }
  </style> 
</head>
<body>
   <<div class="wrapper">
    <div class="dashed-box">Dashed box</div>
    <div class="gold-box">Gold box</div>
    <div class="green-box">Green box</div>
    </div>
</body>
</html>