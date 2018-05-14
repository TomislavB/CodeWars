# Total Competed: 2

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
