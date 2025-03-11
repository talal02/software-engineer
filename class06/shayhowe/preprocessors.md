# **Lesson 5: Preprocessors - Revision Notes**

---

## **1. Introduction to Preprocessors**

- **Purpose**: Preprocessors simplify and enhance HTML and CSS by adding features like variables, nesting, and mixins.
- **Popular Preprocessors**:
  - **Haml**: A markup language that compiles to HTML.
  - **Sass/SCSS**: A stylesheet language that compiles to CSS.

---

## **2. Haml (HTML Abstraction Markup Language)**

- **Goal**: Write clean, DRY (Don’t Repeat Yourself), and well-structured HTML.
- **Installation**:
  - Requires Ruby.
  - Install Haml using the command:  

    ```bash
    gem install haml
    ```

  - Compile Haml to HTML:  

    ```bash
    haml index.haml index.html
    ```

---

### **Haml Syntax**

1. **Doctype**:
   - Use `!!! 5` for HTML5.

   ```haml
   !!! 5
   ```

   ```html
   <!DOCTYPE html>
   ```

2. **Elements**:
   - Use `%` to declare elements.
   - Indentation defines nesting.

   ```haml
   %body
     %header
       %h1 Hello World
   ```

   ```html
   <body>
     <header>
       <h1>Hello World</h1>
     </header>
   </body>
   ```

3. **Attributes**:
   - Use `{}` for Ruby-style or `()` for HTML-style attributes.

   ```haml
   %img{src: "shay.jpg", alt: "Shay Howe"}
   ```

   ```html
   <img src="shay.jpg" alt="Shay Howe">
   ```

4. **Classes & IDs**:
   - Use `.` for classes and `#` for IDs.

   ```haml
   %section.feature
   %section#hello
   ```

   ```html
   <section class="feature"></section>
   <section id="hello"></section>
   ```

5. **Comments**:
   - Use `/` for HTML comments and `-#` for silent comments (not rendered in HTML).

   ```haml
   / This is a comment
   -# This is a silent comment
   ```

6. **Filters**:
   - Use filters like `:javascript`, `:css`, or `:sass` to embed code.

   ```haml
   :javascript
     alert('Hello World');
   ```

---

## **3. Sass & SCSS**

- **Sass**: A strict, indented syntax.
- **SCSS**: A more flexible syntax similar to CSS.
- **Installation**:
  - Requires Ruby.
  - Install Sass using the command:  

    ```bash
    gem install sass
    ```

  - Compile Sass/SCSS to CSS:  

    ```bash
    sass styles.sass styles.css
    ```

  - Watch for changes:  

    ```bash
    sass --watch styles.sass:styles.css
    ```

---

### **Sass/SCSS Features**

1. **Nesting**:
   - Nest selectors for better readability.

   ```scss
   .container {
     width: 960px;
     p {
       color: #333;
     }
   }
   ```

2. **Variables**:
   - Define reusable values.

   ```scss
   $font-base: 1em;
   $primary-color: #ff7b29;

   p {
     font-size: $font-base;
     color: $primary-color;
   }
   ```

3. **Mixins**:
   - Reusable blocks of styles.

   ```scss
   @mixin border-radius($radius) {
     -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
     border-radius: $radius;
   }

   .box {
     @include border-radius(10px);
   }
   ```

4. **Extends**:
   - Share styles between selectors.

   ```scss
   .alert {
     padding: 10px;
     border: 1px solid #ccc;
   }

   .alert-error {
     @extend .alert;
     background: #f2dede;
   }
   ```

5. **Functions**:
   - Perform calculations or manipulate values.

   ```scss
   @function calculate-width($col) {
     @return $col * 100px;
   }

   .col-3 {
     width: calculate-width(3);
   }
   ```

6. **Loops & Conditionals**:
   - Use `@for`, `@each`, `@while`, and `@if` for dynamic styles.

   ```scss
   @for $i from 1 through 3 {
     .col-#{$i} {
       width: 100px * $i;
     }
   }
   ```

7. **Imports**:
   - Combine multiple files into one.

   ```scss
   @import "normalize";
   @import "grid";
   ```

---

## **4. Other Preprocessors**

- **Less**: Similar to Sass but uses JavaScript for compilation.
- **Stylus**: A flexible preprocessor with optional syntax (no braces or semicolons).
- **PostCSS**: A tool for transforming CSS with JavaScript plugins.

---

## **5. Key Takeaways**

- **Haml**: Simplifies HTML by removing closing tags and enforcing structure with indentation.
- **Sass/SCSS**: Enhances CSS with features like variables, nesting, mixins, and functions.
- **Preprocessors**: Improve efficiency, maintainability, and organization of code.
- **Best Practices**:
  - Use variables for reusable values.
  - Use mixins for reusable styles.
  - Use extends to share styles between selectors.
  - Organize code with imports.
