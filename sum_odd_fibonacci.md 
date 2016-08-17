# Sum The Odd Fibonacci Numbers
#### This function takes a positive number num and returns the sum of all the odd Fibonacci numbers that are less than or equal to num.
```
	function sumFibs(num) {
	  var y = total = 0;
	  var x = z = 1;
	  while ( z <= num){
	    if (z % 2 !== 0) {
	        total += x;
	    }
		    z = y + x;
		    x += y;
		    y = x - y;
	  }

	  return total;
	}
	sumFibs(75024);
```