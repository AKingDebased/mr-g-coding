## html basics

### so you wanna build a webpage

building a website really isn't all that hard.  every time you want to make a new web page, you'll need to copy the following code into your page:

```
<html>
  <head>
  <!-- this is where all your CSS links go -->
  </head>

  <body>
  <!-- everything you want to see on your webpage should go here -->

  <body>
</html>
```

we use this exact same code every time we want to make a new webpage.  code that looks exactly the same and does the same thing every time you use it is called **boilerplate code** (it's a reference to the writing on those big boilers people sometimes have in their basements.  trust me on this one).

if the page you are creating is your home page, it should be called `index.html`.  otherwise, you can call it whatever you like, e.g. `your-page-name.html`

### tags
you're probably noticing all of those words surrounded by `<` and `>` symbols, like `head` and `body`.  in html, whenever a word is surrounded by `<` and `>`, we call it a **tag**.

tags are what we use to tell the web browser (like chrome, or firefox, or internet explorer) what we want to see on our webpage.  for example, if we want to see a new paragraph, we use the `<p>` tag.  most tags require a closing tag, which just means you need to add a forward slash, like this: `<p>this is a new paragraph!</p>`  

there are a whole lot of tags in the world of HTML.  here are just a couple:

* `<head></head>` - **the head tag**.  this is a special tag that you can only use once, above your `<body>` tag.  this tag holds stuff like your css links, and the language setting of your web page.
* `<body></body>` - **the body tag**.  this is another special tag that you can only use once, directly below your `head` tag.  this tag holds everything you want to see on your website, like your images, divs, and links.  if you can see it, it goes here.
* `<h1></h1>` - **the header tag**.  not to be confused with the head tag, whatever you type here will become big and bold, like the title on an article.  there are 6 sizes of headers, e.g. `<h1></h1>`, `<h2></h2>`, `<h3></h3>` and so on
* `<div></div>` - **the division tag**, aka **the div tag**.  this tag's job is to divide parts of your page from each other.  every time you have a bunch of tags that are related (for example, a header tag and a bunch of paragraphs that are all part of one article), you will want to wrap them all inside a div tag.
* `<p></p>` - **the paragraph tag**.  text that is wrapped in a paragraph tag will automatically have line breaks before and after it, just like a paragraph should.
* `<img src='www.yoururl.com'>` - **the image tag**.  this is a special tag that allows you to put an image on your website.  it does not use a closing tag, and it has a special `src` **attribute**.  all you need to do is set the `src` attribute equal to your image's link, e.g. `<img src='https://s-media-cache-ak0.pinimg.com/736x/45/22/f5/4522f50716482945a2536f14205220f2.jpg'>`
* `<!-- your comment here -->` -- **the comment tag.** this is a special tag that lets you write notes to yourself that won't appear on your web page.  anything you put in the comment tag will not show up on your page, but will show up in your code.

there are a ton more tags, but for now, these are the ones we're going to work with. try typing the following code into your `index.html`, and see what happens.  **DO NOT COPY PASTE.** it is tempting, but your brain and fingers need to get used to typing code out.

```
<html>
  <head>
  <!-- this is where all your CSS links go -->
  </head>

  <body>
    <!-- this is a special secret comment.  anything you type in here will be invisible on your web page, but visible to you, the designer. -->
    <div>
      <h1>this is a header tag!</h1>

      this is what happens if you type text without a tag. it still works, but it just runs across the page in one long line, and there are no line breaks! even if i put line breaks here in the html, they don't show up on my webpage. that's no good.
    </div>

    <div>
        <h2>this header is a little smaller!</h2>

        <p>this is a new paragraph! it's gonna have a link break if i type anything after it.</p>
        <p>this paragraph is line broken from the previous one!</p>
        <p>also, note that i'm using div tags to keep each of these blocks of text separate from one another.</p>
    </div>

    <div>
         <h3>this header is even smaller than the others!</h3>

        <p>hey, let's see an image!</p>
        <img src='http://media.wizards.com/images/magic/daily/ftl/ftl149_volcanicDragon.jpg'>
        <p>awesome.</p>
    </div>
  <body>
</html>
```

no matter what tags you use, the most important thing is that you **always put your writing between tags**.  no exceptions.  the question is not "do i need a tag?"  rather, it's "what's the right tag for what i'm trying to do?"

**a note on cleanliness**: you probably noticed in my code sample above that i indent some of my tags.  the general rule of thumb is that if a tag is inside another tag, it should get one indentation.

for example:
```
<html>
  <head>
  <!-- the head tag is inside the html tag, so it gets indented -->
  </head>
  <body>
  <!-- the body tag is inside the html tag, but it's not inside the head tag, so it should be
  indented the same amount as the head tag -->
    <div>
    <!-- this div tag is inside the body tag, so it gets indented -->
      <p> <!-- this paragraph tag is inside the div tag, so it's indented even further --></p>
    </div>
  </body>
</html>
```

### linking to other pages

every good website has some way to link to other pages.  what fun is it if your website is only one page?  

there's a special tag we use for just such a purpose: the **anchor tag**, which looks like this: `<a href='your link here'></a>`.  linking to new pages is a little tricky, but not too much.

try typing this into your `index.html`, and see what happens:

```
<html>
  <head>
  <!-- the head tag is inside the html tag, so it gets indented -->
  </head>
  <body>
    <a href='http://www.google.com/''>this is a link to google!</a>
  </body>
</html>
```

here are the steps you need to follow:

1. create a new page in your `pages` folder.  it should be called `yourpagename.html`, making sure to include the `.html` at the end.  you can't use white space when you name pages, so do this `page-name-with-spaces.html`, not this `you can't do this!.html`
2. create an anchor tag in your `index.html`.  
3. in that anchor tag, set the 'href' attribute equal to your new page.  to do this, you need to type in the following: `<a href='pages/your-page-name.html'></a>`.  this is called **linking to a local file.** we do this when the page we want to link to is in our codio, and not yet on the internet.

and now you've done it!  your code should look something like this:

```
<html>
  <head>
  <!-- the head tag is inside the html tag, so it gets indented -->
  </head>
  <body>
    <a href='pages/your-page-name.html'>this is a link to my new page!</a>
  </body>
</html>

```
