# Reduce

##Definition
From the definition on Underscores website:  

~~~
_.reduce(list, iteratee, [memo], [context])
~~~


It is used in the following situation: When you want to loop through an array, taking specific values from the array and inserting them into a single source. 

##Examples

###Example 1
An  example could be as follows: You have an array of values and a single variable which you wish to be equal to the summed values of an array

~~~
var values = [1,2,3,4,5];
~~~

The 'old' way to do this would be as follows:

~~~
/* Using Underscore's each function */
var totalUsingUnderscoreEach = 0;

_.each(values, function(value){
  totalUsingUnderscoreEach += value;
});
console.log(totalUsingUnderscoreEach); //15
~~~

Or

~~~
/* Using Vanilla Javascript */
var totalUsingVanillaForLoop = 0;

for(var i = 0; i < values.length; i++){
  totalUsingVanillaForLoop += values[i];
}
console.log(totalUsingVanillaForLoop); //15
~~~

Reduce can be used as follows:

~~~
var values = [1,2,3,4,5];

var total = _.reduce(values, function(total, value){
    return total + value;
}, 0); //The total is initialised here
~~~

In this example,  the values array is looped through, with the corresponding index equivalent to value. The 'total' variable is initialised at the end of the function with a value of 0.

###TODO
Do an example where we use an object for the initialisation. I have done it before but now I only get:
"Cannot assign to read only property 'world' of 1" is an error I encounter when I try do an example where I use an object. 

Do an example using vanilla javascript. Perhaps you can do an example using ES6 as well?


