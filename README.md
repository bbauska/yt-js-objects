---
title: "YouTube's JavaScript Objects"
author: "bbauska"
date last editted: "2/21/2024 5+pm"
output: 
  markdown:
    with some style
---

## yt-js-objects
<a href="https://www.youtube.com/watch?v=m9FrY5A-tao">JavaScript Objects on YouTube</a>

This Edureka video on "JavaScript Object" will help you understand the different methods of creating objects in JavaScript. It will provide examples for each type and show you how to use objects in JavaScript. ( JavaScript Object Blog: https://www.edureka.co/blog/javascrip... )

<h3><a href="https://www.edureka.co/blog/javascript-object/">JavaScript Objects</a></h3>

<a href="https://www.html-easy.com/learn/how-to-add-a-target-attribute-in-html/">How-To's in HTML (a beginner's guide)</a>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~ readme.md of yt-js-objects.bauska.org ~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 align="center">You Tube's JavaScript Objects</h2>

JavaScript is an Object-Oriented Programming language. The objects form the building blocks which are considered to be the most important data-type for the programming language. This article will provide in-depth knowledge about JavaScript Objects, how they are created and defined in the following sequence:

JavaScript Object
How to Create a new Object?
Properties
Methods
Accessors
Prototypes
 

JavaScript Object
JavaScript objects are similar to objects in real life which consists of different attributes and properties. These objects are defined as an unordered collection of related data, that are of primitive or reference types. These are defined in the form of “key: value” pairs.

 

JavaScript - javascript object - Edureka

These keys are variables or functions which are called as properties and methods of an object. You can create a JavaScript object as:


let ObjectName = {
Property1 : "Value",
Property2 : "Value",
...
...
}
How to Create a new Object?
There are 3 ways to create a new object:

By Object Literal
Syntax:

1
object={property1:value1,property2:value2.....propertyN:valueN}
Example:


<script>  
employee={id:700,name:"Evan",salary:30000}  
document.write(employee.id+" "+employee.name+" "+employee.salary);  
</script>  
Output:

700 Evan 30000
By Creating instance of Object
Syntax:

1
var objectname=new Object();
Example:


<script>  
var emp=new Object();  
emp.id=701;  
emp.name="Karan";  
emp.salary=40000;  
document.write(emp.id+" "+emp.name+" "+emp.salary);  
</script>  
Output:

701 Karan 40000
By Using an Object Constructor
A function is created with arguments. Each argument value can be assigned in the current object by using this keyword.

Course Curriculum
Java Certification Training Course
Instructor-led SessionsReal-life Case StudiesAssignmentsLifetime Access
Example:


<script>  
function employee(id,name,salary){  
this.id=id;  
this.name=name;  
this.salary=salary;  
}  
emp=new employee(702,"Neha",35000);  
   
document.write(emp.id+" "+emp.name+" "+emp.salary);  
</script>  
Output:

702 Neha 35000
Properties
A property of an object is a variable that is attached to the object. They are basically the same as JavaScript variables, except for the attachment to objects.

 

object properties- javascript object- edureka

 

The properties of an object define the characteristics of the object. You can access the properties of an object with a simple dot-notation such as:


objectName.propertyName
You can define a property by assigning it a value. For example, let’s create an object named Car and give it properties like company, model, and color. It can be defined as:


var Car = new Object();
Car.company = 'Ford';
Car.model = 'Mustang';
Car.color = 'Red';
Methods
A method is a function associated with an object. It is also a property of an object. Methods are defined as the normal functions but they have to be assigned as the property of an object.

The object method can be accessed as:

1
objectName.methodName()
Example:


var person = {
firstName: "Tessa",
lastName : "Den",
empid : 7100,
fullName : function() {
return this.firstName + " " + this.lastName;
}
};
Output:

Tessa Den
Some of the commonly used built-in methods are:

Programming & Frameworks Training
Methods	Description
Object.assign()	It is used to copy enumerable and own properties from a source object to a target object
Object.create()	It is used to create a new object with the specified prototype object and properties
Object.defineProperty()	It is used to define behavioral attributes of the property
Object.entries()	It returns an array with the key & value pairs
Object.freeze()	It prevents the existing properties from getting removed
Accessors

The JavaScript Accessors consist of Getters and Setters which are used to define the object accessors.

The Get Keyword
Let’s take an example and see how Getters are used to get any value of the property:


var person = {
firstName: "Daisy",
lastName : "Green",
empid : 401,
get id() {
return this.empid;
}
};
document.getElementById("demo").innerHTML = person.id;
Output:

401
The Set Keyword
Let’s take an example and see how Setters are used to set any value of the property:


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
Output:

401
Prototypes
All JavaScript objects inherit properties and methods from a prototype. For example:

Date objects inherit from Date.prototype
Array objects inherit from Array.prototype
Person objects inherit from Person.prototype
The JavaScript prototype property is used to add new properties to object constructors.

Example:


function Person(first, last, id, age) {
this.firstName = first;
this.lastName = last;
this.empid = id;
this.age = age;
}
 
Person.prototype.nationality = "Indian";
The prototype property also allows you to add new methods to objects constructors.

Example:


function Person(first, last, id, age) {  //Adding methods to constructors
this.firstName = first;
this.lastName = last;
this.empid = id;
this.age = age;
}
Person.prototype.name = function() {
return this.firstName + " " + this.lastName;
};
You can modify your own prototypes but never modify the prototypes of standard JavaScript objects.

Related Learning: Javascript Interview Questions

With this, we have come to the end of our article. I hope you understood JavaScript Objects and the different methods to define them.


