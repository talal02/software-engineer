# Lesson 2: HTML Deep Dive 🚀

**Agenda**: Let's build better websites! Today we'll review HTML basics, learn new tags, and code a brownie recipe + newspaper layout. 🍫📰

---

## 🌟 Key Takeaways
- **HTML = Structure & Content** (CSS handles styling!)
- **Semantic HTML** = Better Accessibility + SEO 🦮🔍
- Always check [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)!

---

## 🧠 HTML Basics Refresher

### Syntax 101
```html
<tagname>Content</tagname>
```

### Golden Rules 🏆
1. Use **semantic tags** for:
   - Screen readers 🎧
   - SEO rankings 📈
   - Proper content structure 🏗️
2. One `<h1>` per page (like a book title!)
3. Google won't love your site if tags are misused 😢

---

## 🆕 HTML Tags Crash Course

### Essential Tags
| Tag       | Purpose                          | Example                      |
|-----------|-----------------------------------|------------------------------|
| `<a>`     | Hyperlinks (king of the web!) 👑 | `<a href="url">Click</a>`    |
| `<h1-h6>` | Headings (h1=most important)      | `<h1>Top News</h1>`          |
| `<p>`     | Paragraphs                        | `<p>Hello world!</p>`        |
| `<ol>`/`<ul>` | Numbered/Bulleted Lists      | `<ul><li>Milk</li></ul>`     |

### Text Formatting ✍️
```html
<em>Italic (for emphasis)</em>
<strong>Bold (super important)</strong>
<br> <!-- Line break -->
<hr> <!-- Horizontal line -->
```

### HTML5 Superstars 🌟
| Tag         | Use Case                          |
|-------------|------------------------------------|
| `<section>` | Group related content              |
| `<article>` | Independent content (blog post)    |
| `<aside>`   | Side content (like fun facts)      |
| `<header>`  | Intro content (logo/nav)           |
| `<footer>`  | Closing content (contact info)     |

---

## 🚫 Avoid These Deprecated Tags
- `<blink>` 😵 (RIP blinking text)
- `<marquee>` 🏃‍♂️ (Scrolling text)
- `<b>`/`<i>` → Use CSS instead! 🎨

*Fun Fact: Many devs started coding on Neopets! 🐾 Leon says: "If anyone doubts you, tell them to go to hell — they probably began with Neopets too!"*

---

## 🛠️ Coding Best Practices

### Pro Tips 💡
1. **Wrap all content** in appropriate tags
2. **Comments** are your friends:
   ```html
   <!-- This helps later-you understand code -->
   ```
3. **Progressive Enhancement**:
   - Start with basic HTML
   - Add CSS/JS later  
   → Works on all browsers! 🌍

---

## 🍫 Brownie Recipe Challenge
**From Class Materials**: [Recipe File](https://drive.google.com/file/d/178XnAGdNHHgF0O1b1zNgTEQpJHGu7RMc/view?usp=sharing)

**Tips**:
- Use proper headings (`h1` for recipe title)
- Organize ingredients with `<ul>`/`<li>`
- Wrap steps in `<ol>`

---

## 📰 Newspaper Project
**Your Mission**: Create a news layout using:
- `<header>` for masthead
- `<article>` for main story
- `<aside>` for related articles
- `<footer>` for contact info

*Remember: Structure first, perfection later! Your code can be "vomity" (Leon's words 😜) as long as it works!*

---

## 💪 Homework
1. Build BBC-News layout
2. Explore [MDN HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
3. Read [Shay Howe: Learn to Code (all 12)](https://learn.shayhowe.com/html-css/)
