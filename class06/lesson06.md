# Lesson 06: Review HTML & CSS 🚀

## **What You'll Learn**

- **Review**: HTML Fundamentals
- **Review**: CSS Fundamentals
- **Review**: Box Model
- **Review**: Float 😱
- **Review**: Three Simple Layouts
- **Learn**: Responsive Basics
- **Homework**: Build a Simple Responsive Site

---

## 📚 **Review - HTML Fundamentals**

- **The Golden Rule**: Separation of Concerns
  - HTML = Content, CSS = Style, JavaScript = Behavior
- **HTML Syntax**:

  ```html
  <p class="intro">Hello, World!</p>
  ```

  - `<p>` is the opening tag, `</p>` is the closing tag.
  - `class` is an attribute, and `"intro"` is its value.
- **Common HTML Tags**:
  - **Headings**: `<h1>` to `<h6>` (importance decreases from `h1` to `h6`)
  - **Text Elements**: `<p>` (paragraph), `<span>` (inline text), `<pre>` (preformatted text)
  - **Structural Elements**: `<div>`, `<section>`, `<article>`, `<aside>`, `<header>`, `<footer>`, `<nav>`
- **Example: Marking Up the BBC News Homepage**
  ![BBC News](./bbc.png)

---

## 🎨 **Review - CSS Fundamentals**

- **Where Does CSS Go?**
  - Inline: Applied directly to an element (not recommended for maintainability).
  - Internal: Defined in the `<head>` within a `<style>` tag.
  - External: A separate CSS file linked in the `<head>` (best practice).

  ```html
  <link rel="stylesheet" href="styles.css">
  ```

- **CSS Syntax**:

  ```css
  p {
    color: red;
    font-weight: bold;
  }
  ```

  - `'red'` is a **value**, `'color'` is a **property**, `'color: red;'` is a **declaration**.
  - `p {}` is a **rule**, and everything inside `{}` is the **declaration block**.
- **Why Use a Separate CSS File?**
  - Improves **separation of concerns**, **reusability**, and **maintainability**.
- **Basic CSS Properties**:
  - **Colors**: Named (yellow), Hex (`#ff0`), RGBA (`rgb(255, 255, 0, 1)`), HSLA (`hsl(60, 100%, 50%, 1)`).
  - **Fonts**: `font-family`, `font-size`, `font-weight`.
- **Resources**:
  - [MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS)
  - [Advanced HTML & CSS by Shay Howe](https://learn.shayhowe.com/advanced-html-css/)
- **Practice**: `basic-css-two` (Follow-along materials)

---

## 📦 **Review - CSS Relationships**

- **Direct Child Selector (`>`)**:

  ```css
  section > p {
    color: red;
  }
  ```

- **Descendant Selector (Any Level)**:

  ```css
  section p {
    color: red;
  }
  ```

- **Adjacent Sibling Selector (`+`)**:

  ```css
  p + p {
    color: red;
  }
  ```

- **Practice**: `relationship-css-two` (Follow-along materials)

---

## 📦 **Review - IDs and Classes**

- **IDs (`#`)**: Unique identifiers, should only be used once per page.

  ```css
  #zebra {
    color: red;
  }
  ```

- **Classes (`.`)**: Reusable, can be applied to multiple elements.

  ```css
  .bob {
    color: red;
  }
  ```

- **Specificity**:
  - **Inline**: 1000 points
  - **ID**: 100 points
  - **Class**: 10 points
  - **Element**: 1 point
- **Practice**: `specificity-practice` (Follow-along materials)

---

## 📦 **Review - Box Model**

![Box Model](./box-model.png)

- **Everything in HTML is a box**:
  - **Content**: The actual text or image inside the element.
  - **Padding**: Space between content and border.
  - **Border**: Surrounds the padding and content.
  - **Margin**: Space outside the element’s border.
- **Box Sizing**:
  - `content-box` (default)
  - `border-box` (includes padding and border in width/height calculations)

  ```css
  * {
    box-sizing: border-box;
  }
  ```

- **Box Model Example**
![Box Model Example](./box-model-example.png)
- **Practice**: `box-model-practice` (Follow-along materials)

---

## 📦 **Review - Float**

- **Floats were used for layouts before Flexbox and Grid.**
- **How Floats Work**:
  - Removes an element from normal document flow.
  - Used to **wrap text around images**.
  - Previously used for creating columns and layouts.
- **Issues with Float-Based Layouts**:
  - Fixed-width designs were not responsive.
  - Required additional clearing techniques (`clear: both;`).
- **Moving Towards Responsive Design**:
  - **Media Queries** help adjust styles for different screen sizes.

  ```css
  @media screen and (max-width: 600px) {
    h1 {
      background-color: blue;
    }
  }
  ```

- **Practice**: Create layouts using float before moving to Flexbox & Grid.

---

## 📱 **Introduction to Responsive Design**

- **Making websites work across devices (mobile, tablet, desktop).**
- Will be covering in upcoming lessons:

---

## 🏠 **Homework**

✅ **Make 15 minutes of pain responsive (use floats and 3 media queries)** – [Preview Here](https://communitytaught.org/img/resources/15-min-pain.png)  
✅ **Read Shay Howe: Advanced (all 10)** – [Advanced HTML & CSS](https://learn.shayhowe.com/advanced-html-css/)  

---
