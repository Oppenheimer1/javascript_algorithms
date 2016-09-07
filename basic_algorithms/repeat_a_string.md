# Repeat A String
#### This function takes a sting as input and repeats it num amount of times where num is the number of times the user wants the string to repeat.
```
function repeatStringNumTimes(str, num) {
  if(num<0){
    return '';
  }else{
  return str.repeat(num);
  }
}

repeatStringNumTimes("abc", 4)

```