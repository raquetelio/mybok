# CSS position

https://developer.mozilla.org/en-US/docs/Web/CSS/position

The position CSS property sets how an element is positioned in a document. The top, right, bottom, and left properties determine the final location of positioned elements.

See [Try it](https://developer.mozilla.org/en-US/docs/Web/CSS/position#try_it).


## position: static. 
The element is positioned according to the [Normal Flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow) of the document. The top, right, bottom, left, and z-index properties have no effect. This is the default value.

## position: relative

The element is positioned according to the normal flow of the document, and then **offset relative to itself** based on the values of top, right, bottom, and left. The offset does not affect the position of any other elements; thus, the space given for the element in the page layout is the same as if position were static.

This value creates a new stacking context when the value of z-index is not auto. Its effect on table-*-group, table-row, table-column, table-cell, and table-caption elements is undefined.

## position: absolute

The element is **removed from the normal document flow**, and no space is created for the element in the page layout. The element is **positioned relative to its closest positioned ancestor (if any) or to the initial containing block**. Its final position is determined by the values of top, right, bottom, and left.

This value creates a new stacking context when the value of z-index is not auto. The margins of absolutely positioned boxes do not collapse with other margins.


## position: fixed
The element is **removed from the normal document flow, and no space is created for the element in the page layout**. The element is positioned relative to its initial containing block, which is the viewport in the case of visual media. Its final position is determined by the values of top, right, bottom, and left.

This value always creates a new stacking context. In printed documents, the element is placed in the same position on every page.


## position: sticky
The element is positioned according to the **normal flow of the document, and then offset relative to its nearest scrolling ancestor and containing block** (nearest block-level ancestor), including table-related elements, based on the values of top, right, bottom, and left. The offset does not affect the position of any other elements.

This value always creates a new stacking context. Note that a sticky element "sticks" to its nearest ancestor that has a "scrolling mechanism" (created when overflow is hidden, scroll, auto, or overlay), even if that ancestor isn't the nearest actually scrolling ancestor.

_Note: At least one inset property (top, inset-block-start, right, inset-inline-end, etc.) needs to be set to a non-auto value for the axis on which the element needs to be made sticky. If both inset properties for an axis are set to auto, on that axis the sticky value will behave as relative._