# Webpage Follow-Along
Students will use HTML and CSS build a webpage using [CodePen](https://codepen.io/pen). They will then learn about JavaScript, and use it to add a simple interactive quiz to their webpage.

## Explain HTML (5m)
Start by showing an example webpage (e.g., https://en.wikipedia.org/wiki/SpongeBob_SquarePants) in Google Chrome. Talk to the students about their experience with the web. Then, right click on the page and view the source to show the HTML that builds the page.

### What is HTML
- HTML tells an internet browser what to show on a webpage
    - Ask students to name internet browsers (chrome, firefox, etc.)
- HTML elements are the building blocks of a webpage
- Browsers use HTML elements to display webpages
    - Examples of HTML elements are links, images, text, tables

## Create a Webpage - Starting with HTML (10m)
Students should follow along to create their own webpages! The webpage will be a "self-portrait" that has some information and a quiz.

### Basic HTML
1. Open a new CodePen: https://codepen.io/pen/ 
    - This allows developers to write HTML code and see it _render_ immediately
1. Change the view so the code appears on the left and the webpage appears on the right
1. Minimize the JS section
1. In the HTML section, add an `h1` header element saying "My Cool Webpage"
    - Explain that this is used for page titles, and there are also smaller header elements (`h2`-`h6`)
1. Add a `p` paragraph element with a greeting
    - Explain that this is used for regular text on the page

```html
<h1>My Cool Webpage</h1>
<p>Hi, I'm me.  Welcome to my cool webpage.</p>
```

#### _TIP: Saving Work_
Direct the students to click the "Save" button in CodePen. They have to make an account in order to save. Students should make note of their pen's URL so they can recover their code and share it!

### Lists
1. Add an `h2` for "My Favorite Foods" beneath the `p`
1. Add a `ul` that will contain a list of foods beneath the `h2`
    - Pause to ask students if they can guess what the `ul` will be
1. Add `li` elements as children of the `ul`
    - Ask them if they can guess what `li` means
1. Give the students a chance to add some additional foods to their lists
1. Show them that there are both unordered _and_ ordered lists in HTML (`ol`)

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
1. Add the `onclick` attribute and have it call a function called `startQuiz()`
    - Explain that **JavaScript** to make the button do something
    - We will come back to this shortly

## Create a Webpage - Styles with CSS (5m)
The current webpage looks fairly boring. Explain that developers use CSS to make their webpages look fun and exciting. HTML is like the skeleton, just the structure of the webpage, and CSS is like the clothes that it wears, giving it style.

1. In the CSS section, add a ruleset to select `body`
1. Add some declarations to update the text color, background color, and font of the page
1. See what would happen if `body` changed to `h1`
    - It only selects the `h1` element
1. Briefly explain web colors to the students: https://en.wikipedia.org/wiki/Web_colors
    - Show them that they can search Google for "color picker" if they want to use custom colors

```css
body {
    color: pink;
    background: black;
    font-family: arial;
}
```

**Make sure the students save their work and copy down their URL!**

## Interactivity with JavaScript (20m)
Explain that JavaScript is the programming language of the web, that allows webpages to be _interactive_. Developers use JavaScript to trigger events, create animations, make games, and much more.

### JavaScript Concepts Presentation
Briefly introduce **variables**, **`if` statements**, and **functions** using the [JavaScript Concepts](JavaScriptConcepts.pptx) presentation. 

### Functions in JavaScript - Unplugged Activity
Within the JavaScript Concepts presentation, there is an unplugged activity to practice writing algorithms in JavaScript pseudocode. The students should learn how to call JavaScript functions, and use made-up functions to create a **self-portrait algorithm**.

## Create a Webpage - Adding JavaScript to the CodePen (20m)
The next step for the CodePen site is to add functionality to the "Quiz Me" button. It should pop up a quiz that allows the user to answer some questions and receive a final score. This is possible with JavaScript!

### Defining the Function
1. Expand the **JS** portion of the code in CodePen
1. Create an empty function definition for the `startQuiz` function
    - This requires the `function` keyword, the function name, parentheses, and curly brackets
1. In the _body_ of the function, add an `alert` statement that welcomes the user
    - If desired, introduce the Windows emoji keyboard (Windows key + semi-colon key)
1. On the webpage, click the button to make sure it is hooked up properly!
    - Note that this is possible because of the `onclick` attribute on the HTML button

```js
function startQuiz() {
    alert("Welcome to my quiz 🙂");
}
```

### Receiving Information from the User
1. Under the `alert`, above the `}`, create a couple new lines
1. Declare a `name` _variable_. How can we ask the user for their name?
    - Use a `prompt` to ask for the user's name
1. On the next line, use an `alert` to say "Good luck" to the user (using their name!)

```js
var name = prompt("What is your name?");
alert("Good luck " + name);
```

### Setting up the Quiz Variables
1. Under the previous `alert`, above the `}`, create a couple new lines
1. Declare a `points` variable
    - This will be used to keep track of how many points the user has earned (i.e., how many questions they have answered correctly)
    - How many points should the user have at the beginning? (`0`)
1. Declare a `numberOfQuestions` variable
    - To start, set this value to `2`

```js
var points = 0;
var numberOfQuestions = 2;
```

### Asking a Question
1. Under the `numberOfQuestions` variable declaration, above the `}`, create a couple new lines
1. Ask the user a question using `prompt` (e.g., "What is my name?")
1. Store the user's answer in a variable called `answer1`
1. Under the `prompt`, create an `if` statement
    - What should happen based on the user's answer?
    - If the user is correct, they should get a point. Otherwise, they should not.
1. Use `if`, parentheses, `===`, and curly brackets to set up the `if`
1. Within the curly brackets, use `++` to increment the value of the `points` variable

```js
var answer1 = prompt("What is my name?");
if (answer1 === "Joseph") {
    points++;
}
```

_NOTE: The students should check the answer against their own name_

### Asking another Question
1. Repeat the steps above to ask another question underneath the first question
1. The differences will be:
    - `answer2` instead of `answer1` for the variable
    - Ask a different question
    - Check a different answer

```js
var answer2 = prompt("Where do I live?");
if (answer2 === "Lakewood") {
    points++;
}
```

_NOTE: The students should check the answer against where they live_

### Calculating the Final Score
1. Consider how to calculate the final score
    - The score will be the number of points the user has, divided by the total number of questions
    - Multiply this by 100 to show a percentage
1. Under the final question, declare a `finalScore` variable
1. Calculate the final score by dividing the `points` variable by the `numberOfQuestions` variable
    - Multiply this by 100 to show a percentage
1. Use an `alert` to show the final score to the user

```js
var finalScore = (points / numberOfQuestions) * 100;
alert("Final score: " + finalScore + "%");
```

## Final CodePen Webpage
https://codepen.io/jmaxwell/pen/BaBVVrO