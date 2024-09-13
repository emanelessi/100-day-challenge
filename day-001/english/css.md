### CSS (Cascading Style Sheets)

CSS is a language used to style and beautify web pages. It aims to separate the content (created using HTML) from the visual presentation. CSS can be applied directly inside the HTML file or externally via a separate CSS file.

### CSS Basics

#### 1. **Selectors**

Selectors are used to choose elements on a webpage to apply styles to them.

- **Type Selector:**  
  Used to apply styles to a specific type of element.

  ```css
  p {
    color: blue;
  }
  ```
  This code changes the color of all `<p>` paragraphs to blue.

- **Class Selector:**  
  The class is used to apply styles to elements that have a specific class name.

  ```css
  .myClass {
    font-size: 18px;
  }
  ```

- **ID Selector:**  
  Targets an element using an `id`, which must be unique on the page.

  ```css
  #header {
    background-color: #f0f0f0;
  }
  ```

#### 2. **Colors and Backgrounds**

- **Changing text color:**

  ```css
  h1 {
    color: #333;
  }
  ```

- **Changing background color:**

  ```css
  body {
    background-color: #f4f4f4;
  }
  ```

- **Adding a background image:**

  ```css
  div {
    background-image: url('image.jpg');
    background-size: cover;
  }
  ```

#### 3. **Dimensions**

CSS allows setting width and height for elements.

- **Width of an element:**

  ```css
  div {
    width: 200px;
  }
  ```

- **Height of an element:**

  ```css
  div {
    height: 300px;
  }
  ```

#### 4. **Margin and Padding**

- **Margin:**  
  The outer space between an element and other elements.

  ```css
  div {
    margin: 20px;
  }
  ```

- **Padding:**  
  The inner space between the element’s borders and its content.

  ```css
  div {
    padding: 10px;
  }
  ```

#### 5. **Text Styling**

CSS is used to style text in various ways.

- **Changing font size:**

  ```css
  p {
    font-size: 16px;
  }
  ```

- **Making text bold:**

  ```css
  p {
    font-weight: bold;
  }
  ```

- **Text alignment:**

  ```css
  p {
    text-align: center;
  }
  ```

#### 6. **Forms**

CSS enhances the appearance of form elements like fields and submit buttons.

- **Styling input fields:**

  ```css
  input[type="text"] {
    border: 1px solid #ccc;
    padding: 10px;
    width: 100%;
  }
  ```

- **Styling submit buttons:**

  ```css
  input[type="submit"] {
    background-color: green;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
  }
  ```

#### 7. **CSS Grid**

Grid layouts allow the division of a page into a flexible grid.

- **Creating a simple grid:**

  ```css
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;
  }
  ```

- **Merging columns or rows:**

  You can merge columns or rows to make an element span more than one column or row.

  ```css
  .item1 {
    grid-column: 1 / span 2;
  }
  ```

#### 8. **Flexbox Layout**

Flexbox allows creating flexible and easy layouts.

- **Using Flexbox to distribute items:**

  ```css
  .container {
    display: flex;
    justify-content: space-between;
  }
  ```

- **Controlling direction with Flex Direction:**

  You can control the direction of elements, either horizontally or vertically:

  ```css
  .container {
    display: flex;
    flex-direction: column;
  }
  ```

  This code arranges the items in a column instead of a row.

- **Flex Grow:**  
  Allows an element to take up more or less space based on its flexibility:

  ```css
  .item {
    flex-grow: 2;
  }
  ```

  This means that the element with `flex-grow: 2` will take twice the space compared to other elements.

### 9. **CSS Grid vs Flexbox**

- **Flexbox:**  
  Suitable for distributing items in a single row or column.

  ```css
  .flex-container {
    display: flex;
    justify-content: space-between;
  }

  .flex-item {
    width: 30%;
  }
  ```

- **CSS Grid:**  
  Ideal for creating multi-dimensional layouts.

  ```css
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }

  .grid-item {
    background: #4CAF50;
    height: 100px;
  }
  ```

### 10. **Transitions and Animations**

- **Transitions:**

  ```css
  button {
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: blue;
  }
  ```

#### 11. **CSS Variables**

CSS variables help reuse values across different styles.

- **Defining a variable:**

  ```css
  :root {
    --main-color: #4CAF50;
    --padding-size: 10px;
  }
  ```

- **Using variables:**

  ```css
  .box {
    background-color: var(--main-color);
    padding: var(--padding-size);
  }
  ```

### 12. **Relative Units**

Units like `em` and `rem` offer greater flexibility in designs.

- **`em` unit:**  
  Based on the current font size of the parent element.

  ```css
  p {
    font-size: 1.5em;
  }
  ```

- **`rem` unit:**  
  Based on the root font size.

  ```css
  body {
    font-size: 16px;
  }

  h1 {
    font-size: 2rem;
  }
  ```

### 13. **Media Queries**

Media queries make websites responsive to different screen sizes.

- **Changing design based on screen width:**

  ```css
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
  }
  ```

### 14. **Z-Index Control**

`z-index` controls the stacking order of elements (front and back).

- **Bringing an element forward:**

  ```css
  .box {
    position: relative;
    z-index: 10;
  }
  ```

### 15. **Box Shadows & Text Shadows**

- **Box shadow:**

  ```css
  .box {
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
  ```

- **Text shadow:**

  ```css
  h1 {
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
  }
  ```

### **CSS Pseudo-Classes and Pseudo-Elements** .16

- **Pseudo-Classes:**

  ```css
  a:hover {
    color: red;
  }
  ```

- **Pseudo-Elements:**

  ```css
  p::first-letter {
    font-size: 2em;
    color: red;
  }
  ```

### 16. **Responsive Design**

- **Using Media Queries:**

  ```css
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
  }

  @media (min-width: 769px) {
    .container {
      flex-direction: row;
    }
  }
  ```

### 18. **Performance Optimization**

- **CSS optimization:**

    - Minify files using tools like [CSSNano](https://cssnano.co/).

    - Lazy Loading with the `media` attribute:

  ```html
  <link rel="stylesheet" href="styles.css" media="(min-width: 600px)">
  ```

### 19. **CSS Tools**

- **Preprocessors (like Sass):**

  ```scss
  $primary-color: #4CAF50;

  body {
    background-color: $primary-color;
  }
  ```

### 20. **Advanced CSS Effects**

- **CSS Filters:**

  ```css
  img {
    filter: grayscale(100%) blur(5px);
  }
  ```

- **Clip-path:**

  ```css
  .clip-box {
    clip-path: circle(50%);
    background: #4CAF50;
    width: 100px;
    height: 100px;
  }
  ```
### 21. **Practical Experience**

**Practical Project:**

You can create a web project that demonstrates how to use Flexbox and Grid simultaneously. For example, design a dashboard with multiple sections using Grid, and within each section, use Flexbox to distribute the elements flexibly.

**Example:**

```html
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Project</title>
    <style>
        :root {
            --main-bg-color: #f0f0f0;
            --primary-color: #4CAF50;
            --font-size: 16px;
        }

        body {
            background-color: var(--main-bg-color);
            font-size: var(--font-size);
            margin: 0;
            padding: 0;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            padding: 20px;
        }

        .box {
            background: var(--primary-color);
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.2em;
            transition: transform 0.3s ease;
        }

        .box:hover {
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>

</body>
</html>
```

This example integrates CSS Grid and Flexbox, demonstrating how to use variables and filters in a simple design.

### Conclusion

CSS is a powerful language that can be used to build complex layouts, apply advanced effects, and create responsive and modern websites. In your lesson, you can focus on these advanced concepts to deliver professional designs that meet modern web development challenges.

---
### Connect with Me

You can follow me on social media:

- **Instagram:** [emanelessi](https://www.instagram.com/emanelessi/)
- **LinkedIn:** [emanelessi](https://www.linkedin.com/in/emanelessi/)

Feel free to reach out for any questions or potential collaborations. I'd love to connect with you!

