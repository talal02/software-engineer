# **Lesson 7: Transforms - Revision Notes**

---

## **1. Introduction to Transforms**

- **Purpose**: CSS transforms allow elements to be repositioned, resized, and altered in 2D or 3D space.
- **Types**:
  - **2D Transforms**: Work on the x (horizontal) and y (vertical) axes.
  - **3D Transforms**: Work on the x, y, and z (depth) axes.
- **Browser Support**: Use vendor prefixes (`-webkit-`, `-moz-`, `-o-`) for better compatibility.

---

## **2. Transform Syntax**

- **Basic Syntax**:

  ```css
  transform: function(value);
  ```

- **Vendor Prefixes**:

  ```css
  div {
    -webkit-transform: scale(1.5);
    -moz-transform: scale(1.5);
    -o-transform: scale(1.5);
    transform: scale(1.5);
  }
  ```

---

## **3. 2D Transforms**

- **Rotate**:
  - Rotates an element clockwise (positive) or counterclockwise (negative).

  ```css
  transform: rotate(45deg);
  ```

- **Scale**:
  - Resizes an element. Values less than 1 shrink, values greater than 1 enlarge.

  ```css
  transform: scale(1.5); /* Scales uniformly */
  transform: scaleX(0.5); /* Scales horizontally */
  transform: scaleY(1.2); /* Scales vertically */
  transform: scale(0.5, 1.2); /* Scales both axes */
  ```

- **Translate**:
  - Moves an element along the x and y axes.

  ```css
  transform: translateX(20px); /* Moves horizontally */
  transform: translateY(-10px); /* Moves vertically */
  transform: translate(20px, -10px); /* Moves both axes */
  ```

- **Skew**:
  - Distorts an element along the x and y axes.

  ```css
  transform: skewX(15deg); /* Skews horizontally */
  transform: skewY(-10deg); /* Skews vertically */
  transform: skew(15deg, -10deg); /* Skews both axes */
  ```

---

## **4. Combining Transforms**

- Multiple transforms can be combined in a single declaration.

  ```css
  transform: rotate(45deg) scale(1.2) translate(10px, 20px);
  ```

---

## **5. Transform Origin**

- **Purpose**: Changes the point around which transformations occur.

- **Syntax**:

  ```css
  transform-origin: x-axis y-axis;
  ```

- **Examples**:

  ```css
  transform-origin: 0 0; /* Top-left corner */
  transform-origin: 100% 100%; /* Bottom-right corner */
  transform-origin: 20px 50px; /* Custom position */
  ```

---

## **6. Perspective**

- **Purpose**: Adds depth to 3D transformations.
- **Syntax**:
  - **Individual Element**:

    ```css
    transform: perspective(200px) rotateX(45deg);
    ```

  - **Parent Element**:

    ```css
    .parent {
      perspective: 200px;
    }
    .child {
      transform: rotateX(45deg);
    }
    ```

- **Perspective Depth**:
  - Higher values create a less intense 3D effect.
  - Lower values create a more intense 3D effect.

  ```css
  transform: perspective(100px) rotateX(45deg);
  ```

- **Perspective Origin**:
  - Sets the vanishing point for 3D transforms.

  ```css
  perspective-origin: 50% 50%; /* Default */
  perspective-origin: 0 0; /* Top-left */
  ```

---

## **7. 3D Transforms**

- **Rotate**:
  - Rotates an element around the x, y, or z axis.

  ```css
  transform: rotateX(45deg); /* Rotates around x-axis */
  transform: rotateY(45deg); /* Rotates around y-axis */
  transform: rotateZ(45deg); /* Rotates around z-axis */
  ```

- **Scale**:
  - Scales an element along the z-axis.

  ```css
  transform: scaleZ(1.5);
  ```

- **Translate**:
  - Moves an element along the z-axis.

  ```css
  transform: translateZ(50px); /* Moves closer */
  transform: translateZ(-50px); /* Moves further */
  ```

---

## **8. Transform Style**

- **Purpose**: Controls how nested 3D transforms are rendered.
- **Values**:
  - `preserve-3d`: Allows nested elements to maintain their 3D space.
  - `flat`: Forces nested elements to lie flat in 2D space.

  ```css
  .parent {
    transform-style: preserve-3d;
  }
  ```

---

## **9. Backface Visibility**

- **Purpose**: Controls whether the backside of a rotated element is visible.
- **Values**:
  - `visible`: Shows the backside (default).
  - `hidden`: Hides the backside.

  ```css
  backface-visibility: hidden;
  ```

---

## **10. Key Examples**

- **2D Cube**:

  ```css
  .cube {
    transform: rotate(-45deg) skew(15deg, 15deg);
  }
  ```

- **3D Cube**:

  ```css
  .cube {
    transform: translateZ(-100px);
    transform-style: preserve-3d;
  }
  .front {
    transform: translateZ(100px);
  }
  .back {
    transform: rotateX(180deg) translateZ(100px);
  }
  ```

---

## **11. Best Practices**

- **Use Vendor Prefixes**: Ensures compatibility across browsers.
- **Combine Transforms**: Apply multiple transformations in a single declaration.
- **Optimize Perspective**: Adjust perspective depth for desired 3D effect.
- **Test Backface Visibility**: Use `hidden` to hide elements facing away.

---

## **12. Summary of Key Properties**

- **2D Transforms**: `rotate()`, `scale()`, `translate()`, `skew()`.
- **3D Transforms**: `rotateX()`, `rotateY()`, `rotateZ()`, `translateZ()`, `scaleZ()`.
- **Perspective**: `perspective`, `perspective-origin`.
- **Transform Style**: `preserve-3d`, `flat`.
- **Backface Visibility**: `visible`, `hidden`.
