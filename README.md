Beginners Guide to JavaScript
=============================

<!--All of the credit for this cheat sheet goes to <a href="http://blog.adtile.me/authors/viljami/">Viljami S.</a>. Majority of this JS Guide is a condensed/straight to the point version of his article.-->

Syntax / Snippets / Best Design Patterns

Function Declaration
---------------------

```
function plus(a,b){
sum=a+b
return sum
};

plus(2,3); // 5

```

Function Expression / Function Literal
---------------------

```
var plus = function(a.b){
return a+b
};

plus(2,3) // 5
```

Self Invocing Function
---------------------

```
(function(){

  // Code get trigger on page load
  
})();

OR

(function(a,b){

  return a+b
  
})(2,4);

```

Object Literal Notation
---------------------

```
var person = {
firstName:"John",
lastName:"Doe",
age:50,
eyeColor:"blue"
};

```

Object Constructor
---------------------

```
var Person = function(sex, fn, ln){
  // Properties
  this.age = 0;
  this.sex = sex;
  this.firstname = fn;
  this.lastname = ln;

  // Methods
  this.setAge = function(value){
                  this.age = value;
  };
};

var Fred = new Person('male', 'Fred', 'Flintstone');
Fred.setAge(45

```

