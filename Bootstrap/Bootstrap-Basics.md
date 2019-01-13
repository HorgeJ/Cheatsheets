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

### Code
* Inline code
```
Wrap inline snippets of code with <code>. Be sure to escape HTML angle brackets.
```
  
```  
For example, <section> should be wrapped as inline.
```
  
```
For example, <code>&lt;section&gt;</code> should be wrapped as inline.
```

* Code Blocks
```Use <pre>s for multiple lines of code. Once again, be sure to escape any angle brackets in the code for proper rendering. You may optionally add the .pre-scrollable class, which will set a max-height of 350px and provide a y-axis scrollbar.
```
```
<p>Sample text here...</p>
<p>And another line of sample text here...</p>
```
```
<pre><code>&lt;p&gt;Sample text here...&lt;/p&gt;
&lt;p&gt;And another line of sample text here...&lt;/p&gt;
</code></pre>
```

### Tables
[Table Docs](https://getbootstrap.com/docs/4.0/content/tables/)

Due to the widespread use of tables across third-party widgets like calendars and date pickers, we’ve designed our tables to be opt-in. Just add the base class .table to any table, then extend with custom styles or our various included modifier classes.
  
  ```html
<div class="table-responsive">
<table class="table table-bordered table-hover table-condensed table-striped">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry</td>
      <td>the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
</div>   
```

### Forms
Be sure to use an appropriate type attribute on all inputs (e.g., email for email address or number for numerical information) to take advantage of newer input controls like email verification, number selection, and more.

```html
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

```

### Butttons
[Button Docs](https://getbootstrap.com/docs/4.0/components/buttons/)
Bootstrap includes several predefined button styles, each serving its own semantic purpose, with a few extras thrown in for more control.

```html
<button type="button" class="btn btn-lg btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>
```

### Helper Classes
[Refrences](https://www.w3schools.com/bootstrap/bootstrap_ref_css_helpers.asp)

.text-muted	Text styled with class "text-muted"

.text-success	Text styled with class "text-success"

.bg-info	Table cell is styled with class "bg-info"

.bg-danger	Table cell is styled with class "bg-danger"
 
 
### Respnsive Utilities
[Layoutit](Layoutit.com) Allows for quick layouts


### Glyphicons
[Icon Docs](https://getbootstrap.com/docs/3.3/components/)

Includes over 250 glyphs in font format from the Glyphicon Halflings set.

For performance reasons, all icons require a base class and individual icon class. To use, place the following code just about anywhere. Be sure to leave a space between the icon and text for proper padding.

Icon classes cannot be directly combined with other components. They should not be used along with other classes on the same element. Instead, add a nested `<span>` and apply the icon classes to the `<span>`.

```html
<button type="button" class="btn btn-default" aria-label="Left Align">
  <span class="glyphicon glyphicon-align-left" aria-hidden="true"></span>
</button>

<button type="button" class="btn btn-default btn-lg">
  <span class="glyphicon glyphicon-star" aria-hidden="true"></span> Star
</button>
```

```html
<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">Error:</span>
  Enter a valid email address
</div>
```

### Drop Downs
[Dropdown Docs](https://getbootstrap.com/docs/4.0/components/dropdowns/)

Dropdowns are toggleable, contextual overlays for displaying lists of links and more. They’re made interactive with the included Bootstrap dropdown JavaScript plugin. They’re toggled by clicking, not by hovering; this is an intentional design decision.

```html
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown button
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
    <a class="dropdown-item" href="#">Action</a>
    <a class="dropdown-item" href="#">Another action</a>
    <a class="dropdown-item" href="#">Something else here</a>
  </div>
</div>
```

### Button Groups
[Button Group Docs](https://getbootstrap.com/docs/4.2/components/button-group/)

Group a series of buttons together on a single line with the button group, and super-power them with JavaScript.

```html
<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-secondary">Left</button>
  <button type="button" class="btn btn-secondary">Middle</button>
  <button type="button" class="btn btn-secondary">Right</button>
</div>
```
```html
<div class="btn-group btn-group-sm" data-toggle="buttons">
  <label class="btn btn-success">
    Discover
  <input type="radio" name="paymentOption" value="d">
  </label>
</div>
```

### Input Groups
[Input Groups Docs](https://getbootstrap.com/docs/4.0/components/input-group/)

```html
<div class="input-group mb-3">
  <div class="input-group-prepend">
    <span class="input-group-text" id="basic-addon1">@</span>
  </div>
  <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
</div>

<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
  <div class="input-group-append">
    <span class="input-group-text" id="basic-addon2">@example.com</span>
  </div>
</div>

<label for="basic-url">Your vanity URL</label>
<div class="input-group mb-3">
  <div class="input-group-prepend">
    <span class="input-group-text" id="basic-addon3">https://example.com/users/</span>
  </div>
  <input type="text" class="form-control" id="basic-url" aria-describedby="basic-addon3">
</div>

<div class="input-group mb-3">
  <div class="input-group-prepend">
    <span class="input-group-text">$</span>
  </div>
  <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
  <div class="input-group-append">
    <span class="input-group-text">.00</span>
  </div>
</div>

<div class="input-group">
  <div class="input-group-prepend">
    <span class="input-group-text">With textarea</span>
  </div>
  <textarea class="form-control" aria-label="With textarea"></textarea>
</div>
```
