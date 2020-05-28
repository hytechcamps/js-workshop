# JavaScript Code-Along
The next step for the webpage is to add functionality to the "Quiz Me" button. It should pop up a quiz that allows the user to answer some questions and receive a final score. This is possible with JavaScript!

## Defining the Function
1. Open the `script.js` file in the Repl
1. Create an empty function definition for the `startQuiz` function
    - This requires the `function` keyword, the function name, parentheses, and curly brackets
1. In the _body_ of the function (between the curly brackets), add an `alert` statement that welcomes the user
    - If desired, use the Windows emoji keyboard (Windows key + semi-colon key)
1. Click the "run" button to generate the webpage
1. On the webpage, click the button to make sure it is hooked up properly!
    - Note that this is possible because of the `onclick` attribute on the HTML button

```js
function startQuiz() {
    alert("Welcome to my quiz 🙂");
}
```

## Receiving Information from the User
1. Under the `alert`, above the `}`, create a couple new lines
1. Declare a `name` _variable_. How is it possible to ask the user for their name?
    - Use a `prompt` to ask for the user's name
1. On the next line, use an `alert` to say "Good luck" to the user (using their name!)

```js
var name = prompt("What is your name?");
alert("Good luck " + name);
```

## Setting up the Quiz Variables
1. Under the previous `alert`, above the `}`, create a couple new lines
1. Declare a `points` variable
    - This will be used to keep track of how many points the user has earned (i.e., how many questions they have answered correctly)
    - How many points should the user have at the beginning? `0`
1. Declare a `numberOfQuestions` variable
    - To start, set this value to `2`

```js
var points = 0;
var numberOfQuestions = 2;
```

## Asking a Question
1. Under the `numberOfQuestions` variable declaration, above the `}`, create a couple new lines
1. Ask the user a question using `prompt` (e.g., "What is my name?")
1. Store the user's answer in a variable called `answer1`
1. Under the `prompt`, create an `if` statement
    - What should happen based on the user's answer? If the user is correct, they should get a point. Otherwise, they should not
1. Use `if`, parentheses, `===`, and curly brackets to set up the `if`
1. Within the curly brackets, use `++` to increment the value of the `points` variable

```js
var answer1 = prompt("What is my name?");
if (answer1 === "Joseph") {
    points++;
}
```

_NOTE: Update the code so it checks for the proper answer!_

## Asking another Question
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

_NOTE: Update the code so it checks for the proper answer!_

## Calculating the Final Score
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

## Final Webpage
- [CodePen](https://codepen.io/jmaxwell/pen/BaBVVrO)
- [Repl](https://repl.it/@JosephMaxwell/WebpageChallenges#script.js)