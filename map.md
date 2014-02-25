The map function operates on an array of values. It transforms each value with an iterator function, and returns a new array with the transformed values.

````
var array = [6, 19, 27, 31];

array = _.map(array, function (val) { return val === 6 });
// [true, false, false, false]
````

