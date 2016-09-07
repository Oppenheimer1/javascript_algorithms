# Title Case
#### This function takes a string as input and capitalizes the first letter in each word in the string.
```

function titleCase(str) {  
	return str.replace(/\w\S*/g, function(txt){return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();});
}

titleCase("I'm a little tea pot");

```