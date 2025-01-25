# HTML
HTML from beginner to advanced ([Code Academy](https://www.codecademy.com/learn))

Remember to put the following command at the beginning of every *HTML* file

```html
<!DOCTYPE html>
<html>
   <head>
      <title> Title of the page (metadata) </title>
   </head>
   <body>
      See below ...
   </body>

</html>
```
Inside the previous block of code insert the following commands.

## The following sections shows commands that are composed entirely of text
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

Moreover, there exists the **section** command which I can use to replace the **div** command.  
Also the **header** command helps in expressing more correctly the meaning of our contents replacing the **div** command (has the same **section** command structure).
```html
<body>
   <section>
      <h1> pippo </h1>
      <section>
         <h1> Pluto </h1>
      </section>
   </section>

   <div id="Section 2">
      <h1>Section #2</h1>
      <h2> Another header </h2>
   </div>
</body>
```
Finally the command **span** is used to separate pieces of the text from the rest line of text.  
Then *em* tag makes the text inside it italic while the **strong** command makes its nested text in bold.  

To get the spacing between HTML elements the **<br>** has to be used (no closing tag is there).
***
The **ul** element should not hold raw text and won’t automatically format raw text into an unordered list of items. Individual list items must be added to the *Unordered list* using the **li** tag. The *li* or list item tag is used to describe an item in a list using the bullet point style.
```html
<body>
   <ul>
      <li> ciao </li>
      <li> sono Nicolò </li>
   </ul>
</body>
```
Instead, for an ordered list, the **ol** command is very useful
```html
<body>
   <ol>
      <li> Cavalieri matricola 2221 </li>
      <li> Sono Nicolò Rosso Malpelo </li>
   </ol>
</body>
```
***

## Images and Videos addition
To add images write as follows (the final forward slash can be omitted with no formatting problems)
```html
<body>
   <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="Add a description of the image in case it is not loaded properly on the web page (to help everyone such impaired users)" />
</body>
```
OR  
```html
<body>
   <img src="images/gatto.jpg" alt="A cat" />
</body>
```
For *videos* write as follows  
```html
<body>
  <video src="videos/myVideo.mp4" width="320" height="240" controls> Video not supported </video>
</body>
```
The **width** and **height** attributes are used to set the size of the video displayed in the browser. The **controls** attribute instructs the browser to include basic video controls such as pausing and playing.

The text, **Video not supported**, will only be displayed if the browser is unable to load the video.

## Comments, Linking text, images and more (tables)
Write comments and links with (**target="_blank"** opens the link in a new window of the browser)   
```html
   <!-- Text of the comment --> 
   <a href="https://www.wikipedia.org/" target="_blank"> This Is A Link To Wikipedia </a>
   <a href="./contact.html"> Contact </a> (this text link the current HTML file to another html file contact.html contained inside the same folder in which contact.html is stored. It is possible to add links linking to the same page in which they are stored)
```
**href** can be used to link the relative path not necessarily a URL link (often are LINKS though)

To turn **images into links** write as follows

```html
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">
   <img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/>
</a>
```

To link elements inside the same webpage it is needed to give an attribute to each element
```html
<p id="top"> This is the top of the page </p>

<ol>
 <li><a href="#top">Top</a></li>
</ol>

```

For creating tables write as follows:  
```html
<table border="1">
   <tr> <!-- Row 1 -->
      <th scope="col"> Pippo </th>
      <td> Element 1 of the first row of the table </td>
      <td> Element 2 of the first row of the table </td>
      ...
  </tr>
  <tr> <!-- Row 2 -->
      <th scope="row"> Pluto </th>
      <td> Another element inserted into the SECOND row of the table </td>
  </tr>
</table>
```
where the table's row element is **<tr>**.
To add titles to rows and columns, you can use the table heading element: **<th>**.
The **border** field represents the thickness of the table's border. 

OR to make data inside **td** span columns using the **colspan** attribute or, analogously, can span multiple rows using the **rowspan** attribute
```html
<table>
  <tbody>
     <thead> <!-- the **thead** element sections off the table’s column headings --> 
     <tr>
       <th>Monday</th>
       <th>Tuesday</th>
       <th>Wednesday</th>
     </tr>
    </thead>
    <tr>
       <td colspan="2">Out of Town</td>
       <td rowspan="2">Back in Town</td>
     </tr>
   </tbody>
</table>
```
Final example of how to use **tbody**, **thead** and **tfoot** is
```html
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>
```

***
OR it's better better to change table's style using *CSS* language such follows:
```css
table, th, td {
  border: 1px solid black;
  font-size: 13px;
  font-family: Arial, sans-serif;
  text-align: center;
}
```

***

Long tables can be sectioned off using the table body element: **<tbody>**.

## Other more expressive commands replacing div command
**nav**, **footer** for footer information (better to use, inside the footer command the **small** tag element for this information) and finally **main**.  
The always have the following style like **div** 
```html
<body>
   <div> ... </div>
</body>
```
