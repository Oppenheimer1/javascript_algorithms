# Smallest common multiple
#### This function finds the smallest common multiple of the provided numbers that can be evenly divided by both the provided numbers and can be evenly divided by all the sequential numbers in the range between the provided numbers.
```
function smallestCommons(arr) {
 
   	var range = arr.sort();
 	var newArr = [];
 	for(var i=arr[0];i<=arr[arr.length-1];i++){
 		newArr.push(i);
 	}
 	
    var x = true;
    var leastCommonMultiple = 0;
    while(x){
    	leastCommonMultiple++;
    	for(var j=newArr[0];j<=newArr[newArr.length-1];j++){
    		if(leastCommonMultiple%j !==0){
    			break;
    		}
    		else if(j==newArr[newArr.length-1]){
    			x = false;
    		}
    	}
    }
    
  return leastCommonMultiple;

}


smallestCommons([1,5]);
```
