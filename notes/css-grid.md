# CSS Grid

It lets you organize content using 2 dimensional layouts and offers many features to simplify the creation of complex layouts.

Allows the developer to divide a container elements into rows and columns.

## Grid Structure

Similar to flexbox we have grid containers and grid items.

## Setting up the grid stucture

We can specifiy the grid structure we want using

- `grid-template-columns`
- `grid-template-rows`
- `gap` also called gutters
  - `column-gap`
  - `row-gap`

Elements will have their height determined automatically to match the tallest element if no value for `grid-template-rows ` are set.

With our new grid structure CSS gives us grid lines that divide the grid container. They range from 1 to the amount of rows or columns + 1.

## Common Grid properties

|       property        | values                                       | use case                                                                                       |
| :-------------------: | -------------------------------------------- | :--------------------------------------------------------------------------------------------- |
|  grid-template-rows   | \<track size\>                               | set the size of the track.                                                                     |
| grid-template-columns | \<track size\>                               | set the size of the track.                                                                     |
|        row-gap        | \<length\>                                   | set the size of the gap between rows                                                           |
|      column-gap       | \<length\>                                   | set the size of the gap between columns                                                        |
|     justify-items     | stretch \| start \| center \| end            | align items inside row track                                                                   |
|      align-items      | stretch \| start \| center \| end            | align items inside column track                                                                |
|      grid-column      | \<start line> / \<endline> \| span \<number> | place a grid item into a specific cell. span keyword allows us to specify the number of cells. |
|       grid-row        | \<start line> / \<endline> \| span \<number> | place a grid item into a specific cell. span keyword allows us to specify the number of cells. |
|     justify-self      | stretch \| start \| center \| end            | allows us to override the container's alignment for a specific item                            |
|      align-self       | stretch \| start \| center \| end            | allows us to override the container's alignment for a specific item                            |

## Dynamic tracks sizes

In order to create dynamic tracks sizes we can use the `fr` unit.
Setting the `grid-template-columns` to `200px 200px 1fr` will make the first two columns have a fixed with of `200px` and the third column will grow to occupy the remaining space.

If the `auto` value is set to a column or row it will only grow to fit its content.

### A nice trick

Using the CSS built-in `repeat` function we can create rows and columns of the same size as well instead of manually typing the sizes for each column/row.

```css
/* create a 2 by 2 grid */
grid-tempalte-columns:repeat(2,1fr)
grid-template-rows: repeat(2,1fr);

/* create a 3 by 3 grid where the first column and row are bigger*/
grid-tempalte-columns: 2fr repeat(2,1fr)
grid-template-rows: 2fr repeat(2,1fr);


```

### Explicit vs Implicit rows

Look for resource on how to style implicit rows.

### Item placement with `grid`

To place items inside the grid we can use the tools provided by CSS making use of the grid lines.

We can specify the values before hand or we can use the `span` keyword to tell CSS that the element should occupy n lines.

|  property   | use case                                                                                       |
| :---------: | :--------------------------------------------------------------------------------------------- |
| grid-column | specify the start line and/or end line for the element. how many columns should it span acorss |
|  grid-row   | specify the start line and/or end line for the element. how many rows should it span acorss    |

```css
my-item {
  /* make the element occupy the cells from line 2 to line 3 */
  grid-column: 2/3;
  /* make the element occupy the cells from line 1 to line 2 */
  grid-row: 1/2;
}
```

### Item Alignment

To align items in the grid CSS gives us several tools.

This will allow us to align the grid tracks inside the container/ distribute empty space.

|    property     | use case                         |
| :-------------: | :------------------------------- |
| justify-content | horizontal alignment             |
|  align-content  | vertical alignment               |
|       gap       | provide whitespace between items |

The following properties allow us to align the items inside the container.

|   property    | use case                                         |
| :-----------: | :----------------------------------------------- |
|  align-items  | same as flexbox. (defaults to `stretch`)         |
| justify-items | same as flexbox. (defaults to `stretch`)         |
|  align-self   | same as flexbox. will override general alignment |
| justify-self  | same as flexbox. will override general alignment |
