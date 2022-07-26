# Program outline

### Preliminary steps:

- Install & set up [Git bash](https://git-scm.com/downloads)
- Install & set up [Visual Studio Code (VSCode)](https://code.visualstudio.com/download)
- Set up a [Github](https://github.com) account

### Resources

- [Mozilla Developer Network (MDN)](https://developer.mozilla.org/) (HTML/CSS/JavaScript documentation)
- [W3Schools](https://w3schools.com) (HTML/CSS/Javascript tutorials)
- [Envato TutsPlus](https://code.tutsplus.com/) (Code tutorials covering numerous verticals)

# Introduction to Javascript

# Javascript 101:

### Variables & Output

Variables store information so we can re-use that information. Let's say, for example, you wanted to display an error message for somebody who was not logged in to your photo-sharing app. This message could pop up whenever an unauthorized user tried to click a button, send a message or "like" a post. The error message's text could be something like this:

> You are not authorized to view this content. Log in to your account or, if you don't have an account, sign up for your free account.

You wouldn't want to have to write all that text for _every single button/message/like_ the unauthorized user attempted - that is just very, very, very, very, very, very, very, very, very, very repetitive. Instead, you could store that text _in a **variable**.

There are two ways to define a variable in Javascript:

- `let`: This is used to define a variable that contains information that can be changed
- `const`: This is used to define a variable whose information _will never change_

Since our error message is always going to be the same, no matter who sees it, we would use `const` to store our message text:

`const errorMessage = "You are not authorized to view this content. Log in to your account or, if you don't have an account, sign up for your free account."`

The next time you need to show an error message, you could simply utilize the `errorMessage` variable you defined.

### Console output

If we wanted to show the error message in the console, we could use the `console.log()` function. Our code would look like this:

`console.log(errorMessage)`

This will show our message text in the browser's console.

### Alerts

If we wanted to show the error message as a popup, we could utilize the `alert()` function. An **alert** shows a popup box with our text inside of it. Our code implementation would be as follows:

`alert(errorMessage)`

This will obnoxiously pop up a box with our message _every time a user attempts an unauthorized action_.

### Functions

A **function** contains several code operations that will be performed one after the other every time the function is called (aka every time it runs). One example is the `console.log()` function: this _calls_ a set of instructions that takes the text we put between the parentheses and makes it appear in our browser's console.

We define (create) functions with the following syntax: `function {nameOfYourFunction}(arguments) {}`

Every function begins with the `function` declaration, meaning that we _must always write the word `function` to indicate that we are writing a function_: `function ...`

Next, we give our function a _name_. The name can be pretty much anything we want it to be: `function bestFunctionEver ...`

Following the function name, we add parentheses `()`, which accept our **function arguments**. Arguments are _placeholders_ for information that we want to provide to the function so that it can run its code based on the given information: `function bestFunctionEver(argument1, argument2) ...`

We could build a function whose sole purpose was to greet a user by name. In that case, we could name our function `greeting` and tell it to accept the _argument_ of the user's _name_: `function greeting(name)`

Once we have defined our function, we must create its _function_ality (eyyyyyyyyy). We do this by wrapping our instructions in curly-braces `{}`: `function greeting(name) {}`

We can put whatever we want between these curly-braces. For our `greeting` example, we will simply use a `console.log()` function to output the personalized greeting:

    function greeting(name) {
        console.log("Hello, ", name)
    }

We would run this function by typing its name and passing in an argument: `greeting('Excision')`
The resulting output would be `Hello, Excision`

### Conditionals (If/Else)

Conditionals are very basic logic processing. We check whether a _statement_ is **true** or **false**. **If** it is _true_, we perform one piece of code. If it is _false_, we do something else (or nothing at all!). The _if_ syntax is as follows:

    if (condition) {
        // do something
    }

What happens if our _condition_ is not met? Well, we are basically saying "We will do X if this is _true_, or _else_ we will do Y." We can use our _else_ syntax in this case:

    `if (condition) {
        // do something
    } else {
        // do something else
    }

What if we have more than one condition we are checking for? For example, perhaps we are checking to see if an age is greater than 50. In that case, our _conditions_ may be as follow:

- If our number (the age) is _less than_ 50, this **does not** meet our condition of being _greater than 50_
- If our number is _greater than_ 50, it meets our condition

This would be implemented using conditionals as shown below:

    if (age < 50) {
        console.log('This person is younger than 50!')
    } else if (age > 50) {
        console.log('This person is older than 50.')
    }

Wait... what if the person _is 50 years of age?!_ 50 is neither _greater than_ 50 nor _less than_ 50. So, we may need a third condition. Lucky for us, we don't always have to use the `else if()` syntax; we can simply say `else`, which is a basically a programmatic way of saying "...otherwise, do _this other thing_."

    if (age < 50) {
        console.log('This person is younger than 50!')
    } else if (age > 50) {
        console.log('This person is older than 50.')
    } else {
        console.log('This person is *exactly* 50!')
    }

### Comparison operators

Comparison operators are the symbols we use to _compare_ values against one another. As you saw above, the greater-than `>` and less-than `<` symbols can compare numbers. We can also test whether strings (basically any character that is not a number) are equal to one another, and even whether numbers are equal. We do this by using a **double-equal** `==`

We compare using `==` (as opposed to `=`) because _the single equal symbol is used for **assignment**_, as demonstrated in our variable declarations. If we wanted to compare `'Apples'` to `'Oranges'`, we would have to write `if ('Apples' == 'Oranges') ...`; if we were to write `if ('Apples' = 'Oranges') ...`, that would mean that we were saying that `Apples` and `Oranges` _are the same thing_, which basically makes us look like _idiots_ in front of our computers, and trust me, that's never a good look.