# **Lesson 3: Complex Selectors - Revision Notes**

---

## **1. Introduction to Selectors**

- **Purpose**: Selectors determine how styles are applied to elements on a webpage.
- **Evolution**: CSS3 introduced new selectors, expanding the possibilities for styling.

---

## **2. Common Selectors**

- **Type Selector**: Selects elements by their type (e.g., `h1`, `p`).
- **Class Selector**: Selects elements by their class attribute (e.g., `.tagline`).
- **ID Selector**: Selects elements by their unique ID attribute (e.g., `#intro`).

**Example**:

```css
h1 { ... }          /* Type Selector */
.tagline { ... }    /* Class Selector */
#intro { ... }      /* ID Selector */
```

---

## **3. Child Selectors**

- **Descendant Selector**: Selects elements nested within an ancestor (e.g., `article h2`).
- **Direct Child Selector**: Selects elements that are direct children of a parent (e.g., `article > p`).

**Example**:

```css
article h2 { ... }  /* Descendant Selector */
article > p { ... } /* Direct Child Selector */
```

---

## **4. Sibling Selectors**

- **General Sibling Selector**: Selects siblings that follow an element (e.g., `h2 ~ p`).
- **Adjacent Sibling Selector**: Selects the sibling directly following an element (e.g., `h2 + p`).

**Example**:

```css
h2 ~ p { ... }  /* General Sibling Selector */
h2 + p { ... }  /* Adjacent Sibling Selector */
```

---

## **5. Attribute Selectors**

- **Attribute Present**: Selects elements with a specific attribute (e.g., `a[target]`).
- **Attribute Equals**: Selects elements with an exact attribute value (e.g., `a[href="http://google.com"]`).
- **Attribute Contains**: Selects elements with an attribute containing a value (e.g., `a[href*="login"]`).
- **Attribute Begins With**: Selects elements with an attribute starting with a value (e.g., `a[href^="https://"]`).
- **Attribute Ends With**: Selects elements with an attribute ending with a value (e.g., `a[href$=".pdf"]`).
- **Attribute Spaced**: Selects elements with an attribute containing a space-separated value (e.g., `a[rel~="tag"]`).
- **Attribute Hyphenated**: Selects elements with a hyphen-separated attribute value (e.g., `a[lang|="en"]`).

**Example**:

```css
a[target] { ... }                   /* Attribute Present */
a[href="http://google.com"] { ... } /* Attribute Equals */
a[href*="login"] { ... }            /* Attribute Contains */
a[href^="https://"] { ... }         /* Attribute Begins With */
a[href$=".pdf"] { ... }             /* Attribute Ends With */
a[rel~="tag"] { ... }               /* Attribute Spaced */
a[lang|="en"] { ... }               /* Attribute Hyphenated */
```

---

## **6. Pseudo-classes**

- **Link Pseudo-classes**: Style links based on their state.
  - `:link`: Unvisited links.
  - `:visited`: Visited links.
- **User Action Pseudo-classes**: Style elements based on user interaction.
  - `:hover`: When the user hovers over an element.
  - `:active`: When the user clicks on an element.
  - `:focus`: When the element is focused (e.g., via keyboard navigation).
- **UI State Pseudo-classes**: Style form elements based on their state.
  - `:enabled`: Enabled form elements.
  - `:disabled`: Disabled form elements.
  - `:checked`: Checked checkboxes or radio buttons.
  - `:indeterminate`: Checkboxes or radio buttons in an indeterminate state.
- **Structural Pseudo-classes**: Style elements based on their position in the document tree.
  - `:first-child`: First child of a parent.
  - `:last-child`: Last child of a parent.
  - `:only-child`: Only child of a parent.
  - `:first-of-type`: First element of its type within a parent.
  - `:last-of-type`: Last element of its type within a parent.
  - `:only-of-type`: Only element of its type within a parent.
  - `:nth-child(n)`: Selects elements based on a formula (e.g., `2n+1` for odd elements).
  - `:nth-last-child(n)`: Selects elements from the end of the parent.
  - `:nth-of-type(n)`: Selects elements of a specific type based on a formula.
  - `:nth-last-of-type(n)`: Selects elements of a specific type from the end.
- **Target Pseudo-class**: Styles the element targeted by the URL fragment (e.g., `:target`).
- **Empty Pseudo-class**: Selects elements with no children or text (e.g., `div:empty`).
- **Negation Pseudo-class**: Selects elements that do not match a selector (e.g., `div:not(.awesome)`).

**Example**:

```css
a:link { ... }          /* Link Pseudo-class */
a:hover { ... }         /* User Action Pseudo-class */
input:checked { ... }   /* UI State Pseudo-class */
li:first-child { ... }  /* Structural Pseudo-class */
section:target { ... }  /* Target Pseudo-class */
div:empty { ... }       /* Empty Pseudo-class */
div:not(.awesome) { ... } /* Negation Pseudo-class */
```

---

## **7. Pseudo-elements**

- **Textual Pseudo-elements**:
  - `:first-letter`: Styles the first letter of text.
  - `:first-line`: Styles the first line of text.
- **Generated Content Pseudo-elements**:
  - `:before`: Inserts content before an element.
  - `:after`: Inserts content after an element.
- **Fragment Pseudo-element**:
  - `::selection`: Styles text selected by the user.

**Example**:

```css
.alpha:first-letter { ... }  /* Textual Pseudo-element */
a:after { content: " (" attr(href) ")"; } /* Generated Content */
::selection { background: #ff7b29; } /* Fragment Pseudo-element */
```

---

## **8. Selector Performance**

- **Best Practices**:
  - Avoid overly complex selectors.
  - Use efficient selectors (e.g., classes over deep descendant selectors).
  - Test selector performance across browsers.

---

## **9. Browser Support**

- **Compatibility**: Some selectors may not work in older browsers (e.g., IE6-8).
- **Tools**:
  - **CSS3 Selectors Test**: Check browser support for selectors.
  - **Selectivizr**: Adds support for advanced selectors in older IE versions.

---

## **10. Key Takeaways**

- **Common Selectors**: Type, class, and ID selectors are foundational.
- **Child & Sibling Selectors**: Allow precise targeting of nested elements.
- **Attribute Selectors**: Provide flexibility for styling based on attributes.
- **Pseudo-classes**: Enable dynamic styling based on element state or position.
- **Pseudo-elements**: Allow styling of specific parts of an element or adding content.
- **Performance**: Optimize selectors for faster page rendering.
