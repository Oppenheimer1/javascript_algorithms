# String Reverse
#### This function takes a string as input and returns the length of the longest word in the string.
```
function findLongestWord(str) {
  
  var newStr = str.split(" ");
  str = newStr.sort(function(a,b){
    return b.length - a.length;
  })[0];
  
  return str.length;
}

findLongestWord("What is the average airspeed velocity of an unladen swallow")

```