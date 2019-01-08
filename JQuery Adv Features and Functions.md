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
