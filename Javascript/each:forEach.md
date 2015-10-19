#Each/ forEach

## Concept Definition
From the definition on Underscore's website:  

~~~
_.each(list, iteratee, [context]) 
~~~

As one would expect, this iterates through each value in the array. You cannot modify the values, you can only **use** them. There was confusion on my side that I have cleared up below.


###Misconceptions:

I map and each/forEach mixed up. for each/forEach, you do **not** get a returned result. You also **cannot** modify the values of the array you are looping through.

Both the assigning and modifying misconception I had are shown below:

~~~
var values = [1,2,3,4,5];

var underscoreResult = _.each(values, function(value){
  return value +=1;
});

var vanillaResult = values.forEach(function(value){
  return value += 1;
});

console.log(underscoreResult); //[1,2,3,4,5] - Nothing achieved
console.log(vanillaResult); //undefined
~~~

Without the assigning misconception, the result is still the same:

~~~
var values = [1,2,3,4,5];
var values2 = [1,2,3,4,5];

_.each(values, function(value){
  return value +=1;
});

values2.forEach(function(value){
  return value += 1;
});

console.log(values); //[1,2,3,4,5] - Nothing achieved
console.log(values2); //[1,2,3,4,5] - Nothing achieved
~~~

This misconception probably arised for my previous usage of for-loops. See the following example. Interestingly, I found that I also have a misconception about scopes. I seem to be unsure of when new variables link to previous ones - TODO a note on this.

~~~
var values = [1,2,3,4,5];
var values2 = [1,2,3,4,5];

//Like Underscores 'Map' function
for(var i = 0; i < values.length; i++){
  values[i] +=10; //'var' is unused here
}

//Like Underscores for/forEach function
for(var y = 0; y < values2.length; y++){
  var value = values2[y]; //Note the use of 'var'
  value += 10;
}

console.log(values); //[11,12,13,14,15] - changed
console.log(values2); //[1,2,3,4,5] - unchanged
~~~

###Example
