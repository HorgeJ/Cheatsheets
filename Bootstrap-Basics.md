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
```css
<div class="col-lg-4 col-lg-offset-2">
  this is a col-lg-4
</div>
```
This will shift the cell by two logical units
