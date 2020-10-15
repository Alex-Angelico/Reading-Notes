# Reading 14: CSS Transforms, Transitions, and Animations

## Transforms

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}

The transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.

Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis.

### Combining Transforms

It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. In this event multiple transforms can be combined together. To combine transforms, list the transform values within the transform property one after the other without the use of commas.

Using multiple transform declarations will not work, as each declaration will overwrite the one above it. The behavior in that case would be the same as if you were to set the height of an element numerous times.

## Transitions & Animations

Animations within CSS allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes. For a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover, :focus, :active,` and `:target` pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, and the first three are the most popular.

### Transitional Property

The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions. If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint.

## Simple, Wow-Worthy CSS Transitions

- **Fade (`.fade, .fade:hover`):** Use this class rule with two different values of `opacity`
- **Change Color (`.color:hover`):** Set a color value for `background`
- **Grow & Shrink (`.grow:hover, .shrink:hover`):** Apply the same decimal value to `-webkit-transform`, `-ms-transform`, and `transform` to either the grow or shrink rule, depending on if the value is greater or less than 1
- **Rotate (`.rotate:hover`):** Give `-webkit-transform`, `-ms-transform`, and `transform` all the same value in degrees
- **Square-to-Circle (`.circle:hover`):** This simply uses a high `border-radius` value to make the change from square to circle
- **3D Shadow (`.threed:hover`):** Add `box-shadow` with three values stacked on consecutive lines in the format `1px 1px [color], 2px 2px [color], 3px 3px [color];` then `-webkit-transform` and `transform` with a value of `translate(positive or negative pixel value)`
- **Swing (`.swing:hover`):** Because it is dependent on actual animation, this transition is acutally quite complex
- **Inset Border (`.border:hover`):** By giving a rule a `box-shadow` property with a value in the format `inset 0 0 0 [pixel width] [color value]`, the effect of a border growing within an image is created
