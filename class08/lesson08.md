# Lesson 08: Write Bad CSS

## The Golder Rule: Separation of concerns

- HTML: Content
- CSS: Presentation
- JS: Behavior
- Make sure to keep these separate, for maintainability and scalability.

## CSS
- Where to put CSS?
  - Inline
  - Internal
  - External
- Some keywords to remember
  ```css
  p {
    color: red;
  }
  ```
  - `p` is the selector
  - `color` is the property
  - `red` is the value
  - `color: red;` is the declaration
  - `{}` is the declaration block
  - `p { color: red; }` is the rule
- CSS is read from top to bottom, so the last rule will override the previous ones (Cascading)
- Specificity: The more specific rule will override the less specific one
- Importance: `!important` will override all other rules
- Selecting by Relationship
  - Descendant: `div p { color: red; }`, it will select all `p` elements that are descendants of `div`.
  - Child: `div > p { color: red; }`, it will select all `p` elements that are direct children of `div`.
  - Sibling: `div + p { color: red; }`, it will select the first `p` element that is a sibling of `div`.
  - General Sibling: `div ~ p { color: red; }`, it will select all `p` elements that are siblings of `div`.
- IDs and Classes
  - IDs: `#id { color: red; }`, it will select the element with the ID `id` and can only be used once.
  - Classes: `.class { color: red; }`, it will select all elements with the class `class`.

## The Box Model
- Everything we see on a webpage is a box.
- It includes the content (height and width), padding, border, and margin.
- The box model can be modified using the properties `padding`, `border`, and `margin`.


## Floats
- Floats are difficult to work with but are still important to know.
- Floats are used to position elements to the left or right of their container.
- The `clear` property is used to prevent elements from wrapping around floated elements.
- WARNING, tonight leon wants to dig deep and find inner value, we are going to write some bad cooode.
- Be a baddie, why you should write bad code? 
- Perfection is for closers, we don't wanna spent too much time on this, we want to move fast and break things.
- We are going to write bad code, and then we are going to fix it.
- Layout 1, that we are gonna code is TechCrunch, and we are going to use floats.
- 