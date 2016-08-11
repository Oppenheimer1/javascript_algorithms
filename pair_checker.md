# Pair Checker
#### This function takes an array arr and finds element pairs whose sums equal the second argument arg and returns the sum of their indices.
```
function pairwise(arr, arg) {

var indexTotal = 0;
for(var i=0;i<arr.length;++i){
    var x=arg-arr[i];

    if (x>0){

    for(j=0;j<arr.length;++j)
    {

    if(x==arr[j])
        {
        if(i!=j)
        {

        indexTotal+=j;
        indexTotal+=i;

            arr[i]=arg+1;
            arr[j]=arg+1;
            break;
        }
        }
    }
    }
}
    return indexTotal;

}


pairwise([1,4,2,3,0,5], 7);
```