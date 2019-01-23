# JavaScript Functions & Scopes 

## short URL to this repo [jsfunc.sage.codes](https://github.com/sagecodes/into-to-sql)

## Setting up your computer:

- Open your web browser. I'll be using [chrome](https://www.google.com/chrome/), but  you can use [Safari](https://www.apple.com/safari/) or [Opera](https://www.opera.com/)(browsers that support [Web SQL](https://en.wikipedia.org/wiki/Web_SQL_Database)). 
- to speed up learning we're going to use an [online editor and database](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all) for SQL from [W3Schools](https://www.w3schools.com/). 

That was easy!


## Galvanize 

### Welcome to Galvanize!

We create a technology ecosystem for learners, entrepreneurs, startups, and established companies to meet the needs of the rapidly changing digital world.

Upcoming JavaScript workshops:


We're an awesome community!!! 

Interested in learnig more about our Galvanize programs reach out to Lauren @ [lauren.lark@galvanize.com](mailto:lauren.lark@galvanize.com)


## Setting up


## About me:
I'm [Sage Elliott](http://sageelliott.com/). I'm a Technology Evangelist at Galvanize Seattle. In the past decade I've worked as a software and hardware engineer with mostly with Startups and Agencies in Seattle and Central Florida. I love technology! I'm currently learning more about Deep Learning & Computer Vision.

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

You can't learn EVERYTHING in ~2 hours. But you can learn enough to get excited and comfortable to keep working and learning on your own!

- This course is for absolute beginners
- Ask Questions!
- Answer Questions!
- Help others when you can
- Its ok to get stuck, just ask for help!
- Feel free to move ahead
- Be patient and nice

### Challenges:

Get the most out of this workkshop! We'll occasionally do a "CHALLENGE" where I give you an exercise to do in several minutes. It can be even more effective to partner up with someome next to you, but you can work on your own if you want. No pressure to solve the challenge. I'll share how I would solve it after the time is up. 

https://repl.it/@SageElliott/jsFunStuff

## What is javaScript?

### Its not Java

"The relationship between Java and JavaScript is almost exactly like that between grapes and grapefruit"

Java is an entirly different programming language.


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

Const is used to declare variables you do not want to change later in your code. This helps yourself and other developers working on your team prevent accidentally re-writting a variables that was not supposed to be.  

What will happen when we try to overwrite the variable in the below example?

```
const greeting = "hello"

console.log(greeting)

// You can NOT change the variable declared with const
greeting = "bye"

console.log(greeting)
```

#####  functions


```

let greeting = "hello"

function greet (saying) {
  console.log(saying)
}

greet(greeting)

```


#### JavaScript Runtime

How does JavaScript run.

below we will see an example of what we just talked about:

### Hoisting in action 
What is hoisting exactly

### Variables hoisting in action

```

```

```

```

```

```

technically `let` & `const` get hoisted, but are caught is something called the *temporal dead zone*. Read more about that [here](
https://stackoverflow.com/questions/31219420/are-variables-declared-with-let-or-const-not-hoisted-in-es6).

### Variable block level declaration

Introduced in  ES6 (newer version of JavaScript)

We can use block level declaration with `let` and `cost`

```
```

```
```


## JavaScript Functions:

### Function Hoisting in action!

```

```

### using return 
console log vs return

### Function Challenges


## JavaScript Scopes

### Scope

What is a Scope?




### Global Scope

##### Global Variables

A good way know if your variables are not global when writting code is look if variables are inside of a function or inside a set of curly brackets `{variable}`. If the variable is not in either of those it would be global and accessible anywhere in your code.

Global Variables:

```
var globalVariable = 'hello'
let globalVariable = 'hello'
const globalVariable = 'hello'
```

Above are examples of global variables. You will be able to access these variables anywhere in your code. including functions

```
let globalVariable = 'hello'

function example
```

often best practice to not use global variables when possible. 

```
Show 
Conflict & overwritting

```


### Local Variables


### Function Scope

```
Function example
```


### Block Scope

```
Block Example
```


### Function hoisting 

how effects scopes 


### lexical scoping


### Scopes Challenge

fix this bug

fix this bug

fix this bug


## JavaScript Closures

What is a closure?

### Closure challenge

Make a closure to fix bug


## Wrap up

<details>
  <summary>let and const are both special because...</summary>
	`let` and `const` declarations don't hoist like `var` and `function` declarations.
</details>



### Interview type questions:



## Keep Learning!!!

### Resources:
- [Free Data Science Prep](https://www.galvanize.com/data-science-prep) - Galvanize
- [Free Software Engineering Prep](https://www.galvanize.com/web-development/prep) - Galvanize

https://github.com/getify/You-Dont-Know-JS
https://github.com/getify/You-Dont-Know-JS/tree/master/scope%20%26%20closures



## Upcoming Events!

We host so many events! check out our [calendar](https://www.galvanize.com/events)

Visit the [Learn to code Seattle](https://www.meetup.com/Learn-Code-Seattle/) meetup for all upcoming events.

[JavaScript Mini Bootcamp: Fundamentals II](https://www.eventbrite.com/e/javascript-mini-bootcamp-fundamentals-ii-tickets-54008664369) - 1/26/19 10am - 4:30pm

[Web Scraping with Python](https://www.eventbrite.com/e/intro-to-web-scraping-with-python-tickets-540100886292) - 1/31/19 6:30 - 8:30pm

## What is Galvanize?

#### Immersive Bootcamp

- [Data Science](https://www.galvanize.com/data-science) - 1/22/19 - 4/19/19
- [Software Engineer](https://www.galvanize.com/web-development) - 2/9/19 - 5/17/19

#### Part-Time Courses

- [Data Analyitcs](https://www.galvanize.com/part-time/data-analytics) 2/12/19 - 5/2/19
- [Python Fundamentals](https://www.galvanize.com/part-time/data-science-fundamentals) - 2/20/19 - 3/29/19

#### Co-working Space

[work in our building!](https://www.galvanize.com/entrepreneur)

#### We are a community

## Questions

Please feel free to reach out to me with any questions!

This was only my 2nd time running this workshop, help improve it by giving me feedback :)

- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

Questions about education at Galvanize SF email [learn@galvanize.com](mailto:learn@galvanize.com)


