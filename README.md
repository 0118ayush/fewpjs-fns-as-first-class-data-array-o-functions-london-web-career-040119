# JavaScript Fns as First Class Data: Array of Functions

## Learning Goals

- Create a JavaScript function that loops through a function `Array`

## Introduction

To reiterate about functions in JavaScript as "first-class" objects, it can
do all the things that regular objects can do, To illustrate this concept,
we're going to create an array that contains a number of JavaScript functions.

### Create a JavaScript Function That Loops Through a Function `Array`

Remember our workout program from "Creating Functions in JavaScript"? Let's take
a similar concept, and create function that will iterate over a daily dog-walking
routine.

```
console.log("Wake Byron the poodle");
console.log("Leash Byron the poodle");
console.log("Walk to the park with Byron the poodle");
console.log("Throw the frisbee for Byron the poodle");
console.log("Walk home with Byron the poodle");
console.log("Unleash Byron the poodle");
```

Let's give this each activity its own function:

```js
function wakeDog() {
  console.log("Wake Byron the poodle");
}
...
```

Continue this pattern for functions `leashDog`, `walkToPark`, and so on. Run `learn` to 
execute the tests. The tests will cue you into the remaining expected functions
that should exist.

Let's take each function that we've created for activities and create variables for each. 
Set them to the corresponding function names you originally created, like below:

```js
var wakeDog = function() {
  console.log("Wake Byron the poodle");
}
```

Now that we have each activity set, we're going to create a function called `exerciseDog`.
Notice that there is repetitious language in each activity. Imagine that we are
professional dog sitters--the dog's name and breed might vary! Abstract out `${name}`
and `${dogBreed}`.

```js
function exerciseDog(dogName, dogBreed) {
...
...
```

Without further ado, let's create our "Array o' Functions!". Create a variable
called `routine`. This variable will be an `Array` all of the functions
we've defined: `wakeDog`, `leashDog`, etc. 

Lastly, create the function called `exerciseDog` that will iterate over our `functionsArray`
and return the full routine that includes a `dogName` and `dogBreed` passed in.

Assign default arguments to your parameters, so that the parameters' values won't be
`undefined`, and avoid errors that look like:

```
"Wake undefined the undefined"  // From: console.log("Wake ${dogName} the ${dogBreed}");
```

Instead, you can create something like this:

```js
function exerciseDog(dogName="Byron", dogBreed="poodle") {
...
```

Now, when the function is run, you should always see results such as:

```
"Wake Byron the poodle"  // From: console.log("Wake ${dogName} the ${dogBreed}");
```

To recap, your code should contain:
- Functions for each dog walking activity, set as variables
- A variable called `routine` set to an `Array` that contains each dog walking
function
- A function called `exerciseDog` with default parameters set that iterates over
the array and returns the full exercise routine.

## Conclusion

This lab demonstrates the power of `Function`s as first-class data. We can
stack them up in `Arrays` or assign them inside of `Objects` or save them
to variables, or iterate over them. Instead of _merely_ having `Array`s of
`String`s and other familiar items, we can stuff them with _work_. And that's
nothing short of amazing!
