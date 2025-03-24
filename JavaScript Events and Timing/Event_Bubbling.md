---- bubbling ----

Event Bubbling is a concept in the javascript where the inner child element is clicked so its outer parents also gets clicked or we can say an event that is triggered on a child element 
will "bubble up" to its parent elements.

complete example of the bubbling
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Event Bubbling Example</title>
</head>
<body>
  <div id="parent">
    <button id="child">Click me!</button>
  </div>

  <script>
    // Adding event listener to the child element
    const child = document.getElementById('child');
    child.addEventListener('click', function() {
      alert('Child button clicked!');
    });

    // Adding event listener to the parent element
    const parent = document.getElementById('parent');
    parent.addEventListener('click', function() {
      alert('Parent div clicked!');
    });
  </script>
</body>
</html>


```

so here in this example you will see the bubbling , means when we will click on the button child then its parent wil also get trigger
Why is it useful?
Event bubbling allows you to attach fewer event listeners to parent elements rather than each individual child. This is known as event 
delegation and is useful when you have many child elements and want to handle events for all of them using a single listener on a parent.

We can stop the bubbling too, if we want
if we want to prevent the parent from being clicked when click on the child then we can do this, event.stopPropagation() method

```
child.addEventListener('click', function(event) {
  alert('Child button clicked!');
  event.stopPropagation(); // Prevents the event from bubbling up to the parent
});

```
