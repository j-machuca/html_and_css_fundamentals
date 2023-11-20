# Flexbox

To arrange the containing elements(knows as flex items) using flexbox we need to set the `display` property to `flex` on the parent container(also know as flex container).

- When we set the display property to flex by default the `flex-direction` is set to `row`.
- Elements inside the container will be as wide as their element's content.
- Elements inside the container will be as high as the highest element.

## Alignment using Flexbox

Items in flexbox are position based on 2 axis.

- The main axis(`justify-content`)
- The cross axis (`align-items`)

## Flex Container

We can set properties to the container to control how the items inside it behave.

1. **gap:** Create space between items,without using margins

   - `gap:0`

2. **justify-content**: Align items along the main axis.

   - `flex-start`
   - `flex-end`
   - `center`
   - `space-between`
   - `space-around`
   - `space-evenly`

3. **align-items:** Align items along the cross axis.

   - `stretch`
   - `flex-start`
   - `flex-end`
   - `center`
   - `baseline`

4. **flex-direction:** set the main axis

   - `row`
   - `row-reverse`
   - `column`
   - `column-reverse`

5. **flex-wrap:** allow items to wrap into a new line if they exceed container's width.

   - `nowrap`
   - `wrap`
   - `wrap-reverse`

6. **align-content:** Used when wrap is enabled to determine the behavior of items.

   - `stretch`
   - `flex-start`
   - `flex-end`
   - `center`
   - `space-between`
   - `space-around`

## Flex Items

We can set properties on the items to control how they are rendered.

1. **align-self:** Overwrites the `align-items` property of the container for this item.

   - `auto`
   - `stretch`
   - `flex-start`
   - `flex-end`
   - `center`
   - `baseline`

2. **flex-grow:** set the ratio at which the flex item should grow by in relation to other items to occupy the remaining space.

   - `flex-grow: 0`

3. **flex-shrink:** set the ratio at which the flex item should shrink by in relation to other items to fit the available space. Default `1`.

   - `flex-shrink: 1`

4. **flex-basis:** sets the initial main size of a flex item.

   - `flex-basis:200px`

5. **order:** can be used to change display order w/out changing source code. By default all itmes have a default value of `0`.

   - `order: integer`

### Shorthand

There is a shorthand version to avoid using `grow`,`shrink`, and `basis` as separate rules.

Using the `flex` property we can set values for all of them in one go.

```css
/* flex: grow shrink basis */
rule {
  flex: 0 1 auto;
}
```
