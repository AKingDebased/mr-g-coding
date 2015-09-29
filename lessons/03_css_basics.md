# CSS basics - pt 1

so, we have some web pages, but they look pretty boring.  there's no color, all the font's the same size, and so on.  turns out, we programmers actually have a special language just for making web pages look pretty.  that language is called **CSS**, or **Cascading Style Sheets** (but we just call it CSS).

CSS is used to decorate your web pages, as well as do other stuff like move images and text around and even create simple animations.  if it changes the way your HTML looks, you're gonna do it with CSS.  there are three ways to put CSS on your webpage, and we're going to talk about all of them here.

## inline styling

so, let's say you have an HTML document that looks like this:

``` html
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>this is my webpage!</h1>
      <p>man this is a rad page.  you can do anything here.  be anyone. do anything.</p>
      <img src="http://i.imgur.com/fXejuh5.gif">
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/lipuke/edit?html,output))

that's pretty cool and all, but maybe i want to change the text color in that first `<p>` tag, and make the font a little bigger. i can do that using **inline styling**:

``` html
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>this is my webpage!</h1>
      <p style="color:blue">man this is a rad page.  you can do anything here.  be anyone. do anything.</p>
      <img src="http://i.imgur.com/fXejuh5.gif">
      <p style="font-size:50px">go go power rangers.</p>
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/feloho/edit?html,output))

see the word `style` up there?  that's a **style attribute**, which is how we use inline styling. by the way, we call it inline styling because you are typing the style attribute in the same line as the tag you want to change. the style attribute lets us say, "okay, i want to change the stuff between this tag". notice how each style attribute only changes the stuff between its pair of tags.  you need style attributes in every tag you want to change.

inside the quotation marks, we have written CSS. that means whenever we type code between the quotation marks of a style attribute, we are **not writing in HTML**.  repeat that with me:

### THE CODE WE WRITE IN THE QUOTATION MARKS OF A `style` TAG IS CSS, NOT HTML.  THEY ARE TWO SEPARATE LANGUAGES. I WILL REMEMBER THIS.

whenever we write our CSS in the `style` attribute, the format is always `style='property-name:property-setting'`

on the left side of the colon (the `:` symbol) is the **property**.  that's the thing you want to change in your tag.  for example, if you want to change the font size, you type `style="font-size:20px` where `font-size` is the property, and `20px` is the property setting (that's 20 pixels, by the way).

### CSS and the `<div>` tag
check out this example:

``` html
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>breaking news: water on mars</h1>
      <hr>
      <img src="http://i.imgur.com/k6z2tsi.jpg">
      <p>turns out there is totally water on mars.  how cool is that? let's type some gibberish here so this article looks really long.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>

    <div>
      <h1>local coding instructor has been awarded 'too cool for for school' award by mayor</h1>
      <hr>
      <img src="http://i.imgur.com/2D7cy4b.jpg">
      <p>an official statement released by the mayor reads: "everything you've heard? completely true."</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/nugono/edit?html,output))

now, maybe all of a sudden i decide, "hmmm, you know, i want to change the font size for all the text in only *one* of my articles, not both. also, i wish i could give each of my posts their own special background." now, you could do this:

``` html
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>breaking news: water on mars</h1>
      <hr>
      <img src="http://i.imgur.com/k6z2tsi.jpg">
      <p style="font-size:10px">turns out there is totally water on mars.  how cool is that? let's type some gibberish here so this article looks really long.</p>
      <p style="font-size:10px">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>

    <div>
      <h1>local coding instructor has been awarded 'too cool for for school' award by mayor</h1>
      <hr>
      <img src="http://i.imgur.com/2D7cy4b.jpg">
      <p style="font-size:25px">an official statement released by the mayor reads: "everything you've heard? completely true."</p>
      <p style="font-size:25px">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/pusegu/edit?html,output))

but that would take sooooo looooooong. who wants to go through every paragraph tag and add new style attributes every single time?  you know what would be better? if we had some sort of container for all of our related tags.  hmmmm, maybe some sort of **division** tag?  man, if only there was a tag used **specifically for dividing up your webpage**...

``` html
<html>
  <head>
  </head>

  <body>
    <div style="font-size:10px">
      <h1>breaking news: water on mars</h1>
      <hr>
      <img src="http://i.imgur.com/k6z2tsi.jpg">
      <p>turns out there is totally water on mars.  how cool is that? let's type some gibberish here so this article looks really long.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>

    <div style="font-size:25px">
      <h1>local coding instructor has been awarded 'too cool for for school' award by mayor</h1>
      <hr>
      <img src="http://i.imgur.com/2D7cy4b.jpg">
      <p>an official statement released by the mayor reads: "everything you've heard? completely true."</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/sahobe/edit?html,output))

putting the style attribute in the `<div>` tag changes **everything inside of the `<div>` tag.** if you've been wondering, "what the heck is the div tag for?", well, now you know. check out this other example where i put background colors in some divs:

``` html
<html>
  <head>
  </head>

  <body>
    <div style="background-color: blue">
      <p>now my div has a background color!>
      <p>hey, this coding stuff isn't so difficult after all.</p>
    </div>
  </body>
</html>
```
(view my code [here](https://jsbin.com/hiceti/edit?html,output))

### CSS properties

there are a whole ton of CSS properties that we add to our tags. here are just a few:

* `background-color` - this property lets you change a tag's background color.
* `color` - this property lets you the font color in a tag. don't confuse this with `background-color`!
* `height` - this property lets you change a tag's height. try it out on an `<img>` tag and see what happens!
* `width` - this property lets you change a tag's width. try it out on an `<img>` tag and see what happens!

here's an example of all those properties in action:

``` html
<html>
<head>
  <meta charset="utf-8">
  <title>JS Bin</title>
</head>
<body>
  <div style="background-color:yellow">
      <img src="http://i.imgur.com/Qgmc6gP.jpg" style="height:300px">

    <p style="color:blue">wow, CSS really let's you do anything!</p>

    <img src="http://i.imgur.com/Qgmc6gP.jpg" style="height:500px;width:100px">
    <!-- if you want more than one property in one style attribute, you need to separate them with a semi-colon -->
  </div>

</body>
</html>
```
(view my code [here](https://jsbin.com/lamecu/edit?html,output))

### classwork
we're gonna make a new web page that talks about your dream vacation. this can be to a real world place, or somewhere totally made up (if i may offer some suggestions, i hear westeros and the shire are both lovely this time of year)

1. create a brand new page in your `pages` folder called `my-dream-vacation.html`. this file should **NOT** be in the same folder as your `index.html`
2. include at least 3 images of this dream land
3. talk about at least 2 people you might meet in on this dream vacation
4. tell me about at least one wild adventure you plan to go on while there
5. make sure to change the font color of at least one of your tags!
6. you should change the background-color of at least one tag.
7. you should change the `height` and/or `width` of at least one of your images
7. there should be at least 20 HTML tags on the page
8. there should be at least one tag that is inside another tag (e.g., `<div><p>i am a paragraph inside a div!</p></div>`)
9. include some links to other websites!
10. throw in at least one animated gif
11. have at least one secret comment in the code
12. HAVE FUN! look at it this way: you could be doing algebra right now
