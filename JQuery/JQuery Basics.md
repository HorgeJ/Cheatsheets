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
 
 ## Element Selector
 Selects all elements with the given tag name.
 
highlight ul:
```javascript
var unordered = $("ul");
highLight(unordered);
```

check for value "Hello":
```javascript
var items = $("input");
highlight(items);
items.each(function(){
  if($(this).val() == "hello"){
    alert("Hi!!");
  }
});
```

## Selecting Elements by ID

```javascript
var items = #("#sidebar");
highlight(sidebar);
```

## Selecting by Class

```javascript
var items = $(".heading");
highlight(items);
```

## Selecting by DOM

```javascript
var items = $(header button);
highlight(items);
```

## Selecting Descendant Elements

highlight direct descendant
```javascript
var items = $("table > tbody > tr > td");
highlight(items);
```

highlight adjacent
```javascript
var items = $("td + td");
highlight(items);
```

highlight sibling
```javascript
var items = $("td ~ td");
highlight(items);
```

## Selecting  by Attributes

```javascript
var items = $("[name='surname']");
highlight(items);
```

```javascript
var items = $("[name]");
```

```javascript
var items = $("th[colspan='3']");
```

## Selecting Attribute Variants

find any variant of attribute value:
```javascript
var items = $('[myAttr*="flag"]');
```

find exact variant of attribute value:
```
var items = $("[myAttr~='flag']");
```

## Psuedo Selectors|First and Last
first:
```javascript
var items = $("ul:first");
```

child:
```
var items = $("ul li:first-child")
```

last:
```
var items = $(ul:last)  
```

odd/even:
```javascript
var items = $("ul li:odd");
```

nth child (not zero based):
```
var items = $("ul :nth-child(3)");
```

## Selecting Children of Query
```javascript
var items = $('table');
var kids = items.find('#theTD');
highlight(kids)';
```

# Animations and Colors
We can use the JQuery CSS function to change colors of elements

```
var colorArray = ["red", "blue", "yellow"];

function colorFunc(){
  var p1 = $(".p1");
  p1.css("color", colorArray[index]);
  index = (index + 1) % colorArray.length;
}

```

using interval:
```
function intFunc(){
  window.setInterval(function(){
  var p1 = $ (".p1");
  p1.css("background-color", colorArray[index]);
  index = (index + 1) % colorArray.length;
  }, 500);
}
```

## Animation Queues
```javascript
<script>
$(document).ready(function(){
  $("button").click(function(){
    var div=$("div");
    div.animate({left:'100px'},slow);
  });
  ```
  
  ## Animate Colors
```javascript
  $("#effect").animate({
    backgroundColor: "#aa0000",
    color: "red",
    width: 500
  }, 1000);
});
```

## Style Changed
```javascript
function boxFunc(){
  $(".boxy").animate({
    opacity: 0.25,
    left: "+=50",
    height: "toggle"
  }, 5000, function(){
    $(this).append("</br>done");
  });
}
```

## Stopping an Animation
```javascript
$(".boxy").finish();
```

```javascript
$(".boxy").stop();
```

## Slide and Fade
```
$("#third").slideUp();
```

```
$(".boxy").slideToggle(500);
```

```
$(".boxy").fadeOut(3000).delay(800).slideDown(2000);
```
