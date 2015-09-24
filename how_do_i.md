# mr. g, mr. g, how do i ... ?!

![even john cena can't believe it](https://i.imgur.com/1Jy4MYN.jpg)

## ... link to a new page on my site?!

well, you'll need to use an anchor tag, which looks like this: `<a href="www.yourlinkname.com">my new page!</a>` (read up on those [here](https://github.com/AKingDebased/mr-g-coding/blob/master/lessons/02-html_basics/html_basics.md)).  for simplicity's sake, let's say you want a link on your `index.html` page to another page in your `pages` folder.  so, first of all, make sure you **put a new web page in your `pages` folder**.  once you've done that, put the anchor tag on your `index.html` somewhere, like so:

```
<html>
  <head>
  </head>

  <body>
    <a href="">go to my new web page!</a>
  </body>
</html>
```

now, your anchor tag is gonna be pretty useless if you don't give the **hyperlink reference** attribute (`href`) a value.  because you are linking to a page in your `pages` folder, you will need to use a special link.  you should NOT put a `www.page-name.com` style link in your anchor tag right now.  here's what you SHOULD do:

```
<html>
  <head>
  </head>

  <body>
    <a href="pages/your-page-name.html">go to my new web page!</a>
  </body>
</html>
```

the word you type before the forward slash ( `/` ) symbol should be the name of the folder holding the page you wanna link to.  the words you type after the `/` should be the exact file name of the page you're linking to. so, if you have a `newpage.html` file in your `pages` folder, your anchor tag should look like this: `<a href='pages/newpage.html'>go to my new page!</a>`


when you link to a page in one of your folders without using `www` or `.com`, you are doing what's called **linking to a local file**.  that means your anchor tag is digging through your files, rather than going on the internet.  pretty sweet, huh?



## ... use a div tag?!

the whole point of the div tag (short for page division tag) is that it **groups related HTML tags together**.  so, for example, let's say you're writing an article on how rad my class is.  you might have a header for your title, a paragraph for your body text, and a picture:


```
<html>
  <head>
  </head>

  <body>
    <h1>mr. g's coding class is the bomb.com</h1>

    <p>a recent survey of students ages 11 to 14 has determined that mr. g, and all his attendant classes, are, in fact, that bomb.com.</p>

    <img src="https://31.media.tumblr.com/56e594fc5bddc70206f0f94f660e9e1e/tumblr_np346hoRIL1uwmsumo1_400.gif">
  </body>
</html>
```

now, i think you and i can agree that the `<h1>`, `<p>`, and `<img>` tag in that previous example are all related to one another, yes? they are all part of the same article.  well, wouldn't it be rad if there was a tag that said, "hey! all the tags between me are related somehow!"  well, let me tell you, there is such a tag:

```
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>mr. g's coding class is the bomb.com</h1>

      <p>a recent survey of students ages 11 to 14 has determined that mr. g, and all his attendant classes, are, in fact, that bomb.com.</p>

      <img src="https://31.media.tumblr.com/56e594fc5bddc70206f0f94f660e9e1e/tumblr_np346hoRIL1uwmsumo1_400.gif">
    </div>
  </body>
</html>
```

now, if i add another article to my page, i can put all that in *another* div tag, since those tags are all related to one another but separate to my previous article:

```
<html>
  <head>
  </head>

  <body>
    <div>
      <h1>mr. g's coding class is the bomb.com</h1>

      <p>a recent survey of students ages 11 to 14 has determined that mr. g, and all his attendant classes, are, in fact, that bomb.com.</p>

      <img src="https://31.media.tumblr.com/56e594fc5bddc70206f0f94f660e9e1e/tumblr_np346hoRIL1uwmsumo1_400.gif">
    </div>

    <div> <!-- a whole other div tag, for this whole other content -->
      <h1>all other coding classes are way sucky</h1>

      <p>according to a popular poll, all other coding classes not
      led by the esteemed and venerable mr. g are, quote, "way mad super lame".</p>

      <img src="http://gifsec.com/wp-content/uploads/GIF/2014/03/You-suck-GIF.gif?gs=a">
    </div>
  </body>
</html>
```

the confusing thing right now is that the `<div>` tag doesn't really look like it **does** anything and, right now, it doesn't.  if you put text in it, it will work just like a `<p>` tag, but that's not very special.  `<div>` tags won't really shine until we start working with CSS, so you're just gonna have to trust me on this for now.
