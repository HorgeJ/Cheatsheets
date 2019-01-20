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

### Variables
Colfusion is not a strongly typed language so a type does not need to be specified before declaring a variable.

