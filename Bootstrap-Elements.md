## Navigation

Navigation available in Bootstrap share general markup and styles, from the base .nav class to the active and disabled states. Swap modifier classes to switch between each style.

The base .nav component is built with flexbox and provide a strong foundation for building all types of navigation components. It includes some style overrides (for working with lists), some link padding for larger hit areas, and basic disabled styling.

```html
<ul id="ss-tabs" class="nav nav-tabs">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
```

JQuery can be used to change the active status for whatever tab is selected

```javascript
<script>
  "use strict";
  var $liQuery = $("#ss-tabs > li") // stores list items under ss-tabs class in var
  
  $liQuery.click(function(){        // upon clicking the list items
    $liQuery.removeClass("active"); // remove the active class from all li
    $(this).addClass("active");     // add active class to current item selected
    
  });
</script>
```

## Dropdown Menu

```html
<ul id="ss-tabs" class="nav nav-pills nav-justified">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="dropdown-toggle" data-toggle="dropdown" href="#">dropdown<span class="caret"></span></a>
      <ul class="dropdown-menu">
        <li class="nav-item"><a href="#">item</a></li>
        <li class="nav-item"><a href="#">item</a></li>
        <li class="divider"></li>
        <li class="nav-item"><a href="#">item</a></li>
      </ul>
  </li>
</ul>
```

## Nav Bar

```html
<nav class="navbar navbar-default" role="navigation">
  <div class="navbar-header">
    <a class="navbar-brand" href="#">Nav Bar</a>
  </div>
<ul id="ss-tabs" class="nav nav-pills nav-justified">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="dropdown-toggle" data-toggle="dropdown" href="#">dropdown<span class="caret"></span></a>
      <ul class="dropdown-menu">
        <li class="nav-item"><a href="#">item</a></li>
        <li class="nav-item"><a href="#">item</a></li>
        <li class="divider"></li>
        <li class="nav-item"><a href="#">item</a></li>
      </ul>
  </li>
</ul>
</nav>
```

## Responsive Navbar

Add hamburger to navbar at smaller size

This responsive navbar with a fixed top positioning requires adding some padding to the top of the body element to bring the content down

```html
<nav class="navbar navbar-default navbar-fixed-top" role="navigation">
  <div class="navbar-header">
    <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#nav-collapse">
      <span class="icon-bar"></span>
      <span class="icon-bar"></span>
      <span class="icon-bar"></span>
    </button>
    <a class="navbar-brand" href="#">Nav Bar</a>
  </div>
<div class="collapse navbar-collapse" id="nav-collapse">
<ul id="ss-tabs" class="nav nav-pills nav-justified">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="dropdown-toggle" data-toggle="dropdown" href="#">dropdown<span class="caret"></span></a>
      <ul class="dropdown-menu">
        <li class="nav-item"><a href="#">item</a></li>
        <li class="nav-item"><a href="#">item</a></li>
        <li class="divider"></li>
        <li class="nav-item"><a href="#">item</a></li>
      </ul>
  </li>
</ul>
  </div>
</nav>
```

## Breadcrumbs

```html
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item active" aria-current="page">Home</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Library</li>
  </ol>
</nav>

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
```

## Pagination
We use a large block of connected links for our pagination, making links hard to miss and easily scalable—all while providing large hit areas. Pagination is built with list HTML elements so screen readers can announce the number of available links.

```html
<nav aria-label="Page navigation example">
  <ul class="pagination pagination-lg">
    <li class="page-item active"><a class="page-link" href="#">Previous</a></li>
    <li class="page-item disabled"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

## Badges/Labels

```
<span class="badge badge-primary">Primary</span>
<span class="badge badge-secondary">Secondary</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-danger">Danger</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-info">Info</span>
<span class="badge badge-light">Light</span>
<span class="badge badge-dark">Dark</span>
```

## Jumbotron
A lightweight, flexible component that can optionally extend the entire viewport to showcase key marketing messages on your site.

```
<div class="jumbotron">
  <h1 class="display-4">Hello, world!</h1>
  <p class="lead">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
  <hr class="my-4">
  <p>It uses utility classes for typography and spacing to space content out within the larger container.</p>
  <p class="lead">
    <a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a>
  </p>
</div>
```

## Page Header

```
<div class="page-header">
  <h1>Example Page Header</h1>
</div>
```

## Thumbnails
```
<div class = "row">
   
   <div class = "col-sm-6 col-md-3">
      <a href = "#" class = "thumbnail">
         <img src = "/bootstrap/images/kittens.jpg" alt = "Generic placeholder thumbnail">
      </a>
   </div>
   
   <div class = "col-sm-6 col-md-3">
      <a href = "#" class = "thumbnail">
         <img src = "/bootstrap/images/kittens.jpg" alt = "Generic placeholder thumbnail">
      </a>
   </div>
   
   <div class = "col-sm-6 col-md-3">
      <a href = "#" class = "thumbnail">
         <img src = "/bootstrap/images/kittens.jpg" alt = "Generic placeholder thumbnail">
      </a>
   </div>
   
   <div class = "col-sm-6 col-md-3">
      <a href = "#" class = "thumbnail">
         <img src = "/bootstrap/images/kittens.jpg" alt = "Generic placeholder thumbnail">
      </a>
   </div>
   
</div>
```

## Accordion
```html
<div class="accordion" id="accordionExample">
  <div class="card z-depth-0 bordered">
    <div class="card-header" id="headingOne">
      <h5 class="mb-0">
        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseOne"
          aria-expanded="true" aria-controls="collapseOne">
          Collapsible Group Item #1
        </button>
      </h5>
    </div>
    <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
      <div class="card-body">
        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3
        wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum
        eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla
        assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred
        nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer
        farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus
        labore sustainable.
      </div>
    </div>
  </div>
  <div class="card z-depth-0 bordered">
    <div class="card-header" id="headingTwo">
      <h5 class="mb-0">
        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseTwo"
          aria-expanded="false" aria-controls="collapseTwo">
          Collapsible Group Item #2
        </button>
      </h5>
    </div>
    <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordionExample">
      <div class="card-body">
        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3
        wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum
        eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla
        assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred
        nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer
        farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus
        labore sustainable.
      </div>
    </div>
  </div>
  <div class="card z-depth-0 bordered">
    <div class="card-header" id="headingThree">
      <h5 class="mb-0">
        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseThree"
          aria-expanded="false" aria-controls="collapseThree">
          Collapsible Group Item #3
        </button>
      </h5>
    </div>
    <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionExample">
      <div class="card-body">
        Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3
        wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum
        eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla
        assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred
        nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer
        farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus
        labore sustainable.
      </div>
    </div>
  </div>
</div>
```

## Alerts

```html
<div class="alert alert-success" role="alert">
  <strong>Well done!</strong> You successfully read this important alert message.
</div>
<div class="alert alert-info" role="alert">
  <strong>Heads up!</strong> This alert needs your attention, but it's not super important.
</div>
<div class="alert alert-warning" role="alert">
  <strong>Warning!</strong> Better check yourself, you're not looking too good.
</div>
<div class="alert alert-danger" role="alert">
  <strong>Oh snap!</strong> Change a few things up and try submitting again.
</div>
```

**Dismissible**
```
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
</div>
```

## Progress Bars
Progress components are built with two HTML elements, some CSS to set the width, and a few attributes. We don’t use the HTML5 progress element, ensuring you can stack progress bars, animate them, and place text labels over them.

* We use the .progress as a wrapper to indicate the max value of the progress bar.
* We use the inner .progress-bar to indicate the progress so far.
* The .progress-bar requires an inline style, utility class, or custom CSS to set their width.
* The .progress-bar also requires some role and aria attributes to make it accessible.

```html
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
</div>
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
</div>
```

## Media Objects
[Place holder images](https://placeholder.com/)

The media object helps build complex and repetitive components where some media is positioned alongside content that doesn’t wrap around said media. Plus, it does this with only two required classes thanks to flexbox.

```html
<div class="container">
  <div class="media">
    <a class="pull-right" href="#">
      <img class="media-object" src="http://www.placehold.it/80x300" alt="Med Obj">
    </a>
     <a class="pull-right" href="#">
      <img class="media-object" src="http://www.placehold.it/80x300" alt="Med Obj">
    </a>
    <div class="media-body">
      <h3 class="media-heading"> Media Heading (media-heading) </h3>
      <p>
        rjegnkrejnfkgjrenkg
      </p>
    </div>
  </div>
</div>
```

## List Groups
```html
<ul class="list-group">
  <li class="list-group-item active">Cras justo odio</li>
  <li class="list-group-item">Dapibus ac facilisis in</li>
  <li class="list-group-item">Morbi leo risus</li>
  <li class="list-group-item">Porta ac consectetur ac</li>
  <li class="list-group-item">Vestibulum at eros</li>
</ul>
```

## Panels
```html
<div class="panel panel-default">
  <div class="panel-heading">Panel Heading</div>
  <div class="panel-body">Panel Content</div>
</div>
```

