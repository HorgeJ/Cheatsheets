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
