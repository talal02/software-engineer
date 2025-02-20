# Lesson 4: Learn CSS 🚀  

## **Agenda:**  
✅ CSS Fundamentals  
✅ Parent / Child Selectors  
✅ Introduction to Classes & IDs  
✅ Understanding Specificity  
✅ Lab - Style a Simple Site  

---

## 🌍 **CSS Fundamentals**

### What is CSS?
CSS (Cascading Style Sheets) is the language used to style web pages, giving them color, layout, and design.

### **Where Does CSS Go?**
1. **External CSS (Best Practice)** – Stored in a separate `.css` file and linked in the `<head>`.
   ```html
   <link rel="stylesheet" href="css/styles.css">
   ```
2. **Internal CSS** – Placed inside `<style>` tags within the `<head>`.
3. **Inline CSS** – Written directly within an HTML tag using `style` attributes.
   ```html
   <p style="color: red;">Hello!</p>
   ```
4. **Amazon’s Approach** – Keep critical styles in the `<head>` to speed up page rendering.

### **CSS Syntax**
CSS follows a simple syntax:
```css
selector {
  property: value;
}
```
Example:
```css
p {
  color: red;
  font-size: 16px;
}
```
- `p` → **Selector** (targets paragraph elements)
- `color` → **Property** (what you want to change)
- `red` → **Value** (new style)

### **Understanding Cascading**
CSS reads styles **top to bottom**. If multiple rules apply to an element, the last rule wins.
```css
p {
  color: red;
}
p {
  color: blue;
}
```
The paragraph will be **blue** because the last rule overrides the first.

### **Ways to Define Colors**
1. **Named Colors**
   ```css
   color: yellow;
   ```
2. **Hex Codes**
   ```css
   color: #ffff00;
   ```
3. **RGB**
   ```css
   color: rgb(255, 255, 0);
   ```
4. **HSL**
   ```css
   color: hsl(60, 100%, 50%);
   ```
🔹 **Hex & RGB are the most commonly used in professional projects.**

### **Fonts & Google Fonts**
1. Link a Google Font in your `<head>`:
   ```html
   <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto">
   ```
2. Apply the font in CSS:
   ```css
   p {
     font-family: 'Roboto', sans-serif;
   }
   ```
3. **Tip:** Always place the font link **before** your CSS file link for proper loading.

---

## 🎯 **Selecting Elements by Relationship**

### **Parent > Child Selector**
Targets **direct** child elements.
```css
section > p {
  color: red;
}
```
```html
<section>
  <p>Hello, World!</p> <!-- Selected -->
</section>
```

### **Parent Space Child Selector**
Targets **all** children inside the parent.
```css
section p {
  color: blue;
}
```
```html
<section>
  <article>
    <p>Hello, World!</p> <!-- Selected -->
  </article>
</section>
```

### **Sibling Selector (`+`)**
Selects an **adjacent sibling**.
```css
p + p {
  color: green;
}
```
```html
<section>
  <p>First paragraph</p>
  <p>Second paragraph</p> <!-- Selected -->
</section>
```

---

## 🔥 **Classes & IDs**

### **ID Selector (`#`)**
IDs are **unique** and should only be used once per page.
```css
#zebra {
  color: red;
}
```
```html
<p id="zebra">This is unique!</p>
```

### **Class Selector (`.`)**
Classes can be used multiple times.
```css
.robot {
  color: blue;
}
```
```html
<p class="robot">Hello, Twitch!</p>
<p class="robot">Hello, YouTube!</p>
```

### **Specificity Rules**
1. **Element (p, h1, div)** → **1 point**
2. **Class (`.class`)** → **10 points**
3. **ID (`#id`)** → **100 points**
4. **Inline Styles (`style=""`)** → **1000 points**
5. **`!important`** → Overrides all other styles!

🚨 **Avoid inline styles!** They are hard to override and maintain.

---

## 🎯 **Let's Code!**

1. **Download Materials:** [Lesson 4 Resources](https://drive.google.com/file/d/1nb5QadNC2Z1x2oqH9zIMZFVbYjarM5Br/view)
2. **Open in VS Code** (Use the `class04` folder).
3. **Skip live server for now** – manually refresh the browser to see changes.

---

## 🏠 **Homework**
✅ **Simple Site Lab** – [Preview Here](https://communitytaught.org/img/resources/simple-site-lab.png)  
✅ **Read CSS Layout Basics** – [Learn Layout](https://learnlayout.com)  

📌 **Pro Tip:** Use **MDN Web Docs** for reference: [Google "CSS + MDN"](https://developer.mozilla.org/en-US/docs/Web/CSS)

🚀 Happy Coding! 🎨

