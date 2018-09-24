# jQuery Interview Questions
1. What differencies between .on('click') and .click() calls?
Answer:
- click() is applied for the specified element, e.g. $('button.alert').click(function() {})
- .on('click') can be used as $('div#container').on('click', 'button.alert', function() {}).
So we just need a single handler for all elements that match your selector, including ones created dynamically.

2. What is `data-*` HTML attribute in jQuery project?
Answer:
- `data-*` attributes in jQuery project is used to easily getting the data by jQuery function `.date(key)` or 
it is a result when we use `.data(key, value)` to set the data from JS to HTML via a selector.

3. Explain what the following code will do:
```
$( "div#first, div.first, ol#items > [name$='first']" )```

Answer:
This code performs a query to retrieve any `<div>` element with the id first, plus all `<div>` elements with the class `first`, plus all elements which are children of the `<ol id="items">` element and whose name attribute ends with the string "first". This is an example of using multiple selectors at once. The function will return a jQuery object containing the results of the query.

4. The code below is for an application that requires defining a click handler for all buttons on the page, including those buttons that may be added later dynamically.

What is wrong with this code, and how can it be fixed to work properly even with buttons that are added later dynamically?
```
// define the click handler for all buttons
$( "button" ).bind( "click", function() {
    alert( "Button Clicked!" )
});

/* ... some time later ... */

// dynamically add another button to the page
$( "html" ).append( "<button>Click Alert!</button>" );```

Answer:
The correct code should be:
```
// define the click handler for all buttons
$( document ).on( "click", "button", function() {
    alert( "Button Clicked!" )
});

/* ... some time later ... */

// dynamically add another button to the page
$( "html" ).append( "<button>Click Alert!</button>" );```

5. Explain what the following code does:
```
$( "div" ).css( "width", "300px" ).add( "p" ).css( "background-color", "blue" );```

Answer:
This code uses method chaining to accomplish a couple of things. First, it selects all the <div> elements and changes their CSS width to 300px. Then, it adds all the <p> elements to the current selection, so it can finally change the CSS background color for both the <div> and <p> elements to blue.

6. What’s the difference between document.ready() and window.onload()?
Answer:
The document.ready() event occurs when all HTML documents have been loaded, but window.onload() occurs when all content (including images) has been loaded. So generally the document.ready() event fires first.





