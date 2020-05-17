# CodecademyHtml
*//
HTML Syntax 
-HMTL is composed of elements
-elements are made up of an opening tag, content, and a closing tag 
  -tags are surrounded by <>
  -example of an element: <p> Hello World! </p>
  
  
  The Body 
  -only content inside the body element is displayed on the screen
  -text, images, and buttons can be added to the body 
  
  <body>
      <p> This is an example </p>
  </body>
  
  
  Structure
  -HTML is organized as a collection of family tree relationships 
  -when an element is contained inside another element, it is considered the child of that element and is nested inside the parent 
  -child elements can inherit behavior and styling from their parent element 
  
  Headings
  -there are six different headings, <h1> through <h6>
  
  Div 
  -<div> is a container that divides the page into sections 
  -<div>s can contain text or any other HTML element 
  
  
  Attributes 
  -attributes are added to the opening tag of an element and can be used to provide information or styling 
  -attributes consist of a name and a value 
    -one commonly used attribute is id, which can be used to specify different content
    -ex: 
      <div id="intro">
         <h1> Introduction </h1>
      </div>
      
 Displaying Text 
 -paragraphs <p> contain a block of plain text 
 -<span> contains short pieces of text or other HTML, they're used to separate small pieces of content that are on the same    line as other content 
  -it's best to use a span element when you want to target a specific piece of content that is inline (on the same line as other text) 
  
  
 Styling Text
 -<em> and <strong> are used for italics and bold respectively 
 -use <br> for line breaks (opening tag only) 
  
  Unordered Lists 
  -you can use the <ul> to create an unordered list of elements
  -the list must be made up of list elements ex: <li> books </li>
  -the items will be listed with bullet points 
  
  Ordered Lists 
  -ordered lists are the same as unordered lists except they are numbered instead of bulleted 
  -you can create an unordered list using the <ul> tag and add <li> elements to it 
  
  Images 
  -the <img> tag allows you to add images to a webpage 
  -it is a self closing tag 
  -it has a required attributed called the src, which is the image url 
  syntax: <img src="image-location.jpg" />
  -img has an optional tag called alt where you can add a description of the image - this is used for visually impaired people and if the webpage fails to load 
  
  
  Videos 
  syntax: 
  <video src="myVideo.mp4" width="320" height="240" controls>
  Video not supported
</video>

-src is the video file, which can be a video hosted alongside your webpage or a URL that points to a video hosted on another webpage 
-the height and width attributes are used to set the size of the video on the webpage
-controls instructs the browser to include the basic controls - play, pause, skip
-the text between the opening and closing tags is only displayed if the video can't load 

Setting up an html document
-always include <!DOCTYPE html> at the top of your document 
-add opening and closing <html> tags so that the computer interprets everything inside as html 
-you can add a head tag between the html tag and the body tag 
    -the head tag contains metadata about the page that isn't displayed directly 
    -the title of the webpage (inside the title tag) is included in the head 
  
Other Body Elements 
-you can add a link as an anchor element using <a>
  -the anchor element has a href attribute which is the url to link to
  -the target attribute specifies how the link should open 
  -for the link to open in a new tab, the target reference should be "_blank"
  -ex: <a href= "www.wikipedia.org"> This is a link to wikipedia </a>
  
  Linking to Relative Page
  when making multipage static website, developers store HTML files in the root directory. 
  HTML files are often stored in the same folder, so webpages can be linked together using relative path. 
  
  ex: <a href="./contact.html">Contact</a>
  -the href in this example is the contact.html file in the same folder 
  -the ./ tells html to look for the file in the same folder 
  
  -you can turn any element into a link by wrapping it with an anchor element 
  -ex: <a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/></a>
  -the image is now a link
  
 -in order to link to a target on the same page, give the target an id
    ex: <p id="top"> Top of the page </p>
 -the target link is a string containing # and then the target id
    ex: <p><a href= "#top"> Top </a></p>
    
 Comments
 -comments in html begin with <!-- and end with -->
 
 Tables 
 -make a table with <table>
 -add rows with <tr>
 -add data with <td> (placed within a row) 
 -add titles to rows and columns with <th> (placed within a row) 
    -the scope attribute is either row or col 
  
  ex: 
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

-data can span columns using the colspan attribute, which accepts an integer to denote the number of columns it spans across 
-the rowspan attribute is used to span across multiple rows 
-long tables can be sectioned off using the table body element <tbody>
   -the tbody element should contain all the table's data except the headings 
-table column headings are sectioned off in the <thead> element 
    -the table head still requires a row in order to contain the table headings
    -only the column headings go under the thead element 
-the bottom part of a table can be sectioned off with the <tfoot> element 
  -footers are often used to contain column sums and similar data 
  
  
Forms 
-computers use HTTP forms to communicate
-example of a form in HTML:
  <form action="./example.html" method = "POST"> </form>
  -the action attribute determines where the form is sent
  -the method attribute is a HTTP verb that is included in the HTTP request 
-form elements can also contain child elements with information such as a header or a paragraph 

Text Input 
-use the <input> element to get input from the user 
-the input element has a type attribute that determines how it renders on the webpage and what kind of data it accepts 
-the input element also needs a name attribute 

example:
<form action="/example.html" method="POST">
  <input type="text" name="first-text-field">
</form>

-this will display a text box that takes in user input 
-when the user types into the box, the value of input's value attribute becomes the text that the user entered 
-the value attributed is paired with the name attributed and sent when the form is submitted 
-in the example above, if the user typed in "important", the text "first-text-field=important" is sent to example.html
-you can also assigned a default value to the value attribute so that the text box is pre-filled 

Adding a Label 
-the label element has an opening and closing tag and displays text that is written between the tags
-to associate the label with an input, the input needs an id attribute 
-assign the id attribute of the input element with the for attribute of the label 

example: 
<form action="/example.html" method="POST">
  <label for="meal"> What do you want to eat? </label>
  <br>
  <input type="text" name="food" id="meal">
</form>

-for password input, use the input element's type attribute and set it to "password"
  -this will replace the input text with asterisks or dots for security 
-for number input, set the type to number 
  -you can also use the step attribute, which provides arrows inside the input field to increase or decrease the input by the value of the step attribute 
-to create a slider, use type=range
  -set the min and max values of the slider with the min and max attributes of input 
  -use step to adjust how much the slider slides 
  
 -create checkboxes with type=checkbox 
    -each input with type checkbox will have a value, but the value will not be displayed 
    -in a group of checkboxes, each input element has the same value for the name attribute (this is used to group them together) but each input has a unique id to pair it to a label 
    
-radio buttons work the same way as checkboxes except with type radio 

-use the select element to create a drop down menu
-add options with the option element 
  -the text rendered is the text included between the <option> tags, but the value of the value attribute is what is included in the form when it is submitted 
  
-when you have a lot of options and want to allow the users to search and type in their own input, use a datalist 
-the datalist element is used with an input element with type text 

example: 
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

-the <input> is associated to the <datalist> via the <input>‘s list attribute and the id of the <datalist>
-users can type in something to search for a particular option
-if they don't find the option they're looking for, they can still use what they typed in 
  -when the form is submitted, the value of the input's name and what the user typed in is sent as a pair 
  
Text area 
-the text area element is used to make a bigger text field that users can type in 
-you can add row and column attributes to determine how big the text field should be 
-if you want default text in the text area, include it in between the tags 

Submit button 
-to create a submit button, create an input element with type submit 
-the value assigned to the value attribute shows up on the button 
-if you don't include a value attribute, submit shows up on the button by default

*//
