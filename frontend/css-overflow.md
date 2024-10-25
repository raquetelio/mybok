# CSS Overflow
https://www.w3schools.com/cssref/pr_pos_overflow.php

The overflow property specifies what should happen if content overflows an element's box.

This property specifies whether to clip content or to add scrollbars when an element's content is too big to fit in a specified area.

Note: The overflow property only works for block elements with a specified height.


Eg.
overflow:hidden/scroll/auto


## CSS Syntax
`overflow: visible|hidden|clip|scroll|auto|initial|inherit;`


## Property Values

| Value	|Description |
| ------ | ------- |
| visible |	The overflow is not clipped. It renders outside the element's box. This is default	
| hidden	| The overflow is clipped, and the rest of the content will be invisible. Content canbe scrolled programmatically (e.g. by setting scrollLeft or scrollTo())	
| clip	| The overflow is clipped, and the rest of the content will be invisible. Forbids scrolling, including programmatic scrolling.	
| scroll | The overflow is clipped, but a scroll-bar is added to see the rest of the content.
| auto	| If overflow is clipped, a scroll-bar should be added to see the rest of the content.
| initial |	Sets this property to its default value.
| inherit |	Inherits this property from its parent element.