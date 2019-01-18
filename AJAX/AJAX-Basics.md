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

## Modifying the DOM
Using JavaScript to manipulate the DOM we can add content to elements

### Modifying by ID
```javascript
<div id="update">
    <!-- AJAX CONTENT GOES HERE -->
</div>

<script>
    var request = new XMLHttpRequest();
    request.open('GET', 'data.txt', true);
    request.onreadystatechange = function(){
      if((request.readyState === 4) && (request.status === 200)){
        var modify = document.getElementById('update'); // targets our div
        modify.innerHTML = request.responseText;
    }
    request.send();
    }
  </script>
```

### Modifying Elements

