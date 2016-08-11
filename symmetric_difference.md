# Symmetric Difference
### This function takes two or more arrays and returns an array of the symmetric difference 
```
function sym(a,b,c,d,e,f) {
  
  function sym_diff(a, b) {
    return a.filter(function(elem) {
      return b.indexOf(elem) == -1;
    });
}

    var x =  sym_diff(a,b).concat(sym_diff(b,a));

	if(c == null && d == null){
		return x;
	}
	else if(c!==null && d == null && e == null && f == null){
		var y = sym_diff(x,c);
		var z = sym_diff(x,c).concat(sym_diff(c,x));
		function onlyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
	var filterdArray = z.filter(onlyUnique);
	var finalArray = filterdArray.filter(function(e){
		return e;
	}); 
	return finalArray;
	}
	else if(c!==null && d !== null && e == null && f == null){
		var z = sym_diff(x,c).concat(sym_diff(c,x));
		function onlyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var n = sym_diff(z,d).concat(sym_diff(d,z));
		function trulyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}	
	
	var filterdArray = n.filter(trulyUnique);
	var finalArray = filterdArray.filter(function(e){
		return e;
	}); 
	return finalArray.sort();
	}
	else if(c!==null && d !== null && e !== null && f == null){
		var z = sym_diff(x,c).concat(sym_diff(c,x));
		function onlyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var n = sym_diff(z,d).concat(sym_diff(d,z));
		function trulyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var o = sym_diff(n,e).concat(sym_diff(e,n));
		function finalUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}	
	
	var filterdArray = o.filter(finalUnique);
	var finalArray = filterdArray.filter(function(e){
		return e;
	}); 
	return finalArray.sort();
	}
	else{
		var z = sym_diff(x,c).concat(sym_diff(c,x));
		function onlyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var n = sym_diff(z,d).concat(sym_diff(d,z));
		function trulyUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var o = sym_diff(n,e).concat(sym_diff(e,n));
		function finalUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
		var p = sym_diff(o,f).concat(sym_diff(f,o));
		function superFinalUnique(value, index, self) { 
	    return self.indexOf(value) === index;
	}
	
	var filterdArray = p.filter(superFinalUnique);
	var finalArray = filterdArray.filter(function(e){
		return e;
	}); 
	return finalArray.sort();
	}
	
}

sym([1, 2, 3], [5, 2, 1, 4]);

```