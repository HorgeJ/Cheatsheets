# Essential Features and Functions

## Adding Content to an Element
### append():
```javascript
var newBox = $("<div> inner text </div>");
$("#main").append(newBox);
```

### appendTo():
The appendTo() method inserts HTML elements at the end of the selected elements.
Tip: To insert HTML elements at the beginning of the selected elements, use the prependTo() method.

```
$(content).appendTo(selector)
```
ex: Insert a span element at the end of each p element:
```javascript
$("button").click(function(){
  $("<span>Hello World!</span>").appendTo("p");
});
```

### css()
The css() method sets or returns one or more style properties for the selected elements.

To return the value of a specified CSS property, use the following syntax:
```
css("propertyname");
```

To set a specified CSS property, use the following syntax:
```
css("propertyname","value");
```

he following example will set the background-color value for ALL matched elements:
```javascript
$("p").css("background-color", "yellow");
```

### Finding an Elements Position
```
var bounce = $(".bouncer");
bounce.each(function(){
  $(this).html("POSITION " + $(this).position().top + "</br>";
  $(this).append("OFFSET: " +  $(this).offset().top + "</br>");
  $(this).append("CSS " + $(this).css("top"));
});
```

### Overwriting Contents of an Element
the HTML function overwrites the existing content
we should use append to add content

The html() method sets or returns the content (innerHTML) of the selected elements.

When this method is used to return content, it returns the content of the FIRST matched element.

When this method is used to set content, it overwrites the content of ALL matched elements.

Tip: To set or return only the text content of the selected elements, use the text() method.

Return Content:
```
$(selector).html()
```

set content:
```
$(selector).html(content)
```

ex:
```javascript
$("#box").html($("#box2"));
```

### Inserting Content to Doc

**.after**
The after() method inserts specified content after the selected elements.
```
$(selector).after(content,function(index))
```

insert after p element:
```
$("button").click(function(){
  $("p").after("<p>Hello world!</p>");
});
```

**.before**
The before() method inserts specified content in front of (before) the selected elements.


### Replacing Content

**replaceAll**
The replaceAll() method replaces selected elements with new HTML elements.

```
$(content).replaceAll(selector)
```

**replaceWith**
Replaces selected elements with new content

```
$(selector).replaceWith(content,function(index))
```

Replace the first p element with new text:
```javascript
$("button").click(function(){
   $("p:first").replaceWith("Hello world!");
});
```
  
### Clone
The clone() method makes a copy of selected elements, including child nodes, text and attributes.

Syntax:
```
$(selector).clone(true|false)
```

* true specifies that event handlers should also be copied
* false Default: Event handlers should not be copied

clone all p elements and insert them at the end of the body element:
```javascript
$("button").click(function(){
  $("p").clone().appendTo("body");
});
```

ex:
```javascript
$("#box" + count).clone(true)appendTo.(".boxHolder");
count = (count + 1) % 3;
```

### Detach | Remove
**Detach**
The detach() method removes the selected elements, including all text and child nodes. However, it keeps data and events.

This method also keeps a copy of the removed elements, which allows them to be reinserted at a later time.

Tip: To remove the elements and its data and events, use the remove() method instead.

Tip: To remove only the content from the selected elements, use the empty() method.

syntax:
```
$(selector).detach()
```

ex: remove all p elements
```javascript
$("button").click(function(){
  $("p").detach();
});
```

**remove**
The remove() method removes the selected elements, including all text and child nodes.

This method also removes data and events of the selected elements.

Syntax:
```
$(selector).remove(selector);
```

ex: remove all p elements
```javascript
$("button").click(function(){
  $("p").remove();
});
```

ex:
```javascript
function func1(){
  var hold = $("#box1").detach();
  $("#boxHolder").append(hold);
}

function func2(){
  hold = $("#box2").detach();
  $("#boxHolder").append(hold);
}
```
**empty**
REMOVES EVERYTHING

```javascript
function func3(){
  $("#boxHolder").empty();
}
```

### Getting Values
***text**
The text() method sets or returns the text content of the selected elements.

When this method is used to return content, it returns the text content of all matched elements (HTML markup will be removed).

When this method is used to set content, it overwrites the content of ALL matched elements.

Tip: To set or return the innerHTML (text + HTML markup) of the selected elements, use the html() method.
```
$(selector).text()
```

**value**
The val() method returns or sets the value attribute of the selected elements.

When used to return value:
This method returns the value of the value attribute of the FIRST matched element.

When used to set value:
This method sets the value of the value attribute for ALL matched elements.

Note: The val() method is mostly used with HTML form elements.

ex:
```javascript
var inputs = $("div.row .hasValue");
inputs.parent().append(inputs.text());

inputs.each(function(item){
  $(this).parent().append($(this).val());
});
```

### Wrapping
The wrap() method wraps specified HTML element(s) around each selected element.

```
function func(){
  var input = $("div.row .hasValue").first(); // wraps only the first element
  input.wrap("<div class ='bord'><div>");
}

function func2(){
  var input = $("div.row .hasValue");     // wraps all elements
  input.wrap(<div class='bord'><div>");
}
```

**wrapAll**
The wrapAll() method wraps specified HTML element(s) around all selected elements.

**wrapInner**
The wrapInner() method wraps specified HTML element(s) around the content (innerHTML) of each selected element.

Syntax:
```
$(selector).wrapInner(wrappingElement,function(index))
```

**unwrap**
The unwrap() method removes the parent element of the selected elements.

Syntax:
```
$(selector).unwrap()
```

remove the parent element of all p elements
```javascript
$("button").click(function(){
  $("p").unwrap();
});
```

**val()**
The val() method returns or sets the value attribute of the selected elements.

When used to return value: 
This method returns the value of the value attribute of the FIRST matched element.

When used to set value: 
This method sets the value of the value attribute for ALL matched elements.

Note: The val() method is mostly used with HTML form elements.

Syntax:
```
$(selector).val(val)
```

```javascript
function func1(){
  var input = $("input");
  input.val(2018-10-04);
}

function func2(){
  var d = new Date();
  $("input").val(d.toDateString());
}

function func3(){
  var userInput = $("textarea").val();
  $("select").val(userInput);
  
  var text = $("select option:selected").text();
  $("textarea").val(text);
}

```

**hidden**
makes the element dissapear from that page, height and width will be set to 0, opacity set to 0 and all its attributes will be stored in the jQuery object incase we need to being the object back.

```javascript
function func(){
  $("#third").hide
}
```

