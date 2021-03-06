# AJAX Basics
AJAX allows web pages to be updated asynchronously by exchanging data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

**How AJAX Works:**

1. Create an XMLHTTP Request Object
2. Create a call back function
3. Open a request (provide the METHOD and URL)
4. Send the request

## Creating a request

**The XMLHttpRequest Object**
The XMLHttpRequest object can be used to exchange data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

Syntax for creating an XMLHttpRequest object:
```
variable = new XMLHttpRequest();
```

ex: 
```javascript
var request = new XMLHttpRequest(); 
```

**onreadystatechange**
Defines a function to be called when the readyState property changes

**open(): specifies the request**
* *method*: The request type, GET or POST
* *url*: the file location
* *async*: true(asynchornous), false(synchronous)
* *user*: optional user name
* *password*: optional password

**send()**
Sends the request to the server
Used for GET requests


**readyState: Holds the status of the XMLHttpRequest**
* 0: request not initialized
* 1: server connection established
* 2: request received
* 3: processing request
* 4: request finished and response is ready

**responseText**
Returns the response data as a string

**responseXML**
Returns the response data as XML data

**status**
returns the status number of a request
* 200: OK
* 403: Forbidden
* 404: Not Found

**statusText**
Returns the status-text (e.g. "OK" or "Not Found")

```javascript
<script>
    var request = new XMLHttpRequest();
    request.open('GET', 'data.txt', true);
    request.onreadystatechange = function(){
      if((request.readyState === 4) && (request.status === 200)){
        console.log(request);
        document.writeln(request.responseText);
    }
    request.send();
    }
  </script>
```

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <link href='//fonts.googleapis.com/css?family=Varela+Round' rel='stylesheet' type='text/css'>
  <link rel="stylesheet" href="css/main.css">
  <title>AJAX with JavaScript</title>
  <script>
    var xhr = new XMLHttpRequest();
    xhr.onreadystatechange = function(){ // Our call back function
      if(xhr.readyState === 4){           // If readuState is 4 (success) then place our response in DIV
        document.getElementById('ajax').innerHTML=xhr.responseText;
      }
    xhr.open('GET', 'sidebar.html'); // 3. Open the Request
    function sendAJAX(){
          xhr.send(); // send the request
      document.getElementById('load').style.display="none";
      }
    };
  </script>
</head>
<body>
  <div class="grid-container centered">
    <div class="grid-100">
      <div class="contained">
        <div class="grid-100">
          <div class="heading">
            <h1>Bring on the AJAX</h1>
            <button id="load" onclick="sendAJAX()">Send me AJAX!</button>
          </div>
          <div id="ajax">
            
          </div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
```

### AJAX Callbacks

```
var xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
	if(xhr.readyState === 4){
  	if(xhr.status === 200){
    	document.getElementById('sidebar').innerHTML=xhr.responseText
    }
  }
};
xhr.open('GET', 'sidebar.html');
xhr.send();
```

### Intro to JSON
Key: Double Quotes
Value: Double Quotes


```JSON
{
    "name": "Jim",
    "phone": "555-555-5555"
}
```

### Parsin JSON Data
The **JSON.parse()** method parses a JSON string, constructing the JavaScript value or object described by the string. An optional reviver function can be provided to perform a transformation on the resulting object before it is returned.

```
var json = '{"result":true, "count":42}';
obj = JSON.parse(json);

console.log(obj.count);
// expected output: 42

console.log(obj.result);
// expected output: true
```

```javascript
var xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
	if(xhr.readyState === 4){
  	var employees = JSON.parse(xhr.responseText)
	console.log(typeOf employees);
	console.log(employees);
    }
  }
};
xhr.open('GET', 'sidebar.html');
xhr.send();
```

Now: JSON is in usable JS

```javascript
var xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
  if(xhr.readyState === 4){
    var employees = JSON.parse(xhr.responseText);
    var statusHTML = '<ul class="bulleted">';
    for ( var i = 0; i < employees.length; i++){
      if(employees[i].inoffice === true){
        statusHTML += '<li class="in">';
      } else {
        statusHTML += '<li class="out">';
      }
      statusHTML += employees[i].name;
      statusHTML += '</li>';
    }
    statusHTML += '</ul>';
    document.getElementById('employeeList').innerHTML = statusHTML;
  }
};

xhr.open('GET', 'data/employees.json');
xhr.send();
```

```html
<aside class="grid-30 list">
    <h2>Employee Office Status</h2>
     <div id="employeeList">

     </div>
</aside>
```

## Modifying the DOM
Using JavaScript to manipulate the DOM we can add content to elements


### AJAX with JQuery
.load() loads content onto an element on the page

#### GET method
```
var callback = function(response){
	// do something with data
}

$.get(url, data (optional in Query String), callback)
```

```javascript
$(document).ready(function () {
  var url = "../data/employees.json";
  $.getJSON(url, function(response){
    var statusHTML = '<ul class="bulleted">';
    $.each(response, function(index, employee) {
      if(employee.inoffice === true){
        statusHTML += '<li class = "in">';
      } else {
        statusHTML += '<li class = "out">';
      }
      statusHTML += employee.name + '</li>';
    }); // end each
    statusHTML += '</ul>';
    $('#employeeList').html(statusHTML);
  }); // end getJSON
}); //end ready
```







