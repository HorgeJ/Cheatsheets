#JQuery Basics
jQuery is a lightweight, "write less, do more", JavaScript library.

The purpose of jQuery is to make it much easier to use JavaScript on your website.

jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.

jQuery also simplifies a lot of the complicated things from JavaScript, like AJAX calls and DOM manipulation.

The jQuery library contains the following features:

* HTML
/DOM manipulation
* CSS manipulation
* HTML event methods
* Effects and animations
* AJAX
* Utilities

## Installation and Setup

* Make sure JavaScript is installed
* Include JQuery JavaScript file that includes the JQuery Library
* Could use JQuery through google API

## Modifying over Query Result

```javascript
function func(){
  var list = $(".shift");   // selects all elements with the shift class
  list.each(function(i){
    $(this).css("margin-left", (i * 50) + "px");
  });
}
```

## Load Function
We can use JQuery's load function. First we create a JQuery objects with selector as a target element to put our content, then the load content function takes the URL from the page we will get out content from.

```javascript
function func(){
  $(".responses").load(
    "scripts./myServer.php h2",
    {
    action: info,
    }, function(){
      alert("done!");
    }
  );
}
```
