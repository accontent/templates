# HTML Forms

Forms provide the backbone to any website with communication between client and server. We use forms every day on the websites we interact with, comments are submitted through forms, Facebook posts, Twitter Tweets, and every time you upload a picture, you're posting data through a form. Forms provide a variety of functionality to collect various types of data.

To make our forms functional we need a backend or server-side language like PHP or Python. These server-side languages along with the databases help us to receive, process and store the information.

```js
const number = 3
```

## The form tag
To start adding a form to our HTML page we start by adding the `<form></form>` tag. Any information we want to collect using this form will be added inside the opening `<form>` and closing `</form>` form tags.

```html
<form action="thanks.html" method="post">

</form>
```

**Form Attributes**
The two most important attributes we add to the form tag are `action` and `method`
- `action` attribute is used to add the URL or file path where the form will be sending its information.
- `method` attribute defines how the information is sent. There are two values used for this attribute. `get` and `post`
  - `get` is used when the information being sent is not sensitive and can benefit from being added to the URL when sending over to the action page. Example: Product search on Amazon or search form on Google
  - `post` is used when the information needs to be hidden from the user when sent to the action page. Example login credentials.

## Inputs and Labels
Inside the `<form></form>` tag we use different input types to allow the user to input the data. Each input is linked to a label to tell the user what information they need to add to the input field.

- Each input must have a label attached to it for accessibility. 
- We add an `id` attribute to the input which matches with the `for` attribute of the label, to connect an input with the label
- **It is important to use a unique value for the id attribute of each input in one form.**
```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Inputs and Labels" src="https://codepen.io/IMD/embed/PoXGKWW?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/PoXGKWW">
  HTML Forms - Inputs and Labels</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Input Types
There are different types of inputs used in HTML forms. These inputs allow the browser to style the inputs accordingly and in some cases validate the data of the input. 

Using the specific input type also helps with improving the user experience on mobile devices by changing the keyboard based on the input type.

We define the type of an input by using the `type` attribute in the `<input>` tag. If not type attribute is set then by default the input type is set to text. Which is a single line of text. 

```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname" type="text">
</form>
```

- `text` - for generic single-line text.
- `number` - for accepting numbers, the browser will validate that the data is a number
- `email` - for an email address, this will be validated to contain the `@` symbol in the email
- `url` - for accepting a URL, the browser will validate the URL to start with `http://` or `https://`
- `password` - for allowing the user to type in passwords, the input will hide the entered data with dots
- `tel` - for telephone numbers
- `time` - for accepting time in hours, minutes, seconds
- `date` - for accepting dates, browsers will display a calendar picker
- `range` - for selecting from a range of numbers, this will need the `min` and `max` attributes
- `color` - for picking colors, shows a color picker tool
- `file` - for allowing file uploads

## Input Name
Just like the type it is important to add the `name` attribute to an input field. The `name` attribute is defined to give a name to the data that is being submitted. The value of the `name` attribute is then used by the receiving page to understand the content.

**It is important to use a unique value for the name attribute of each input in one form.**
```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname" type="text" name="fullname">
</form>
```

## Other Attributes
We can use some additional attributes in our input fields for different purposes

### Placeholder
The placeholder attribute is used to display placeholder text inside an input field.
```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname" type="text" name="fullname" placeholder="John Doe">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Placeholder" src="https://codepen.io/IMD/embed/abPmypx?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/abPmypx">
  HTML Forms - Placeholder</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Value
The value attribute is used to pre-fill the value of an input field. This is useful when we are getting the previously saved information by the used from the database and then displaying it to the user for editing in a form.
```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname" type="text" name="fullname" placeholder="John Doe" value="Mr. ">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Value" src="https://codepen.io/IMD/embed/gOZwxmL?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/gOZwxmL">
  HTML Forms - Value</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Required
Required field is used for making an input field required. 

Required is a boolean attribute, which means we do not need to give it a value. It is either set or unset.

If the `required` attribute is added to an input field the browser will not allow the form to submit if that field is empty.

```html
<form action="thanks.html" method="post">
  <label for="fullname">Name</label>
  <input id="fullname" type="text" name="fullname" placeholder="John Doe" required>
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Required" src="https://codepen.io/IMD/embed/WNLGEpX?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/WNLGEpX">
  HTML Forms - Required</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Min, Max and Step
`min` and `max` attributes are used to specify the minimum number required and maximum number allowed in the numeric fields.

```HTML
<form action="thanks.html" method="post">
  <label for="quantity">Quantity</label>
  <input id="quantity" type="number" name="quantity" min="2" max="10">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Min and Max" src="https://codepen.io/IMD/embed/poqEreV?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/poqEreV">
  HTML Forms - Min and Max</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

`step` attribute is used to define the step in which the number should increment. Mainly used with the number and range fields.
```HTML
<form action="thanks.html" method="post">
  <label for="quantity">Quantity</label>
  <input id="quantity" type="number" name="quantity" min="2" max="10" step="2">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Step" src="https://codepen.io/IMD/embed/yLGaoME?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/yLGaoME">
  HTML Forms - Step</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Textarea
A larger area for multi-line text input, these are very common with varied content updates. Posts, tweets, etc.
- Textarea is a paired tag
- We add a label to textarea the same way as an input
- We require the `name` attribute for the data processing on submission

```HTML
<form action="thanks.html" method="post">
  <label for="message">Your Message</label>
  <textarea id="message"></textarea>
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Textarea" src="https://codepen.io/IMD/embed/XWojaMo?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/XWojaMo">
  HTML Forms - Textarea</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Select
A group of elements organized in a drop-down container. Built-in accessibility controls to expand and select options. A select menu is the best way to organize a large list of selections like countries, states or provinces.

- Select is a paired tag
- Each dropdown option is added in its own `<option></option>` tag
- Each option must have the `value` attribute which will be sent as the data when the option is selected
- We add a label to select for accessibility
- We require the `name` attribute for the data processing on submission

```html
<form action="thanks.html" method="post">
  <label for="rock">Choose your Rock</label>
  <select id="rock" name="rock">
    <option value="mars">Mars</option>
    <option value="earth">Earth</option>
    <option value="venus">Venus</option>
  </select>
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Select" src="https://codepen.io/IMD/embed/mdarMmE?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/mdarMmE">
  HTML Forms - Select</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

> #### Selected Attribute
> We can add the `selected` attribute to any option that we want to be pre-selected when the form loads.

## Checkboxes
A small multi-selection grouping. More than one selection can apply.
- Checkbox is a `type` of input element
- Each `checkbox` input field must have its own `label`
- Each `checkbox` must have its own `name` attribute vale
```html
<h3>What music you like?</h3>
<form action="thanks.html" method="post">
  <label for="pop">Pop</label>
  <input type="checkbox" id="pop" name="pop">
  
  <label for="classic">Classic</label>
  <input type="checkbox" id="classic" name="classic">

  <label for="prog">Progressive</label>
  <input type="checkbox" id="prog" name="prog" checked>
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Checkboxes" src="https://codepen.io/IMD/embed/MWZjvEP?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/MWZjvEP">
  HTML Forms - Checkboxes</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

> #### Checked Attribute
> We can add the `checked` attribute to any checkbox type input that we want to be pre-checked when the form loads.

## Radio Buttons
A single choice in a grouping of elements. Commonly used for toggles, only one radio option can be selected for each grouping.
- Radiobutton is a `type` of input element
- Each `radio` input field must have its own `label`
- All `radio` input fields **must have the same** `name` attribute value
- Each `radio` input must have a unique `value` attribute, which will be sent as a form is submitted

```html
<h3>How many hours you listen to music?</h3>
<form action="thanks.html" method="post">
  <label for="little">0-1</label>
  <input type="radio" id="little" name="musictime" value="0-1">
  <label for="some">2-3</label>
  <input type="radio" id="some" name="musictime" value="2-3" checked>
  <label for="alot">4-5</label>
  <input type="radio" id="alot" name="musictime" value="4-5">
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Radio buttons" src="https://codepen.io/IMD/embed/qBLaXVB?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/qBLaXVB">
  HTML Forms - Radio buttons</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

> #### Checked Attribute
> We can add the `checked` attribute to any radio type input that we want to be pre-checked when the form loads.

## Button
Buttons are used to allow the users to submit the form. The `type` attribute is added to the button to define its action. 
```html
<form action="thanks.html" method="post">
  <label for="fullname">Full Name</label>
  <input type="text" id="fullname" name="fullname" required>
  <button type="submit">Send</button>
</form>
```
<iframe height="300" style="width: 100%;" scrolling="no" title="HTML Forms - Button" src="https://codepen.io/IMD/embed/NWeRvwX?theme-id=47863&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/IMD/pen/NWeRvwX">
  HTML Forms - Button</a> by IMD (<a href="https://codepen.io/IMD">@IMD</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Full Example
<iframe height="265" style="width: 100%;" scrolling="no" title="YWKXLW" src="//codepen.io/IMD/embed/YWKXLW/?height=265&theme-id=47863&default-tab=html,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/IMD/pen/YWKXLW/'>YWKXLW</a> by IMD
  (<a href='https://codepen.io/IMD'>@IMD</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## Form submission
For having the form functional and submitting the information we need a server to receive and process the information.

We are creating a static website with HTML and CSS and do not have backend or server-side technology such as PHP to make our form functional we can use a third-party service, mainly for sending emails.

The process these services use is as follows:

- You create a form, that points to their service. Using the `action` attribute
- The user submits the form.
- The data is sent to the service’s website.
- The service composes an email and sends it to you.
- The service redirects the user back to your website to display a message.
- The services work well for simple information collection but aren’t great for complex registration forms, etc.

### Form services

- [Formspree](https://formspree.io/)
- [Woofoo](https://www.wufoo.com/)
- [JotForms](https://www.jotform.com/)