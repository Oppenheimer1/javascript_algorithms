```Validate US Telephone Numbers Algorithm
function telephoneCheck(str) {
  // Good luck!
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