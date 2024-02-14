# CSS/Tailwind CSS

### Agenda

**CSS**
1. **Introduction to CSS**
2. **Basic CSS Syntax**:
      + Selectors
      + Properties and Values
      + Comments
3. **Applying CSS**:
      + Inline CSS  
      + Internal CSS    
      + External CSS
4. **CSS Selectors**:
      + Element 
      + ID 
      + Class
      + Universal
      + Attribute
5. **CSS Properties**
      + Text Properties
      + Box Model
      + Display
      + Positioning
      + Flexbox
      + Grids
      + Colors and Backgrounds
      + Fonts and Typography
      + Transitions and Animation
6. **Responsive Design and Media Queries**
7. **Advance Topics**
      + CSS variables
      + CSS Grid Layout
      + CSS Custom Properties
      + CSS Transformations and Transitions
      + CSS Animation
8. **Assignment**


**Tailwind**
  
1. **Introduction**  
2. **Getting Started**:
      + Installation
      + Configuration 
3. **Basic Concepts**:
      + Utility Classes
      + Responsive Design
4. **Layouts and Components**
      + Grid System
      + Flexbox Utilities
5. **Customization**
           
---            


## CSS

### 1. Introduction to CSS

CSS (Cascading Style Sheets) is a language used for describing the presentation of a document written in HTML or XML. It enhances the visual appearance and layout of web pages.



###  2. Basic CSS Syntax

+ Selectors

Selectors are patterns used to select and style HTML elements. They can target elements based on their tag name, class, ID, attributes, or relationships with other elements.




+ Properties and Values

Properties are attributes that define the visual presentation of an element. Each property has a value that determines how the property affects the element's appearance.




+ Comments

Comments in CSS are notes that are not displayed in the browser but help developers document their code for clarity and future reference.

``` bash
/* Selectors */
/* Targeting elements by tag name */
p {
    color: blue;
}

/* Targeting elements by class */
.myClass {
    font-size: 18px;
}

/* Targeting elements by ID */
#myID {
    background-color: lightgray;
}

/* Targeting elements by attributes */
input[type="text"] {
    border: 1px solid #ccc;
}

/* Targeting based on relationships */
ul li {
    list-style-type: square;
}

/* Properties and Values */
/* Property: color, Value: blue */
/* Applies blue color to all <p> elements */
p {
    color: blue;
}

/* Property: font-size, Value: 18px */
/* Applies font size of 18px to elements with class .myClass */
.myClass {
    font-size: 18px;
}

/* Property: background-color, Value: lightgray */
/* Applies light gray background to element with ID myID */
#myID {
    background-color: lightgray;
}

/* Property: border, Value: 1px solid #ccc */
/* Applies a 1px solid border with #ccc color to text input elements */
input[type="text"] {
    border: 1px solid #ccc;
}

/* Property: list-style-type, Value: square */
/* Applies square list-style-type to <li> elements within <ul> */
ul li {
    list-style-type: square;
}

/* Comments */
/* This is a comment explaining the color property */
p {
    color: blue;
}

/* Another comment describing the font-size property */
.myClass {
    font-size: 18px;
}

/* Commenting out specific styles */
/*
#myID {
    background-color: lightgray;
}
*/

/* A comment explaining list-style-type */
ul li {
    list-style-type: square; /* Comment about square bullets */
}
```


### 3. Applying CSS

+ Inline CSS

Inline CSS is applied directly within HTML elements using the style attribute.

+ Internal CSS

Internal CSS is placed within the <style> tag in an HTML document's <head> section.

+ External CSS

External CSS involves linking an external CSS file to an HTML document using the <link> tag. This method allows for the separation of concerns and reusability of styles across multiple pages.

```bash
<!DOCTYPE html>
<html>
<head>
    <title>CSS Example</title>

    <!-- Internal CSS -->
    <style>
        /* Internal CSS */
        h1 {
            color: blue;
        }

        p {
            font-size: 16px;
        }
    </style>

    <!-- External CSS (linking to an external stylesheet) -->
    <link rel="stylesheet" href="styles.css">

</head>
<body>

    <!-- Inline CSS -->
    <h1 style="color: red;">Heading with Inline CSS</h1>

    <p style="font-style: italic;">Paragraph with Inline CSS</p>

    <div class="external-style">
        <h2>Styled with External CSS</h2>
        <p>Content with styles from an external CSS file.</p>
    </div>

</body>
</html>
```
**External CSS**
```bash
/* styles.css */

/* Styles for elements with class external-style */
.external-style h2 {
    color: green;
}

.external-style p {
    font-weight: bold;
}


```


### 4. CSS Selectors

Types of Selectors

+ **Element Selectors**: Target specific HTML elements by their tag names. For example, p targets all <p> elements.

+ **ID Selectors**: Select elements by their unique id attribute. Use # followed by the ID name. For instance, #header targets an element with id="header".

+ **Class Selectors**: Target elements with a specific class attribute using .classname. For example, .highlight selects all elements with class="highlight".

+ **Universal Selector**: * selects all elements on a page.

+ **Attribute Selectors**: Target elements based on their attributes. For example, [type="text"] selects all elements with type="text".

```bash
/* CSS Stylesheet */

/* Element Selector */
/* Targets all <p> elements */
p {
    color: blue;
}

/* ID Selector */
/* Targets an element with id="header" */
#header {
    background-color: lightgray;
}

/* Class Selector */
/* Targets all elements with class="highlight" */
.highlight {
    font-weight: bold;
}

/* Universal Selector */
/* Applies styles to all elements */
* {
    margin: 0;
    padding: 0;
}

/* Attribute Selector */
/* Targets all elements with type="text" */
input[type="text"] {
    border: 1px solid #ccc;
}

```



### 4. CSS Properties 

+ **Text Properties**

1. **Color**: Sets the color of text. 
2. **Font-family**: Defines the font family for text.
3. **font size**: Specifies the size of the font.
4. **font-weight**: Determines the thickness of characters.
5. **text-align**: Aligns text within its container (left, right, center, justify).


```bash
/* CSS Stylesheet */

/* Color Property */
p {
    color: blue;
}

/* Font-family Property */
h1 {
    font-family: 'Arial', sans-serif;
}

/* Font size Property */
h2 {
    font-size: 24px;
}

/* Font-weight Property */
.bold-text {
    font-weight: bold;
}

/* Text-align Property */
.text-center {
    text-align: center;
}

```

+ **Box Model**

1. **Margin**: Sets space around an element.
2. **Border**: Defines the border properties (width, style, color).
3. **padding**: Specifies space between the element's content and its border.
4. **width and height**: Determines the dimensions of an element's content area.

```bash
/* CSS Stylesheet */

/* Margin Property */
.container {
    margin: 20px; /* Applies 20px margin on all sides */
}

/* Border Property */
.box {
    border: 2px solid #333; /* 2px solid border with color #333 */
}

/* Padding Property */
.inner-box {
    padding: 10px; /* Applies 10px padding inside the border */
}

/* Width and Height Properties */
.square {
    width: 100px; /* Sets width to 100px */
    height: 100px; /* Sets height to 100px */
}


```

+ **Display**

1. **display**: Defines how an element is displayed (e.g., block, inline, inline-block).
2. **visibility**: Controls the visibility of an element without affecting the layout.

```bash
/* CSS Stylesheet */

/* Display Property */
.block-element {
    display: block; /* Renders as a block-level element */
}

.inline-element {
    display: inline; /* Renders as an inline element */
}

.inline-block-element {
    display: inline-block; /* Renders as an inline-block element */
}

/* Visibility Property */
.hidden-element {
    visibility: hidden; /* Hides the element, but it still occupies space */
}

```

+ **Positioning**

1. **position**: Specifies the positioning method (static, relative, absolute, fixed).
2. **top**, **bottom**, **left**, **right**: Positioning properties used with non-static positioning.

![Alt text](https://chenhuijing.com/assets/images/posts/css-positioning.jpg)


```bash
 /* CSS Stylesheet */

/* Position Property */
.static {
    position: static; /* Default positioning */
}

.relative {
    position: relative; /* Positioned relative to its normal position */
}

.absolute {
    position: absolute; /* Positioned relative to its first positioned ancestor */
}

.fixed {
    position: fixed; /* Positioned relative to the viewport */
}

/* Top, Bottom, Left, Right Properties */
.absolute {
    position: absolute;
    top: 50px;
    left: 50px;
}

.fixed {
    position: fixed;
    bottom: 20px;
    right: 20px;
}

```

+ **Flexbox**

1. **display**: flex: Establishes a flex container and enables flex properties.
2. **Flex properties**: flex-direction, flex-wrap, flex-grow, flex-shrink, flex-basis, etc., for flexible layouts.

```bash
/* CSS Stylesheet */

/* Flex Container Property */
.flex-container {
    display: flex; /* Establishes a flex container */
    justify-content: space-around; /* Aligns items along the main axis */
    align-items: center; /* Aligns items along the cross axis */
    flex-direction: row; /* Arranges items in a row (default) */
    flex-wrap: wrap; /* Allows items to wrap to the next line */
}

/* Flex Item Properties */
.flex-item {
    flex: 1 1 200px; /* flex-grow | flex-shrink | flex-basis */
    margin: 10px; /* Adds space around the items */
    min-height: 100px; /* Minimum height for the items */
}


```


+ **Grid**

1. **display**: grid: Establishes a grid container and enables grid properties.
2. **Grid properties**: grid-template-columns, grid-template-rows, grid-gap, grid-column, grid-row, etc., for grid-based layouts.


```bash

/* CSS Stylesheet */

/* Grid Container Property */
.grid-container {
    display: grid; /* Establishes a grid container */
    grid-template-columns: repeat(3, 100px); /* Creates three columns of 100px each */
    grid-template-rows: 150px 200px; /* Creates two rows with specific heights */
    gap: 10px; /* Defines the gap between grid items */
    justify-items: center; /* Aligns grid items along the inline (row) axis */
    align-items: center; /* Aligns grid items along the block (column) axis */
}

/* Grid Item Properties */
.grid-item {
    border: 1px solid #333; /* Adds border to grid items */
    padding: 20px; /* Adds padding to grid items */
}
```

+ **Colors and Backgrounds**
1. **background-color**: Sets the background color of an element.
2. **background-image**: Specifies an image as the background.
3. **background-size**: Controls the size of a background image.
4. **background-repeat**: Determines how a background image repeats.

```bash
/* CSS Stylesheet */

/* Background Color Property */
.element-with-color {
    background-color: lightblue; /* Sets the background color */
}

/* Background Image Property */
.element-with-image {
    background-image: url('example-image.jpg'); /* Specifies an image as the background */
    background-size: cover; /* Controls the size of the background image */
    background-repeat: no-repeat; /* Prevents background image from repeating */
}
```


+ **Fonts and Typography**

1. **font-style**: Sets the style of the font (italic, normal).
2. **text-decoration**: Adds decorations to text (underline, line-through).
3. **line-height**: Defines the height of a line of text.
4. **letter-spacing**: Adjusts spacing between characters.

```bash
/* CSS Stylesheet */

/* Font Style Property */
.italic-text {
    font-style: italic; /* Sets the font style to italic */
}

/* Text Decoration Property */
.underlined-text {
    text-decoration: underline; /* Adds an underline to the text */
}

.line-through-text {
    text-decoration: line-through; /* Adds a line through the text */
}

/* Line Height Property */
.spaced-lines {
    line-height: 1.5; /* Sets the height of a line of text */
}

/* Letter Spacing Property */
.spaced-letters {
    letter-spacing: 2px; /* Adjusts spacing between characters */
}

```


+ **Transitions and Animation**

1. **transition**: Creates smooth transitions between property changes.
2. **animation**: Defines keyframes for animating elements.

```bash

/* CSS Stylesheet */

/* Transition Property */
.button {
    background-color: #3498db;
    color: #fff;
    padding: 10px 20px;
    border: none;
    transition: background-color 0.3s ease-in-out; /* Creates a transition effect */
}

.button:hover {
    background-color: #2980b9; /* Color change on hover */
}

/* Animation Property */
@keyframes slide {
    0% {
        transform: translateX(0); /* Starting position */
    }
    100% {
        transform: translateX(200px); /* Ending position */
    }
}

.box {
    width: 100px;
    height: 100px;
    background-color: #f39c12;
    animation: slide 2s ease-in-out infinite alternate; /* Animation using keyframes */
}
```



### 5. Responsive Design and Media Queries

+ **Viewport Meta Tag**

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Sets the viewport width to the device's width and initial scale to 1.0. Ensures proper rendering and scaling on different devices. For more information refer HTML Doc.

+ **Media Queries for Different Screen Sizes**

Responsive design ensures that websites look and function well across various devices, such as desktops, laptops, tablets, and mobile phones. Media queries play a pivotal role in applying different styles based on device characteristics like screen width, height, orientation, and resolution. By employing flexible and fluid design techniques, developers can create adaptable layouts that gracefully adjust to different screen sizes and resolutions.

Media Query Syntax: 

```bash
@media screen and (max-width: 768px) { ... }
```
Breakpoints: Designates specific screen widths where styles should change.


Example:

```bash
@media screen and (max-width: 768px) {
  /* CSS rules for screens up to 768px wide */
}
```




+ **Flexibility and Fluid Grids**

1. **Flexible Layouts**: Use relative units (percentages, em, rem) to create designs that adapt to different screen sizes.

```bash
/* CSS Stylesheet */

/* Flexible Layout Using Relative Units */
.container {
    width: 80%; /* Set container width to 80% of its parent */
    margin: 0 auto; /* Center the container */
    font-size: 16px; /* Base font size */
}

.relative-size {
    width: 50%; /* Element width set to 50% of its parent */
    padding: 2em; /* Padding using em units */
    margin-bottom: 1rem; /* Margin using rem units */
}
```


2. **Fluid Grids**: Utilize percentage-based widths for grid systems, allowing elements to resize proportionally with the viewport.

```bash
/* CSS Stylesheet */

/* Fluid Grid System with Percentage-Based Widths */
.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Responsive grid with minimum width of 200px */
    gap: 20px; /* Gap between grid items */
}

.grid-item {
    width: 100%; /* Item width set to 100% of its container */
    padding: 20px; /* Padding for grid items */
    background-color: #f0f0f0;
}

```


### 6. Advance Topics

+ **CSS Variables**

var() Function: Allows the definition and use of custom properties (variables) within CSS. 
Example:

```bash
 --main-color: #3498db;.
```

+ **CSS Grid Layout**

1. **display: grid**: Creates grid-based layouts with rows and columns.
2. **grid-template-columns and grid-template-rows**: Define the size of grid tracks (columns and rows).
3. **grid-gap**: Sets the spacing between grid items.

```bash
/* CSS Stylesheet */

/* Grid Container Property */
.grid-container {
    display: grid; /* Creates a grid-based layout */
    grid-template-columns: 100px 200px 1fr; /* Defines columns of different sizes */
    grid-template-rows: 50px 100px; /* Defines rows of specific heights */
    grid-gap: 10px; /* Sets the gap between grid items */
}

/* Grid Item Properties */
.grid-item {
    background-color: #3498db; /* Background color for grid items */
    color: #fff; /* Text color */
    padding: 20px; /* Padding for grid items */
}

```

+ **CSS Custom Properties**

1. **--property-name**: Syntax for creating custom properties in CSS. These properties can be reused across the stylesheet.

2. **Benefits**: Enhance code maintainability, allow for easier theming, and provide more flexibility.

```bash
/* CSS Stylesheet */

/* Custom Property Definition */
:root {
    --primary-color: #3498db; /* Define a custom property for primary color */
    --secondary-color: #2ecc71; /* Define a custom property for secondary color */
    --font-size: 16px; /* Define a custom property for font size */
}

/* Usage of Custom Properties */
.element {
    color: var(--primary-color); /* Use the custom property as a value */
    font-size: var(--font-size); /* Use the custom property for font size */
    background-color: var(--secondary-color); /* Use another custom property */
}

```

+ **CSS Transformations and Transitions**

1. **transform**: Modifies the appearance of an element (e.g., translate, rotate, scale).
2. **transition**: Creates smooth animations when an element changes from one state to another (e.g., hover effects).

```bash
/* CSS Stylesheet */

/* Transform Property */
.transform-element {
    width: 100px;
    height: 100px;
    background-color: #3498db;
    transition: transform 0.3s ease-in-out; /* Smooth transition for transform */
}

.transform-element:hover {
    transform: rotate(45deg) scale(1.2); /* Applies rotation and scaling on hover */
}

/* Transition Property */
.transition-element {
    width: 200px;
    height: 50px;
    background-color: #2ecc71;
    transition: width 0.5s ease-in-out, height 0.5s ease-in-out; /* Smooth transition for width and height */
}

.transition-element:hover {
    width: 300px; /* Width change on hover */
    height: 100px; /* Height change on hover */
}

```

+ **CSS Animation**

1. **@keyframes**: Defines animation sequences by specifying styles at various points in time.

2. **animation**: Applies the animation to an element and specifies its duration, timing function, and other properties.
  
```bash                                      
/* CSS Stylesheet */

/* Keyframes Animation Definition */
@keyframes slide {
    0% {
        transform: translateX(0); /* Starting position */
        opacity: 1; /* Starting opacity */
    }
    50% {
        transform: translateX(100px); /* Midpoint position */
        opacity: 0.5; /* Midpoint opacity */
    }
    100% {
        transform: translateX(200px); /* Ending position */
        opacity: 0; /* Ending opacity */
    }
}

/* Animation Application */
.animated-element {
    width: 100px;
    height: 100px;
    background-color: #3498db;
    animation: slide 3s ease-in-out infinite; /* Applies the 'slide' animation */
}

```


### 7. Assignment:

For the following assignments use the given Figma link:

[Figma Link for assignments](https://shorturl.at/clP68)


+ **Task 1**: Design a Navigation Bar using HTML and CSS.

Desired Output:

![Alt text](https://i.postimg.cc/wM02FbnC/NavBar.jpg)

                           

Code:

HTML

HTML code is as follows: 

```bash
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Navigation Bar</title>
  <link rel="stylesheet" href="styles.css"> <!-- Link to your CSS file -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"> <!-- Font Awesome CDN -->
</head>
<body>


<header>
  <nav>
    <div class="left">
      <div class="logo">
        <img src="logo.png" alt="Logo">
      </div>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">TV Shows</a></li>
        <li><a href="#">Movies</a></li>
        <li><a href="#">New & Popular</a></li>
        <li><a href="#">My List</a></li>
        <li><a href="#">Browse by Language</a></li>
     
       
    </ul>
    </div>
    <div class="right">
      <div class="search-bar">
        <input type="text" placeholder="Title, people, genres">
    </div>
       Children
      <div class="icons">
        <img src="bell_logo.png" alt="Bell Icon"> <!-- Bell icon -->
        <img src="account_logo.jpeg" alt="Account Icon">
        <div class="dropdown">
           
          <button class="dropbtn"><i class="fas fa-caret-down"></i></button> <!-- Account dropdown -->
          <div class="dropdown-content">
            <a href="#">Profile</a>
            <a href="#">Settings</a>
            <a href="#">Logout</a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</header>


</body>
</html>

```
**CSS**

For CSS, create a file named styles.css and write the following code: 

```bash
/* Basic reset and styles */
body {
    margin: 0;
    font-family: Arial, sans-serif;
  }
 
  /* Header and Navigation styles */
  header {
    background-color: #333;
    color: #fff;
    padding: 10px 20px;
  }
 
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
 
  nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
  }
 
  nav ul li {
    margin-left: 15px;
  }
 
  nav ul li a {
    text-decoration: none;
    color: #fff;
    font-size: small;
  }
 
  nav ul li a:hover {
    background-color: #555;
  }
 
  /* Logo and Items on the Left */
  .logo img {
    max-height: 40px; /* Set maximum height for the logo */
  }
 
  /* Right-side Elements */
  .right {
    display: flex;
    align-items: center;
  }
 
  .search-bar {
    display: flex;
    align-items: center;
    margin-right: 20px;
  }
 
  .search-bar input[type="text"],
  .search-bar button {
    padding: 8px;
    background-color: #060606;
  }
 
 
 
  .icons {
    display: flex;
    align-items: center;
  }
 
  .icons img {
    height: 40px; /* Set the height for the bell icon */
    margin: 0 10px;
  }
 
  /* Dropdown */
  .dropdown {
    position: relative;
    display: inline-block;
  }
 
  .dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 120px;
    z-index: 1;
  }
 
  .dropdown-content a {
    display: block;
    padding: 10px;
    text-decoration: none;
    color: #333;
  }
 
  .dropdown-content a:hover {
    background-color: #ddd;
  }
 
  .dropdown:hover .dropdown-content {
    display: block;
  }
 
  .dropbtn {
    background-color: transparent;
    color: #fff;
    border: none;
    cursor: pointer;
    align-items: center;
  }
 
  .left {
    display: flex;
    align-items: center;
  }
```


+ **Task 2**: Develop cards for the home page 

Desired Output: 

![Alt text](https://i.postimg.cc/kGHzKB35/dasc.jpg)
   


+ **Task 3**: Develop the Home page by combing Navigation Bar and cards

Desired Output: 

![Alt text](https://i.postimg.cc/nzTqt9T7/homepage.jpg)



---


## Tailwind CSS

### 1. Introduction to Tailwind CSS

Tailwind CSS is a utility-first CSS framework that promotes building designs using small, single-purpose utility classes rather than writing custom CSS. It allows for rapid development by providing a comprehensive set of pre-defined utility classes.

**Benefits of Tailwind CSS over traditional CSS**

+ **Speed and Efficiency**: Quickly create layouts without writing custom CSS.
+ **Consistency**: Ensures consistent styling across the project.
+ **Customization**: Highly customizable to match specific design needs.



### 2. Getting Started

+ **Installation**

Follow the given steps to install Tailwind into your project.

**Step 1**: Open the official Tailwind documentation on the following link: https://tailwindcss.com/

**Step 2**: After opening the link you will land on the following page. On this page, click the “Get Started” button.


![Alt Image](https://i.postimg.cc/YqQMDjY3/1.jpg)

**Step 3**: A new page will open, on this page scroll down a bit and you will see the “Installation” section on the web page” as shown. 

![Alt Image](https://i.postimg.cc/CKx0KNtP/2.jpg



**Step 4**: Now copy the command mentioned to the left of the first point i.e.” Install tailwind CSS”  and paste it into the terminal of your project 

![Alt Image](https://i.postimg.cc/fL3hcbMY/3.jpg)


And paste it into the terminal of your project and hit ‘Enter’:


![Alt Image](https://i.postimg.cc/MHV2LrMT/4.jpg)


**Step 5**: After the above step tailwind will be installed in your project and a file named ‘tailwind.config.js’ will be created.

![Alt Image](https://i.postimg.cc/1501c217/5.jpg)


**Step 6**: Open this “tailwind.config.js” file and add the following paths to it. 

![Alt Image](https://i.postimg.cc/cJCqWJgP/6.jpg)


**Step 7**: Now in your project open the App.css file, delete all the prewritten code, and add the following code:

![Alt Image](https://i.postimg.cc/cCQ2hg2t/7.jpg)


**Now you can use your tailwind CSS in your project.**


+ **Configuration**

Tailwind CSS offers a configuration file (tailwind.config.js) where users can customize various aspects such as colors, fonts, breakpoints, and more to tailor the framework to their project's needs.


### 3. Basic Concepts

+ **Utility Classes**

Utility classes are small, single-purpose classes that apply specific styling. For example:

```bash
<div class="bg-blue-500 text-white p-4 rounded-lg">Hello, Tailwind!</div>
```

Here, classes like bg-blue-500, text-white, p-4, and rounded-lg provide background color, text color, padding, and rounded corners respectively.

+ **Responsive Design**

Tailwind CSS offers responsive utility classes that allow developers to create designs that adapt to different screen sizes. For instance:

```bash
<div class="text-center md:text-left">Responsive Text Alignment</div>
```

The text-center class centers the text by default, but on medium-sized screens (md:), it aligns the text to the left.

### 4. Layouts and Components

+ **Grid System**

Tailwind CSS provides a flexible grid system using utility classes like grid-cols-{number} and gap-{size} to create responsive grid layouts.

+ **Flexbox Utilities**

Flexbox utilities such as flex, justify-center, and items-center allow for easy alignment and distribution of elements in a flex container.

### 5. Customization

+ **Adding Variants**

Tailwind CSS supports extending utility classes with variants. For instance, adding active variants to backgroundColor:

```bash
// In tailwind.config.js
module.exports = {
  variants: {
    extend: {
      backgroundColor: ['active'],
    },
  },
};
```

+ **Customizing Themes**

Tailwind CSS's theme configuration enables users to customize various aspects like colors, fonts, spacing, etc., allowing for extensive theming options:

```bash
// In tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        'custom-blue': '#123456',
      },
    },
  },
};
```

