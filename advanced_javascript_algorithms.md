```
function telephoneCheck(str) {

	if (str.match(/^((1\s*)?(\(\s*(\d{3})\s*\)|(\d{3}))\s*([-]\s*)?)(\d\d{2})\s*([-]\s*)?(\d{4})$/g)) {
	            return true;
	        }
	        else
	        {
	            return false;
	        }
}
```