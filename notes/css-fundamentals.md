# CSS Fundamentals

- [CSS Fundamentals](#css-fundamentals)
  - [Common structure](#common-structure)
  - [CSS Environments](#css-environments)
  - [Selectors](#selectors)
  - [Text Styling](#text-styling)
  - [Colors](#colors)
  - [Pseudo Classes](#pseudo-classes)
  - [Pseudo Elements](#pseudo-elements)

**CSS** stands for Cascading Style Sheets.

It is used to describe the **visual style and presentation** of the **content written in HTML**

It consists of rules that set **properties** for given elements in the HTML.

## Common structure

The basic structure of a CSS rule is made of the following.

- Selector
- Declaration block
- Properties
- Values

```css
h1 {
  color: blue;
  text-align: center;
  font-size: 20px;
}
```

## CSS Environments

There are 3 ways we can write our CSS

- Inline (applied directly on the element).
- Internal (using the `style` tag inside the `head` tag in the html code).
- External (`link`ing the external css file to the html document).

## Selectors

There are different ways we can select elements to create our CSS rules. Check out the [MDN docs on CSS selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_selectors) for the complete list.

|  Selector Type   |        Syntax        | Use Case                                           |
| :--------------: | :------------------: | :------------------------------------------------- |
|     Multiple     | `selector, selector` | create a rule for multiple selectors               |
|    Descendant    |    `parent child`    | Select all children that are descendants of parent |
|      child       |   `parent > child`   | Select a direct child of parent                    |
|      by ID       |        `#id`         | Select an element by its id                        |
|     by class     |       `.class`       | Select an element that has a `class`               |
|    Universal     |         `*`          | Select all elements                                |
| Adjacent Sibling |       `a + b`        | Select the adjacent sibling                        |
| General Sibling  |       `a ~ b`        | will select all `b`s that are a sibling to `a`     |

## Text Styling

Some of the most common properties used to style text are:

|    property    | use case                                    |
| :------------: | :------------------------------------------ |
|   font-size    | set the size of the text                    |
|  font-family   | set the font to be used                     |
| text-transform | Control capitalization of the text          |
|   font-style   | style the font face (i.e. italic)           |
|  line-height   | Determine the size of the text content area |
|   text-align   | Align content horizontally                  |

## Colors

Colors in CSS can be represented is several ways. Some of them are

- RGB / RGBA
- HSL / HSLA
- HEX / HEXA
- color keywords

## Pseudo Classes

A Pseudo class is a keyword added to a selector that specifies a special state of the selected element(s).

Some of the most common Pseudo classes are:

| Pseudo class | Use case                                                                                                  |
| :----------: | :-------------------------------------------------------------------------------------------------------- |
|   :active    | Matches when an item is being activated by the user. For example, when the item is clicked on             |
|    :hover    | Matches when a user designates an item with a pointing device                                             |
|    :focus    | Matches when an element has focus                                                                         |
|   :checked   | Elements such as checkboxes and radio buttons are toggled on                                              |
|  :nth-child  | Select elements from a list of sibling elements                                                           |
| :first-child | Select the first of its siblings                                                                          |
| :last-child  | Select the last of its siblings                                                                           |
| :nth-of-type | select elements from a list of sibling elements that match a certain type from a list of sibling elements |
|   :visited   | Matches links that have been visited.                                                                     |

## Pseudo Elements

Pseudo Elements let you style a specific part of the selected element(s).

**Double colons (`::`)** are used for pseudo-elements.

The complete list of pseudo elements can be found [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements#list_of_pseudo-elements)

Most common pseudo elements are

- `::before`
- `::after`
