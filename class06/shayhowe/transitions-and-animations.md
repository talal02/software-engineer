# **Lesson 8: Transitions & Animations - Revision Notes**

---

## **1. Introduction to Transitions & Animations**

- **Purpose**: CSS transitions and animations allow elements to change styles smoothly over time, enhancing user experience without JavaScript or Flash.
- **Transitions**: Change from one state to another (e.g., hover, focus).
- **Animations**: Define multiple points of transition using keyframes for more complex effects.

---

## **2. Transitions**

- **Trigger**: State changes like `:hover`, `:focus`, `:active`, or `:target`.
- **Properties**:
  - `transition-property`: Specifies which properties to transition.
  - `transition-duration`: Sets the duration of the transition.
  - `transition-timing-function`: Defines the speed curve of the transition.
  - `transition-delay`: Delays the start of the transition.

---

## **3. Transition Properties**

- **`transition-property`**:
  - Specifies the CSS properties to transition.
  - Use `all` to transition all properties.

  ```css
  transition-property: background, border-radius;
  ```

- **`transition-duration`**:
  - Sets how long the transition takes (e.g., `1s`, `500ms`).

  ```css
  transition-duration: 1s;
  ```

- **`transition-timing-function`**:
  - Controls the speed curve of the transition.
  - Common values: `linear`, `ease-in`, `ease-out`, `ease-in-out`.

  ```css
  transition-timing-function: ease-in-out;
  ```

- **`transition-delay`**:
  - Delays the start of the transition.

  ```css
  transition-delay: 0.5s;
  ```

---

## **4. Shorthand Transitions**

- Combine all transition properties into one declaration:

  ```css
  transition: property duration timing-function delay;
  ```

- Example:

  ```css
  transition: background 1s ease-in-out 0.5s;
  ```

---

## **5. Animations**

- **Keyframes**: Define the stages of an animation using `@keyframes`.

  ```css
  @keyframes slide {
    0% { left: 0; }
    50% { left: 50%; }
    100% { left: 100%; }
  }
  ```

- **Animation Properties**:
  - `animation-name`: Name of the keyframes.
  - `animation-duration`: Duration of the animation.
  - `animation-timing-function`: Speed curve of the animation.
  - `animation-delay`: Delay before the animation starts.
  - `animation-iteration-count`: Number of times the animation repeats.
  - `animation-direction`: Direction of the animation (e.g., `normal`, `reverse`).
  - `animation-fill-mode`: Styles applied before/after the animation.
  - `animation-play-state`: Pause or play the animation.

---

## **6. Customizing Animations**

- **`animation-iteration-count`**:
  - Set how many times the animation repeats.
  - Use `infinite` for endless looping.

  ```css
  animation-iteration-count: 3;
  ```

- **`animation-direction`**:
  - Control the direction of the animation.
  - Values: `normal`, `reverse`, `alternate`, `alternate-reverse`.

  ```css
  animation-direction: alternate;
  ```

- **`animation-fill-mode`**:
  - Defines styles before/after the animation.
  - Values: `none`, `forwards`, `backwards`, `both`.

  ```css
  animation-fill-mode: forwards;
  ```

- **`animation-play-state`**:
  - Pause or play the animation.
  - Values: `running`, `paused`.

  ```css
  animation-play-state: paused;
  ```

---

## **7. Shorthand Animations**

- Combine all animation properties into one declaration:

  ```css
  animation: name duration timing-function delay iteration-count direction fill-mode play-state;
  ```

- Example:

  ```css
  animation: slide 2s ease-in-out 0.5s infinite alternate;
  ```

---

## **8. Examples**

- **Transition Example**:

  ```css
  .box {
    background: #2db34a;
    transition: background 1s ease-in-out;
  }
  .box:hover {
    background: #ff7b29;
  }
  ```

- **Animation Example**:

  ```css
  @keyframes slide {
    0% { left: 0; }
    100% { left: 100%; }
  }
  .ball {
    animation: slide 2s ease-in-out infinite;
  }
  ```

---

## **9. Best Practices**

- **Use Vendor Prefixes**: Ensure compatibility across browsers.
- **Optimize Performance**: Avoid animating properties that trigger reflows (e.g., `width`, `height`).
- **Keep It Simple**: Use transitions for simple state changes and animations for complex sequences.

---

## **10. Summary of Key Properties**

- **Transitions**:
  - `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`.
- **Animations**:
  - `@keyframes`, `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`, `animation-play-state`.
