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
