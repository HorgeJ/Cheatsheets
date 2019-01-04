# Bootstrap Basics
Twitter Bootstrap or simply Bootstrap is an open-source HTML, CSS and JavaScript Framework that is used in front-end web development.

## Set Up
* Download Bootstrap
* Download JQuery
* Include JQuery first
* Include Bootstrap

#### CSS
Bootstrap CSS file is included in the header and is located in content directory

overriding Bootstrap CSS is done in the custom.css file

## Grid System
Bootstrap’s grid system uses a series of containers, rows, and columns to layout and align content. It’s built with flexbox and is fully responsive. Below is an example and an in-depth look at how the grid comes together.

* creating a row create 12 logical units
* a column should be nested in apporiate classes, col should be in a row that is nested in a container

## Grid Layout
**Grid Offest**
* within a logical row the units must add up to 12

* Can use offsets to center data:
```html
<div class="col-lg-4 col-lg-offset-2">
  this is a col-lg-4
</div>
```
This will shift the cell by two logical units

### Simple Layout
lg >= 1200px Desktop
md >= 992px Tablet Landscape
sm >= 768px Portrait Tablets
xs < 768px Cell Phones

When the screen pixels fall short of the current screen resultion, the column will wrap around

### Fixed Grids
using the visible class, elements can be hidden when certain breakpoints are reached

This column will only be visible when greater than or equal to the lg breakpoint
```html
<div class="row-md-2 col-md-offset-1 visible-lg">
```

This column will only be visible when greater than or equal to the md or sm breakpoints. doesnt include xs
```html
<div class="row-xs-2 col-md-offset-1 visible-md visible-sm">
```

### Typography
Can use basic headings (H1 - H6)

Lead class makes text appear slighly larger
```
<p class="lead"> Hello </p>
```

**Alignment** can be achieved through classes
* text-center : Center aligned text
* text-left : Left aligned text
* text-right: Right align text
