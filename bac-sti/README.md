bac-sti

Sure! CSS transitions and animations are powerful tools for adding movement and interactivity to your web designs. Here's a brief overview of how to use both:

### CSS Transitions:

CSS transitions allow you to change property values smoothly (over a specified duration) when they are triggered by events such as hover, focus, or page load. Here's a basic example:

```css
/* Define the initial state of the element */
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  transition: width 0.5s ease-in-out;
}

/* Define the new state on hover */
.box:hover {
  width: 200px;
}
```

In this example, when you hover over the `.box` element, its width will transition from 100px to 200px smoothly over a duration of 0.5 seconds with an ease-in-out timing function.

### CSS Animations:

CSS animations offer more control over the timing and sequence of changes to an element's properties. You define keyframes that describe the style changes at various points during the animation. Here's an example:

```css
/* Define the animation */
@keyframes slidein {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

/* Apply the animation to an element */
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  animation: slidein 1s ease-in-out;
}
```

In this example, the `.box` element will slide in from the left (`translateX(-100%)` to `translateX(0)`) over a duration of 1 second with an ease-in-out timing function.

### Combining Transitions and Animations:

You can also combine transitions and animations for more complex effects. For instance, you can use transitions for simple property changes triggered by events, and animations for more elaborate, timed sequences of changes.

```css
.box {
  width: 100px;
  height: 100px;
  background-color: red;
  transition: width 0.5s ease-in-out;
}

.box:hover {
  width: 200px;
  animation: pulse 2s infinite alternate;
}

@keyframes pulse {
  from {
    transform: scale(1);
  }
  to {
    transform: scale(1.2);
  }
}
```

In this example, when you hover over the `.box` element, its width will transition smoothly from 100px to 200px over 0.5 seconds, and it will also pulse with a scale animation over 2 seconds infinitely.
