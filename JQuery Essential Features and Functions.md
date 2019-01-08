# Essential Features and Functions

## Adding Content to an Element
**append()**:
```javascript
var newBox = $("<div> inner text </div>");
$("#main").append(newBox);
```

**appendTo()**:
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



