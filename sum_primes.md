# Sums the Primes
#### This function sums all the prime numbers up to and including the provided number.
```
function sumPrimes(num) {
  var numArr = [];
  for(var i =2; i<=num; i++){
    for(var j=2; j<=i; j++){
      if(i===j){
        numArr.push(i);
      }
      if(i%j===0){
        break;
      }
    }
  }
  return numArr.reduce(function(x,y){return x+y;});
}

sumPrimes(10);
```