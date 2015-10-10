## Workshop 3: JQuery

#### What is JQuery and why do I need it?

* JQuery is a Javascript Library that makes writing Javascript a lot easier
* The following is a comparison of a function written in Javascript to hide an element and another function to do the same thing in JQuery

###### Javascript
'''
function() hideOnClick(element) {
	if(element.style.visibility == "hidden") {
		element.style.visibility = "visible";
	} else {
		element.style.visibility = "hidden";
	}
}

...

<p id="some_text" onclick="hideOnClick(this)"> ... </p>

'''

###### JQuery

'''
$("#some_text").on("click", function() {
	$("#some_text").toggle();
})

'''