# Lesson 3: Mastering More HTML 🚀  

**Agenda:**  
✅ Review: Client-Server Model & HTML Basics  
✅ Brownie Recipe Walkthrough 🍫  
✅ New HTML Tags & Forms  
✅ Progressive Enhancement: Build Better Websites  
✅ Hands-on Coding: News Layout & Khan Academy Clone  

---

## 🌍 Understanding the Client-Server Model  

- Websites work by **sending requests** (client) and **receiving responses** (server).  
- What technology makes this possible? **HTTP** (HyperText Transfer Protocol).  
- Think of it as ordering food:  
  - You (client) order a pizza (request).  
  - The restaurant (server) prepares and delivers it (response).  

---

## 🎨 The Golden Rule: Separation of Concerns  

1️⃣ **HTML** → Structure & Content  
2️⃣ **CSS** → Styling & Visual Design  
3️⃣ **JavaScript** → Behavior & Interactivity  

Each plays a unique role—keep them separate for cleaner, maintainable code!  

---

## 🏗️ HTML Syntax 101  

```html
<p class="my-paragraph">This is a paragraph</p>
```
- **Opening tag:** `<p>`  
- **Closing tag:** `</p>`  
- **Text Content:** `"This is a paragraph"`  
- **Attribute:** `class="my-paragraph"` (adds extra info to the element)  

💡 **Why follow proper syntax?**  
1. **Better User Experience** → Consistency across browsers  
2. **Accessibility** → Screen readers for visually impaired users  
3. **SEO (Search Engine Optimization)** → Helps Google rank your site higher  

---

## 🍫 Brownie Recipe Deep Dive  

**How to add an image?**  
1. **Download** the image  
2. **Store** it in your project folder  
3. **Use the `<img>` tag:**  

```html
<img src="brownie.jpg" alt="Delicious chocolate brownies">
```
✅ `src` → Image file location  
✅ `alt` → Alternative text (important for accessibility!)  

---

## 🚀 Uploading Your First Code to Glitch  

Want to share your work online? Glitch makes it easy!  

1. **Create a Glitch account**  
2. **Start a new project**  
3. **Copy & paste your HTML code**  
4. **Upload images** in the "Assets" folder  
5. **Get the image URL** from Glitch  
6. 🎉 **Boom! Your first webpage is live!**  

🔗 **Now, share your link with friends!**  

---

## 📜 HTML Page Structure  

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Info for the browser (metadata, styles, scripts) -->
  </head>
  <body>
    <!-- Everything users see -->
    <h1>Hello World</h1>
  </body>
</html>
```
- `<head>` = **Behind-the-scenes info** (title, links, scripts)  
- `<body>` = **Everything visible on the webpage**  
- **Analogy:** You can **see and interact** with a person's body, but not their thoughts (head).  

👀 **Fun Fact:** Everything in the Brownie Recipe was inside the `<body>` tag!  

---

## 🌟 New HTML Tags  

### 🧭 **Navigation Bar (`<nav>`)**  

```html
<nav>
  <ul>
    <li><a href="news.html">News</a></li>
    <li><a href="sports.html">Sports</a></li>
    <li><a href="weather.html">Weather</a></li>
  </ul>
</nav>
```
✅ Helps users navigate your site  
✅ Essential for structuring **menus & links**  

---

### 📋 **How to Collect User Input? (`<form>`)**  

Forms let users enter data like emails, passwords, and feedback!  

```html
<form action="submit.html" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="username">
  <button type="submit">Submit</button>
</form>
```
📝 **Common Input Types:**  
- `text` → For names & messages  
- `email` → Email input  
- `password` → Hidden password field  
- `radio` & `checkbox` → Multiple choice options  
- `submit` → Button to send data  

---

## 🚀 What is Progressive Enhancement?  

🛠️ **Build websites in layers:**  
1. **Start with HTML** → Focus on content first!  
2. **Add CSS** → Make it look amazing  
3. **Enhance with JavaScript** → Add animations & interactivity  

💡 **Why?** Even if CSS/JS fails, the core content remains accessible!  

---

## 🎯 Homework  

🚀 **Challenge yourself!** Recreate the HTML structure of these websites:  

📌 **TechCrunch Layout** → ![TechCrunch](https://communitytaught.org/img/resources/techcrunch.png)  
📌 **Khan Academy Layout** → ![Khan Academy](https://communitytaught.org/img/resources/khan-academy.png)  

📖 **Reading:** [Learn Layout](https://learnlayout.com/)  

---

## 🛟 Feeling Stuck? Try This!  

✅ **Ask for help in Discord** 💬  
✅ **Rewatch the lesson video** 📺  
✅ **Experiment! Mess around with the code** 🧪  
✅ **Check MDN Docs** → [MDN HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)
