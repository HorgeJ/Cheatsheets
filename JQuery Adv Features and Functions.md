# Advanced Features

## Doughnut Chart

```
var donutData = [
  {value : 30,
   color: "#FDB45C"
  }
]

<script>
var donutWheel = new Chart(document.getElementById("canvas").getContext("2d")).Doughnut(donutData);
</script>
```

## Bar Chart

```
var barChartData = {}

var myLine = new Chart(document.getElementById("canvas").getContext("2d")).Bar(barChartData);
```

## Line Chart

```
var myLine = new Chart(document.getElementById("canvas").getContext("2d")).Line(lineChrtData);
```

## Pie Chart

```
var myPie = new Chart(document.getElementById("canvas").getContext("2d")).Pie(pieData);
```

## UI Animations
syntax:
```
$(selector).animate({params},speed,callback);
```

* Params defines the CSS properties that are to be animated
* Optional speed: "Fast, Slow or milliseconds"
* Callback Optional: Call back function to be executed once animation has campleted

ex. 
```javascript
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("div").animate({left:'250px'});
  });
});
</script>
```

all CSS properties are to be manipulated with animate()

all prop. names must be camel-cased when using the animate function. 
ex: paddingLeft instead of padding-left.

## Using Relative Values
using +=
```javascript
$('button').click(function(){
  $('div').animate({
    height:'+=250px'
  });
});
```

## UI Draggables

```javascript
function int(){
  $('#dragme').draggable();
}
```

## UI Droppable

```javascript
$("#droppable").droppable({
  drop: function(event, ui){
    $(this)
    .addClass("ui-highlight")
    .find("p")
    .html("Drop!");
  }
});
```

## UI Radios
```javascript
$("#isSelect").click(function(){
  alert($('input:radio[name=sex]:checked').val());
});

$("#selectMale").click(function(){
  $('input:radio[name=sex]:nth(0)').attr('checked', true);
});
```

## UI Animated Dialog

```html
  <script>
  $( function() {
    $( "#dialog" ).dialog({
      autoOpen: false,
      show: {
        effect: "blind",
        duration: 1000
      },
      hide: {
        effect: "explode",
        duration: 1000
      }
    });
 
    $( "#opener" ).on( "click", function() {
      $( "#dialog" ).dialog( "open" );
    });
  } );
  </script>
</head>
<body>
 
<div id="dialog" title="Basic dialog">
  <p>This is an animated dialog which is useful for displaying information. The dialog window can be moved, resized and closed with the 'x' icon.</p>
</div>
 
<button id="opener">Open Dialog</button>
```

## UI Autocomplete
creating array of available autocomplete options, they can be shown in the widget (var availableTags=[])
```
$("#tags").autocomplete({
  source:availableTags
});
```

**Catagories**:
upon making an array or object with available information (var data = {[]})
```javascript
$("#search").catcomplete({
  delay:0,
  source: data
});
```

**Custom Data and Display**:
```javascript
$("#project").autocomplete({
  minLength: 0,
  source: projects,
  focus: function(event, ui){
    $("#project").val(ui.item.label);
    return false;
  }
});
```
