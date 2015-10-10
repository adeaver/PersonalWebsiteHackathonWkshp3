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