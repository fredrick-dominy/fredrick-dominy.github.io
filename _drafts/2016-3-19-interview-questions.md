---
title: Answers to Front-End Development Questions
author: Fredrick Dominy
layout: post
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

### What is a closure, and how/why would you use one? 

A closure refers to how the inner workings of a function have access to the properties of its parent function and the global object. Whereas the outer functions do not have access to the locally declared properties.

### What's a typical use case for anonymous functions? 

Anonymous functions are often used as a callback passed into the scope of another function: 

```javascript
var val = [2,3,4];
var doubleIt = arr.map(function(num) {
    return num * 2; 
});
```

### Can you explain how inheritance works in JavaScript? 

### Explain how JSONP works (and how it's not really AJAX) 

### Why is extending built in JavaScript objects not a good idea? 

### Explain the "JavaScript module pattern" and when you'd use it. 

# CSS/LESS/SASS Questions

### Please explain box model. 

# HTML Questions

### What's a doctype do? 

### What's the difference between standards mode and quirks mode? 

### Consider HTML5 as an open web platform. What are the building blocks of HTML5? 

### Describe the difference between cookies, sessionStorage and localStorage. 

### Can you explain the difference between GET and POST?