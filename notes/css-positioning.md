# Element Positioning

There are several positioning modes in CSS.

- Static (Normal Flow)
- Absolute
- Relative
- Fixed
- Sticky

## Static

Positioned according to the normal flow of the page

## Absolute

Positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

**Note:** Absolute positioned elements are removed from the normal flow, and can overlap elements.

## Relative

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

## Fixed

Always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

## Sticky

Positioned based on the user's scroll position.

A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).
