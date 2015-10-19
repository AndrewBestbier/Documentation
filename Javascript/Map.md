#Map

##Definition
From the definition on underscore's website:  

~~~
_.map(list, iteratee, [context])
~~~

Produces a **new array** of values by mapping each value in list through a transformation function (iteratee). It is used when you want to loop through an array, and have the result returned as a modified array.



##Examples

###Simple Example
In this example, we modifiy this array of values, to sqaure each value in the array.

~~~
var values = [1,2,3,4,5];

var result = _.map(values, function(value){
  return value * value;
});
~~~

###TODO 1: ES6 Mapping
I was looking through an ES6 React Project and found the following lines of code:

~~~
const topicListItems = this.props.topics.toKeyedSeq().map((topic, key) => {
      return (<TopicCountItem key={key} title={topic.get('text')} count={topic.get('count')}/>);
    }).toArray();
~~~

 
New things in this that need exploring and writing about. I think these are all fundemental ES6 concepts.

* **const** When do we use this properly? Var, val in other cases?
* **.get('key')** diffent syntax to topic.key? Can topic.key be used?
* **toArray()** Doesn't map already return an array?
* **toKeyedSeq()** 
* **=>** I have seen this in a few places, fundemental concept

###TODO 2: ES5 Mapping and vanilla javascript
Do an ES5 React example as well as a vanilla javascript example. Perhaps do speed tests on the internet and find the best of the three