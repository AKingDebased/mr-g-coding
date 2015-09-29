# css basics

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
(view my website [here](https://jsbin.com/lipuke/edit?html,output))

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
(view my website [here](https://jsbin.com/feloho/edit?html,output))

see the word `style` up there?  that's a **style attribute**, which is how we use inline styling. by the way, we call it inline styling because you are typing the style attribute in the same line as the tag you want to change. the style attribute lets us say, "okay, i want to change the stuff between this tag". notice how each style attribute only changes the stuff between its pair of tags.  you need style attributes in every tag you want to change.

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
(view my website [here](https://jsbin.com/nugono/edit?html,output))

now, maybe all of a sudden i decide, "hmmm, you know, i want to change the font size for all the text in only *one* of my articles, not both." now, you could do this:

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
(view my website [here](https://jsbin.com/pusegu/edit?html,output))

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

    <div style="font-size:10px">
      <h1>local coding instructor has been awarded 'too cool for for school' award by mayor</h1>
      <hr>
      <img src="http://i.imgur.com/2D7cy4b.jpg">
      <p>an official statement released by the mayor reads: "everything you've heard? completely true."</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```
(view my website [here](https://jsbin.com/sahobe/edit?html,output))

putting the style attribute in the `<div>` tag changes **everything inside of the `<div>` tag.** if you've been wondering, "what the heck is the div tag for?", well, now you know. we can use it to easily style groups of related tags.  how awesome is that?
