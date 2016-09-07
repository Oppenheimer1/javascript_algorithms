# Palindrome
#### This function takes a sting as input and returns true if the given string is a palindrome. Otherwise, it returns false. A palindrome is a word or sentence that's spelled the same way both forward and backward, ignoring punctuation, case, and spacing.
```
function palindrome(str) {
  var softString = str.replace(/[^A-Z0-9]/ig, "").toLowerCase();  
  var newString = softString.split('').reverse().join('');
      
   if(newString === softString){
    return true;
  }
  else{
    return false;
  }
  
}

palindrome("never odd or even")

```