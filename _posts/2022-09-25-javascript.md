---
keywords: fastai
description: Javascript Learning
title: Javascript
toc: true
layout: post
categories: [jupyter]
comments: true
---
# Javascript

## Main Class
```
// define a function to hold data for a Person
function Schedule(class, period, teacher) {
    this.class = class;
    this.period = period;
    this.teacher = teacher;
    this.role = "";
}

// define a setter for role in Person data
Schedule.prototype.setRole = function(role) {
    this.role = role;
}

// define a JSON conversion "method" associated with Person
Schedule.prototype.toJSON = function() {
    const obj = {class: this.class, period: this.period, teacher: this.teacher, role: this.role};
    const json = JSON.stringify(obj);  // json/string is useful when passing data on internet
    return json;
}

var mainset = new Schedule("Statistics", "3", "Deputron");  // object type is easy to work with in JavaScript
logItType(mainset);  // before role
logItType(mainset.toJSON());  // ok to do this even though role is not yet defined

// output of Object and JSON/string associated with Teacher
mainset.setRole("Main Set");   // set the role
logItType(mainset); 
logItType(mainset.toJSON());
```

## Array
```
var animals = [ 
    new Person("Cow", "moo", "black and white"),
    new Person("Dog", "ruff", "many colors"),
    new Person("Cat", "meow", "many colors"),
    new Person("Giraffe", "idk", "brown and yellow"),
    new Person("Mouse", "squeak", "gray")
];

function Farm(home, animals){ =
    home.setRole("Home");
    this.home = home;
    this.Farm = [home];
    this.animals = animals;
    this.animals.forEach(animal => { animal.setRole("Animal"); this.Farm.push(animals); });
    // build json/string format of Classroom
    this.json = [];
    this.Farm.forEach(thing => this.json.push(thing.toJSON()));
}

// make a CompSci classroom from formerly defined teacher and students
barn = new Farm(home, animals);

// output of Objects and JSON in CompSci classroom
logItType(barn.home);  // constructed classroom object
logItType(barn.home[0].name);  // abstract 1st objects name
logItType(barn.json[0]);  // show json conversion of 1st object to string
logItType(JSON.parse(barn.json[0]));  // show JSON.parse inverse of JSON.stringify
```

## HTML
```
Set.prototype._toHtml = function() {
    // HTML Style is build using inline structure
    var style = (
      "display:inline-block;" +
      "border: 2px solid grey;" +
      "box-shadow: 0.8em 0.4em 0.4em grey;"
    );
  
    // HTML Body of Table is build as a series of concatenations (+=)
    var body = "";
    // Heading for Array Columns
    body += "<tr>";
    body += "<th><mark>" + "Class" + "</mark></th>";
    body += "<th><mark>" + "Period" + "</mark></th>";
    body += "<th><mark>" + "Teacher" + "</mark></th>";
    body += "</tr>";
    // Data of Array, iterate through each row of compsci.classroom 
    for (var row in math.classroom) {
      // tr for each row, a new line
      body += "<tr>";
      // td for each column of data
      body += "<td>" + math.classroom[row].numbers + "</td>";
      body += "<td>" + math.classroom[row].mean + "</td>";
      body += "<td>" + math.classroom[row].mode + "</td>";
      // tr to end line
      body += "<tr>";
    }
  
     // Build and HTML fragment of div, table, table body
    return (
      "<div style='" + style + "'>" +
        "<table>" +
          body +
        "</table>" +
      "</div>"
    );
  
  };
  
  // IJavaScript HTML processor receive parameter of defined HTML fragment
  $$.html(math._toHtml());
  ```
