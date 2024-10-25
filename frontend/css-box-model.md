# Box model

https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model


Everything in CSS has a box around it, and understanding these boxes is key to being able to create more complex layouts with CSS, or to align items with other items.


## Block and inline boxes
In CSS we have several types of boxes that generally fit into the categories of:
- block boxes and
- inline boxes. 

**The type refers to how the box behaves in terms of page flow and in relation to other boxes on the page.** Boxes have an inner display type and an outer display type.

In general, you can set various values for the display type using the **display property**, which can have various values.

## Outer display

### Outer display type Block
If a box has an outer display type of block, then:

- The box will break onto a new line.
- The width and height properties are respected.
- Padding, margin and border will cause other elements to be pushed away from the box.
- If width is not specified, the box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.

Some HTML elements, such as `<h1>` and `<p>`, use block as their outer display type by default.


### Outer display type Inline 

If a box has an outer display type of inline, then:

- The box will not break onto a new line.
- The width and height properties will not apply.
- Top and bottom padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
- Left and right padding, margins, and borders will apply and will cause other inline - boxes to move away from the box.
- Some HTML elements, such as `<a>`, `<span>`, `<em>` and `<strong>` use inline as their outer display type by default.



## Inner display type
Boxes also have an inner display type, which dictates how elements inside that box are laid out.

**Block and inline layout is the default way things behave on the web**. By default and without any other instruction, **the elements inside a box are also laid out in normal flow and behave as block or inline boxes**.

**You can change the inner display type for example by setting display: flex;. The element will still use the outer display type block but this changes the inner display type to flex. Any direct children of this box will become flex items and behave according to the Flexbox specification.**

When you move on to learn about CSS Layout in more detail, you will encounter flex, and various other inner values that your boxes can have, for example grid.


See also: 
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flow_layout/Block_and_inline_layout_in_normal_flow
- https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow


## Parts of a box
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#parts_of_a_box

Making up a block box in CSS we have the:

### Content box: 
The area where your content is displayed; size it using properties like inline-size and block-size or width and height.

### Padding box: 
The padding sits around the content as white space; size it using padding and related properties.

### Border box: 
The border box wraps the content and any padding; size it using border and related properties.

### Margin box: 
The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using margin and related properties.

## Diagram

The below diagram shows these layers:


![The box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/box-model.png)


## box-sizing property
See: https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_alternative_css_box_model

### box-sizing: content-box;
Default value. Only takes the content to calculate width and height of content.

### box-sizing: border-box;
Used to set size. Values should be provided, like:

```html

.box {
  box-sizing: border-box;
}


.box {
  width: 350px;
  inline-size: 350px;
  height: 150px;
  block-size: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}

```

Now, the actual space taken up by the box will be 350px in the inline direction and 150px in the block direction.

![Box height and width](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/alternate-box-model.png)


Example:

Source:

```
<!DOCTYPE html>
<head>
  <style>
        .box {
        border: 5px solid rebeccapurple;
        background-color: lightgray;
        padding: 40px;
        margin: 40px;
        width: 300px;
        height: 150px;
        }

        .alternate {
        box-sizing: border-box;
        }
  </style> 
</head>
<body>
    <div class="box">I use the standard box model.</div>
    <div class="box alternate">I use the alternate box model.</div>
</body>
</html>
```

Result:

<!DOCTYPE html>
<head>
  <style>    
        .box {
        border: 5px solid rebeccapurple;
        background-color: lightgray;
        color: black;
        padding: 40px;
        margin: 40px;
        width: 300px;
        height: 150px;        
        }
        .alternate {
          box-sizing: border-box;
        }
  </style> 
</head>
<body>
    <div class="box">I use the standard box model. (box-sizing: content-box; - default)</div>
    <div class="box alternate">I use the alternate box model. (box-sizing: border-box)</div>
</body>
</html>


## Margins, padding, and borders

[Margins, padding, and borders](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#margins_padding_and_borders)



#### The box model and inline boxes
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_box_model_and_inline_boxes

All of the above fully applies to block boxes. Some of the properties can apply to inline boxes too, such as those created by a `<span>` element.

In the example below, we have a `<span>` inside a paragraph. We have applied a width, height, margin, border, and padding to it. You can see that the width and height are ignored. The top and bottom margin, padding, and border are respected but don't change the relationship of other content to our inline box. The padding and border overlap other words in the paragraph. The left and right padding, margins, and borders move other content away from the box.

Source:

``` 
<!DOCTYPE html>
<head>
  <style>    
        span {
            margin: 20px;
            padding: 20px;
            width: 80px;
            height: 50px;
            background-color: lightblue;
            border: 2px solid blue;
            color: black;
            }
  </style> 
</head>
<body>
   <p>
      I am a paragraph and this is a <span>span</span> inside that paragraph. A  span is an inline element and so does not respect width and height.
    </p>
</body>
</html>
```


Result:

<!DOCTYPE html>
<head>
  <style>    
        span {
            margin: 20px;
            padding: 20px;
            width: 80px;
            height: 50px;
            background-color: lightblue;
            border: 2px solid blue;
            color: black;
            }
  </style> 
</head>
<body>
   <p>
      I am a paragraph and this is a <span>span</span> inside that paragraph. A  span is an inline element and so does not respect width and height.
    </p>
</body>
</html>


## Using display: inline-block
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#using_display_inline-block

display: inline-block is a special value of display, which provides a middle ground between inline and block. Use it if you do not want an item to break onto a new line, but do want it to respect width and height and avoid the overlapping seen above.

An element with display: inline-block does a subset of the block things we already know about:

The width and height properties are respected.
padding, margin, and border will cause other elements to be pushed away from the box.
It does not, however, break onto a new line, and will only become larger than its content if you explicitly add width and height properties.

In this next example, we have added display: inline-block to our `<span>` element. Try changing this to display: block or removing the line completely to see the difference in display models.


``` 
<!DOCTYPE html>
<head>
  <style>    
        span {
            margin: 20px;
            padding: 20px;
            width: 80px;
            height: 50px;
            background-color: lightblue;
            border: 2px solid blue;
            display: inline-block;
            }
  </style> 
</head>
<body>
   p>
    I am a paragraph and this is a <span>span</span> inside that paragraph. A span is an inline element and so does not respect width and height.
    </p>
</body>
</html>
```


Result:

<!DOCTYPE html>
<head>
  <style>    
        span {
            margin: 20px;
            padding: 20px;
            width: 80px;
            height: 50px;
            background-color: lightblue;
            border: 2px solid blue;
            display: inline-block;
            }
  </style> 
</head>
<body>
   <p>
    I am a paragraph and this is a <span>span</span> inside that paragraph. A span is an inline element and so does not respect width and height.
    </p>
</body>
</html>


Where this can be useful is when you want to give a link a larger hit area by adding padding. `<a>` is an inline element like `<span>`; you can use display: inline-block to allow padding to be set on it, making it easier for a user to click the link.

You see this fairly frequently in navigation bars. The navigation below is displayed in a row using flexbox and we have added padding to the `<a>` element as we want to be able to change the background-color when the `<a>` is hovered. The padding appears to overlap the border on the `<ul>` element. This is because the `<a>` is an inline element.


Add display: inline-block to the rule with the .links-list a selector, and you will see how it fixes this issue by causing the padding to be respected by other elements.


``` 
<!DOCTYPE html>
<head>
  <style>    
        span {
            margin: 20px;
            padding: 20px;
            width: 80px;
            height: 50px;
            background-color: lightblue;
            border: 2px solid blue;
            display: inline-block;
            }
  </style> 
</head>
<body>
   p>
    I am a paragraph and this is a <span>span</span> inside that paragraph. A span is an inline element and so does not respect width and height.
    </p>
</body>
</html>
```


Result:

<!DOCTYPE html>
<head>
  <style>    
        .links-list a {
            background-color: rgb(179 57 81);
            color: #fff;
            text-decoration: none;
            padding: 1em 2em;
            display: inline-block;               
        }
        .links-list a:hover {
            background-color: rgb(66 28 40);
            color: #fff;
        }
        ul {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
            border: 1px solid #000;
        }
        li {
            margin: 5px;
        }    
  </style> 
</head>
<body>
   <nav>
    <ul class="links-list">
        <li><a href="">Link one</a></li>
        <li><a href="">Link two</a></li>
        <li><a href="">Link three</a></li>
  </ul>
</nav>
</body>
</html>


## Summary

The display property specifies the display behavior (the type of rendering box) of an element.


- ### display: inline
**inline** Displays an element as an inline element (like `<span>`). Any height and width properties will have no effect. This is default. `span, em,b`. 

- ### display: block

**block** Displays an element as a block element (like `<p>`). It starts on a new line, and takes up the whole width.
`div, section, p`.

- ### display: inline-block
**inline-block** Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values.


See full list of property values in https://www.w3schools.com/cssref/pr_class_display.php