# Week 13: 5/4/26

## Agenda

1. Breakout Rooms on Final Project
2. Tutorial: Text, External Data, and Classes

---

## Breakout Rooms on Final Project

In the replies of the discussion post:

- Take some time to answer the questions written by your peer on what they specifically wanted feedback on.

Once you have answered their questions, write your own thoughts and feedback:

- Values: What is working for you? What do you find interesting, compelling, unique, striking of the project?
- Questions: What are you curious about? Interaction? Implementation? Theme?
- Polish: How would you improve this project?

## Tutorial: Text, External Data, and Classes

### Coding Glossary

<!-- prettier-ignore -->
| Vocab | Definition | Example |
| ----- | ---------- | ------- |
| string | a data structure that holds an array of characters ([mdn docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)).  | `let word = "cat"` |
| concatenation | using "+" to add strings together | `word = word + "!"` |
| string literal | also known as `template literal` or `template string`, using \` (backtick: a symbol on your keyboard shared with ~ key and next to 1) and `${}` to inject variables into a string | `${word}!` |

You can import any font to p5, and they have a pretty nice blog post about it: https://github.com/processing/p5.js/wiki/Drawing-Text-Using-Web-Fonts

### External Data

We can load in data from files, or other external resources like using APIs. This class won't touch too much on APIs but we can create or find data sources for our own projects. 

Some places to find data sources: 
- https://github.com/dariusk/corpora/
- https://github.com/public-apis/public-apis
- https://tinytools.directory/

We can also manipulate that data using the `loadStrings` function. This is done inside the preload:

```js
// global variable to store data
let entireText;

function preload(){
    entireText = loadStrings('myFile.txt')
}
```

We can do any of our string manipulations with the entire text, such as splitting it into an array of words. Because strings are *arrays of characters*, you can do anything on an array inside of a string. 

### Classes

A class is a template that allows us to create customizable objects. 

Some useful resources:
- [p5 class definition](https://p5js.org/reference/p5/class/)
- Coding Train [Part 6: Classes in ES6](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/6-objects/2-classes)
- https://javascript.info/constructor-new

Classes are an object that use `{}`. To create a class, we usually write them in an external file or at the bottom of the code. 

```js
class MyClass{

}
```

Classes always require a function called a `constructor()` that is the starting point of the template. 

```js
class MyClass{
    constructor(){

    }
}
```

There is a special keyword for a class for properties that are a part of an object: `this`. What it means is the reference to the object you are creating. Why this is helpful is you can create multiple objects following a template.

Let's look at two objects:

```js
let myObject1 = {
    x: width/2,
    y: width/2,
    size: 50
}

let myObject2 = {
    x: width/4,
    y: width/4,
    size: 50
}
```

These have the same properties of `x` and `y`. When we want to access one of those properties, we use `myObject1.x` or `myObject2.y`. Instead of duplicating object variables, we can create a template:

```js
class Object {
    constructor(startingX, startingY){
        this.x = startingX
        this.y = startingY
        this.size = 50
    }
}
```

If we want to create a copy of this template, we can populate with customizable values passed into the constructor.

```js
let myObject1 = new Object(width/2, height/2)
let myObject2 = new Object(width/4, height/4)
```

Each time we use the `new` keyword, it calls the `constructor()` function. `this` is in reference to the object being created, so by using `this` we are saying that `myObject1` has a property of `x` and can access it just as we did in our basic object example `myObject1.x`.

Classes also allow us to create `methods` inside of them. 

```js
class Object {
    constructor(startingX, startingY){
        this.x = startingX
        this.y = startingY
        this.size = 50
    }
    move(){
        this.x++
        if(this.x > width){
            this.x = 0
        }
    }
}
```

We can move our object by calling `myObject1.move()` in our draw.