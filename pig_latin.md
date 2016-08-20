# Pig Latin
#### This function translates the provided string to pig latin.
```
function translatePigLatin(str) {
 
  var newStr = str.split('');
  
      if(newStr[0]==='a' || newStr[0]==='e' || newStr[0] === 'i' || newStr[0] === 'o' || newStr[0]=== 'u' )
      {
         return str.replace(/\b([aeiou][a-z]*)\b/gi, "$1way");
      }
      else
      {
        return str.replace(/\b([bcdfghjklmnpqrstvwxy]+)([a-z]*)\b/gi, "$2$1ay");
      }
  
}

translatePigLatin("algorithm");
```