# Total Completed: 8

## Check your arrows

https://www.codewars.com/kata/559f860f8c0d6c7784000119

You have a quiver of arrows, but some have been damaged. The quiver contains arrows with an optional range information (different types of targets are positioned at different ranges), so each item is an arrow.
You need to verify that you have some good ones left, in order to prepare for battle:

anyArrows([{range: 5}, {range: 10, damaged: true}, {damaged: true}])
If an arrow in the quiver does not have a damaged status, it means it's new.

The expected result is a boolean, indicating whether you have any good arrows left.

```javascript
const anyArrows = arrows => arrows.some(arrow => !arrow.damaged);
```

## Multiply

https://www.codewars.com/kata/multiply/train/javascript

Multiply two numbers.

```javascript
const multiply = (a, b) => a * b;
```

## Even or Odd

https://www.codewars.com/kata/even-or-odd

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```javascript
function even_or_odd(number) {
  return number % 2 === 0 ? "Even" : "Odd";
}
```

## Counting Sheep

https://www.codewars.com/kata/counting-sheep-dot-dot-dot

Consider an array of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example,

```javascript
[true, true, true, false, true, true, true, true, false];
```

The correct answer would be 7.

```javascript
function countSheeps(arrayOfSheep) {
  var trueCounter = 0;
  for (i = 0; i <= arrayOfSheep.length; i++) {
    if (arrayOfSheep[i] === true) {
      trueCounter++;
    }
  }
  return trueCounter;
}
```

## String Repeat

https://www.codewars.com/kata/string-repeat

Write a function called repeatStr which repeats the given string string exactly n times.

```javascript
repeatStr(6, "I"); // "IIIIII"
repeatStr(5, "Hello"); // "HelloHelloHelloHelloHello"
```

Solution:

```javascript
function repeatStr(n, s) {
  var a = "";
  for (i = 0; i < n; i++) {
    a = a + s;
  }
  return a;
}
```

## Love Message

https://www.codewars.com/kata/jennys-secret-message

Write a function that returns a string "Johnny, my love" if the name entered is Johnny and if other name is entered function returns "Hello, ${name}!

Solution:

```javascript
const greet = name => "Hello, " + (name == "Johnny" ? "my love" : name) + "!";
```

## Grasshopper - Summation

https://www.codewars.com/kata/grasshopper-summation

Write a program that finds the summation of every number between 1 and num. The number will always be a positive integer greater than 0.

Solution:

```javascript
var summation = function(num) {
  var sum = 0;
  for (i = 1; i <= num; i++) {
    sum = sum + i;
  }
  return sum;
};
```

## UEFA EURO 2016

https://www.codewars.com/kata/57613fb1033d766171000d60

Finish the uefaEuro2016() function so it return string just like in the examples below:

uefaEuro2016(['Germany', 'Ukraine'],[2, 0]) // "At match Germany - Ukraine, Germany won!"
uefaEuro2016(['Belgium', 'Italy'],[0, 2]) // "At match Belgium - Italy, Italy won!"
uefaEuro2016(['Portugal', 'Iceland'],[1, 1]) // "At match Portugal - Iceland, teams played draw."

```javascript
function uefaEuro2016(teams, scores) {
  var teamA = teams[0];
  var teamB = teams[1];

  if (scores[0] > scores[1]) {
    return "At match " + teamA + " - " + teamB + ", " + teamA + " won!";
  } else if (scores[0] < scores[1]) {
    return "At match " + teamA + " - " + teamB + ", " + teamB + " won!";
  } else if (scores[0] === scores[1]) {
    return "At match " + teamA + " - " + teamB + ", teams played draw.";
  }
}
```
