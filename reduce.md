Reduce performs a compounding operation on an array of values, returning a single value. A 'memo' value is given, which is transformed by each step of the iterator and then returned.

````
var array = [15, 23, 45, 21];
array = _.reduce(array, function (memo, num) { return memo - num; }, 0);
// -104
````