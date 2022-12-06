# Forms

- the <form> tool is for collecting information
- then we need to supply the <form> element with the location of where the <form>'s info goes
- and what HTTP request to make

```
<form action="/example.html" method="POST">
</form>
```

- the above form will send the info to example.html as a POST request
- the **action** attribute determines where the information is sent
- the **method** attribute assigns a HTTP action verb

- the form element can also contain child elements
- like a heading
- a paragraph expalining the form

```
<form action="/example.html" method="POST">
  <h1>Creating a form</h1>
  <p>Looks like you want to learn how to create an HTML form. Well, the best way to learn is to play around with it.</p>
</form>
```

### Text Input

- <input> creates an input field for our form
- the <input> elemt has a type attribute which determines how it renders on the page and what kind of data it can accept
- there is the "text" value for type
- we also need a name attribute for the input in order to send the info

```
<form action="/example.html" method="POST">
  <input type="text" name="first-text-field">
</form>
```

- the text the user types in becomes the value that is assigned to the name attribute, and bot are sent to the action
- we can set a default value for the value in the text field

```
<form action="/example.html" method="POST">
  <input type="text" name="first-text-field" value="already pre-filled">
</form>
```

- for a user to properly identify an input we use the <label> element.
- the <label> element has an opening an closing tag and displays text written within
- to associate a <label> and an <input> the <input> needs an id
- we then assign for="" of the label to the id of the input

```
<form action="/example.html" method="POST">
  <label for="meal">What do you want to eat?</label>
  <br>
  <input type="text" name="food" id="meal">
</form>
```

### Password Input

- type <password> attribute
- it will replace text with with another character

```
<form>
  <label for="user-password">Password: </label>
  <input type="password" id="user-password" name="user-password">
</form>
```

### Number Input

- we can restrict what users type into the field to just numbers and a few special characters
- we can also provide a **step** attribute
- the step attribute creates arrows to decrease and increase

```
<form>
  <label for="years"> Years of experience: </label>
  <input id="years" name="years" type="number" step="1">
</form>
```

### Range Input

- if we want to limit what numbers our users can type we use:
- type="range" min="0" max="100" step="1"
- this will create a slider

```
<form>
  <label for="volume"> Volume Control</label>
  <input id="volume" name="volume" type="range" min="0" max="100" step="1">
</form>
```

### Checkbox Input

- a checkbox allows the selection of multiple options
- type="checkbox"
- we use default values for the value so that the option value is displayed

```
 <label for="anchovy">Anchovy</label>
  <input id="anchovy" name="topping" type="checkbox" value="anchovy">
</form>
```

### Radio Button Input

- type="radio"
- allows for only one selection from multiple options
- needs to a label to display the value

### Dropdown List

- allows users to choose an option from an organized list

```
<form>
  <label for="lunch">What's for lunch?</label>
  <select id="lunch" name="lunch">
    <option value="pizza">Pizza</option>
    <option value="curry">Curry</option>
    <option value="salad">Salad</option>
    <option value="ramen">Ramen</option>
    <option value="tacos">Tacos</option>
  </select>
</form>
```

- we use the <select> element to create the dropdown list
- we add multiple <option> elements to populate the list
- we use a value attribute to mark the value chosen

### Datalist Input

- the <datalist> is used with <input type="test">
- users can type into the field to filter down options

```
<form>
  <label for="city">Ideal city to visit?</label>
  <input type="text" list="cities" id="city" name="city">

  <datalist id="cities">
    <option value="New York City"></option>
    <option value="Tokyo"></option>
    <option value="Barcelona"></option>
    <option value="Mexico City"></option>
    <option value="Melbourne"></option>
    <option value="Other"></option>
  </datalist>
</form>
```

### Textarea Element

- there are cases where users need to write more text
- <textarea>
- we can add the attributes rows="" and cols="" to add more area

```
<form>
  <label for="blog">New Blog Post: </label>
  <br>
  <textarea id="blog" name="blog" rows="5" cols="30">
  </textarea>
</form>
```

### Submit Form

- we use the <input> element and set the type="submit"

```
<form>
  <input type="submit" value="Send">
</form>
```

- the default value is "submit" however we can change that with the value attribute
