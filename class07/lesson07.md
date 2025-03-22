# Lesson 07: Learn Responsive CSS

# Networking

- Just applying to jobs won't get you a job.
- If you click apply, that is worst that crumbling your resume and throwing it out the window.
- Connect with atleast 3 individuals already in Tech.
- Have 2 coffee chats.
- You might hate it at first, but it will get easier.
- You will get better at it.
- Stranger > Acquaintance > Friend > Referral > Coworker
- Only add people on LinkedIn that you know.
- Don't be afraid to ask for help.

## How to make friends

- Most of us aren't comfortable with networking.
- Read book "How to Win Friends and Influence People" by Dale Carnegie.

- Start with this book.

## How to meet people

- Meetup.com

## Maintain an excel sheet of people you meet

- Name, Date, Contact, Notes, Follow up, Spark (One thing you remember about them)
- Always follow up with them after every month.
- Create google alerts for them.
- Send them articles that they might like.
- Send them a thank you note.

## Coming back to Code (CSS) - Class 07 Follow Along Materials
- Complete The Box Model Example
- Complete The Layout 3 Alongside again

## Elastic
- EMs & REMs
- EMs are relative to the font-size of the parent.
- REMs are relative to the font-size of the root element.
- REMs are more predictable than EMs.
```html
<section>
  <p>Spam dominos in chat</p>
</section>
```
```css
html {
  font-size: 62.5%;
  # Default font-size is 16px
  # 62.5% of 16px is 10px
}
section {
  font-size: 10px;
}
p {
  font-size: 1em;
}
# vs
p {
  font-size: 1rem;
}
```
- p will be 10px in the first case and 16px in the second case.
s`

## Important addition to the template
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- These media queries are not working on mobile devices.
- This is because the mobile devices are trying to fit the entire website on the screen.
- This meta tag tells the browser to set the width of the viewport to the width of the device and set the initial zoom level to 1.0.

## Flexbox
- Flexbox is a one-dimensional layout method for laying out items in rows or columns.
- `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.
- `flex-start`: Items are packed toward the start of the flex-direction.
- `flex-end`: Items are packed toward the end of the flex-direction.
- `center`: Items are centered along the line.
- `space-between`: Items are evenly distributed in the line; first item is on the start line, last item on the end line.
- `space-around`: Items are evenly distributed in the line with equal space around them.
- `space-evenly`: Items are distributed so that the spacing between any two items (and the space to the edges) is equal.
- See flexbox example in follow along materials of class 07.
