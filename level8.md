# Total Completed: 3

## Check your arrows

https://www.codewars.com/kata/559f860f8c0d6c7784000119

You have a quiver of arrows, but some have been damaged. The quiver contains arrows with an optional range information (different types of targets are positioned at different ranges), so each item is an arrow.
You need to verify that you have some good ones left, in order to prepare for battle:

anyArrows([{range: 5}, {range: 10, damaged: true}, {damaged: true}])
If an arrow in the quiver does not have a damaged status, it means it's new.

The expected result is a boolean, indicating whether you have any good arrows left.

```javascript
function anyArrows(arrows) {
  return arrows.some(elem => elem.damaged !== true);
}
```

## Multiply

https://www.codewars.com/kata/multiply/train/javascript

Multiply two numbers.

```javascript
function multiply(a, b) {
  return a * b;
}
```

## Even or Odd

https://www.codewars.com/kata/even-or-odd

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```javascript
function even_or_odd(number) {
  return number % 2 === 0 ? "Even" : "Odd";
  //  return number % 2 === 1 || number % 2 === -1 ? "Odd" : "Even";
}
```
