# DNA PAIR CHECKER
#### This function takes as it's input a DNA strand that is missing it's paired element. The function Takes each character, get its pair, and returns the result as a 2d array.
```
function pairElement(str){
    var newArr = [];
    for (var i = 0; i < str.length; i++) {
        switch(str[i]){
           case "A":
             newArr.push([str[i],"T"]);
             break;
           case "C":
             newArr.push([str[i],"G"]);
             break;
           case "G":
             newArr.push([str[i],"C"]);
             break;
	       case "T":
             newArr.push([str[i],"A"]);
             break;
            }
        }
    return newArr;
}

pairElement("GCG");
```
