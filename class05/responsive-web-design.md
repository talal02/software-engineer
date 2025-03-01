# Responsive Web Design (RWD)

It ensures websites provide an optimal viewing experience across a wide range of devices and screen sizes. Shay Howe's guide on RWD breaks down the concept into three main components: flexible layouts, media queries, and flexible media.

## 1. Flexible Layouts

Flexible layouts utilize relative length units, such as percentages or `em`s, instead of fixed units like pixels, allowing the design to adapt fluidly to different screen sizes.

*Example: Converting a fixed width to a percentage:*

```css
/* Fixed width */
.container {
  width: 960px;
}

/* Flexible width */
.container {
  width: 100%;
}
```

To calculate the percentage for a flexible layout:

```text
target ÷ context = result
```

For instance, if a sidebar has a fixed width of 300px within a 960px container, the percentage width would be:

```css
300px ÷ 960px ≈ 31.25%
```

Applying this:

```css
.sidebar {
  width: 31.25%;
}
```

## 2. Media Queries

Media queries allow the application of CSS rules based on device characteristics, such as screen width, height, or orientation.

*Example: Adjusting styles for devices with a maximum width of 768px:*

```css
@media (max-width: 768px) {
  .container {
    width: 100%;
  }
}
```

This approach enables designs to adapt to various screen sizes, enhancing usability across devices.

## 3. Mobile First

The mobile-first strategy involves designing for smaller screens initially and progressively enhancing the design for larger screens.

*Example:*

```css
/* Base styles for mobile devices */
.container {
  width: 100%;
}

/* Styles for larger devices */
@media (min-width: 768px) {
  .container {
    width: 960px;
}
```

This methodology ensures core content and functionality are accessible on all devices.

## 4. Flexible Media

Flexible media ensures that media elements like images and videos scale within their containing elements.

*Example: Making images responsive:*

```css
img {
  max-width: 100%;
  height: auto;
}
```

This approach prevents media from overflowing their containers, maintaining design integrity across devices.

By integrating these components—flexible layouts, media queries, and flexible media—developers can create responsive websites that provide an optimal user experience across a diverse range of devices and screen sizes.
