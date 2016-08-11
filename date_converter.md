# Date Converter
#### This function converts a date range consisting of two dates formatted as YYYY-MM-DD into a more readable format.
```
function makeFriendlyDates(arr) {

    var newArray = [];

    var d1 = arr[0].split("-");
    var d2 = arr[1].split("-");

    d1[1] = Number(d1[1]) - 1;
    d2[1] = Number(d2[1]) - 1;
    d1[2] = Number(d1[2]);
    d2[2] = Number(d2[2]);
    d1[0] = Number(d1[0]);
    d2[0] = Number(d2[0]);

    var months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];
    if((d1[0] === d2[0]) && (d1[1] === d2[1]) && (d1[2] === d2[2]) ){
        newArray.push(months[d1[1]] + " " + days(d1[2]) + ", " + d1[0]);
        return newArray;
    }
    else if(d2[1] - d1[1]>= 1 && (d2[0] - d1[0] === 0))
    {
        newArray.push(months[d1[1]] + " " + days(d1[2]) + ", " + d1[0]);
        newArray.push(months[d2[1]] + " " + days(d2[2]));
        return newArray;
    }
    else if((d1[1]===d2[1]) && d2[2]===d1[2] && (d2[0]-d1[0]>=1))
    {
        newArray.push(months[d1[1]] + " " + days(d1[2]) + ", " + d1[0]);
        newArray.push(months[d2[1]] + " " + days(d2[2]) + ", " + d2[0]);
        return newArray;
    }
  else if((d1[1] === d2[1]) && d2[0]-d1[0]>=1){
        newArray.push(months[d1[1]] + " " + days(d1[2]) + ", " + d1[0]);
        newArray.push(months[d2[1]] + " " + days(d2[2]));
        return newArray;
    }
  else if(d1[1] === d2[1]){   
    newArray.push(months[d1[1]] + " " + days(d1[2]));
    newArray.push(days(d2[2]));
  return newArray;
  }
  else if(d2[0] - d1[0] > 1)
  {
    newArray.push(months[d1[1]] + " " + days(d1[2]) + ", " + d1[0]);
    newArray.push(months[d2[1]] + " " + days(d2[2]) + ", " + d2[0]);
    return newArray;
  }
  else{
    newArray.push(months[d1[1]] + " " + days(d1[2]));
    newArray.push(months[d2[1]] + " " + days(d2[2]));
    return newArray;
  }
  function days(day){
    if(day === 1){
        return day + "st";
    }
    else if(day === 3)
    {
        return day + "rd";
    }
    else
    {
        return day + "th";
    }
  }
}


makeFriendlyDates(['2016-07-01', '2016-07-04']);
```