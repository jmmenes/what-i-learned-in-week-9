# What I Learned In Week 9 At Code Immersives

&nbsp;

## Types of Functions

&nbsp;

    // Named functions
    function doSomething() {
    console.log('you clicked the red box!');
    }

    const redBox = document.querySelector('.centered-box');

    redBox.addEventListener('click', doSomething);

&nbsp;

An anonymous function is a function without a name. An anonymous function is often not accessible after its initial creation.

    // Anonymous functions
    const bigGreenBox = document.querySelector('.box-2');

    bigGreenBox.addEventListener('click', function () {
    console.log('you clicked the big green box');
    });

&nbsp;

An arrow function expression is a compact alternative to a traditional function expression, but is limited and can't be used in all situations.

Differences & Limitations:

- Does not have its own bindings to this or super, and should not be used as methods.
- Does not have arguments, or new.target keywords.
- Not suitable for call, apply and bind methods, which generally rely on establishing a scope.
- Can not be used as constructors.
- Can not use yield, within its body.

        // Anonymous arrow function
        const container = document.querySelector('.container');
        container.addEventListener('click', () => {
        console.log('you clicked the first gray container');
        });

&nbsp;

## Adding Event Listeners In a Loop

    // Adding event listeners in a loop
    const purpleBoxes = document.querySelectorAll('.small-inner-box');

    for (const box of purpleBoxes) {

    box.addEventListener('click', function (event) {

    console.log(event);
    const elementThatWasClicked = event.target;
    elementThatWasClicked.style.backgroundColor = 'green';
    });

    }

&nbsp;

## Transitions

    // Transitions
    const pinkSquare = document.querySelector('.transition-element');
    pinkSquare.addEventListener('click', function () {
    pinkSquare.classList.add('invisible');
    });

The classList property returns the class name(s) of an element, as a DOMTokenList object.

This property is useful to add, remove and toggle CSS classes on an element.

The classList property is read-only, however, you can modify it by using the add() and remove() methods.

&nbsp;

## Math.random()

The Math.random() function returns a floating-point, pseudo-random number in the range 0 to less than 1

- Will return a number between 0 and 1, you can then time it up to get larger numbers.
- When using bigger numbers remember to use Math.floor if you want it to be a integer

        // Will return a integer between 0 and 9
        Math.floor(Math.random() _ 10)

        // Will return a integer between 0 and 10
        Math.floor(Math.random() _ 11)

&nbsp;

## Math.floor()

The Math.floor() function returns the largest integer less than or equal to a given number.

    console.log(Math.floor(5.95));
    // expected output: 5

    console.log(Math.floor(5.05));
    // expected output: 5

    console.log(Math.floor(5));
    // expected output: 5

    console.log(Math.floor(-5.05));
    // expected output: -6

&nbsp;

## sort()

The sort() method sorts the items of an array.

The sort order can be either alphabetic or numeric, and either ascending (up) or descending (down).

By default, the sort() method sorts the values as strings in alphabetical and ascending order.

This works well for strings ("Apple" comes before "Banana"). However, if numbers are sorted as strings, "25" is bigger than "100", because "2" is bigger than "1".

Because of this, the sort() method will produce an incorrect result when sorting numbers.

    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.sort();

    // output: Apple, Banana, Mango, Orange
