# Document Object Model (DOM)

## Viewing DOM

Browser (any page)
* Right-click 
  - Inspect
    - Console
      > clear() <br>
      > document   // Can see the DOM <br>
      > console.dir(document)  // Can see as Java Script objects - properties and their values
    
## How to grab the objects in DOM?

- Grabbing large groups of elements (eg. head, body)
- Grabbing specific HTML elements (eg. id, class)

### Important document attributes

> document.URL
> document.body
> document.head
> document.links

### Methods for grabbing elements of DOM
> document.getElementById() - Returns the element with the id <br>
> document.getElementByClassName() - Returns the list of all elements belonging to a class <br>
> document.getElementsByTagName() - Returns the list of all elements with the tag <br>
> document.querySelector() - returns the first object matching the CSS style selector <br>
> document.querySelectorAll() - returns all object matching the CSS style selector <br>

Note: For querySelector() and querySelectorAll() you have to give # for id selector (#myid), . for class selector (.myclass).

## How to interact and affect DOM objects using JS?

> var myheader = document.querySelector("h1") <br>
> myheader <br>
> myheader.style.color = 'red'


### Random color changer in JS

```html
function getRandomColor() {
  var letters = "0123456789ABCDEF";
  var color = "#";
  for (var i=0; i<6; i++) {
    color += letters[Math.floor(Math.random()*16)];
  }
  return color;
}

function changeHeaderColor() {
  colorInput = getRandomColor();
  header.style.color = colorInput;  
}

// Now perform the action over intervals (milliseconds)
setInterval("changeHeaderColor()",500)
```

## Changing Text, HTML content and Attributes with DOM

> myvar.textContent - This returns the text <br>
> myvar.innerHTML - This returns the actual HTML <br>
> myvar.getAttribute() - Returns the original attributed <br>
> myvar.setAttribute() - Allows to set an attribute

// special refers to an id for an element. You have to refer to html to know this

> var special = document.querySelector("#special") <br>
> special  // Returns the html element with special id <br>
> var specialA = special.querySelector("a") <br>
> specialA  // Returns the html element with anchor tag <br>
> specialA.getAttribute("href") <br>
> specialA.setAttribute("href", "https://www.amazon.com")

```


