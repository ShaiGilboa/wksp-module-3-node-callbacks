# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here
HTML - header + input
     - unordered list
JS   - once submitting pushing new value to array
     - refreshing page
     - renders the indexes as <li> foreach
CSS  - make purrty

```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here
body-parser allows us to access information from "other" pages, using forms and the method "POST"
https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters

```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here
.post allows you to access req.body
we use .get when rendring a page. and we use .post when manipulating data
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here
this line retrives the functions that handle the actions for each url. those functions are in a separate file ('handlers.js'),so we need to "go get them". in object form. this is a short hand, the longer version would be:
const { handleHomePage: handleHomePage, handleFormData: handleFormData, handle404: handle404 } = require('./handlers');


```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here
itmes is the array that holds the "to do tasks". it reacives them through the .post and req.body functions. when we render the homepage we use the items to create the <li> tags in the HTML.
```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here
because we only have one page, and we render it through the "/" url. there is no need to have a second render. when we render the page we use the itmes array. bacuse we've updated it it will have the new "to do item".
``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here
because we are using the .post method we are doing things in the background then the break point might not be HTML related. so there are two different 404. one - if there is an error on the front. two - if there is an error in then back.
```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here
homepage.ejs - 
    1. includes the header partials with the title, and the h1
    2. creates the duv for the css "input-container'
    3. includes the todoInput partial
    4. closes the div
    5. creates the 'content' div
    6. creates the <ul> list that will hold the to do itmes
    7. starts the foreach on the items array (all the to do items inputed by the user)
    8. for each to do item creates a <li> with the text of the currulated input from the user. class 'todo-list--item;
    9. closes the for each loop
    10. closes the <ul>
    11. closes the 'content' div
    12. includes the footer partial
todoInput.ejs -
    1. creats the form that will have the input button that will add the text as an item in the items array. in order to do that we will use the .post method that - so we have the "method='POST' " syntex. the "action" syntex sends us to the '/form-data' url, in which we will use the data entered by the user.
    2. labels the input as 'item'
    3. this is where the user can enter the data. it is labled as 'item' and it will be text. before the user enters anything there is a placeholder text 'Item Description'.
    4. the submit button that send the information to the .post method.
    5. closes the form tag

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here
creates the variables that can be used in any linked scss file
```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here
the syntex for sass interpalation (like the `${}` in JS)
```







