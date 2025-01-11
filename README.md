# HTML
HTML from beginner to advanced ([Code Academy](https://www.codecademy.com/learn))

***
Write the title (header) on a page by writing 
```html
<h1>
   The title ...
</h1>
```
There exist also h2, h3, h4, h5 and h6 for smaller headings (subheadings)

Now let's write a paragraph by writing as follows

```html
<p>
   Paragraph element ...
</p>
```
***


***
Now let's write the body to write something on the screen by writing as follows (**better to put all the elements of an html page inside body tags** (this holds for *p*, *div*, *h1* and more)

Indeed

```html
<body>
   <div>
      <p> What's up? </p> ...
   </div>
</body>
```
***

Remember that **p and h1 are at the same level of hierarchy** and another common command in *HTML* is *div*
```html
<div>
   <p> What's your name? </p>
   <h1> Another header </h1>
</div>
```

Remember that the command **div** is very useful to create sections and can be used with the *attribute* **id** to so that I can have
```html
<body>
   <div id="Section 1">
      <h1>Section #1</h1>
      <h2> Another header </h2>
   </div>

   <div id="Section 2">
      <h1>Section #2</h1>
      <h2> Another header </h2>
   </div>
</body>
```

   Finally the command **span** is used to separate pieces of the text from the rest line of text.  
   Then *em* tag makes the text inside it italic while the **strong** command makes its nested text in bold.  

   To get the spacing between HTML elements the **<br>** has to be used (no closing tag is there).



