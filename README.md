## lap

## What is LAP?

LAP is an alternative to a PHP framework. It offers many features that the most popular frameworks offer. This makes your website more dynamic with little effort and is then more secure and faster. Our URL router can work with both static and dynamic URLs.



## Structure

1. apps/
2. assets/
3. includes/
4. functions/
5. manager/
6. templates/



## Router

You will find a url.php in the apps as well as in the manager with which you can set up the routing.

### Static routing

Within the two apostrophes you can specify which URL your page is accessible via

`Route::add('/',function(){
  require('templates/main.php');
});`

When you go to their website they will see main.php

### Dynamic routing

In this file you can define the urls for the individual files.
Set dynamic values with ([]*) to read this value. Add a value to function()

`Route::add('/([a-z,A-Z]*)',function(){
  require('templates/main.php');
});`

You have the possibility to read the value of the URL by adding a variable in the brackets.

Here in the example we use $routing. You can also call it something else.

`Route::add('/([a-z,A-Z]*)',function($routing){
  require('templates/main.php');
});`

Now we have the possibility to read this value in our main.php and can display it.
