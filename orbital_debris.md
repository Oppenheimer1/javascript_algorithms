# Orbital Debris
#### This function returns a new array that transforms the element's average altitude into their orbital periods.
```
function orbitalPeriod(arr) {

	  var standard_gravitational_parameter_Earth = 398600.4418;
	  var radius_Earth = 6367.4447;

	    return arr.reduce(function(newArray,satellite)
                       {
	  	 var satelliteOrbitalPeriod = Math.round(2*Math.PI*Math.sqrt(Math.pow(radius_Earth + satellite.avgAlt, 3)/standard_gravitational_parameter_Earth));
	  		newArray.push({name:satellite.name, orbitalPeriod: satelliteOrbitalPeriod});
        
	  		return newArray;
	  }, []);
  
  
}

orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);
```
