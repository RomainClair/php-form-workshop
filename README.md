# Workshop : PHP forms

You have decided to share your knowledge about web dev languages using a simple web site.
The web site will have a landing page (index) and a page per language.
The main objective of this workshop is to have search bar navigation feature. 

All the pages will display a simple search text box. 
If the user enters a keyword corresponding to an available language on the web site (an existing web page), it will be redirected to this page.
If the user input is not a keyword, a message "Language not available yet" will be displayed and the user will stay on the same page.

## Skills & concepts

* Display proper HTML form
* Process Form with PHP
* Use redirections

## Walkthrough

* First : let's create a page building module containing :
  * A function to display the begining of a web page
  * A function to display the end of a web page
* Now let's create some pages using this function and adding some simple content. For example a page about JS, PHP, SQL...
* Create a new module for the naviguation form feature providing two functions :
  * A function to display the form
  * A function to process the form, returning the potential error message.
  * Advice : you should probably use a constant array for the list of available pages/languages. You could try an associative array indexed by keywords and containing the page URL for that keyword.
* Test !

## Hints

The PHP [```header()```](https://www.php.net/manual/fr/function.header) function is used to redirect the user from one page to another.

It expect a string argument. And when this argument begins with "Location: " followed by an URL (can be a short one. Just a path for example), the HTTP reponse resulting from this php script will ask the browser to go the provided URL.

It is common to send an empty HTML page with this response because most browser will not display the page anyway.

**Warning** : HTTP headers are quite strict on spaces. There must be no spaces between "Location" and ":".

Example :

```php
  header("Location: index.php");
```
