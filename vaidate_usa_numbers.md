# Validate US Telephone Numbers
#### This function returns true if the passed string is a valid US phone number.
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

telephoneCheck("555-555-5555");
```


