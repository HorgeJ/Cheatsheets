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


### INPUT element
The input element is used to create many different types of form controls. The type attribute specifies what kind of form control should be rendered, such as text, email, passwords, and more. The name attribute is submitted with form data so that server-side code can parse the information.
