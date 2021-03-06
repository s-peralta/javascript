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
<i> The trick is to add the "(" before the function and "()" after </i>

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

Parsing Json
---------------------

```

var data={
  "firstName":"Ray",
  "lastName":"Villalobos",
  "joined":2012
};

var placeholder = document.querySelector(".placeholder");
    placeholder.innerHTML = data.firstName +" "+ data.lastName +" "+ data.joined;

```
Declare an html element with the "class" attribute of ".placehoder" and the "innerHTML" will inject json object inside of it 

```
var shell = document.querySelector("ul.shell"),
output = "";

for(var i=0; i < newData.users.length ; i++){

	console.log(newData.users[i].firstName +" "+ newData.users[i].lastName + " -Joined- " + newData.users[i].joined.month + "/" + newData.users[i].joined.day +"/"+ newData.users[i].joined.year);

	output+= "<li>" + newData.users[i].firstName +" "+ newData.users[i].lastName + " -Joined- " + newData.users[i].joined.month + "/" + newData.users[i].joined.day +"/"+ newData.users[i].joined.year + "</li>";

}

shell.innerHTML = output

```

Canvas
---------------------
Resource : http://hop.ie/blog/particles/?utm_source=gamedevjsweekly&utm_medium=email
```

var canvas = document.createElement("canvas"); // Create the canvas html element
var context = canvas.getContext("2d"); // Define whether canvas will be 2D or 3D
canvas.width = 500; // Define width
canvas.height =500; // Define height
document.body.appendChild(canvas); // Throw the canvas node in the body

context.fillRect(0, 0, canvas.width, canvas.height);  //The fillRect method draws a filled rectangle on the canvas. It is used by setting the starting X and Y values in pixels, then the shape to draw. In this case we start the rectangle at the top left corner (0,0) and draw a rectangle

// When a fillStyle is not specified, it will default to black.

// TIME TO MAKE A BADASS PARTICLE
context.fillStyle = "white";
context.fillRect(300, 200, 10, 10); // X , Y , width , height

//Canvas includes an arc function that can draw curved shapes, and we can use it to make a round particle.
//content.arc(x, y, radius, startAngle, endAngle, anticlockwise)


// After setting the fill style, draw an arc on the canvas
context.arc(400, 200, 10, 0, Math.PI*2, true);
context.fillStyle = "white"; 
context.fill();

// Let's get some movement going - Set up a position variable 
var posX = 20,
posY = 100;

// Draw shapes on the canvas using an interval of 30ms

setInterval(function() {

	posX += 1;
	posY += 0.25;
	
	//This will result in the canvas being redrawn each time, creating what looks like the particle moving across the canvas
	context.fillStyle = "black";
	context.fillRect(0,0,canvas.width, canvas.height)
	
	// Draw a circle particle on the canvas
	context.beginPath();
	context.fillStyle = "white";
	
	// After setting the fill style, draw an arc on the canvas
	context.arc(posX, posY, 10, 0, Math.PI*2, true); 
	context.closePath();
	context.fill();

}, 30);
```

