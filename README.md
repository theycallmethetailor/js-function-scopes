# JavaScript Functions & Scopes 

## short URL to this repo [jsfunc.sage.codes](https://github.com/sagecodes/js-function-scopes)

## Setting up your computer:

- Open your web browser. I'll be using [chrome](https://www.google.com/chrome/), but  you can use whatever one you want.
- go to [repl.it](https://repl.it/repls) and create a new JavsScript repo

That was easy!


## Galvanize 

### Welcome to Galvanize!

We create a technology ecosystem for learners, entrepreneurs, startups, and established companies to meet the needs of the rapidly changing digital world.

Upcoming JavaScript workshops:


We're an awesome community!!! 

Interested in learning more about our Galvanize programs reach out to Lauren @ [lauren.lark@galvanize.com](mailto:lauren.lark@galvanize.com)


## Setting up


## About me:
I'm [Sage Elliott](http://sageelliott.com/). I'm a Technology Evangelist at Galvanize Seattle. In the past decade I've worked as a software and hardware engineer with mostly with Startups and Agencies in Seattle and Central Florida. I love technology! I'm currently learning more about Deep Learning & Computer Vision. If you're looking for a job or next steps in learning, let me know!

*caveat* I'm not an Galvanize instructor, They have much more industry experience and are better at teaching difficult topics!

If you have an event you would like to see or put on let me know! I'm always looking for ideas. Talk to me after the workshop or find me online at one of these:

- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)


## About you!

Give a quick Intro!

- Whats your name?
- Whats your background?
- Why are you interested in SQL and data?

One of the best things about these in person workshops is being able to meet new people! Talk to each other!


## What this workshop is

A super friendly introduction to JavaScript Functions and Scopes. Some of the javaScript weirdness!

You can't learn EVERYTHING in ~2 hours. But you can learn enough to get excited and comfortable to keep working and learning on your own! This workshop will introduce you to concepts you'll encounter later in your learning journey or career (and sometimes interviews)

- This course is for absolute beginners
- Ask Questions!
- Answer Questions!
- Help others when you can
- Its ok to get stuck, just ask for help!
- Feel free to move ahead
- Be patient and nice


## What is javaScript?

### Its not Java

"The relationship between Java and JavaScript is almost exactly like that between grapes and grapefruit"

Java is an entirely different programming language.


### A very brief history

Created by Brendan Eich in 1995 in ONLY 10 days during his time at Netscape Communications.

A lot of updates have happened of course since then, but its still fun to see some of the [quirks](https://www.destroyallsoftware.com/talks/wat) still in the language!

Read more about the history of JavaScript [here](https://en.wikipedia.org/wiki/JavaScript).

Javascript is often used with HTML and CSS to create dynamic web pages. 

### Who uses javaScript?

Almost everyone!

- Large Companies (Google, Facebook)
- Startups
- Agencies
- Pretty much anyone using web technology 


### What can you do with JavaScript

- Web Development
	- Front-End
	- Back-End
- Mobile Development 
- [Machine learning](https://js.tensorflow.org/) 😱
- [Embedded(Hardware) Programming](http://ejs.co/) 😲

#### Popular Frameworks to keep in mind

When learning more about JS you'll probably keep learning about these!

- Node
- Express
- React
- Angular
- Vue


## JavaScript Refresher:

We'll do a quick refresher on some javaScript Basics that we need to know for this workshop. If you'd like to refresh more you can check out this [repo](https://github.com/sagecodes/Learn-to-code-javascript) or the resource section of near the bottom. 

### Variables

These are three ways of creating a variable.

##### var

var is the older way of declaring a variable. You'll probably still see this quite a bit, but when learning from new content you'll probably start seeing `let` and `cosnt` more frequently. var is function scoped (we'll go into scoping later)

```
var greeting = "hello"

console.log(greeting)

// You can change the variable declared with var
greeting = "bye"

console.log(greeting)
```

##### Let

`let` is similar to `var`. except that let is block scoped. (We'll go into scoping later). You'll see this variable declaration a lot and when in doubt its probably the one to use. 

```
let greeting = "hello"

console.log(greeting)

// You can change the variable declared with let
greeting = "bye"

console.log(greeting)
```

#####  Const

Const is used to declare variables you do not want to change later in your code. This helps yourself and other developers working on your team prevent accidentally rewriting a variables that was not supposed to be.  

What will happen when we try to overwrite the variable in the below example?

```
const greeting = "hello"

console.log(greeting)

// You can NOT change the variable declared with const
greeting = "bye"

console.log(greeting)
```

Essentially `let` and `const` are considered "safer" to use.

#####  Functions

Reduce, Reuse, Recycle

Functions make it easy to reuse code. If you find yourself repeating code you may want to turn it into a function!

Example: these functions take in two arguments(a, b) and returns the value of them added together.



You'll see two common ways of creating a function called `Declaration` and `Expression`. We'll go into the differences with these types later when we get into scoping. Just remember there are two types!


Declaration:

```
function add(a, b) {  
  return a + b
}
add(2, 3)

```


Expression:

```
var sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```

## Hoisting

We're going to just cover the basic of *hoisting* in javascript. This can help with understanding scopes. 



#### JavaScript Runtime

When you run javaScript there are essentially two steps that happen:

1. Variables are declared in memory 
2. Then the code is actually executed

below we will see an example of what we just talked about:

Due to the way javaScript runs(see above), it can cause some interesting things to happen! 

Hoisting basically happens at step one. When variables are declared in memory it will "hoist" them up to the top of their scopes. The effects variables declared with `var` and declarative functions. We'll see what this all means soon!

### Variable hoisting in action

`var`

What do you think will happen when we run this code? Lets run it in [repl](https://repl.it).


```
console.log(greeting)

var greeting = "hello"

console.log(greeting)

```
 
 It didn't throw an error! This is because of *hoisting*. The variable `greeting` gets declared in computer memory before we run the code. So the first `console.log()` will run just fine even though greeting does not have an assigned value to it.  
 
Visualizing it how it looks to the computer is something like this:
 
```
var greeting;

console.log(greeting);

greeting = "hello";

console.log(greeting);
```

Does it work with `let` and `const`?


`let`

```
console.log(greeting)

let greeting = "hello"

console.log(greeting)

```

`const`

```
console.log(greeting)

const greeting = "hello"

console.log(greeting)

```

`let` and `const` get treated differently.

To keep it simple you can remember that `let` and `const` cannot be accessed before they are declared. 

Technically they do get hoisted, but are caught is something called the *temporal dead zone*(a period between entering scope and being declared where they cannot be accessed). Read more about that [here](
https://stackoverflow.com/questions/31219420/are-variables-declared-with-let-or-const-not-hoisted-in-es6).


### Function Hoisting in action!

Similar to variables, functions also have get hoisted.

Lets see how it behaves with a Declaration function:

```
add(2, 3)
function add(a, b) {  
  return a + b
}
add(2, 3)

```
Declaration functions DO get hoisted.


Lets see how it behaves with a Expression functions:

We'll try with both `var` and `let`

```
sum(2, 3)
var sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```

```
sum(2, 3)
let sum = function(a, b) {  
  return a + b
}
sum(2, 3)

```

Expression functions do NOT get hoisted. 

Because of hoisting can get confusing in a larger codebase [here is a long article suggesting to us Function Expression over declaration](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/). 

<!--### using return 
console log vs return-->


<!--### Function Challenges
-->

## Scopes

### Scope

What is a Scope?

Put simply a scope in JavaScript defines what variables you have access to.

Two types of scopes exists:

1. Global Scope
2. Local Scopes

### Global Scope

What is global Scope?

Something with Global scope means you can access it anywhere in your code. Usually it will not be defined inside any function or curly brackets `{}`

##### Global Variables


```
var globalVariableOne = 'hello 1'
let globalVariableTwo = 'hello 2'
const globalVariableThree = 'hello 3'

function greeting() {
  console.log(globalVariableOne)
  console.log(globalVariableTwo)
  console.log(globalVariableThree)
}

greeting()

```

Above are examples of global variables. You will be able to access these variables anywhere in your code. including functions. *Note that we did not have to even pass these into our functions.*


Often best practice to not use global variables when possible. This will decreases the chance of developers changing variables by accident in other parts of the code or variable name collision. When you're working as a developer chances are your code base may be massive and you will not exactly know all the variables names.

##### name collision example:

Lets try these out in repl to see what happens

```
let globalvar = 'hello'
let globalvar = 'by'
```

```
var globalvar = 'hello'
var globalvar = 'by'
```

This is a good example why `let` is safer to use. It at least lets you know when you're re-declaring it. 


### Local Scope

Anything with a local scope can only be used in that part of the code. CANNOT be accessed everywhere in your code. There are two types of local scopes

1. Function scope
2. block scopes



### Function Scope

Functions scopes occur when you declare a variable inside of a function

this example created a local variable and calls it inside the function and outside of the function. What do you think will happen?

```
function greeting () {
  const say = 'hello'
  console.log(say)
}

greeting()
console.log(say)
```

Here is the same thing except the variable is global. What do you think will happen this time if we run this?

```
const say = 'hello'
function greeting () {
  console.log(say)
}

greeting()
console.log(say)
```


### Block Scope

Introduced in  ES6 (newer version of JavaScript)

We can use block level declaration with `let` and `cost`

```
{
  const say = 'hello'
  console.log(say)
}

console.log(say)
```

Again if we move the variable outside of the brackets this will make it global.

```
  const say = 'hello'
{
  console.log(say)
}
console.log(say)
```


### Scopes with functions 

We talked about hoisting in functions. When the function is declared it gets hoisted to the top of the scope its in. Which can be confusing when debugging / developing. Hence why most people say using the function expression is safer. Note that this is probably debatable and may depend on your team. They should probably all at least be consistent. 

##### Functions cannot access local variables from other functions

```
function one () {
  const oneVar = `Hello, this is oneVar`
}

function two () {
  one()
  console.log(oneVar)
}

two()
```

If you're new to programming this and wondering, well how would I get that value into another function to actually do something with it???

```
function one () {
  const oneVar = `Hello, this is oneVar`
  return oneVar
}

function two () {
  console.log(one()) 
}

two()
```



### Lexical scoping

Lexical scopes are nested scopes. Example a function inside of a function. the inner function has access to the outer functions variables, but the outer function cannot access the inner function variables.

Think of this as only having one way street from the inner function. It can move out and look at whats in the outer function. But the outer function cannot move into the inner function


Here we will try to print the inner variable from the outer function. Can you guess what will happen?

```
function outer () {
  const outerVar = `Hello, this is outerVar`

  function inner() {
    const innerVar = `Hello, this is innerVar`
    console.log(outerVar) 
  }

console.log(innerVar)
}

outer()

```

Here we will print the outer variable from the inner function. Based on what we talked about what do you think will happen?

```
function outer () {
  const outerVar = `Hello, this is outerVar`

  function inner() {
    const innerVar = `Hello, this is innerVar`
    console.log(outerVar) 
  }

inner()
}

outer()

```



## JavaScript Closures

What is a closure?

A closure a inner function with access to the outer (enclosing) function’s variables(aka scope chain).

Reiterating: When a function is created inside of another function thats called a closure. Often the inner function(closure) is used to return values. It has access to its outer scope variables and to global variables. 


```
let globalVar ="Hello, this is globalVar";
function outer () {
  const outerVar = `Hello, this is outerVar`;

  function inner() {
    const innerVar = `Hello, this is innerVar`;
    console.log(outerVar) 
    console.log(innerVar)
    console.log(globalVar)
  }

return inner()
}

outer()
```


##### Private variables

the variables inside the scope of a function that cannot be accessed outside of it are often called private variables. 

Returning the function with private variables similar to above allows you get access to the variables in parts of your code that you want. 


there is a lot more to learn about closures, this is just the basics. checkout these resources:

more about closure interview questions:
https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36

## Wrap up


### Lets Review:

<details>
  <summary>What is a Scope?</summary>
	a scope in JavaScript defines what variables you have access to
</details>

<details>
  <summary>What is a global scope?</summary>
	Something with global scope means you can access it anywhere in your code. 
</details>


<details>
  <summary>What is a local scope?</summary>
	a local scope can only be used in that part of the code. CANNOT be accessed everywhere in your code.
</details>


<details>
  <summary>What is hoisting?</summary>
  Hoisting basically happens at step one. When variables are declared in memory it will "hoist" them up to the top of their scopes. The effects variables declared with `var` and declarative functions.
</details>


<details>
  <summary>What type of function does not get hoisted?</summary>
	Expression functions
</details>


<details>
  <summary>What is the temporal dead zone?</summary>
	a period between entering scope and being declared where they cannot be accessed
</details>


<details>
  <summary>let and const are different from let because..?</summary>
	They do not get hoisted the same way as `var` they also throw name collision error. 
</details>


<details>
  <summary>What is special about const </summary>
		`const` value cannot be changed later in the code. It will throw an error if you try.
</details>

<details>
  <summary>What is a closure? </summary>
  A closure is inner function that access to the outer (enclosing) function’s variables(scope chain).
	
</details>

<details>
  <summary>What is lexical scoping?</summary>
  Lexical scopes are nested scopes. Example a function inside of a function. the inner function has access to the outer functions variables, but the outer function cannot access the inner function variables.
	
</details>

What type of function declaration is usually considered less confusing/safer?

Expression functions

<details>
  <summary>What are the two things that happen when JavaScript runs </summary>
  1. Variables are declared in memory 
	2. Then the code is actually executed
</details>



## Keep Learning!!!

### Resources:

- [Hack reactor Premium Prep](https://www.galvanize.com/gift-of-code?utm_medium=Seattle&utm_source=Meetup&utm_campaign=LearnToCode) FREE until 2/15 (usually $250)

- [Free Data Science Prep](https://www.galvanize.com/data-science-prep) - Galvanize

- [Free Software Engineering Prep](https://www.galvanize.com/web-development/prep) - Galvanize

- [https://github.com/getify/You-Dont-Know-JS](You-Dont-Know-JS)

- [You-Dont-Know-JS Scopes and Closures](https://github.com/getify/You-Dont-Know-JS/tree/master/scope%20%26%20closures)

- [hoisting interview questions](https://medium.freecodecamp.org/function-hoisting-hoisting-interview-questions-b6f91dbc2be8)

- [Work through problems here](https://repl.it/@SageElliott/scopesProblems)



## Upcoming Events!

We host so many events! check out our [calendar](https://www.galvanize.com/events)

Visit the [Learn to code Seattle](https://www.meetup.com/Learn-Code-Seattle/) meetup for all upcoming events.

[Python 101](https://www.eventbrite.com/e/javascript-mini-bootcamp-fundamentals-i-tickets-54952026992) - 2/21/19 6:30 - 8:30pm

[JavaScript Mini Bootcamp: Fundamentals I](https://www.eventbrite.com/e/javascript-mini-bootcamp-fundamentals-i-tickets-54952026992) - 2/23/19 10am - 4:30pm

[JavaScript 101](https://www.eventbrite.com/e/javascript-101-tickets-54952136319) - 2/27/19 6:30 - 8:30pm

## What is Galvanize?

#### Immersive Bootcamp


- [Software Engineer](https://www.galvanize.com/web-development) - 4/8/19 - 7/5/19
- [Data Science](https://www.galvanize.com/data-science) - 5/6/19 - 8/6/19


#### Part-Time Courses

- [Intro to Data Science](https://www.galvanize.com/part-time/intro-to-data-science) - 3/4/19 - 4/24/19

- [Digital Marketing](https://www.galvanize.com/part-time/digital-marketing) - 4/15/19 - 6/7/19

#### Co-working Space

[work in our building!](https://www.galvanize.com/entrepreneur)

#### We are a community

## Questions

Please feel free to reach out to me with any questions! Let me know what you're planning to do next and how I can help!


- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

Questions about education at Galvanize SF email [learn@galvanize.com](mailto:learn@galvanize.com)


