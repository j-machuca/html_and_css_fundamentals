# CSS Theory

- [CSS Theory](#css-theory)
  - [Cascade and Specificity](#cascade-and-specificity)
  - [Inheritance](#inheritance)
  - [Box Model](#box-model)
    - [Basic formula to calculate sizes](#basic-formula-to-calculate-sizes)
    - [Collapsing Margins](#collapsing-margins)
  - [Types of elements](#types-of-elements)
  - [Rendering Box](#rendering-box)
    - [Block](#block)
    - [Inline](#inline)
    - [Inline Block](#inline-block)
    - [Flex](#flex)
    - [Grid](#grid)

## Cascade and Specificity

CSS resolves what rules are going to be applied taking in consideration 2 things:

- **Specificity** will determine the precedence the rule has over others. The rule with the highest specificity will take presedence over the lower ones.
- **Order** is important since the last rule with the same specificity will determine what value a property will have.
- To ignore CSS specificity resolution and disregard specificity CSS gives us the `!important` keyword to override the property/value.

```css
/* ID-Class-Type 1-1-1  */
#about .section a {
  /* Your properties go here */
}
```

## Inheritance

Some styles and properties get inherited from their parent.
_Most properties that are inherited are the ones regarding text._

The universal selector (`*`) allows us to set properties to all elements but they DO NOT get inherited.

## Box Model

CSS uses a box model to determine the size of each element.
Each element's size is determined by the values of the following:

- Content
  - The actual content of the element
- Width
  - The specified width. If not specified the width of the content will determine it
- Height
  - The specified height. If not specified the width of the content will determine it
- Padding
  - The whitespace that surrounds the content
- Border
  - A line surrounding the element
- Margin
  - The space between elements
- Fill Area
  - Area that goes from the center up to the border.

### Basic formula to calculate sizes

CSS default calculations use the following formulas. (`box-sizing:border-box;`)

- width `width = left border + left padding + width + right padding + right border`

- height `height = top border + top padding + height + bottom padding + bottom border`

To change how to calculate the element's size to be of the width we specify we change the `box-sizing` property and assign the value of `border-box`

### Collapsing Margins

The top and bottom margins of blocks are sometimes combined (collapsed) into a single margin whose size is the largest of the individual margins(or just one if they're equal). [MDN Docs reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_box_model/Mastering_margin_collapsing)
_Margin of floating and absolutely positioned elements never collapse_

This occurs in 3 basic cases

- Adjacent Siblings
  - The margins of adjacent siblings are collapsed.
- No content separating parent and descendants
- Empty blocks

## Types of elements

In CSS we can specify the type of element we want.

## Rendering Box

We can set different values to the `display` property in css to change the was the element is rendered.

The most common values are:

- block
- inline
- inline-block
- flex
- grid

### Block

Displays an element as a block element (like `<p>`). It starts on a new line, and takes up the whole width

### Inline

Displays an element as an inline element (like `<span>`). Any height and width properties will have no effect

### Inline Block

Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values

### Flex

Displays an element as a block-level flex container

### Grid

Displays an element as a block-level grid container
