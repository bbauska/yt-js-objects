---
title: "YouTube's JavaScript Objects"
author: "bbauska"
date last editted: "2/21/2024 5+pm"
output: 
  markdown:
    with some style
---

<h2>YT-JS-Objects</h2>

<h3><a href="https://www.youtube.com/watch?v=m9FrY5A-tao">JavaScript Objects on YouTube</a></h3>

This Edureka video on "JavaScript Object" will help you understand the different methods 
of creating objects in JavaScript. It will provide examples for each type and show you 
how to use objects in JavaScript.<br/>
( JavaScript Object Blog: https://www.edureka.co/blog/javascrip... )

<h3><a href="https://www.edureka.co/blog/javascript-object/">JavaScript Objects</a></h3>

<h3><a href="https://www.html-easy.com/learn/how-to-add-a-target-attribute-in-html/">
How-To's in HTML (a beginner's guide)</a></h3>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~ readme.md of yt-js-objects.bauska.org ~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 align="center">YouTube's JavaScript Objects</h2>

JavaScript is an Object-Oriented Programming language. The objects form the building 
blocks which are considered to be the most important data-type for the programming 
language. This article will provide in-depth knowledge about JavaScript Objects, 
how they are created and defined in the following sequence:

	- JavaScript Object
	- How to Create a new Object?
	- Properties
	- Methods
	- Accessors
	- Prototypes

<h3>JavaScript Object</h3>
JavaScript objects are similar to objects in real life which consists of different 
attributes and properties. These objects are defined as an unordered collection of 
related data, that are of primitive or reference types. These are defined in the 
form of “key: value” pairs.

<h4>JavaScript - javascript object - Edureka</h3>

These keys are variables or functions which are called as properties and methods 
of an object. You can create a JavaScript object as:

<pre>
let ObjectName = {
Property1 : "Value",
Property2 : "Value",
...
...
}
</pre>

<h3>How to Create a new Object?</h3>
There are 3 ways to create a new object:

<h4>By Object Literal</h4>
Syntax:

<pre>
object={property1:value1,property2:value2.....propertyN:valueN}
</pre>

Example:

<pre>
&lt;script&gt;
employee={id:700,name:"Evan",salary:30000}  
document.write(employee.id+" "+employee.name+" "+employee.salary);  
&lt;/script&gt;
</pre>

Output:
700 Evan 30000

<h4>By Creating instance of Object</h4>
Syntax:

<pre>
var objectname=new Object();
</pre>

Example:
<pre>
&lt;script&gt;
var emp=new Object();  
emp.id=701;  
emp.name="Karan";  
emp.salary=40000;  
document.write(emp.id+" "+emp.name+" "+emp.salary);  
&lt;/script&gt;
</pre>

Output:
701 Karan 40000

<h4>By Using an Object Constructor</h4>
A function is created with arguments. Each argument value can be assigned in the 
current object by using this keyword.

<pre>
&lt;script&gt;
function employee(id,name,salary){  
this.id=id;  
this.name=name;  
this.salary=salary;  
}  
emp=new employee(702,"Neha",35000);  
   
document.write(emp.id+" "+emp.name+" "+emp.salary);  
&lt;/script&gt;
</pre>

Output:
702 Neha 35000

<h3>Properties</h3>
A property of an object is a variable that is attached to the object. They are 
basically the same as JavaScript variables, except for the attachment to objects.

<h4>object properties- javascript object- edureka</h4>

The properties of an object define the characteristics of the object. You can 
access the properties of an object with a simple dot-notation such as:

<h4>objectName.propertyName</h4>
You can define a property by assigning it a value. For example, let’s create an 
object named Car and give it properties like company, model, and color. It can 
be defined as:

<pre>
var Car = new Object();
Car.company = 'Ford';
Car.model = 'Mustang';
Car.color = 'Red';
</pre>

<h3>Methods</h3>
A method is a function associated with an object. It is also a property of an object. 
Methods are defined as the normal functions but they have to be assigned as the 
property of an object.

<h4>The object method can be accessed as:</h4>

<pre>
objectName.methodName()
</pre>

<h4>Example:</h4>

<pre>
var person = {
  firstName: "Tessa",
  lastName : "Den",
  empid : 7100,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
</pre>

<h4>Output:</h4>
Tessa Den

<h4>Some of the commonly used built-in methods are:</h4>

Programming & Frameworks Training

<h4>Methods &amp; Description:</h4>

  - Object.assign() - It is used to copy enumerable and own properties from a source object to a target object.
  - Object.create() - It is used to create a new object with the specified prototype object and properties.
  - Object.defineProperty() - It is used to define behavioral attributes of the property.
  - Object.entries() - It returns an array with the key & value pairs.
  - Object.freeze() - It prevents the existing properties from getting removed.

<h3>Accessors</h3>
The JavaScript Accessors consist of Getters and Setters which are used to define the object accessors.

<h4>The Get Keyword</h4>
Let’s take an example and see how Getters are used to get any value of the property:

<pre>
var person = {
  firstName: "Daisy",
  lastName : "Green",
  empid : 401,
  get id() {
    return this.empid;
  }
};
document.getElementById("demo").innerHTML = person.id;
</pre>

Output:
401

<h4>The Set Keyword</h4>
Let’s take an example and see how Setters are used to set any value of the property:

<pre>
var person = {
  firstName: "Daisy",
  lastName : "Green",
  empid : 00,
  set id(value) {
    this.empid = value;
  }
};
person.id = 401;
document.getElementById("demo").innerHTML = person.empid;
</pre>

Output:
401

<h3>Prototypes</h3>
All JavaScript objects inherit properties and methods from a prototype. For example:

	- Date objects inherit from Date.prototype
	- Array objects inherit from Array.prototype
	- Person objects inherit from Person.prototype

The JavaScript prototype property is used to add new properties to object constructors.

Example:

<pre>
function Person(first, last, id, age) {
  this.firstName = first;
  this.lastName = last;
  this.empid = id;
  this.age = age;
}
Person.prototype.nationality = "Indian";
</pre>

The prototype property also allows you to add new methods to objects constructors.

Example:

<pre>
function Person(first, last, id, age) {  // Adding methods to constructors
  this.firstName = first;
  this.lastName = last;
  this.empid = id;
  this.age = age;
}
Person.prototype.name = function() {
  return this.firstName + " " + this.lastName;
};
</pre>

You can modify your own prototypes but never modify the prototypes of standard JavaScript 
objects.

With this, we have come to the end of our article. I hope you understood JavaScript 
Objects and the different methods to define them.


