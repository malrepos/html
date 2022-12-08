### The body

- only content inside the opening and closing tags can be displayed on the screen.

```
<body>

</body>
```

- we can then add different types of content to the body

### HTML Structure

- when an element is placed inside another element it is consdiered a child of that element.
- the child is nested

```
<body>
  <p>This paragraph is a child of the body</p>
</body>
```

- there can be multiple levels of nesting
- multiple elements at the same level are consdered siblings.
- child elements can inherit characteristics from their parent

### Headings

- there are 6 different headings
- from largest to smallest:

```
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
```

### Divs

- short for division
- a container that divides the page into sections
- great for grouping elements
- allow us to group elements to apply the same style for all inside.

```
<body>
  <div>
    <h1>Why use divs?</h1>
    <p>Great for grouping elements!</p>
  </div>
</body>
```

### Attributes

- attributes are content added to the opening tag of an element
- made up of two parts:
  - name
  - value
- a common attribute is id
- id's can help identify content

```
<div id="intro">
  <h1>Introduction</h1>
</div>
```

### Displaying Text

- to display test use paragraph or span
- paragraphs <p> display a block of text
- <span> contains short pieces of test or other HTML
  - <span> separates small pieces of content that are on the same line as other content

```
<div>
  <h1>Technology</h1>
</div>
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>
```

### Styling Text

- the <em> tag emphasizes text : italic
- the <strong> tag highlights text : bold

```
<p><strong>The Nile River</strong> is the <em>longest</em> river in the world, measuring over 6,850 kilometers long (approximately 4,260 miles).</p>
```

### Line Breaks

- to modify the spacing in the browser us <br>
- only has a starting tag
- can be used anywhere in the HTML code

```
<p>The Nile River is the longest river <br> in the world, measuring over 6,850 <br> kilometers long (approximately 4,260 <br> miles).</p>
```

Will produce:

The Nile River is the longest river
in the world, measuring over 6,850
kilometers long (approximately 4,260
miles).

### Unordered Lists

- a list of items in no particular order
- <ul> should not hold raw text
- items must be added to the <ul> using <li>

```
<ul>
  <li>Limes</li>
  <li>Tortillas</li>
  <li>Chicken</li>
</ul>
```

### Ordered Lists

- each item is numbered
- use <ol>

```
<ol>
  <li>Preheat the oven to 350 degrees.</li>
  <li>Mix whole wheat flour, baking soda, and salt.</li>
  <li>Cream the butter, sugar in separate bowl.</li>
  <li>Add eggs and vanilla extract to bowl.</li>
</ol>
```

### Images

- <img>
- is a self closing tag

```
<img src="image-location.jpg" />
```

- has a required attribute src
- src is set to the image's location, such as URL

### Image Alts

- alt tag is a description of the image

```
<img src="#" alt="A field of yellow sunflowers" />
```

### Videos

- <video> element requires opening and closing tag

```
<video src="myVideo.mp4" width="320" height="240" controls>
  Video not supported
</video>
```

- width and height set the size of the video in the browser
- controls attribute instructs the browser to include video controls
- the text is displayed if the video fails to load

---

- we can let web browsers know we are using HTML:

```
<!DOCTYPE html>
```

- now we add opening and closing html tags so that anything inside will be interpreted as HTML code

```
<html>

</html>
```

### head element

- goes above the body
- contains metadata for a web page

```
<!DOCTYPE html>
<html>
  <head>
  </head>
```

- inside the <head> we have <title>

### Links to Other Web Pages

- we use an ancor element <a>
- we put the text of the link inside the opening and closing tags
- we also add a href for the link address

```
<a href="https://www.wikipedia.org/">This Is A Link To Wikipedia</a>
```

- we can open links in new windows using the target attribute
- to open in a new window target needs a value of "\_blank"

```
<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">The Brown Bear</a>
```

#### Linking to Internal Pages

- if files are stored in the same folder we can link web pages together using a relative path

```
<a href="./contact.html">Contact</a>
```

#### Using Images as Anchors for Links

- we can also turn images into links by wrapping it in a <a> anchor

```
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/></a>
```

#### Linking to the Same Page

- in order to link to a target on the smae page, we must give the target an id

```
<p id="top">This is the top of the page!</p>
<h1 id="bottom">This is the bottom! </h1>
```

- an id can be added to most elements on a page
- the target link is a string containing a # and then the target id

```
<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>
```

### Whitespace

- the browser ignores whitespace in a html file
- so we can use whitespace to make the html code easier to read

### Comments

- comments begin with <!-- and end with -->

```
<!-- This is a comment that the browser will not display. -->
```

---

# HTML Tables

### Create a Table

- before dispalying data we must first create the table

```
<table>
</table>
```

### Table Rows

- the first step is creating rows with the table rows element: <tr></tr>
- here we add 2 rows

```
<table>
<tr>
</tr>
<tr>
</tr>
</table>
```

### Table Data

- each cell must also be defined to add data to it
- we use the table data element: <td>

```
<table>
  <tr>
    <td>Go fuck yourself</td>
    <td>Or whatever</td>
  </tr>
</table>
```

- the display of this table would show 1 row and 2 columns

### Table Headings

- to add titles to rows and columns we use the table heading element: <th>
- it must be placed within a table row

```
<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

- the above code creates 2 column headings
- it uses an empty heading so that the headings align over the column
- a row heading was created
- the scope="" attribute dictates whether it is a row or col heading

### Table Borders

- we use CSS to add style to our tables

### Spanning Columns

- if data spans multiple columns, for example you have 2 columns Monday, Tuesday and the data holiday spans both
- we use the "colspan" attribute in the table data <td> opening and define how many columns to span

```
<table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>
```

### Spanning Rows

- data can also span multiple rows
- the rowspan attribute

```
<td rowspan="3">Blah</td>
```

- perhaps an event goes on for multiple hours

### Table Body

- when a table gets long we can section off all of the table data using
- <tbody></tbody>
- this excludes the table headings

### Table Head

- we section off the table's head using <thead></thead>

### Table Footer

- footers are often used to contain sums, differences, or other results
- <tfoot></tfoot>

# Form Validation

### Requiring an Input

- when fields in our forms are not optional
- require attribute

```
<input id="allergies" name="allergies" type="text" required>
```

### Set A Minimum or Maximum

- we can assign a minimum or maximum value for a number field

```
<input id="guests" name="guests" type="number" min="1" max="4">
```

### Checking Text Length

- to set a minimum or max number of characters for a text field
- minlength or maxlength

```
<input id="summary" name="summary" type="text" minlength="5" maxlength="250" required>
```

### Matching A pattern

- when we want a user input to follow specific guidleines
- pattern attribute and assign it a regular expression

```
<input id="payment" name="payment" type="text" required pattern="[0-9]{14,16}">
```

- this will check the user entered only numbers, and that it is >=14 <= 16 numbers>
- [a-zA-z0-9]+ will have only letters lower and upper and numbers
- the + sign means 1 or more times, so the character can be repeated

# Semantic HTML

- semantic = "relating to meaning"
- semantic elements provide info about the content between the opening and closing tags
- so we select HTML elements based on their meaning, not on how they're presented
- For example, by using the <header> element we provide info on what is in the tag

### Header and Nav

- a <header> is a container usually for navigational links
- or intoductory content <h1> to <h6>

- a <nav> is used to define a block of navigation links such as menus
- a <nav> can be used inside of the header

```
<header>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
    </ul>
  </nav>
</header>
```

### Main and Footer

- <main> is used to encapsulate the dominant content within a webpage
- this is the buld of the page content

```
<main>
  <header>
    <h1>Types of Sports</h1>
  </header>
  <article>
    <h3>Baseball</h3>
    <p>
      The first game of baseball was played in Cooperstown, New York in the summer of 1839.
    </p>
  </article>
</main>
```

- <footer> contains info such as:
  Contact information
  Copyright information
  Terms of use
  Site Map
  Reference to top of page links

```
<footer>
  <p>Email me at Codey@Codecademy.com</p>
</footer>
```

### Article and Section

- <section> defines elements in a document, such as chapters, headings, areas of the document with the same theme

```
<section>
  <h2>Fun Facts About Cricket</h2>
</section>
```

- the <article> element holds content that makes sense on its own

```
<section>
  <h2>Fun Facts About Cricket</h2>
  <article>
    <p>A single match of cricket can last up to 5 days.</p>
  </article>
</section>
```

### Aside

- <aside> is used to mark additional info that can enhance another element but isn't required to understand the main content
- commonly used for:
  - Bibliographies
  - Endnotes
  - Comments
  - Pull quotes
  - Editorial sidebars
  - Additional information

```
<article>
  <p>The first World Series was played between Pittsburgh and Boston in 1903 and was a nine-game series.</p>
</article>
<aside>
  <p>
   Babe Ruth once stated, “Heroes get remembered, but legends never die.”
  </p>
</aside>
```

### Figure and Figcaption

- <figure> is an element used to encapsulate media such as an image, illustration, diagram, code snippet, etc, which is referenced in the main flow of the document.

```
<figure>
  <img src="overwatch.jpg">
</figure>
```

- <figcaption> is an element used to describe the media in the <figure> tag. Usually, <figcaption> will go inside <figure>

```
<figure>
  <img src="overwatch.jpg">
  <figcaption>This picture shows characters from Overwatch.</figcaption>
</figure>
```

### Audio and Attributes

- <audio> element is used to embed audio content into a document. Like <video>, <audio> uses src to link the audio source.

```
<audio>
  <source src="iAmAnAudioFile.mp3" type="audio/mp3">
</audio>
```

- Although not always necessary, it’s recommended that we state the type of audio as it helps the browser identify it more easily and determine if that type of audio file is supported by the browser.

- Attributes provide additional information about an element.
- There are many attributes for <audio>
- controls: automatically displays the audio controls into the browser such as play and mute.

```
<audio autoplay controls>
```

### Video and Embed

- <video> element makes it clear that a developer is attempting to display a video to the user.
- some attributes:
  - controls: When added in, a play/pause button will be added onto the video along with volume control and a fullscreen option.
  - autoplay: The attribute which results in a video automatically playing as soon as the page is loaded.
  - loop: This attribute results in the video continuously playing on repeat.

```
  <video src="coding.mp4" controls>Video not supported</video>
```

- <embed> tag, which can embed any media content including videos, audio files, and gifs from an external source
- <embed> is a deprecated tag
