# Week 06: 3/9/26

## Agenda

1. Review: Loops
2. Tutorial: Data Structures Part 1: Arrays
3. Tutorial: Data Structures Part 2: Objects
4. [Demos, Videos, Useful Links](#demos)

---

## Review: Questions on _anything_ so far?

Add to [this doc](https://cryptpad.fr/doc/#/2/doc/view/GR52yjmdqsIORMLveeYsc18PCZt1+7oqvvGBCxA1+Mo/)

## Data Structures Part 1: Arrays

### Coding Glossary: Arrays

| Review         |                                                                                          |
| -------------- | ---------------------------------------------------------------------------------------- |
| variable       | name for a placeholder piece of data                                                     |
| declaration    | using `let` to assign a value to a variable or using `function` to create a new function |
| variable types | `boolean`, `number`, `string` (words)                                                    |

| New terms |                                                                             |
| --------- | --------------------------------------------------------------------------- |
| array     | data structure that holds a _series_ of variables, uses `[]`, order matters |
| element   | one piece of array data                                                     |
| index     | location of a particular element, starting at index of 0                    |

#### Declaring an **_Array_**

```js
let myNewArray = [];
```

#### Initializing an array with **_Elements_**

```js
let myNewArray = [10, 15, 20];
```

#### Retrieving a specific **_Element_** with the **_Index_**

The index is the location of the data we want to grab. The location is automatically assigned because of the `array`, since it is a _series_ of data, so it always starts at 0 and increases by one for every element. When we want to retrieve a specific element, we use `[]` and the index (location) we want to grab.

```js
myNewArray[0]; // 10
myNewArray[1]; // 15
myNewArray[2]; // 20
```

#### Arrays are like tables

<table>
<tbody>
<tr><td>index</td><td>0</td><td>1</td><td>2</td><td>3</td></tr>
<tr><td>value</td><td>"this"</td><td>"is"</td><td>"a"</td><td>"sentence"</td></tr>
</tbody>
</table>

```js
let data = ['this', 'is', 'a', 'sentence'];
```

In code, we typically only want an array to hold 1 type of data. So it should be _either_ a list of numbers, booleans, or strings.

#### Arrays are Living Variables

We can change the value of an element in the array by reassigning it, like we do with normal variables.

```js
let teachers = ['Sam', 'Patrick', 'Rory'];
teachers[1] = 'Sam';
// override the old value, reassign to new
// teachers is now ["Sam", "Sam", "Rory"]
```

If we use an index (location), that does not exist yet, it will add empty `undefined` items in the series until it gets to that location.

```js
let animals = ['Cat', 'Dog']; // animals has elements at 0 and 1
animals[4] = 'Giraffe';
// animals is now ["Cat", "Dog", undefined, undefined, "Giraffe"]
```

This isn't the best way to add to an array, because we don't want to accidentally create empty variables.

---

#### Unique Attributes of an Array

JavaScript is an object-oriented programming language, so whenever we create a piece of data (like a variable or an array), it is considered an `object`.

`Objects` allow us to enact specific actions _on_ them. We need to reference the specific object in order to do that action.

##### `.push()`

`push()` is a function we have seen inside of p5, but [`.push()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push) is a function that exists in an array. We need to use the name of our array, and the `.` to use the specific function.

```js
let myArray = [2, 4, 6];
myArray.push(8);
// this automatically adds 8 to the end of the array
// the new array is [2, 4, 6, 8]
```

This adds an element to the end of the array.

**Note**: This is different from p5's `push()` method. p5 has redefined `push()`/`pop()` to store states. `.push()` has different syntax and _must_ be used _on_ an array. So anytime we see the prepending `.`, it likely means it needs to be used on an object.

##### properties

Properties are variables that are unique to an object (in this instance an array). We again use the `.` to reference a specific property we want to access.

Arrays have a property called [`length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length). This gives us how many items exist in the array.

```js
let myArray = [2, 4, 6]; // 3 items total
myArray.length; // this is 3
```

This counts the number of **_elements_** that exist inside the array.

##### Arrays and Loops

Typically it is very cumbersome to access every element inside of a loop every time. Given an array:

```js
let pets = ['dog', 'cat', 'hamster', 'giraffe', 'horse'];
```

If we want to use or reference any one of these we would need to do something like:

```js
print(pets[0]); // prints: dog
print(pets[1]); // prints: cat
print(pets[2]); // prints: hamster
print(pets[3]); // prints: giraffe
print(pets[4]); // prints: horse
```

But, we already see a pattern of a number increasing every time. So, using the attributes we know so far, we can go through the loop. We already know our end condition, because it is the number of elements in our loop. So we could write:

```js
for (let count = 0; count < 5; count++) {
	print(pets[count]);
}
```

But, our end condition might be malleable, or we might add another pet later on. So we can use the property `.length` instead of 5.

```js
for (let count = 0; count < pets.length; count++) {
	print(pets[count]);
}
```

If we wanted to make it clearer, we could declare a local variable:

```js
for (let count = 0; count < pets.length; count++) {
	let currentPet = pets[count];
	print(currentPet);
}
```

There is a shorthand for this! If we don't need to know the number, we can automatically create and assign `currentPet`:

```js
for (let currentPet of pets) {
	print(currentPet);
}
```

This is a special loop _just for arrays_, that is shorthand for assigning a variable to the index of the current iteration.

---

## Review Videos

- [7.1 What is an array?](https://www.youtube.com/watch?v=VIQoUghHSxU)
- [7.2 Arrays and loops](https://www.youtube.com/watch?v=RXWO3mFuW-I)

## Review Documentation (these are textbook definitions)

- [for...of](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) loops with arrays
- [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
