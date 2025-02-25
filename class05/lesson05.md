# Lesson 5: Learn CSS Layout 🚀  

## **Agenda:**  
✅ Learn - Box Model
✅ Learn - Simple Layout
✅ Lab - Create a Simple Layout
✅ Homework - 3 Simple Layouts

---

## 🌍 **Learn - Box Model**

### What is Box Model?
- Every element in HTML is a box.
- Box model is concered with why things take up space and how to control that space.
- Box model is a way to understand how elements are laid out on a page.
- Let's have a section with 100px height and 100px width.  
  ![Box Model](images/box-model.png)
- Going horizontally we have width, padding, border.
- Going vertically we have height, padding, border.
- Margin is the space outside the border.
- Lets give this border 5px solid red.
![Box Model](images/box-model-2.png)
- How wide is this model now? 
  `100px (width) + 10px (border) = 110px`
- How tall is this model now? 
  `100px (height) + 10px (border) = 110px`
- Let's add padding on right side of 20px (Green).
- Padding is inside the border and pushes the content away from the border.
![Box Model](images/box-model-3.png)
- How wide is this model now? 
  `100px (width) + 10px (border) + 20px (padding) = 130px`
- If I have 300px wide section, how many of above sections can I fit in?
  `300px / 130px = 2`
- So, if I have 3rd it will go to the next line.

### Time for Some Layouts
- Let's talk about float...
- Flexbox and Grid are far better than float.
- But, float is still used in some cases. So, let's learn it.
- Let's create a simple layout with float.
- Float needs percentages, so we need to set width in percentage.
- Whenever you use float, they will fight as hard as possible to go to the right or left corner.

### 15 Minutes of PAIN
- We got a header, footer and 3 sections.
- Each section is 300px tall.
![Simple Layout](images/box-model-4.png)
- We need 3 sections next to each other maybe 33% width.
```html
<body>
  <header>Header</header>
  <section>Section 1</section>
  <section>Section 2</section>
  <section>Section 3</section>
  <footer>Footer</footer>
</body>
```
```css
header, footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
}
section {
  float: left;
  width: 33%;
  height: 300px;
  background-color: #f4f4f4;
  border: 1px solid #ccc;
}
```
