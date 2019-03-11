# CSS Fundamentals

To begin open your index.html file in your browser. As is the tradition of our people you should see "Hello World". As you make changes press Refresh in the browser to see them.

## Demonstrating Precedence

The rules of CSS precedence are as follows:
* inline styles
* internal stylesheets
* The order the external stylesheets or CDNs are linked in the header
* !important
* styles further down your stylesheet overwriting those that are farther up

We will demonstrate this in the activity below.

1. Link your external stylesheet name style.css to the html file using:
```
<link rel="stylesheet" href="style.css">
```
Place this code in the head section of the html file. You know it is working when you see "Hello World" turn red.

2. In your html file, add the style attribute below to your opening h1 tag for "Hello World".
```
<h1 style="color:blue;">Hello World</h1>
```
You will notice your "Hello World" turn blue. This means that inline styles have precedence over external stylesheets. Inline styles are not best practice because they are more difficult to locate and change in large scale applications. Because they overwrite all other stylesheets they can cause problems for other developers who work with your code.

3. REMOVE step 2, the style attribute, from your html. Below your body tags (but still inside your html tags) add in html style tags and set h1 to be green:
```
<style>
  h1{
    color:green
  }
</style>
```
This is an internal stylesheet. This practice is rarely used for the same reasons as inline styles should be rarely used. In large scale applications, it is more convenient to have stylesheets separate from your html so that all the code pertaining to style can be found in one place.

4. REMOVE step 3, the internal stylesheet, from your html. Link your second external named style2.css to your html file UNDER THE STYLE.CSS link like this:
```
<link rel="stylesheet" href="style.css">
<link rel="stylesheet" href="style2.css">
```
You should see the "Hello World" turn orange. This demonstrates that stylesheets linked lower in the header overwrite those linked higher. A common mistake as we get to frameworks is that people will link a framework CDN stylesheet below their custom stylesheet. This will overwrite your custom styles.

## Classes and Ids

In order to continue demonstrating precedence, we need to dive into classes and ids.
We use classes and ids to label our html. This makes it easier to retrieve for adding styles in css or functionality in JavaScript.
A class can be placed on multiple html elements. Making it easier to apply styles to a larger group of elements.
An id can only be placed on one html element. It is designed to give unique styles and functionality to ONE SPECIFIC ELEMENT.

You can add a class or in id to your html by creating a class or id attribute in your opening html tag.

Adding a class:
```
<h1 class="titles">Hello World</h1>
```
Adding an id:
```
<h1 id="header-style">Hello World<h1>
```
In CSS we can now grab these attributes:
Grabbing element by class:
```
.titles{
  font-family: verdana;
}
```
Grabbing element by id:
```
#header-style{
  font-family: arial;
}
```
One way to remember the syntax for a class is to think of a "class period" in school.

5. Take out the internal stylesheet and the link to style2.css. Now lets add the html below:
```
<h1>Noodle Splash Guard</h1>
<p>Protect your noodles from your hair and your hair from your noodles</p>
<h2>Only $5.99!!!!</h2>
<img src="https://theawesomedaily.com/wp-content/uploads/2017/06/crazy-japanese-inventions-21.jpeg" />
```
You can get rid of the h1 for "Hello World". We are now selling the greatest new product on the market "Noodle Splash Guard".

We are going to add classes and ids to the html tags then we are going to grab those elements and style them. When we are "grabbing the html element" we are using selectors.
The selector for a class is:
```
.titles{}
```
The selector for an id is:
```
#header-style{}
```
The selector for an html element h1 tag is:
```
h1{}
```
The selector for a different style on mouse hover over element.
```
h1:hover{}
```

6. Take 10 min and [CSS Diner](https://flukeout.github.io/) to learn how to use advanced Selectors.

7. Now that you know how to grab elements by various selectors. Add to the current HTML and CSS to answer these questions.
Which has precedence?
* a class or an id on the same element
* the first class or the second class on the same element
* the first class or the second class on the same element with !important next to the first in css
(**** bad practice ****)
