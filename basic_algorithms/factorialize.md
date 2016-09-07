# Factorialize
#### This function takes an integer as input and returns the factorial of the provided integer.
```
function factorialize(num) {
  var x = 1;
  for(var i=num; i>0; i--){
     x *=i ;
  }
  return x;
  
}

factorialize(20);

```