---
title: Answers to Front-End Development Questions
author: Fredrick Dominy
layout: post
comments: true
tags:
- Questions
- Interview
- Tests
---

Part of the process of interviewing for a new job is the inevitable test of your depth of knowledge. Therefore, it makes sense to be able to speak to these topics with confidence and competence. Below are my answers to some common interview questions around the topic of Front-End Web Application Development.
    
# Javascript Questions
    
### What is the difference between Jquery & Javascript? 

This one should be easy: Javascript is a scripting language used by browsers (primarily) whereas jQuery is a library that adds easily accessible functionality to web development.

If we dive in a little deeper on Javascript we will see that it was developed in 1995 by Brendan Eich, its formal name is ECMAScript, and it is one of the three primary technologies of web development (HTML, CSS, and Javascript).

Looking at jQuery, it abstracted alot of the difficult functionality that was necessary to make web applications, such as DOM manipulation, AJAX, event handling, and javascript related animation events. 

___

### What are undefined and undeclared variables, or ?

I referenced a great article by [Lucy Bain](http://lucybain.com/blog/2014/null-undefined-undeclared/) which discussed undeclared, undefined and null variable assignments. 

In my own words: Variables can be instantiated with no definition, i.e., `undefined`.  Whereas an undeclared variable is placed on the global object.

```javascript
// undeclared - placed on global object
bob = 'bob';

// undefined
var bob; // bob = undefined

// null is an object and is falsey and is a primitive within javascript
var bob = null;  // assigned the value of null
```
___

### What is a closure, and how/why would you use one? 

A closure refers to how the inner workings of a function have access to the properties of its parent function and the global object. Whereas the outer functions do not have access to the locally declared properties.

___

### What's a typical use case for anonymous functions? 

Anonymous functions are often used as a callback passed into the scope of another function: 

```javascript
var val = [2,3,4];
var doubleIt = arr.map(function(num) {
    return num * 2; 
});
```

Its worthwhile to say that if the callback is a substantial function, you can name it and create a function expression.

```javascript
var callbackFunction = function(data) {
    return data.something;
}

var doubleIt = arr.map(callbackFunction);
```
___

### Can you explain how inheritance works in JavaScript? 

In javascript, inheritance refers to the access given of child objects to their parents. For example if the method `Obj1.method()` doesn't exist, then javascript will look at the parent and keep looking until it reaches the prototype.

___

### Explain how JSONP works (and how it's not really AJAX) 

JSON stands for javascript object notation and the P stands for padding which is some type of javascript function attached to the JSON object. 

The 'P' allows for circumvention of CORS (Cross origin resource sharing). According to Widipedia, [CORS](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) is a set of 'rules' for the transfer of data between domains.

___

### Why is extending built in JavaScript objects not a good idea? 

It could possibly interfere with other programs that use javascript.

___

### Explain the "JavaScript module pattern" and when you'd use it. 

The javascript module pattern is as follows:

```javascript
var module = (function(){
    var _privateFunction = function() {
        //code
    }
    
    var publicObject = {};
    publicObject.publicFunction() {
        // code
    }
    
    return publicObject;
    
})(); 
```

In this case the IFFE is immediately invoked and the module is available on the global scope to which the public functions are available.

___

# CSS/LESS/SASS Questions

### Explain box model. 

The box model represents the width and height of the border, padding, and content of an element.

___

# HTML Questions

### What's a doctype do? 

The DOCTYPE tells the browser how to handle the HTML. Almost useless but necessary for HTML5 according to Wikipedia.

___

### What's the difference between standards mode and quirks mode? 

As opposed to "standards" mode, "quirks" mode is an attempt by browsers to maintain backwards compatibility.  Apparently a major differnce is how CSS is handled in quirks mode. The prime example was how the browser handled the box model.

___

### Consider HTML5 as an open web platform. What are the building blocks of HTML5? 

This is such an odd question... My first thought was the document, the ability to handle different elements, handle javascript and css.  I had to search and found this bulleted list from [Mathew Zhong's Site](http://flowerszhong.github.io/2013/11/20/html-questions.html).

* more semantic text markup
* new form elements
* video and audio
* new javascript API
* canvas and SVG
* new communication API
* geolocation API
* web worker API
* new data storage

Thanks Mathew!

### Describe the difference between cookies, sessionStorage and localStorage. 

Cookies are used for authentication and security purposes often as a means of identification.

Whereas sessionStorage is and localStorage are very similar, used to save various bits of information about the user's selections or preferences within an application. SessionStorage implies that the data is temporary while localStorage can be saved for use in later sessions. 

___

### Can you explain the difference between GET and POST?

Both are HTTP requests - typically a GET request implies the non-secure transfer of data between the server and the client while POST implies a secure transfer of protected or personal data.

A minor detail - a GET request is meant to be idempotent (same data every time). Whereas a POST is meant to be dynamic (like a shopping cart.)
