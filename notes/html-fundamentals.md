# HTML Fundamentals

- [HTML Fundamentals](#html-fundamentals)
  - [Anatomy of HTML](#anatomy-of-html)
    - [Tag Syntax](#tag-syntax)
    - [HTML Document](#html-document)
  - [HTML Elements](#html-elements)
    - [Important](#important)
    - [Typography](#typography)
    - [Comments](#comments)
    - [Lists](#lists)
    - [Images](#images)
    - [Hyperlinks](#hyperlinks)
    - [Stucturing HTML Document](#stucturing-html-document)

**HTML** Stands for HyperText Markup Language.

It is a markup langage that web developers use to **structure and describe the content** of a webpage

HTML consists of elements(a.k.a Tags) that describe different types of content.

Web browsers parses the HTML structure and **render HTML code** onto the screen.

## Anatomy of HTML

### Tag Syntax

---

Basic Anatomy of HTML tags is an **opening tag** the **content** and the **closing tag**.

_Some elements contain no content and the **closing tag** can be ommitted_

`<p>Text content</p>`

An example of a self closing tag are `img`'s

`<img src="placeholder.jpg" />`

### HTML Document

---

- The `<!DOCTYPE html>` tag indicate browsers the type of document (html5).
- After specifying the document type we start building the actual html structure.
- The first element should always be the `<head>` element.
  - This element is not rendered.
- The `<body>` tag is where elements that should be rendered should be included.

## HTML Elements

### Important

---

We can specify the language for the html document by using the `lang` attribute

```html
<html lang="en">
  <!-- Rest of the code goes here -->
</html>
```

We can also specify the character set uset in the `meta` tag

```html
<html lang="en">
  <head>
    <meta charset="UTF-8" />
  </head>
  <body></body>
  <!-- Rest of the code goes here -->
</html>
```

### Typography

---

For headings we have 6 different tags

|  Tags  |                     Semantic Meaning                      |
| :----: | :-------------------------------------------------------: |
|   h1   |       Top level heading. Usually only one per page        |
|   h2   | Subheading more important than the ones below. (Multiple) |
|   h3   | Subheading more important than the ones below. (Multiple) |
|   h4   | Subheading more important than the ones below. (Multiple) |
|   h5   | Subheading more important than the ones below. (Multiple) |
|   h6   |       Subheading least important of all. (Multiple)       |
|   b    |           Font Weight bold. No semantic meaning           |
| strong |       Should use over `b` tag for semantic reasons        |
|   i    |           Italizices text. No semantic meaning            |
|   em   |  Emphasis. Should use over `i` tag for semantic reasons   |

### Comments

---

To comment code in HTML use the following syntax `<!-- code goes here -->`

### Lists

---

| tag | Semantic Meaning |
| :-: | :--------------: |
| ol  |   Ordered List   |
| ul  |  Unordered List  |
| li  |    List Item     |

We have 2 types of lists in html

- Ordered Lists

- Unordered Lists

The `<ol>` and `<ul>` tag by themselves only specify the type of list.
To actually specify the items inside it we use the `<li>` tag.

### Images

---

Images are a self closing tag and do not contain children.

By default they are considered `display:inline-block;` more on this later.

**Always** provide an `alt` attribute for SEO purposes and Screen readers

### Hyperlinks

---

Hyperlinks allow us to link to other resources.

We can indicate the reference by using the `href` attribute

- To open link in a new tab `target='_blank'`
- To create a reference to an external URL provide entire URL
- To link to another file you can provide the relative route to the file. i.e. `href="./about.html"`
- To link to other parts of the page you can use the `id` i.e. `href="#section-1"`

### Stucturing HTML Document

---

There are some tags that allow us to specify or group elements that are related either semantically or based on the content.

|   tag   | Semantic meaning                                                                                                                                                 |
| :-----: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   nav   | Used to group up links and site navigation                                                                                                                       |
| header  | Introductory information of the page and section                                                                                                                 |
| article | Define content that could stand independently of the page (i.e. one product in a product list). <br/> A self contained item that can be used in various contexts |
|  main   | contains the main content (also called the body) of the page.                                                                                                    |
| section | Grouping nearby content of a similar theme. Not neccesarily self contained, but its part of something else                                                       |
|  aside  | Content that is less important. Often used for complementary but nonessential information                                                                        |
| footer  | Usually indicates contact info, copyright and some site navigation                                                                                               |
|   div   | Generic tag to group elements together. Has no semantic meaning                                                                                                  |
| figure  | Also used for images inside cards.                                                                                                                               |
