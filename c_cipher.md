# Caesar cipher
#### This function takes a ROT13 encoded string as input and returns a decoded string.
```
function rot13(str) { 
  
  return str.replace( /[A-Za-z]/g , function(newStr) {
    return String.fromCharCode( newStr.charCodeAt(0) + ( newStr.toUpperCase() <= "M" ? 13 : -13 ) );
  } );
}

rot13("SERR CVMMN!");
```


