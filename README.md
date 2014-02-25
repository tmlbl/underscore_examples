The map function operates on an array of values. It transforms each value with an iterator function, and returns a new array with the transformed values.

````
var array = [6, 19, 27, 31];

array = _.map(array, function (val) { return val === 6 });
// [true, false, false, false]
````
Reduce performs a compounding operation on an array of values, returning a single value. A 'memo' value is given, which is transformed by each step of the iterator and then returned.

````
var array = [15, 23, 45, 21];
array = _.reduce(array, function (memo, num) { return memo - num; }, 0);
// -104
````
Extend creates a new object with the same set of values as one or many source objects. The operation is performed in order, so if multiple input objects have properties of the same name, they will be overwritten.
````
var plant = {
  strain: 'Blue Dream',
  plant_date: 'Aug 27 2013'
};
var plant2 = _.extend(plant);
````
Invert takes an object in and returns a new object where the keys and values of the input object have been switched. This will, of course, only work an an objects in which all values are string serializable.
````
var person = {
  name: 'Jim',
  occupation: 'unemployed'
};
var inversePerson = _.invert(person);
// {
//  Jim: 'name',
//  unemployed: 'occupation'
// }
````
Pluck is a convenience function for a map function that takes an array of objects and returns an array of just one property of those objects. This is a common use case for data parsing with Underscore.
````
var plants = [{ strain: 'Blue Dream', clone: true }, { strain: 'Trainwreck', clone: false }];
var strains = _.pluck(plants, 'strain');
// ['Blue Dream', 'Trainwreck']
````
Pick returns a copy of an object, but only having the properties specified in the pick function.
````
var object = {
  fee: 'fi',
  fo: 'fum'
}
var foo = _.pick(object, 'fee');
// { fee: 'fi' }
````
Union takes any number of arrays and returns an array of all unique values, removing any duplicates.
````
var array1 = ['James', 42, true, null]
var array2 = [42, 'Boolean', null]
var newArray = _.union(array1, array2);
// ['James', 'Boolean', 42, true, null]
````
Zip is useful when dealing with data tables stored as rows in arrays. It returns a column version of the data.
````
var table = _.zip(['Tim', 'Dan'], [true, false]);
// [['Tim', true], ['Dan', false]]
````