Given the string representations of two integers, return the string representation of the sum of those integers.

For example:

sumStrings('1','2') // => '3'

A string representation of an integer will contain no characters besides the ten numerals "0" to "9".

first idea was wrong: 
```js
//This one is not correct 
function sumStrings(a,b) { 
  return (+a + +b).toString()
}
//this is correct
function sumStrings(a,b) { 
  return ((BigInt(a)) + BigInt(b)).toString();
}
```

```diff
! BigInt is a special numeric type that provides support for integers of arbitrary length.

! A bigint is created by appending n to the end of an integer literal or by calling the function BigInt that creates bigints from strings, numbers etc.
```
