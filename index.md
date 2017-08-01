---
layout: default
---
# [](#header-1)Caesar's Cipher

>It is better to create than to learn. Creating is the essence of life.
>
>-Juslis Caesar


I have been going through coding problems and came across the Caesars Cipher and thought it might be useful enough to reference the functions.
_.charCodeAt()_ and _.fromCharCode()_. These two function will either produce a numeric value for a character or vice-versa.

```js
//Javascript example
String.charCodeAt(65); ==> A
String.FromCharCode(A); ==> 65
```

The range for capital letters is 65 to 90. This is the range for these letters so it is important for Caesar's Cipher challenge to remember that you fall with in rage.

the challenge involves creating a function that will replace a letter with the **ROT13** cipher. So, if we land on 65 and want to decode that letter "A", we add 13 to the code. We end up with 78, the letter N. 

to better illustrate...

| **65** | **66** | **67** | **68** | **69** | **70** | **71** | **72** | **73** | **74** | **75** | **76** | **77** |
|   A    |   B    |   C    |   D    |   E    |   F    |   G    |   H    |   I    |   J    |   K    |   L    |   M    |
|   N    |   O    |   P    |   Q    |   R    |   S    |   T    |   U    |   V    |   W    |   X    |   Y    |   Z    |
| **78** | **79** | **80** | **81** | **82** | **83** | **84** | **85** | **86** | **87** | **88** | **89** | **90** |

let's say you land on code 80 and you add ROT13 to it. We get 93, this is a code outside the range and to convert to ROT 83 we must subtract from 80. 80 - 13 we get 67, C. 

the solution to this is really 2 parts. Gathering the cipher code numbers and converting them properly in their appropriate range.

_sort out empty/spaces from string_
```js
if (str.CharCodeAt(i) < 65 || str.charCodeAt(i) > 90) {
  //return the new char using str.charAt(i);
}
```

_spliting what characters you subtract 13 vs add 13_
_sort out empty/spaces from string_
```js
if (str.charCodeAt(i) > 77) {
   //use the str.fromCharCode('converted number' - 13);
  } else {
  ////use the str.fromCharCode('converted number' + 13);
  }
}
```

this is the guts of the problem and the rest should be easy from here.

Cheers!





