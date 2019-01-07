# JQuery Basics
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

## Find Function
The find() method returns descendant elements of the selected element.

A descendant is a child, grandchild, great-grandchild, and so on.

Return all span elements that are descendants of ul:
```
  $(document).ready(function(){
  $("ul").find("span").css({"color": "red", "border": "2px solid red"});
});
```
  
## Filter Function
The filter() method returns elements that match a certain criteria.

This method lets you specify a criteria. Elements that do not match the criteria are removed from the selection, and those that match will be returned.

Syntax:
```
$(selector).filter(criteria,function(index))
```

ex. turn checked items red:
```javascript
function funcRed(){
  var boxes = $("input");
  boxes.filter(":checked").parent().addClass("red");
}
```

ex. Float checked boxes
```javascript
function float(){
  var labels = $("label input");
  var checked = labels.filter(function(index){
    if($(this).filter(":checked").length > 0)
      return true;
  });
  labels.parent().css("float", "left");
  checked.parent().css("float", right);
}
```

## Asynchronous Requests
Can be accomplished through JQuery Ajax function

```javascript
var message = $(#messageToServer).val();
$.ajax({
  type:"post",
  url: "scripts/myServer.php",
  data: {
    action: "wait"
  },
  success: callback
});
```

## Document Ready Function
 page can't be manipulated safely until the document is "ready." jQuery detects this state of readiness for you. Code included inside $( document ).ready() will only run once the page Document Object Model (DOM) is ready for JavaScript code to execute. Code included inside $( window ).on( "load", function() { ... }) will run once the entire page (images or iframes), not just the DOM, is ready.
 
 syntax:
 ```
 // A $( document ).ready() block.
$( document ).ready(function() {
    console.log( "ready!" );
});
 ```
 ex:
 ```javascript
 $(document).ready(function(){
  $("#main").append("<p> This line is added after doc is read </p>");
 });
 ```
 
 ```javascript
<script>
  $( function() {
    $( "#tabs" ).tabs();
  } );
</script>
 ```
 
 ## Child and Parent Functions
 
 ex. Parents:
 ```javascript
 function func(){
  var input = $("input");
  input.parent().parents("div.boxStack").addClass("color");
 }
 ```
 
 ex. Child:
 ```javascript
 var top = $(#first);
 top.children().addClass("color");
 ```
 
 
 
