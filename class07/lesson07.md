# Lesson 07: Learn Responsive CSS & Networking Strategies

## Networking in Tech

- **Job Applications Aren't Enough**: Simply applying to jobs online is often ineffective. Submitting applications without networking is like crumpling your resume and throwing it away.
- **Build Connections**: Reach out to at least 3 individuals already working in tech. Networking is key to unlocking opportunities.
- **Coffee Chats**: Schedule at least 2 informal coffee chats (virtual or in-person) to build relationships.
- **It Gets Easier**: Networking might feel uncomfortable at first, but with practice, it becomes more natural and rewarding.
- **Relationship Progression**: Stranger → Acquaintance → Friend → Referral → Coworker. Focus on building genuine connections.
- **LinkedIn Etiquette**: Only connect with people you know or have interacted with. Avoid random connections.
- **Ask for Help**: Don’t hesitate to ask for advice or guidance. Most people are willing to help if you approach them respectfully.

---

## How to Make Friends and Network Effectively

- **Overcoming Discomfort**: Many people find networking awkward, but it’s a skill that improves with practice.
- **Recommended Reading**: Read *How to Win Friends and Influence People* by Dale Carnegie. This book provides timeless advice on building relationships and networking effectively.
- **Start Small**: Begin with the book and practice its principles in your daily interactions.

---

## How to Meet People

- **Meetup.com**: Use platforms like Meetup.com to find local or virtual events related to tech, coding, or your interests. Attend events to meet like-minded individuals.

---

## Organizing Your Network

- **Track Your Connections**: Maintain an Excel sheet or CRM to organize the people you meet. Include:
  - **Name**
  - **Date Met**
  - **Contact Information**
  - **Notes** (key details about them)
  - **Follow-Up** (schedule regular check-ins)
  - **Spark** (one memorable thing about them to personalize future conversations).
- **Follow Up**: Reach out to your connections every month to maintain the relationship.
- **Google Alerts**: Set up Google Alerts for their name or company to stay updated on their achievements.
- **Share Relevant Content**: Send them articles, resources, or opportunities that might interest them.
- **Thank You Notes**: Always send a thank-you note after meetings or helpful conversations.

---

## Responsive CSS: Class 07 Follow-Along Materials

- **Complete The Box Model Example**: Practice understanding how padding, margin, and borders affect layout.
- **Complete The Layout 3 Exercise**: Revisit this exercise to reinforce your understanding of CSS layout principles.

---

## Elastic Units: EMs vs. REMs

- **EMs**: Relative to the font size of the parent element. Can lead to unpredictable results when nested.
- **REMs**: Relative to the font size of the root element (`<html>`). More predictable and easier to manage.
- **Example**:
  ```html
  <section>
    <p>Spam dominos in chat</p>
  </section>
  ```
  ```css
  html {
    font-size: 62.5%; /* Default font-size is 16px; 62.5% of 16px = 10px */
  }
  section {
    font-size: 10px;
  }
  p {
    font-size: 1em; /* 1em = 10px (parent font-size) */
  }
  /* vs */
  p {
    font-size: 1rem; /* 1rem = 16px (root font-size) */
  }
  ```
  - In the first case, the `<p>` font size is 10px (based on the parent’s font size).
  - In the second case, the `<p>` font size is 16px (based on the root font size).

---

## Viewport Meta Tag for Responsive Design

- **Why It’s Important**: Without the viewport meta tag, mobile devices may try to fit the entire website on the screen, causing layout issues.
- **How to Fix It**:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
  - This tag ensures the browser sets the viewport width to the device width and initial zoom level to 1.0, making your site responsive.

---

## Flexbox Basics

- **What is Flexbox?**: A one-dimensional layout method for arranging items in rows or columns.
- **Common Properties**:
  - `flex-start`: Items align to the start of the container.
  - `flex-end`: Items align to the end of the container.
  - `center`: Items align to the center of the container.
  - `space-between`: Items are evenly distributed, with the first item at the start and the last item at the end.
  - `space-around`: Items are evenly distributed with equal space around them.
  - `space-evenly`: Items are evenly distributed with equal space between them and the edges.
- **Practice**: Refer to the Flexbox example in the Class 07 follow-along materials.

---

## Homework

1. **Read**: *A Guide to Flexbox* on CSS-Tricks: [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).
2. **Play**: Complete the Flexbox Froggy game to practice Flexbox concepts: [http://flexboxfroggy.com/](http://flexboxfroggy.com/).
