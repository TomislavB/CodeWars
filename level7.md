# Total Competed: 4

## Highest and Lowest number

https://www.codewars.com/kata/highest-and-lowest

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

Example:

highAndLow("1 2 3 4 5"); // return "5 1"
highAndLow("1 2 -3 4 5"); // return "5 -3"
highAndLow("1 9 3 4 -5"); // return "9 -5"
Notes:

All numbers are valid Int32, no need to validate them.
There will always be at least one number in the input string.
Output string must be two numbers separated by a single space, and highest number is first.

```javascript
function highAndLow(numbers) {
  var a = numbers.split(" ");
  var b = Math.max(...a).toString();
  var c = Math.min(...a).toString();
  return b + " " + c;
}
```

## Exes and Ohs

https://www.codewars.com/kata/exes-and-ohs/javascript

Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.

Examples input/output:

```javascript
XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false
```

```javascript
function XO(str) {
  var x = 0;
  var o = 0;

  var arr = str.toLowerCase();

  for (i = 0; i <= arr.length; i++) {
    if (arr[i] === "x") {
      x++;
    }
    if (arr[i] === "o") {
      o++;
    }
  }

  if (x === o || (x === 0 && o === 0)) {
    return true;
  } else {
    return false;
  }
}
```

## Categorize New Member

https://www.codewars.com/kata/categorize-new-member

The Western Suburbs Croquet Club has two categories of membership, Senior and Open. They would like your help with an application form that will tell prospective members which category they will be placed.

To be a senior, a member must be at least 55 years old and have a handicap greater than 7. In this croquet club, handicaps range from -2 to +26; the better the player the lower the handicap.

Input
Input will consist of a list of lists containing two items each. Each list contains information for a single potential member. Information consists of an integer for the person's age and an integer for the person's handicap.

Note for F#: The input will be of (int list list) which is a List>

Example Input
[[18, 20],[45, 2],[61, 12],[37, 6],[21, 21],[78, 9]]
Output
Output will consist of a list of string values (in Haskell: Open or Senior) stating whether the respective member is to be placed in the senior or open category.

Example Output
["Open", "Open", "Senior", "Open", "Open", "Senior"]

```javascript
function openOrSenior(data) {
  return data.map(
    ([age, handicap]) => (age > 54 && handicap > 7 ? "Senior" : "Open")
  );
}
```

## Binary Addition

https://www.codewars.com/kata/551f37452ff852b7bd000139

Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

```javascript
function addBinary(a, b) {
  return (a + b).toString(2);
}
```
