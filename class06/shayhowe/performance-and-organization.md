# Lesson 1 Notes: Performance & Organization

## Overview

In this lesson, we focus on improving website performance and organizing code effectively. A well-structured codebase and optimized performance are crucial for faster development and better user experience.

---

## Key Topics

### 1. **HTML**

- **Minify & Compress Files**: Reduce file size by removing unnecessary characters (e.g., spaces, comments).
- **Cache Common Files**: Store frequently used files (like CSS, JS) in the browser cache to reduce load times on repeat visits.

---

### 2. **CSS**

- **Strategy & Structure**: Organize CSS files logically for better maintainability.
- **Performance-Driven Selectors**: Use efficient CSS selectors to improve rendering speed.
- **Reusable Code**: Write modular and reusable CSS to reduce redundancy.
- **Reduce HTTP Requests**: Combine files and use techniques like image sprites to minimize server requests.

---

## Detailed Breakdown

### **Strategy & Structure**

- Organize CSS into logical directories:
  - **Base**: Common styles (e.g., `normalize.css`, `layout.css`, `typography.css`).
  - **Components**: UI elements (e.g., `buttons.css`, `forms.css`).
  - **Modules**: Page sections (e.g., `header.css`, `footer.css`).

Example Structure:

```plaintext
# Base
  – normalize.css
  – layout.css
  – typography.css

# Components
  – buttons.css
  – forms.css
  – nav.css

# Modules
  – header.css
  – footer.css
```

---

### **CSS Methodologies**

1. **Object-Oriented CSS (OOCSS)**:
   - **Separate Structure from Skin**: Keep layout and theme styles separate.
   - **Separate Content from Container**: Avoid dependency on parent elements.

   Example:

   ```html
   <div class="alert alert-error">
     <p class="msg">...</p>
   </div>
   ```

   ```css
   .alert {...}
   .alert-error {...}
   .msg {...}
   ```

2. **Scalable & Modular Architecture for CSS (SMACSS)**:
   - Categories: Base, Layout, Module, State, Theme.
   - Example:

     ```html
     <div class="alert is-error">
       <p>...</p>
     </div>
     ```

     ```css
     .alert {...}
     .alert.is-error {...}
     ```

---

### **Performance-Driven Selectors**

- **Keep Selectors Short**: Avoid long, overly specific selectors.
  - Bad: `header nav ul li a {...}`
  - Good: `.primary-link {...}`

- **Favor Classes**: Use classes for better reusability and lower specificity.
  - Bad: `#container header nav {...}`
  - Good: `.primary-nav {...}`

---

### **Reusable Code**

- Combine shared styles to reduce redundancy.
  - Bad:

    ```css
    .news { background: #eee; border-radius: 5px; }
    .social { background: #eee; border-radius: 5px; }
    ```
  - Good:

    ```css
    .news, .social { background: #eee; border-radius: 5px; }
    ```

---

### **Minify & Compress Files**

- Use tools to minify CSS, JS, and HTML.
- Enable **gzip compression** on the server to reduce file sizes.

---

### **Reduce HTTP Requests**

- **Combine Like Files**: Merge CSS and JS files into single files.
  - Bad:

    ```html
    <link href="css/reset.css" rel="stylesheet">
    <link href="css/base.css" rel="stylesheet">
    ```

  - Good:

    ```html
    <link href="css/styles.css" rel="stylesheet">
    ```

- **Image Sprites**: Combine multiple images into one to reduce requests.
  - Example:

    ```css
    .icon { background: url("sprite.png") 0 0 no-repeat; }
    .icon-home { background-position: -16px 0; }
    ```

- **Data URIs**: Embed small images directly in CSS/HTML.
  - Example:

    ```css
    div { background: url("data:image/png;base64,..."); }
    ```

---

### **Cache Common Files**

- Set **expires headers** to cache files for a specific duration.
  - Example:

    ```plaintext
    ExpiresByType text/css "access plus 1 year"
    ExpiresByType application/javascript "access plus 1 year"
    ```

---

## Key Takeaways

1. **Organize Code**: Use a logical structure for CSS (Base, Components, Modules).
2. **Optimize Selectors**: Keep them short and favor classes for better performance.
3. **Reuse Code**: Combine shared styles to reduce redundancy.
4. **Minify & Compress**: Reduce file sizes for faster loading.
5. **Reduce HTTP Requests**: Combine files, use sprites, and cache resources.
