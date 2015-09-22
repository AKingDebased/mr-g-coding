## html basics

### so you wanna build a webpage

building a website really isn't all that hard.  every time you want to make a new web page, you'll need to copy the following code into your codio:

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

### tags
you're probably noticing all of those words surrounded by `<` and `>` symbols, like `head` and `body`.  in html, whenever a word is surrounded by `<` and `>`, we call it a **tag**.

tags are what we use to tell the web browser (like chrome, or firefox, or internet explorer) what we want to see on our webpage.  for example, if we want to see a new paragraph, we use the `<p>` tag.  most tags require a closing tag, which just means you need to add a forward slash, like this: `<p>this is a new paragraph!</p>`  

there are a whole lot of tags in the world of HTML.  here are just a couple:

* `<h1></h1>` - **the header tag**.  whatever you here will become big and bold, like the title on an article.  there are 6 sizes of headers, e.g. `<h1></h1>`, `<h2></h2>`, `<h3></h3>` and so on
* `<p></p>` - **the paragraph tag**.  

```
<html>
  <head>
  <!-- this is where all your CSS links go -->
  </head>

  <body>
  <h1>this is a header tag!
  <p>this is a new paragraph!  it's gonna have a link break if i type anything after it.</p>

  <body>
</html>
```
