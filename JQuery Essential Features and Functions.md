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
