# Cold Fusion Basics
Adobe ColdFusion is a commercial rapid web application development platform created by J. J. Allaire in 1995. 
ColdFusion was originally designed to make it easier to connect simple HTML pages to a database.

### Syntax

You can write ColdFusion Markup Language (CFML) in two ways- tag-based and script-based. 
For example:
```coldfusion
<cfset greeting="Hello World!">
<cfoutput>
```

or:
```coldfusion
<cfscript>
  greeting = "Hello, World!"
  WriteOutput(greeting);
</cfscript>
```

### Evaluating a Variable or Function
In order to evaluate a variable or function it must be placed between two pound signs.

```coldfusion
<cfset myString = "Hello World!">

<cfoutput>
  #myString#  // evaluates to "Hello World!
</cfoutput>
```

### Variables
Colfusion is not a strongly typed language so a type does not need to be specified before declaring a variable.

There are two tpyes of variables:
* Simple: String, Numeric, Boolean and DateTime
* Complex: Structs, Arrays, Queries and Images

### Strings
In ColdFusion, a string is a quote ( ' or " ) followed by zero or more letters, numbers, or symbols, and followed by another quote ( ' or " ). For example:

```coldfusion
<cfscript>
       myString="That's one small step for man, one giant leap for mankind.";
       myStringLen=Len(myString);
       WriteOutput(myStringLen);  //would output 58, the length of the string
</cfscript>
```

### Arrays
In ColdFusion, you can create arrays explicitly, by using a function to declare the array and then assigning it data, or implicitly by using an assignment statement. You can create simple or complex, multidimensional arrays.

[Additonal coldfusion array functions](https://helpx.adobe.com/coldfusion/cfml-reference/coldfusion-functions/functions-by-category/array-functions.html)

To create an array, first create an array object using the ArrayNew function. 

Example:
```coldfusion
<cfscript>
   myArray = [];
   myArray=[0,1,1,2,3,5,8,13,21];
</cfscript>
```
The example creates an array object for a one-dimensional array and then populates the array with the Fibonacci series.

### Lists
A list in ColdFusion is a string with delimiters.

[Additional List functions](https://helpx.adobe.com/coldfusion/cfml-reference/coldfusion-functions/functions-by-category/list-functions.html)

A delimiter separates each item in the list. For example: myList="a,b,c,d,e";

```coldfusion
<cfscript>
       myList="Tokyo,Bangkok,Jakarta,Manila,Bangalore,Shanghai";
       WriteOutput(ListLast(myList)); //Outputs the last element in the list, Shanghai
</cfscript>
```

### Structs
