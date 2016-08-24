# Spinal Case
#### This function taks a string and converts it so that all the words are converted to lowercase words and are joined by dashes.
```
function spinalCase(str) {

  return str.replace(/[_]/g, "-").replace(/ /g, "-").replace(/(?!^)([A-Z])/g, '-$1').replace(/--/g, "-").toLowerCase();
   
}

spinalCase("Teletubbies say Eh-oh");
```