# Exact Change
### This is a cash register function that accepts purchase price as the first argument (price), payment as the second argument (cash), and cash-in-drawer (cid) as the third argument. The answer will return "Insufficient Funds" if the cash in the drawer is less than the change that is due. If the cash in the drawyer is equal to the change that is due the answer will return "Closed". Else the answer will return the change in coin and bills which are sorted in highest to lowest order.
```
function checkCashRegister(price, cash, cid) {
    
  var currency = [
    {name: 'ONE HUNDRED', value:100.00},
    {name: 'TWENTY', value:20.00},
    {name: 'TEN', value:10.00},
    {name: 'FIVE', value:5},
    {name: 'ONE', value:1.00},
    {name: 'QUARTER', value:0.25},
    {name: 'DIME', value:0.10},
    {name: 'NICKEL', value:0.05},
    {name: 'PENNY', value:0.01}
    ];
  
    var change = cash - price;

    var total_cash_in_drawer = cid.reduce(function(x, y){
        return x + y[1];
    }, 0.0);

    if(total_cash_in_drawer < change){
        return 'Insufficient Funds';
    }
    else if(total_cash_in_drawer === change){
        return 'Closed';
    }

    cid = cid.reverse();

    var finalAmt = currency.reduce(function(x, y, index){
        if(change >= y.value){
            var currentTotal = 0.0;
            while(change >= y.value && cid[index][1] >=y.value){
                currentTotal += y.value;
                change -= y.value;
                change = Math.round(change * 100) / 100;
                cid[index][1] -= y.value;
            }
            x.push([y.name, currentTotal]);
            return x;
        }else{
            return x;
        }
    }, []);
    return finalAmt.length > 0 && change === 0 ? finalAmt : 'Insufficient Funds';
}


checkCashRegister(19.50, 20.00, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.10], ["QUARTER", 4.25], ["ONE", 90.00], ["FIVE", 55.00], ["TEN", 20.00], ["TWENTY", 60.00], ["ONE HUNDRED", 100.00]]);
```