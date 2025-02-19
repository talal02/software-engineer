# Lesson 4: Learn CSS 🚀  

**Agenda:**  
✅ Learn - CSS Fundamentals
✅ Learn - Parent / Child Selectors
✅ Hint At - Classes & IDs
✅ Learn - Specificity
✅ Lab - Style a Simple Site

---

## 🌍 Learn - CSS Fundamentals

- CSS is the language for styling web pages and it stands for Cascading Style Sheets.
Where does CSS go?
- CSS can go in a separate file or in the `<head>` of an HTML file or maybe even inline with the HTML.
- Why you should put styles in head?
- Only if you work at Amazon, why? every time you load a page, the browser has to download the CSS file, so if you have a lot of CSS, it can slow down the page load time. Whatever comes in first fold of website should be in head to reduce the load time. Everything else can go in the separate file.
- It's the best practice to put CSS in a separate file.
How?
- You can link the CSS file in the head of the HTML file using the `<link>` tag.
```html
<link rel="stylesheet" href="css/styles.css">
```
- We are going into css folder, from where our current html file is, and then we are going into styles.css file.

### CSS Syntax
- It's a markup language, so it has a specific syntax.
- It consists of a selector, property, and value.
- Here's an example:
```css
p {
  color: red;
  font-size: 16px;
}
```
- Here `p` is the selector, which selects the HTML element you want to style.
- `color` is the property, which is the style you want to apply.
- `red` is the value, which is the color you want to apply.
- You're writing a rule here, which is a combination of property and value.
- Each rule has a declaration block, which is the property and value inside the curly braces `{}`.
- You can have multiple declarations in a rule.
- You can have multiple rules in a CSS file.
- In above example rule, we have two declarations, one declaration is `color: red;` and other is `font-size: 16px;`. These are two declarations in a declaration block, and this declaration block is inside the curly braces `{}`. This is a rule.
- This can be asked in interview, what is a rule? A rule is a combination of property and value, and it has a declaration block inside the curly braces `{}`.

- CSS is read from top to bottom, so if you have two rules that conflict, the one that comes last will be applied.
- This is called the **Cascading** part of CSS.
- This is why it's called Cascading Style Sheets.
```css
p {
  color: red;
}
p {
  color: blue;
}
```
- In above example, the color of the paragraph will be blue, because the last rule is `color: blue;`.

### Let's learn simple CSS
- Color
- 4 Main Ways to color in CSS
  - Color Name
  - Hex Code
  - RGB
  - HSL
```css
p {
  color: yellow; # Color Name
}
p {
  color: #ffff00; # Hex Code
}
p {
  color: rgb(255, 255, 0); # RGB
}
p {
  color: hsl(75, 50%, 50%); # HSL
}
```
- Using only color name will end up with limited colors, so we use hex code, RGB, and HSL.
- Professionaly rgba and hex color are most used.

- Font Family
- html
```html
<head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto">
</head>
```
- css
```css
p {
  font-family: 'Roboto', sans-serif;
}
```

- You shall always have link tag before the css file link tag in the head of the html file. Again cascading, if you have css file link tag before the link tag of the font, then the font will not be applied.
- Fall back font is `sans-serif`, if the font is not available, then the browser will use the `sans-serif` font.
- Go to fonts.google.com, select a font, and then copy the link tag and paste it in the head of the html file in order to use that font.
- Make sure to have weight of the font, if you want to use a specific weight of the font, then you can add that in the link tag. For speed you should use only the weight you need.

- Need Help with CSS?
- Use MDN Web Docs, it's the best resource for CSS.
- How to research CSS?
- Google "concept name + MDN", and you will get the MDN link.
- Also, you can use https://learn.shayhowe.com, it's a great resource for learning CSS.

### Let's Code
- Download the class04 materials from this link https://drive.google.com/file/d/1nb5QadNC2Z1x2oqH9zIMZFVbYjarM5Br/view
- Open the class04 folder in VS Code.