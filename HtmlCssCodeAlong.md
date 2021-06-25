# HTML & CSS Code-Along
Use HTML and CSS build a webpage using [CodePen](https://codepen.io/pen).

## HTML Introduction
All websites come from HTML. One example is the Wikipedia page for SpongeBob: https://en.wikipedia.org/wiki/SpongeBob_SquarePants. While viewing a website in Google Chrome, right click on anywhere and select "View page source" to look at the HTML that makes up the site!

### What is HTML?
- HTML tells an internet browser what to show on a webpage
    - Some examples of web browsers are Google Chrome, Mozilla Firefox, and Safari
- HTML **elements** are the building blocks of a webpage
- Browsers use HTML elements to display webpages
    - Examples of HTML elements are links, images, text, tables

## Creating a Webpage - HTML
The webpage will be a "self-portrait" that has some information and a quiz.

### Basic HTML
1. Open a new CodePen: https://codepen.io/pen/ 
    - CodePen is a tool that allows developers to write HTML code and see it _render_ immediately
1. Change the view so the code appears on the left and the webpage appears on the right
1. Minimize the JS section
1. In the HTML section, add an `h1` **header** element saying "My Cool Webpage"
    - This is used for page headers, and there are also smaller header elements (`h2`-`h6`)
1. Add a `p` **paragraph** element with a greeting
    - This is used for regular text on the page

```html
<h1>My Cool Webpage</h1>
<p>Hi, I'm me.  Welcome to my cool webpage.</p>
```

#### _TIP: Saving Work_
Click the "Save" button in CodePen to save the code. It is necessary to make an account in order to save. Make note of the URL to recover the code if necessary, or to share it!

### Lists
1. Add an `h2` for "My Favorite Foods" beneath the `p`
1. Add a `ul` that will contain a **list** of foods beneath the `h2`
1. Add `li` elements as children of the `ul`
    - `li` stands for **list item**
1. Add some additional foods to fill out the list

>Note: There are both unordered _and_ ordered lists in HTML. An `ol` will have numbers instead of bullet points!

```html
<h2>My Favorite Foods</h2>
<ul>
  <li>Pizza</li>
  <li>Burritos</li>
</ul>
```

### Buttons
1. Add a `button` with the text "Quiz Me"
    - This button will start the quiz
1. Add the `onclick` attribute and have it call a function named `startQuiz()`
    - Later, **JavaScript** will make the button do something

```html
<button onclick="startQuiz()">Quiz Me</button>
```

## Creating a Webpage - Styles with CSS
The current webpage looks fairly boring. Luckily, developers can use CSS to make their webpages look fun and exciting. HTML is like the skeleton, just the structure of the webpage, and CSS is like the clothes that it wears, giving it style.

1. In the CSS section, type `body {}`, then go in between the brackets and press `Enter`
1. Add some code to update the text `color`, `background` color, and `font-family` of the page
1. Change `body` to `h1` to see what happens
    - It only selects the `h1` element - so only the `h1` header will change style!
1. Look into web colors to learn more about color options: https://en.wikipedia.org/wiki/Web_colors
1. Google "color picker" to find some custom colors, and set them in the CSS if desired!

```css
body {
    color: pink;
    background: black;
    font-family: arial;
}
```

**Make sure to save the code and copy down the CodePen URL!**

## HTML & CSS Code
https://codepen.io/jmaxwell/pen/MWaJLrB