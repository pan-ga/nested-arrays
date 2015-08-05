# Nested Arrays
## Opening
 - What are they going to learn?
  - Today we will be going over Nested Arrays, which is exactly like how it sounds. Think of it like the movie **Inception**  - dream within a dream. We will learn how to create an array within an array or a nested arrays. Then look into how we could operate on them. This will be taught as if it was the first time.
 - Why is is it important? **(Ask students what they think)**
  - Can be used to organize sets of data
  - Can be used to represent hiearchy
 - How it relates to previous work?
  - We learned about arrays in the past
    - what can arrays store (numbers, strings, objects,...arrays)?
  - How will learning occur?
   - To learn this material we'll use what we know about arrays (creating, traversal, accessing) then do an **Inception** on it.

## Objectives
by the end of this lesson you will be able to
- Do inception on Arrays
- Understand practical use cases for nested arrays
- Manipulate nested arrays using `map`
- Manipulate nested arrays using `filter`


> **Editor:** http://repl.it/BAJE

**Warm up**
- Let's start off with regular array to review
- We'll take a array of names and append 'the great' to it

> **Code along (5 minutes)**

```javascript
// Array Manipulation
var names = ['Lichard', 'Kathew', 'Omily'];

// Make them all name... the great
var theGreatNames = names.map(function(name){
    return name + '... the great';
});
```

> **We do** - what should the result be?

### Introduce Nested Arrays
> **I do (5 minutes)** - We mentioned earlier that arrays can do inception and hold any type of data.

```javascript
// Array Within Array Manipulation
var meals = [
    ['milk', 'cereal'],
    ['meat', 'sauce', 'bread'],
    ['pasta', 'sauce', 'meat']
];
```
> **Check Understanding** - how is this?


### Looping through Nested Arrays
> **You do** - If arrays could do inception, what about loops? Individually write code to print all values in this array.

> **Review** - If we recall, this is the structure for a loop

```javascript
for(var i = 0; i < array.length; i++) {...}
```

> **Activity (15 minutes)** - check understanding

```javascript
var meals = [
    ['milk', 'cereal'],
    ['meat', 'sauce', 'bread'],
    ['pasta', 'sauce', 'meat']
];

for(var i = 0; i < meals.length; i++) {
  for(var j = 0; j < meals[i].length; j++) {
    console.log(meals[i][j]);
  }
}
```

### Filtering through Nested Arrays

> **Review** - Filter returns a new array with all elements that passes a test implemented by your provided function
```javascript
someArray.filter(function() {
 if(something) {
  return true;
 }
 return false;
});
```
**Check Understanding** - check understanding.

**You do (15 minutes)** - Individually, filter for a all meals with sauce

**Outcome**
```javascript
// Array Within Array Manipulation
var meals = [
    ['milk', 'cereal'],
    ['meat', 'sauce', 'bread'],
    ['pasta', 'sauce', 'meat']
];

// Obtain all meals with sauce
var saucyMeals = meals.filter(function(thatMeal){
    for(var i=0; i<thatMeal.length; i++){
        if (thatMeal[i] === 'sauce'){
            return true
        }
    }
    return false;
});
```

### Objects within Arrays

> **Code along** - Often we work with many types of objects. If we wanted to group them, how would we do that? (Ask class)
**Review** - JavaScript Objects are key value pairs

> `{name: 'lichard', age: 3}`.

**Show code**
```javascript
// Object Within Array Manipulation
var people = [
    {name: 'lichard', age: 3},
    {name: 'kathew', age: 33},
    {name: 'omily', age: 13}
];
```

> **Review**
```javascript
myArray.map(function(element, index) {
 // do something...
});
```

> **You do (15 minutes)** - update each person object to have a club attribute set to Koalas using map

**Outcome**
```javascript
// Object Within Array Manipulation
var people = [
    {name: 'lichard', age: 3},
    {name: 'kathew', age: 33},
    {name: 'omily', age: 13}
];

// Each is in the koala club! Place that in their attributes
var koalaClub = people.map(function(person){
    person.club = 'Koalas';
    return person;
});
```

> **Check understanding**

<br>

> **I do** - based on what we know about objects we could also store any type of data in an object as well.
As a person I have many hobbies. How do you think we could represent that in an object? Hint hint, remember **inception**.

**Outcome**
```javascript
// Array Within Object Within Array Manipulation
var people =[
    {name: 'lichard', age: 3, hobbies: ['bug picking', 'eating', 'music']},
    {name: 'kathew', age: 33, hobbies: ['fencing', 'dat bass']},
    {name: 'omily', age: 13, hobbies: ['skateboarding', 'music']}
];
```

> **Acivitity (20 minutes)** - In groups of two or three filter through an array of people for people who like music

**Outcome**
```javascript
// Array Within Object Within Array Manipulation
var people =[
    {name: 'lichard', age: 3, hobbies: ['bug picking', 'eating', 'music']},
    {name: 'kathew', age: 33, hobbies: ['fencing', 'dat bass']},
    {name: 'omily', age: 13, hobbies: ['skateboarding', 'music']}
];

// Find all the music fans
var musicFans = people.filter(function(person){
    var hobbies = person.hobbies;
    for(var i=0; i<hobbies.length; i++){
        if (hobbies[i]==='music'){
            return true;
        }
    }
    return false;
});
```

> **Check understanding**

## Closing
- Today we went over arrays within array AKA Inception
- Then we incepted loops - loops within loops
- Then inception within inception - objects with arrays within arrays
- Then used filter and mapped on this objects with arrays within arrays
- And this could go on and on - arrays within array within arrays, so enjoy!
