# HTML Forms

### FORM element 
The form element wraps a section of the document that contains form controls. The action attribute specifies the web address of a program that processes the information submitted via the form. The method attribute specifies the HTTP method that the browser should use to submit the form, such as POST or GET. Forms cannot be nested inside one another.

```html
<form action="index.html" method="POST">
  ... form controls ...
</form>
```

* The action attribute is the web address of a program that process the information submitted by the form
* The METHOD attribute is the HTTP method that the browser uses to submit the form 

The POST verb is most-often utilized to **create** new resources. In particular, it's used to create subordinate resources. That is, subordinate to some other (e.g. parent) resource. In other words, when creating a new resource, POST to the parent and the service takes care of associating the new resource with the parent, assigning an ID (new resource URI), etc.

The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.
when sending data, the GET method adds the data to the URL;

On successful creation, return HTTP status 201, returning a Location header with a link to the newly-created resource with the 201 HTTP status.


### INPUT element
The input element is used to create many different types of form controls. The type attribute specifies what kind of form control should be rendered, such as text, email, passwords, and more. The name attribute is submitted with form data so that server-side code can parse the information.

```html
<form action="URL" method="post">
  <input type="text "name="name" id="user_name">
  <input type="email" name"mail" id=""user_email>
  <input type="password" name="password"  id="user_password">

  <textarea id="bio" name="user_bio"></textarea>
  
  <button type="submit">Sign Up</button>
</form>
```

* type: the type of input
* name: needed for when the form is submited the server side code and processess it
* id: useful for targeting with JS
* submit: The <input type="submit"> defines a submit button which submits all form values to a form-handler.
  * The form-handler is typically a server page with a script for processing the input data.
  * The form-handler is specified in the form's action attribute.

### Organizing Forms

Add label element to give fields context
The label attribute associates the label with a form element by ID

```html
<form action="URL" method="post">
  <label for="name">Name:</label>
  <input type="text "name="name" id="user_name">
  
  <label for="mail">Email:</label>
  <input type="email" name"user_email" id="mail">
  
  <label for="password">Password:</label>
  <input type="password" name="user_password"  id="password">

  <label for="bio">Biography:</label>
  <textarea id="bio" name="user_bio"></textarea>
  
  <button type="submit">Sign Up</button>
</form>
```
