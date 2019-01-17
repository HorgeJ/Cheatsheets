# AJAX Basics
AJAX allows web pages to be updated asynchronously by exchanging data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

**How AJAX Works:**
1. Create an XMLHTTP Request Object
2. Create a call back function
3. Open a request (provide the METHOD and URL)
4. Send the request

### Creating a request
**The XMLHttpRequest Object**
The XMLHttpRequest object can be used to exchange data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

Syntax for creating an XMLHttpRequest object:
```
variable = new XMLHttpRequest();
```

ex: 
```javascript
var xhttp = new XMLHttpRequest(); 
```
