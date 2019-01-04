## Navigation

Navigation available in Bootstrap share general markup and styles, from the base .nav class to the active and disabled states. Swap modifier classes to switch between each style.

The base .nav component is built with flexbox and provide a strong foundation for building all types of navigation components. It includes some style overrides (for working with lists), some link padding for larger hit areas, and basic disabled styling.

```
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
