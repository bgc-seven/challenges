## Center the world
 
The app is really coming along. What would make it better if it was centered in the middle of the page

Let's use flexbox to move our items around.Go ahead and add the following lines of code to your style element

```
body {
  display: flex;
}
```

Let's take a look at the result....wait a minute why are my elements side by side. By default flexbox aligns elements side by side instead of one on top of the other.
Let's change that.

Under ```display: flex``` Add the following line of code

```
flex-flow: column nowrap;
```

Ok so now we're back where we started.

## Challenge

- First take a look at the property [justify-content](https://css-tricks.com/almanac/properties/j/justify-content/)
  Also take a look at [align-items](https://css-tricks.com/almanac/properties/a/align-items/)
  
1. Center the items on your webpage
2. Play around with the different properties justify-content and align-items
