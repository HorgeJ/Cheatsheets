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

**Autocomplete Scroll**:
```javascript
$(function () {
    var availableTags = [
        "ActionScript",
        "AppleScript",
        "Asp",
        "BASIC",
        "C",
        "C++",
        "Clojure",
        "COBOL",
        "ColdFusion",
        "Erlang",
        "Fortran",
        "Groovy",
        "Haskell",
        "Java",
        "JavaScript",
        "Lisp",
        "Perl",
        "PHP",
        "Python",
        "Ruby",
        "Scala",
        "Scheme"];
    $("#tags").autocomplete({
        source: availableTags
    });

     $("#tags2").autocomplete({
        source: availableTags
    });
    
    $("#tags3").autocomplete({
        source: availableTags
    });
    
    $("#tags2").autocomplete("widget").addClass('fixed-height');
   $("#tags3").autocomplete("widget").attr('style', 'max-height: 400px; overflow-y: auto; overflow-x: hidden;')
});
```

## Sliders
Basic Slider:
```html
  <script>
  $( function() {
    $( "#slider" ).slider();
  } );
  </script>
</head>
<body>
 
<div id="slider"></div>
 
 
</body>
</html>
```

**Color Picker:**
```html
  <style>
  #red, #green, #blue {
    float: left;
    clear: left;
    width: 300px;
    margin: 15px;
  }
  #swatch {
    width: 120px;
    height: 100px;
    margin-top: 18px;
    margin-left: 350px;
    background-image: none;
  }
  #red .ui-slider-range { background: #ef2929; }
  #red .ui-slider-handle { border-color: #ef2929; }
  #green .ui-slider-range { background: #8ae234; }
  #green .ui-slider-handle { border-color: #8ae234; }
  #blue .ui-slider-range { background: #729fcf; }
  #blue .ui-slider-handle { border-color: #729fcf; }
  </style>
  <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
  <script>
  $( function() {
    function hexFromRGB(r, g, b) {
      var hex = [
        r.toString( 16 ),
        g.toString( 16 ),
        b.toString( 16 )
      ];
      $.each( hex, function( nr, val ) {
        if ( val.length === 1 ) {
          hex[ nr ] = "0" + val;
        }
      });
      return hex.join( "" ).toUpperCase();
    }
    function refreshSwatch() {
      var red = $( "#red" ).slider( "value" ),
        green = $( "#green" ).slider( "value" ),
        blue = $( "#blue" ).slider( "value" ),
        hex = hexFromRGB( red, green, blue );
      $( "#swatch" ).css( "background-color", "#" + hex );
    }
 
    $( "#red, #green, #blue" ).slider({
      orientation: "horizontal",
      range: "min",
      max: 255,
      value: 127,
      slide: refreshSwatch,
      change: refreshSwatch
    });
    $( "#red" ).slider( "value", 255 );
    $( "#green" ).slider( "value", 140 );
    $( "#blue" ).slider( "value", 60 );
  } );
  </script>
</head>
<body class="ui-widget-content" style="border:0;">
 
<p class="ui-state-default ui-corner-all ui-helper-clearfix" style="padding:4px;">
  <span class="ui-icon ui-icon-pencil" style="float:left; margin:-2px 5px 0 0;"></span>
  Simple Colorpicker
</p>
 
<div id="red"></div>
<div id="green"></div>
<div id="blue"></div>
 
<div id="swatch" class="ui-widget-content ui-corner-all"></div>
```

**Ranger Slider:**
```html
  <script>
  $( function() {
    $( "#slider-range" ).slider({
      range: true,
      min: 0,
      max: 500,
      values: [ 75, 300 ],
      slide: function( event, ui ) {
        $( "#amount" ).val( "$" + ui.values[ 0 ] + " - $" + ui.values[ 1 ] );
      }
    });
    $( "#amount" ).val( "$" + $( "#slider-range" ).slider( "values", 0 ) +
      " - $" + $( "#slider-range" ).slider( "values", 1 ) );
  } );
  </script>
</head>
<body>
 
<p>
  <label for="amount">Price range:</label>
  <input type="text" id="amount" readonly style="border:0; color:#f6931f; font-weight:bold;">
</p>
```

**Select Slider:**
```html
  <script>
  $( function() {
    $( "#slider-range-max" ).slider({
      range: "max",
      min: 1,
      max: 10,
      value: 2,
      slide: function( event, ui ) {
        $( "#amount" ).val( ui.value );
      }
    });
    $( "#amount" ).val( $( "#slider-range-max" ).slider( "value" ) );
  } );
  </script>
</head>
<body>
 
<p>
  <label for="amount">Minimum number of bedrooms:</label>
  <input type="text" id="amount" readonly style="border:0; color:#f6931f; font-weight:bold;">
</p>
<div id="slider-range-max"></div>
```

**Vertical:**
```html
  <script>
  $( function() {
    $( "#slider-vertical" ).slider({
      orientation: "vertical",
      range: "min",
      min: 0,
      max: 100,
      value: 60,
      slide: function( event, ui ) {
        $( "#amount" ).val( ui.value );
      }
    });
    $( "#amount" ).val( $( "#slider-vertical" ).slider( "value" ) );
  } );
  </script>
</head>
<body>
 
<p>
  <label for="amount">Volume:</label>
  <input type="text" id="amount" readonly style="border:0; color:#f6931f; font-weight:bold;">
</p>
 
<div id="slider-vertical" style="height:200px;"></div>
```

**Increment:**
```html
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
  <script>
  $( function() {
    $( "#slider" ).slider({
      value:100,
      min: 0,
      max: 500,
      step: 50,
      slide: function( event, ui ) {
        $( "#amount" ).val( "$" + ui.value );
      }
    });
    $( "#amount" ).val( "$" + $( "#slider" ).slider( "value" ) );
  } );
  </script>
</head>
<body>
 
<p>
  <label for="amount">Donation amount ($50 increments):</label>
  <input type="text" id="amount" readonly style="border:0; color:#f6931f; font-weight:bold;">
</p>
 
<div id="slider"></div>
```

## Ajax
Post and Get requests

**Short Hand Functions:**

jQuery.post( url [, data ] [, success ] [, dataType ] )
```javascript
  function func(){
    var msg = $("msgToServer").val();
    $.post("scripts/myServer.php",
    {
      action: "simple",
      message: msg,
    }, callback);
    $("msgToServer").val("");
  }
```

**getJSON:**
```javascript
$.getJSON("data/jsondata.js", parseData);

function parseData(response){
  var x = response;
  try{
    var data = JSON.stringify(response)
    $.(".responses").append(data);
    catch (e){
      alert("Oops");
    }
  }
}
```
