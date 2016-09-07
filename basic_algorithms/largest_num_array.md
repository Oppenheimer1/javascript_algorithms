# Largest Number From Each Array
#### This function takes an array of array's as input and returns an array consisting of the largest number from each provided sub-array.
```
function largestOfFour(arr) {

  var finalArr = [];
  for(var i=0; i<arr.length; i++){
    finalArr.push(Math.max.apply(Math, arr[i]));
  }
  return finalArr;
}

largestOfFour([[13, 27, 18, 26], [4, 5, 1, 3], [32, 35, 37, 39], [1000, 1001, 857, 1]])


```