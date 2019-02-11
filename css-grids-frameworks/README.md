# CSS Grid Systems and other Positioning Tools
I'm going to spare you the world of floats and pixel pushing in favor of one of the most essential tools in your CSS arsenal. Grid Systems!

There are an infinite number of grid systems you can use to set boundaries and organize your code.
CSS Grid requires little to no install, but most css frameworks also come with their own grid systems.

Why do we need grid systems?
In the world of floats and pixel pushing, you may eventually see that you tell an element to go right and it does not budge. Sometimes the reason becomes apparent and other times you spend an hour of your time trying to move a box. Grid systems tell the box where it should and should not be leaving us with much more time to fret over other stylistic choices. Grid systems are also responsive. Meaning they adjust to changes in screen size. We will get into more on Responsive later.

Today we are learning Bootstrap's grid system because its the one I know the best. Bootstrap is a CSS framework created by Twitter. It comes with a grid and many precoded components.

* Setup for Rails is [here](https://github.com/twbs/bootstrap-rubygem).

* Setup for React is [here](https://react-bootstrap.github.io/getting-started/introduction).

## Getting Started
1. Follow the instructions below to setup up your index.html file.
* Setup for standard index.html is [here](https://getbootstrap.com/docs/4.3/getting-started/introduction/).
- Take the CSS link and ALL the JS links and paste them in the head tags of your html.
** You know Bootstrap is installed when you see the font change from Times.

## Wrappers, Containers, and Divs Oh My!
Generally CSS frameworks have a class that will designate a container that wraps other components. In bootstrap that containers class name is container, but be wary it comes with some margin. If you do not want style to come with your container use a div.
Why do I want to wrap my elements?
Well this opens the conversation into positioning. When we use css to center something, it centers it in reference to the outer container.

2. Take 10 min and play some [flexbox froggy](https://flexboxfroggy.com/). You can use flexbox in your css files, no install required just like css grid. You can also build a grid with flexbox itself.

Notice the game is asking us to move the frogs around the container. Think of your grid as a series of containers that we use to organize our page.

## Columns and Rows
Rule 1 of bootstrap grid is to always put a column inside your row. Every row is 12 units long. Rows and columns divs with the class of row or col-(size)-(number of units). For example:
```
<div class="container">
 <!-- row 2 with 2 columns -->
    <div class="row">
      <!-- column 1 of 2 -->
      <div class="main col-lg-8">
        <h1 id="title-area">About Me</h1>                       
      </div>
      <!-- column 2 of 2 -->
      <div class="main col-lg-4">
        <a href="http://melmacd.com">My Portfolio</a>
      </div>
    </div>
</div>
```  
Column sizes designate at what screen size the columns will stack and fill 100% of the screen.  The number of units designates the proportion of the screen that the column will take up. So in the example above 8/12 is 2/3 of your screen size and 4/12 is the remaining 1/3.
The best way to visualize this is by setting different color borders to visualize the grids.

The css for border is (width, pattern, color) respectively:
```
row {
  border: 5px solid red;
}
```
3. Take 10 min and build yourself a bootstrap grid in the index.html file.

## Adding in Components
You can find all the bootstrap components [here](https://getbootstrap.com/docs/4.3/components/alerts/).
Find one you like then copy and paste the code into your grid. Feel free to fill in the html fields you need.
4. Take 5 min and add some components you like.

## What is the catch? -- Modifying Bootstrap
If you can help it, try to be happy with the look of the framework of your choosing. If you try to change your bootstrap it will fight you every step of the way. If you need to change a couple things that is totally fine, just pull out your chrome inspector and your selectors foo. In order to change bootstrap you have to overwrite the bootstrap styles. The bootstrap styles are associated with the classes. This means you need to find the EXACT class that is controlling the style you want and overwrite the exact style you want to change.

For example, if I go to bootstraps home page, open my inspector and click on a link in the navbar I see the element is "a" and the class is "nav-link". I can also see the styles associated with those elements. If I want to put an underline under each link, I would be looking for where they set text-decoration. In this case it is under the styles for "a". So in my custom styles I write:
```
a{
  text-decoration: underline;
}
```

This example was a simple fix, but when doing things like changing the color of a component it may take longer to find the correct selector.
