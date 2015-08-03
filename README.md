# nested-arrays
## Opening
- What are they going to learn?
  - Today we will be going over Nested Arrays, which is exactly like how it sounds. This will be taught as if it was the first. time.
- Why is is it important?
- How it relates to previous work?
- How will learning occur?

## Objectives
by the end of this lesson you will be able to
- Explain a nominal example for using different data structures
- Manipulate data structures using `map`
- Select data from structures using `filter`


```javascript

// Array Manipulation
var names = ['Lichard', 'Kathew', 'Omily'];

// Make them all name... the great
var theGreatNames = names.map(function(name){
    return name + '... the great';
})


// --------------

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
})

// --------------

// Object Within Array Manipulation
var people =[
    {name: 'lichard', age: 3},
    {name: 'kathew', age: 33},
    {name: 'omily', age: 13}
];

// Each is in the koala club!  Place that in their attributes
var koalaClub = people.map(function(person){
    person.club = 'Koalas';
    return person;
})

// --------------


// Object Manipulation
var lichard = {
    name: 'Lichard',
    age: 23,
    run: function(){
        console.log('Like the wind...');
    }
};

// Make lichard dance!!!
lichard.dance = function(){
    console.log('Booooogie!!!');
}


// --------------

// Array Within Object Within Array Manipulation
var people =[
    {name: 'lichard', age: 3, favs: ['movies', 'music']},
    {name: 'kathew', age: 33, favs: ['bananas', 'dat bass']},
    {name: 'omily', age: 13, favs: ['candy', 'music']}
];

// Find all the music fans
var musicFans = people.filter(function(person){
    var favs = person.favs;
    for(var i=0; i<favs.length; i++){
        if (favs[i]==='music'){
            return true;
        }
    }
    return false;
});
```
