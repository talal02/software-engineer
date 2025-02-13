# Lesson 3: Learn More HTML 🚀

Agenda:
Review - Client Server Model
Review - HTML Tags
Review - Brownie Recipe
Learn - New HTML Tags
Learn - Progressive Enhancement
Code - Newspaper Time
Code - Khan Academy
Code - Newspaper Time Two

## Review - Client Server Model
- Request and Response are sent between the client and server
- What technology is used to send requests and responses?
- HTTP (HyperText Transfer Protocol)

## The Golden Rule (Separation of Concerns)
- HTML is for content
- CSS is for style
- JavaScript is for behavior / Interaction

## HTML Syntax
```html
<p class="my-paragraph">This is a paragraph</p>
```
- Opening tag: `<p>`
- Closing tag: `</p>`
- Text Content: `This is a paragraph`
- Attribute and its value: `class="my-paragraph"`

## Why follow the syntax?
- 3 Main Things
- General Users (TO have a consistent experience)
- Accessibility (Screen Readers | Some users can't see)
- SEO (Search Engine Optimization)

## Explaining the Brownie Recipe
- How to add image to the recipe?
- Download the image
- Add the image to the folder
- Use the `<img>` tag
- Add the `src` attribute
- Add the `alt` attribute

## How to upload your first code to Glitch?
- Create an account on Glitch
- Create a new project
- Copy and paste your code
- Upload the image in the assets folder
- Get the URL of the image from assets folder
- Wallah! You have your first code on Glitch
- Share the link

## HTML Structure
```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Stuff the browser needs to know about -->
  </head>
  <body>
    <!-- Stuff the user sees -->
     <h1>Hello World</h1>
  </body>
</html>
```
- Parent child relationship being used here
- head and body are children of html
- h1 is a child of body
- You can see someone's body but not whats going on in their head
- You can intereact with someone's body but not with their head
- Every single thing that we coded in brownies recipe is a child of body

## New HTML Tags
- Navigation
```html
<nav>
  <ul>
    <li><a href="news.html">News</a></li>
    <li><a href="sports.html">Sports</a></li>
    <li><a href="weather.html">Weather</a></li>
  </ul>
</nav>
```

### How to get data from the user?
- Form
```html
<form action="submit.html" method="post">
  <!-- Data Collection Elements -->
</form>
```
- Input types - text, email, password, radio, checkbox, submit, button

## Progressive Enhancement
-- Really important concept, we should build website in a way that firstly focus on content that is HTML and then add CSS and JS to make it look good and interactive