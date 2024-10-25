# Flexbox


Crea layouts flexibles y responsivos organizando elementos automáticamente.

https://www.w3schools.com/css/css3_flexbox.asp

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox


Created to solve problems with `float` (which should be avoided)

**The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.**

The flexible box layout module (usually referred to as flexbox) is a one-dimensional layout model for distributing space between items and includes numerous alignment capabilities.

When we describe flexbox as being one-dimensional we are describing the fact that flexbox deals with layout in one dimension at a time — either as a row or as a column. This can be contrasted with the two-dimensional model of CSS Grid Layout, which controls columns and rows together.

# The two axes of flexbox

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox#the_two_axes_of_flexbox

When working with flexbox you need to think in terms of two axes — the main axis and the cross axis. The main axis is defined by the flex-direction property, and the cross axis runs perpendicular to it. Everything we do with flexbox refers back to these axes, so it is worth understanding how they work from the outset.

## The main axis
The main axis is defined by flex-direction, which has four possible values:

row
row-reverse
column
column-reverse
Should you choose row or row-reverse, your main axis will run along the row in the inline direction.

![Main axis row](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox/basics1.svg)

If flex-direction is set to row the main axis runs along the row in the inline direction.

Choose column or column-reverse and your main axis will run in the block direction, from the top of the page to the bottom.
![Main axis column](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox/basics2.svg)

If flex-direction is set to column the main axis runs in the block direction.

## The cross axis
The cross axis runs perpendicular to the main axis. Therefore, if your flex-direction (main axis) is set to row or row-reverse the cross axis runs down the columns.

![Cross axis - row](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox/basics3.svg)

If flex-direction is set to row then the cross axis runs in the block direction.


If your main axis is column or column-reverse then the cross axis runs along the rows.

![Cross axis - column](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox/basics4.svg)

If flex-direction is set to column then the cross axis runs in the inline direction.


## Summary

### display: flex

Flexbox with 100% of block space.

### display: inline-flex

Flexbox with minimum space.


### flex-direction

- flex-direction: row; (_default_)| row-reverse;
- flex-direction: column; | column-reverse;

### flex-wrap

- flex-wrap: nowrap; (_default_) + overflow=> hidden scroll
- wrap; -> creates new rows/columns
- wrap-reverse; -> creates new rows/columns from the beginning


### justify-content
The justify-content property is used to align the items on the main axis, the direction in which flex-direction has set the flow.
Organizacion of items inside the container.

- flex-start.
- flex-end.
- center. 
- space-between. -> equidistant to 1º and last.
- space-around. -> equidistant with 1º and last with half the space.
- space-evenly. -> all equidistant.


### align-content
The align-content property sets the distribution of space between and around content items along a flexbox's cross axis.


- flex-start.
- flex-end.
- center. 
- strech.
- space-between.
- space-around.

### align-items
The align-items property align all the flex items on the cross axis.

- flex-start.
- flex-end.
- center. 
- strech.
- baseline.

## CSS Flex items
https://www.w3schools.com/css/css3_flexbox_items.asp 

### Child Elements (Items)
The direct child elements of a flex container automatically becomes flexible (flex) items.


### The order Property
The order property specifies the order of the flex items.

The first flex item in the code does not have to appear as the first item in the layout.

The order value must be a number, default value is 0.

```
<div class="flex-container">
  <div style="order: 3">1</div>
  <div style="order: 2">2</div>
  <div style="order: 4">3</div> 
  <div style="order: 1">4</div>
</div>
```


<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
  display: flex;
  align-items: stretch;
  background-color: #f1f1f1;
}
.flex-container>div {
  background-color: DodgerBlue;
  color: white;
  width: 100px;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
</style>
</head>
<body>

<h1>The order Property</h1>

<p>Use the order property to sort the flex items as you like:</p>

<div class="flex-container">
  <div style="order: 3">1</div>
  <div style="order: 2">2</div>
  <div style="order: 4">3</div> 
  <div style="order: 1">4</div>
</div>

</body>
</html>


### The flex-grow Property
The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items.

The value must be a number, default value is 0.

Example
Make the third flex item grow eight times faster than the other flex items:

``` 
<div class="flex-container">
  <div style="flex-grow: 1">1</div>
  <div style="flex-grow: 1">2</div>
  <div style="flex-grow: 8">3</div>
</div>
```
<div class="flex-container">
  <div style="flex-grow: 1">1</div>
  <div style="flex-grow: 1">2</div>
  <div style="flex-grow: 8">3</div>
</div>

### The flex-shrink Property
The flex-shrink property specifies how much a flex item will shrink relative to the rest of the flex items.

The value must be a number, default value is 1.

Example
Do not let the third flex item shrink as much as the other flex items:

```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-shrink: 0">3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
</div>
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-shrink: 0">3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
</div>

### The flex-basis Property
The flex-basis property specifies the initial length of a flex item.


Example
Set the initial length of the third flex item to 200 pixels:

```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-basis: 200px">3</div>
  <div>4</div>
</div>
```

<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-basis: 200px">3</div>
  <div>4</div>
</div>

### The flex Property
The flex property is a shorthand property for the flex-grow, flex-shrink, and flex-basis properties.


Example
Make the third flex item not growable (0), not shrinkable (0), and with an initial length of 200 pixels:

```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex: 0 0 200px">3</div>
  <div>4</div>
</div>
```

<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex: 0 0 200px">3</div>
  <div>4</div>
</div>

### The align-self Property
The align-self property specifies the alignment for the selected item inside the flexible container.

**The align-self property overrides the default alignment set by the container's align-items property.**


In these examples we use a 200 pixels high container, to better demonstrate the align-self property:


Example
Align the third flex item in the middle of the container:

```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="align-self: center">3</div>
  <div>4</div>
</div>

```

<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="align-self: center">3</div>
  <div>4</div>
</div>


