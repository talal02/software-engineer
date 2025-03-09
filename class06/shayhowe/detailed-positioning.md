# **Lesson 2: Detailed Positioning - Revision Notes**

---

## **1. CSS Positioning Overview**

- **Goal**: Control the layout and positioning of elements on a webpage.
- **Techniques**: Floats, Position Property, Z-Index Property.
- **Choice of Technique**: Depends on the content and layout goals.

---

## **2. Containing Floats**

- **Floats**: Used to position elements side by side or apart.
- **Common Issue**: Parent elements containing floated elements may collapse (height = 0) because floated elements don’t impact the parent’s outer edges.
- **Example**:

  ```html
  <div class="box-set">
    <figure class="box">Box 1</figure>
    <figure class="box">Box 2</figure>
    <figure class="box">Box 3</figure>
  </div>
  ```

  ```css
  .box-set { background: #eaeaed; }
  .box { background: #2db34a; float: left; margin: 1.858736059%; width: 29.615861214%; }

  ```
  - **Problem**: `.box-set` has a height of 0 because all child elements are floated.

---

### **Solutions to Contain Floats**

1. **Empty Element with `clear: both;`**:
   - Add an empty element before the parent’s closing tag with `clear: both;`.
   - **Drawback**: Not semantic; adds unnecessary elements.

2. **Overflow Technique**:
   - Use `overflow: auto;` or `overflow: hidden;` on the parent element.
   - **Drawback**: May crop content (e.g., box shadows, dropdowns) and cause scrollbars in some browsers.

   ```css
   .box-set { overflow: auto; }
   ```

3. **Clearfix Technique**:
   - Use `:before` and `:after` pseudo-elements to clear floats.
   - **Advantage**: More consistent and flexible.
   - **Code**:

     ```css
     .box-set:before, .box-set:after { content: ""; display: table; }
     .box-set:after { clear: both; }
     .box-set { *zoom: 1; }
     ```

4. **Common Practice**:
   - Use a class like `.group` for clearfix and apply it to parent elements.

     ```css
     .group:before, .group:after { content: ""; display: table; }
     .group:after { clear: both; }
     .group { *zoom: 1; }
     ```

---

## **3. Position Property**

- **Values**: `static`, `relative`, `absolute`, `fixed`, `sticky`.
- **Box Offset Properties**: `top`, `right`, `bottom`, `left`.

---

### **Position Values**

1. **Static (Default)**:
   - Elements follow the normal document flow.
   - **Example**:

     ```css
     .box { position: static; }
     ```

2. **Relative**:
   - Elements are positioned relative to their default position.
   - **Box Offsets**: Move the element without affecting surrounding elements.
   - **Example**:

     ```css
     .box { position: relative; top: 20px; left: 40px; }
     ```

3. **Absolute**:
   - Elements are removed from the normal flow and positioned relative to the nearest positioned ancestor (or the body if none exists).
   - **Example**:

     ```css
     .box { position: absolute; top: 6%; left: 2%; }
     ```

4. **Fixed**:
   - Elements are positioned relative to the viewport and do not scroll with the page.
   - **Example**:

     ```css
     .box { position: fixed; bottom: 0; right: 0; }
     ```

5. **Sticky**:
   - Elements toggle between `relative` and `fixed` based on the user’s scroll position.

---

## **4. Z-Index Property**

- **Purpose**: Control the stacking order of elements on the z-axis.
- **Usage**: Requires `position: relative`, `absolute`, or `fixed`.
- **Rule**: Higher `z-index` values appear on top.
- **Example**:

  ```css
  .box-1 { z-index: 1; }
  .box-2 { z-index: 3; } /* Appears on top */
  .box-3 { z-index: 2; }
  ```

---

## **5. Practical Applications**

1. **Fixed Header/Footer**:
   - Use `position: fixed` to create headers or footers that stay visible while scrolling.
   - **Example**:

     ```html
     <footer>Fixed Footer</footer>
     ```

     ```css
     footer { position: fixed; bottom: 0; left: 0; right: 0; }
     ```

2. **Overlapping Elements**:
   - Use `z-index` to control which elements appear on top.

---

## **6. Key Takeaways**

- **Floats**: Useful for layouts but require containment techniques like clearfix.
- **Position Property**: Provides precise control over element placement.
- **Z-Index**: Manages stacking order for overlapping elements.
- **Best Practices**: Choose techniques based on content and maintain consistency.

---

## **7. Common Pitfalls**

- **Floats**: Parent collapse issue; use clearfix or overflow.
- **Overflow Technique**: May crop content or cause scrollbars.
- **Z-Index**: Only works with positioned elements (`relative`, `absolute`, `fixed`).
