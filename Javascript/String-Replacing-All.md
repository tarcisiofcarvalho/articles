# Javascript - Replace function

As Java and other languages, Javascript has the .replace(...) function for strings. Please see below some examples:
   
#### Replacing the first occurrence

```javascript
var my_str = "& I love my car &";

my_str.replace("&", " ");

```
Printing the my_str you will see "  I love my car &"

#### Replacing all occurrences

There are more ways to replace all occurrences, the suggestion below looks like the simplest 

```javascript
var my_str = "& I love my car &";

my_str.replace(/[&]/g," ");

```
To replace all we are using *regex* in the first argument of the replace function. The char **g** means (global), then the char **&** will be replaced globally in the string.
Printing the my_str you will see "  I love my car  "
