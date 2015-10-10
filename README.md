## Workshop 3: JQuery

#### What is JQuery and why do I need it?

* JQuery is a Javascript Library that makes writing Javascript a lot easier

The following is a comparison of a function written in Javascript to hide an element and another function to do the same thing in JQuery:

###### Javascript
```
function() hideOnClick(element) {
	if(element.style.visibility == "hidden") {
		element.style.visibility = "visible";
	} else {
		element.style.visibility = "hidden";
	}
}

...

<p id="some_text" onclick="hideOnClick(this)"> ... </p>

```

###### JQuery

```
$("#some_text").on("click", function() {
	$("#some_text").toggle();
})

```

#### Setting Up JQuery

* To set up JQuery, all you have to do is include the following line of code somewhere in the `<head>` tag before any other JQuery.

```<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>```

* This will tell your browser how to compile JQuery. If you're getting syntax errors or 'key not found' errors, make sure you have this before any other JQuery

#### Selectors

* Selectors allow you to choose an element on the page to do some work on.
* Selectors can be ids, classes, types of tags, or even the entire document.

###### Examples of selectors

```
$("#some_text") // This is will select an element with the id 'some_text'
$(".nav") // This will select every element in the class "nav"
$("p") // This will select every paragraph tag on the page
$(document) // We'll talk about this selector later

```

#### Events

* JQuery is centered around listening for events (i.e., when a button is clicked, when the mouse goes over something, etc). After these events happen, some work is done on an element
* Common events include:
	* click - fires when element has been clicked
	* dblclick - fires when element has been clicked twice
	* mouseenter - fires when mouse goes over an element
	* mouseleave - fires when mouse leaves an element
	* hover - fires when mouse goes over an element, then reverts when mouse leaves
	* focus - fires when an element has focus (i.e., input is being typed into)
	* blur - fires when an element loses focus

###### Examples of events

```

// Assigning click event to navbar class

$(".navbar").click(function() { 
	// code goes here
});

// Assigning hover event to the element with id "hover_here"
$("#hover_here").hover(function() {
	// code goes here
});

// Assigning focus event to all inputs
$("input").focus(function() {
	// code goes here
});

```

###### Special Events

* ready
	* This function can only be called after the document selector, this is the only time you'll use the $(document) selector
	* This event fires after the page has been loaded, which is useful if you want to do some work right at the beginning
* on
	* This function is how you assign multiple events to an element
	* This function can also be used to assign single events

```

// Doing work when the page loads

$(document).ready(function() {
	// code goes here
});

// Assigning click and hover functions to the id "header"

$("#header").on({
	"click": function() {
		// code for click goes here
	},
	"hover": function() {
		// code for hover goes here
	}
});

// Assigning just click function for "header" id

$("#header").on("click", function() {
	// code goes here
	// Notice that there are no brackets after .on
});

```