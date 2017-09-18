# Personal Website Tutorial
Welcome to this personal website tutorial! Today we're going to be using **HTML** (Hypertext Markup Language), **CSS** (Cascading Style Sheets), and a little **Javascript** to spice things up.

## Prerequisites
* Prior to this tutorial please install a text editor such as [Atom](https://atom.io/) or [Sublime](https://www.sublimetext.com/). I recommend Sublime because it's very lightweight and easy to use but I recommend Atom because it has a nice integration with Github and you can download packages to make it feel like an IDE (Integrated Development Environment).

* Download this repository

## What is HTML/CSS? What is Javascript?
Wikipedia says:
>Hypertext Markup Language (HTML) is the standard markup language for creating web pages and web applications. With Cascading Style Sheets (CSS) and JavaScript it forms a triad of cornerstone technologies for the World Wide Web.[2] Web browsers receive documents from a web server or from local storage and render them into multimedia web pages. HTML describes the structure of a web page semantically and originally included cues for the appearance of the document.

##What does it actually mean?
HTML is like a skeleton of a webpage. When you create a website, this is what gives it a structure. HTML is not a programming language. The neat but sometimes frustrating thing is that your browser will try its best to load your website even if you're missing brackets somewhere along the way.
CSS is what makes everything look pretty and you can even have some simple functionality built into CSS like drawing shapes or transformations.

>HTML can embed programs written in a scripting language such as JavaScript which affect the behavior and content of web pages.

Have you ever wondered why Facebook looks different every time you load it? Or why going to www.Facebook.com looks different with your friend's account than on yours? That's because Javascript is able to change the content of a webpage depending on variables.

## Let's take a look at the final product...
Before we begin let's see what it will eventually look like

![final](final.png)

Here it is live:
http://dtravie.com/tutorial-website/final-website/index.html
WOW! :sparkling_heart:

It takes quite a bit of work to get to that point, however. Let's go on to look at how these languages all work together

## Inspect Element Tool

If you're using Chrome, right click on the website and select **Inspect**
If you're using Firefox, go to your menu bar and follow this chain: **Tools -> Web Developer -> Inspector**

Feel free to play around with it!

## Now onto the actual coding part...

##Quickstart guide to HTML/CSS
```html

<h1> Title </h1>
    <p>
        My first HTML snippet of code!
    </p>


```

HTML works by enclosing your content with tags that communicate information about how its supposed to look or act.
Structural tags include:
```html
    <html>
        <head>

        </head>
        <body>

        </body>
    </html>
```
Headers:
```html
    <h1> Big
    </h1>
        <h2> Medium
        </h2>
            ...
                <h#> Smol
                </h#>
```
Some more examples of different types of tags:
```html
    <p> This is a paragraph with a line <br> break
    </p>
    <a href = "https://www.google.com">This is an anchor tag</a>
```

HTML code is composed of command code (what it is) and variable code (defines how it changes)

```html
    <img src = "img/forest.jpg"></img>

```
```html
    <!-- The code within 'style' is CSS -->
    <div style = "text-align: center;
                    color: red;">
        <ul>
            This is an unordered list:
            <li>Feed the dog</li>
            <li>Make lunch</li>
            <li>Go to SEC's meeting</li>

        </ul>
    </div>

```
CSS is similar in that it has a selector (determines which element you want to change), a property (what you want to change about the element), and an attribute (how you change the element)
Below are some examples of the different types of selectors. For a more complete list here is a link: https://www.w3schools.com/cssref/css_selectors.asp
```css
    #example {
        /*selects elements with id = example*/
        width: 100px;
        height: 100%;
        background: #a4a89f;
    }
    .example {
        /*selects elements with class = example*/
        width: 100px;
        height: 100%;
        background: #a4a89f;
    }
    p{
        /*selects all elements with p tags*/
        text-align: center;
    }
    #example p{
        /*you can nest selectors, this is selecting all p tags within the division containing an id = example*/
        text-align: center;
    }

```

## More on structural tags
The head is at the beginning of your html code. The head contains meta data, scripts, links, and some other things you'd like to load to your website. The content in head is not displayed in your browser.

```html
<head>
    <meta ...>
    <link ...>
    <title></title>
</head>
```

This is all included with the starter-website index.html file so you don't have to worry about that right now.

The body contains the bread and butter of your website's HTML code. It's where you'd put all those p tags and img tags.

## This scary thing called Javascript
We will be using **Bootstrap**, an open-source, front-end framework. It contains templates we'll be calling upon in our files. This is Bootstrap's responsive navigation header which we will be using. If you remove the link in the header then our navigation bar looks completely different.

```html

    <nav class="navbar fixed-top navbar-expand-lg navbar-light bg-light" id = "navbar-font">

      <div class="collapse navbar-collapse" id="navbarNavDropdown">
       <ul class="navbar-nav">
         <li class="nav-item active">
           <a class="nav-link" href="#">nav<span class="sr-only">(current)</span></a>
         </li>
         <li class="nav-item">
           <a class="nav-link" href="#">nav</a>
         </li>

         <li class="nav-item">
           <a class="nav-link" href="#">nav</a>
         </li>

         <li class="nav-item">
           <a class="nav-link" href="#">nav</a>
         </li>

       </ul>
     </div>
    </nav>

```
And here's how we're changing the font of this navigation bar
```css
#navbar-font{
    font-family: 'Sanchez', serif;
}
```

##Let's make the landing page!

Feel free to write your name in the header and a quick blurb in the paragraph tags
```html
    <div class="image">
        <div class="text">
            <h1>...</h1>
            <p>...</p>
          </div>
    </div>
```
This looks kind of boring so let's spice things up by adding style to our style fyle

```css

    .image{
        height: 100%;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
    }
    .text{
        text-align: center;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: white;
        font-family: 'Work Sans', sans-serif;
    }

```
Now that we have this in place let's add an image which will be specific to the index in the index.html file. Why do we do this? Well, we want to make each tab have a different picture but we can't do that if they're inheriting the picture from the same file

```css
.image{
    background-image: url("img/forest.jpg");
}
```

I want to make the header and the button look different from the rest, however, so we can play around with selectors to make it do just that

```css
.text h1{
    font-family: 'Sanchez', serif;
}
.text button{
    font-family: 'Sanchez', serif;

}
```

##Blog style posts

```html

    <div id = "first" class = "post">
        <h1></h1>

        <p id = "paragraph-post">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </p>
    </div>

```

Let's add some style to these posts.
```css
#paragraph-post{
    text-align: justify;
    font-family: 'Work Sans', sans-serif;
}

.post{
    width: 100%;
    height: 1000px;
    padding-right: 100px;
    padding-left: 100px;
    text-align: center;
    font-family: 'Sanchez', serif;
    padding-top: 100px;
    color: white;
}

```

Right now they are white but if we add the following code to our index.html file we can change the color of individual posts

```css
#first{
    background: #a4a89f;
}
#second{
    background: #737a6b;
}
#third{
    background: #545b4b;
}

```

## Now you can scroll down...
But you can also use buttons to make this experience feel more dynamic! Let's add buttons to our landing and our blog style posts

```html
<p>
    <button type="button" class="btn btn-outline-light" onclick="...">NAME</button>
</p>

```
Try removing the class and type so you can see what a button looks like in plain HTML. As of right now clicking it doesn't do anything so this is where we're going to be using some Javascript to add functionality.
I found the following code on Stack Overflow which allows us to scroll automatically when we click.
https://stackoverflow.com/questions/18071046/smooth-scroll-to-specific-div-on-click

```Javascript
window.smoothScroll = function(target) {
    var scrollContainer = target;
    do {
        //find scroll container
        scrollContainer = scrollContainer.parentNode;
        if (!scrollContainer) return;
        scrollContainer.scrollTop += 1;
    } while (scrollContainer.scrollTop == 0);

    var targetY = 0;
    do {
        //find the top of target relatively to the container
        if (target == scrollContainer) break;
        targetY += target.offsetTop;
    } while (target = target.offsetParent);

    scroll = function(c, a, b, i) {
        i++; if (i > 30) return;
        c.scrollTop = a + (b - a) / 30 * i;
        setTimeout(function(){ scroll(c, a, b, i); }, 20);
    }
    // start scrolling
    scroll(scrollContainer, scrollContainer.scrollTop, targetY, 0);
}
```

Try clicking the buttons now!

## Let's get started with the about page

Make a landing page just like before, this time we're going to make h3 tags within a p tag to put our name number location and email. Let's add another blog style post to add an About page with all the details of who you are and what you're looking for.
Change the image by adding this code in the style tag:
```css
.image{
    background-image: url("img/building.jpg");
}
#first{
    background: #f7cea3;
}
```
Now we're going to include little icons that link to a profile like your linked in or github. They're by Font Awesome and it's already included in the header so you don't have to worry about getting it in your html for right now.
We're going to create anchor tags which are used to enclose anything that links to another website
The i tag represents a range of text set off from the normal text

```html
<a href = "https://www.spotify.com"><i class="fa fa-spotify fa-2x" aria-hidden="true"></i></a>
```
Feel free to change the size by manipulating the '2'

This blue color doesn't match our theme and it's a little too close so let's change it with some internal styling

```css
i{
    color: white;
    padding: 10px;
}
```
We're ready to move onto our resume
##Resume page
Same as before, we're going to make a landing page by copying over our navigation bar and making a post.
Here's the color we're going to use and the image for our landing page
```css
#first{
    background: #b18c75;
}
.image{
    background-image: url("img/backpack.jpg");
}
```

Now we're going to use the embed tag to add a resume on that first post.
```html
<embed src="devyd.pdf" type="application/pdf" width="100%" height="80%">
```

Awesome! And now we're done with our website!

## Challenge Time!

If you haven't noticed already, the project.html file is empty. I challenge you guys to finish it!
I recommend using 'cards'. Bootstrap's website has a neat content container which can hold information, pictures, and links. Below is the documentation from Bootstrap's website.
http://getbootstrap.com/docs/4.0/components/card/

Another option is to use the slides/blog style posts we have on the homepage.

You can get creative with it and do something else entirely!

Email or facebook message me your completed challenge, live website, or any other ways you get creative with this template and you'll get mad brownie points :sparkles:

With your permission, we can even feature your website on our Facebook and website!
## Helpful links, tips, and sources
Special thank you to w3schools for being my main source of learning how to make websites!
https://www.w3schools.com/
Bootstrap documentation
https://getbootstrap.com/docs/4.0/getting-started/introduction/
Small html/css cheatsheet https://www.bluehost.com/blog/website-design/html-css-cheat-sheet-infographic-4181/
Unsplash photos
https://www.Unsplash.com
HTML quickstart guide
http://ptgmedia.pearsoncmg.com/images/9780321928832/samplepages/0321928830.pdf
Google fonts
https://fonts.google.com/
Font awesome icons
http://fontawesome.io/icons/
Design inspo over at muz.li
https://muz.li/
Hosting your website with github
https://pages.github.com/
## Thanks for following along!
My name is Daniela and my email is dtravie@gmail.com if you have any questions or comments
