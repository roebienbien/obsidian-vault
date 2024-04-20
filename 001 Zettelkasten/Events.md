2023-12-04 16:36

Status: #idea

Tags: 

# Events
Events are actions when a user interacts with the page - like clicking an element, typing in a field, or loading a page.

## Event Object


## What is "Event Handling"?
Event Handling is the process where the browsers detects a change and alerts a function (event handler) that is listening to a particular event. these function/s then perform the actions as desired.

Example of `click` event handler:


```jsx
//index.html
<div class="buttons">
  <button>Press 1</button>
  <button>Press 2</button>
  <button>Press 3</button>
</div>
```

```js
//index.js
function initializeButtonEvent() {
  //Select the container that holds the buttons
  const buttonContainer = document.querySelector('.buttons');
  console.log('buttonContainer', buttonContainer);

  //add event listener for when the button is clicked
  buttonContainer.addEventListener('click', function (event) {
	// check if the clicked element is a button
    if (event.target.tagName === 'BUTTON') {
      console.log('Button Pressed:', event.target.textContent);
    }
  });
}
// call the initilizeButtonEvent function when the DOM content is fully loaded
document.addEventListener('DOMContentLoaded', initializeButtonEvent);
```

## Different Types of Events
An event can be triggered any time a user interacts with the page. These events could be a user scrolling through the page, clicking on an item, or loading a page.
Here are some common events: 
```
onclick mousedown onblur onfocus onload onscroll
```

# References
