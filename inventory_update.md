# Inventory Update
#### This function compares and updates the inventory stored in a 2D array against a second 2D array of a fresh delivery. If an item cannot be found, it adds the new item and quantity into the inventory array. The returned inventory array is in alphabetical order by item.
```
function updateInventory(arr1, arr2) {
    var newInventory = arr1.concat(arr2).reduce(function(x, y){
        if(x[y[1]])
        {
            x[y[1]] += y[0];
        }
        else
        {
            x[y[1]] = y[0];
        }
        return x;
    }, {});

    return Object.keys(newInventory).map(function(z){
        return [newInventory[z], z];
    }).sort(function(a,b){
        if(a[1] === b[1])
        {
            return 0;
        }
        else
        {
            return (a[1] < b[1]) ? -1 : 1;
        }
    });
}

var curInv = [
    [21, "Bowling Ball"],
    [2, "Dirty Sock"],
    [1, "Hair Pin"],
    [5, "Microphone"]
];

var newInv = [
    [2, "Hair Pin"],
    [3, "Half-Eaten Apple"],
    [67, "Bowling Ball"],
    [7, "Toothpaste"]
];

updateInventory(curInv, newInv);
```