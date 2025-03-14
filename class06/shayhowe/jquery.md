# **Lesson 6: jQuery - Revision Notes**

---

## **1. JavaScript Overview**

- **Purpose**: Adds interactivity to websites, enhancing user experience.
- **Placement**: 
  - External file with `.js` extension.
  - Referenced in HTML using `<script>` tag.
  - Best practice: Place before closing `</body>` tag for faster loading.
- **Values & Variables**:
  - **Values**: Strings, Booleans, numbers, `undefined`, `null`, functions, objects.
  - **Variables**: Defined using `var`, `let`, or `const`.
  - Naming convention: `camelCase`.
- **Statements**: Commands executed in sequence, separated by semicolons.
- **Functions**: 
  - Defined using `function` keyword.
  - Can accept arguments and return values.
- **Arrays**: Lists of items stored in `[]`, indexed starting from 0.
- **Objects**: Collections of key-value pairs wrapped in `{}`.

---

## **2. jQuery Overview**

- **Purpose**: Simplifies interaction between HTML, CSS, and JavaScript.
- **Usage**: 
  - Used by 63% of top 10,000 websites.
  - Simplifies DOM manipulation, event handling, and animations.
- **Getting Started**:
  - Reference jQuery in HTML using `<script>` tag.
  - Use CDN for faster loading:

    ```html
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js"></script>
    ```

  - Custom jQuery code should be in a separate file, referenced after jQuery.

---

## **3. jQuery Basics**

- **jQuery Object**: `$` or `jQuery` is used to select elements.
- **Document Ready**: Ensures jQuery runs only after DOM is fully loaded.

  ```javascript
  $(document).ready(function() {
    // jQuery code
  });
  ```

---

## **4. Selectors**

- Mimic CSS selectors for easy element selection.
- Examples:

  ```javascript
  $('.class');          // Class selector
  $('element');         // Element selector
  $('parent child');    // Descendant selector
  $('selector1, selector2'); // Multiple selector
  $('element[attribute="value"]'); // Attribute selector
  ```

- **`this` Keyword**: Refers to the current element in a handler.

  ```javascript
  $('div').click(function() {
    $(this).addClass('active');
  });
  ```

---

## **5. Traversing**

- **Purpose**: Navigate and filter elements in the DOM.
- **Methods**:
  - **Filtering**: `.filter()`, `.not()`, `.first()`, `.last()`, etc.
  - **DOM Traversal**: `.parent()`, `.children()`, `.find()`, `.siblings()`, etc.
- **Chaining**: Combine multiple methods for precise selection.

  ```javascript
  $('div').not('.type').parent();
  ```

---

## **6. Manipulation**

- **Attributes**: Add, remove, or change element attributes.

  ```javascript
  $('img').attr('alt', 'New Alt Text');
  $('li').addClass('highlight');
  ```

- **Styles**: Manipulate CSS properties.

  ```javascript
  $('div').css('background-color', 'yellow');
  $('header').height(200);
  ```

- **DOM Manipulation**: Add, remove, or move elements.

  ```javascript
  $('section').prepend('<h3>Featured</h3>');
  $('h1').text('Hello World');
  ```

---

## **7. Events**

- **Purpose**: Trigger actions based on user interactions.
- **Event Methods**:
  - `.click()`, `.hover()`, `.on()`, etc.

  ```javascript
  $('li').click(function() {
    $(this).addClass('selected');
  });
  ```

- **Event Delegation**: Use `.on()` for dynamic elements.

  ```javascript
  $('ul').on('click', 'li', function() {
    $(this).toggleClass('active');
  });
  ```

---

## **8. Effects**

- **Purpose**: Add animations and transitions.
- **Basic Effects**:
  - `.show()`, `.hide()`, `.toggle()`

  ```javascript
  $('.error').show('slow');
  ```

- **Fading Effects**:
  - `.fadeIn()`, `.fadeOut()`, `.fadeToggle()`

  ```javascript
  $('.notice').fadeOut('slow');
  ```

- **Sliding Effects**:
  - `.slideDown()`, `.slideUp()`, `.slideToggle()`

  ```javascript
  $('.panel').slideToggle('fast');
  ```

- **Custom Animations**:
  - Use `.animate()` for custom CSS animations.

  ```javascript
  $('div').animate({ opacity: 0.5, height: '+=50px' }, 1000);
  ```

---

## **9. jQuery UI**

- **Purpose**: Extends jQuery with additional interactions, widgets, and effects.
- **Features**:
  - Advanced easing options.
  - Widgets like date pickers, sliders, and accordions.
  - Custom animations and effects.

---

## **10. Key Methods Summary**

- **Selectors**: `$()`, `.find()`, `.filter()`
- **Traversing**: `.parent()`, `.children()`, `.siblings()`
- **Manipulation**: `.attr()`, `.css()`, `.text()`, `.append()`, `.remove()`
- **Events**: `.click()`, `.on()`, `.hover()`
- **Effects**: `.show()`, `.hide()`, `.fadeIn()`, `.slideToggle()`

---

## **11. Best Practices**

- **Minify jQuery**: Use minified version for production.
- **Use CDN**: Improves loading speed and caching.
- **Separate Concerns**: Keep HTML, CSS, and JavaScript/jQuery in separate files.
- **Optimize Selectors**: Use efficient selectors for better performance.

---

## **12. Example Use Cases**

- **Alert Message**:

  ```javascript
  $('.notice-close').click(function() {
    $('.notice-warning').fadeOut('slow', function() {
      $(this).remove();
    });
  });
  ```

- **Tabs**:

  ```javascript
  $('.tabs-nav a').click(function() {
    $('.tabs-stage div').hide();
    $($(this).attr('href')).show();
  });
  ```
