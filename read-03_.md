# Reading Assignment - 03

## Mustache

 Mustache is a template syntax used in a wide array of projects. It is commonly referred to 
 as "logic-less" since there are no if/else statements or for loops required. The syntax
 uses tags that can pass values to be displayed in HTML. 

 ```  
 Mustache.render("Hello, {{name}}, {name: "Leaundrae});
 //returns: Hello, Sherlynn
 ```
 The values we input are placeholders that Mustache uses to find the associated value. The placeholder
 in the example above is name that references the value "Leaundrae". 

## Flexbox

- `display: flex ` - Defines a flex container and enables a flex context for all its direct children.
- `flex-direction` - Establishes the main-axis and defines the direction flex items are placed in the flex container.
- `order` - Controls the order in which they appear in the flex container
- `flex-grow` - Defines the ability for a flex item to grow if necessary. The value accepted serves as a proportion. If all items have `flex-grow` set to 1, the remaining space in the container will be distributed equally to all children. If one of the children has a value of 2, the remaining space would take up twice as much space as the others.
- `flex-wrap` - By default, flex items try to fit onto one line. `flex-wrap` allows the items to wrap as needed.
    - `nowrap` - This default parameter places all flex items on a single line.
    - `wrap` - Allows flex items to wrap onto multiple lines
    - `wrap-reverse` - Allows items to wrap onto multiple lines in reverse
- `flex-grow` - Defines the ability for flex items to grow. It accepts a unitless value that serves as a proportion. If all items have `flex-grow` set to 1, the remaining space in the ocntainer will be distributed equally to all children. If one of the children as a value of 2,the remaining space would take up twice as much space.
- `flex-shrink` - Allows the flex item to shrink by passing in a positive number.
- `flex-basis` - Defines the default size of an element before the remaining space is distributed. The 
- `auto` keyword means uses the items current height and width values. The `content` keyword sizes the item based on its content. 
- `flex-flow` - Shorthand for `flex-direction` and `flex-wrap` defining the container's main and cross axis. Its default value is `row nowrap`.
- `flex` - Shorthand for `flex-grow`, `flex-shrink` and `flex-basis` combined. Using the propery instead of the individual parameters will set the other values intelligently. 
- `align-self` - Allows the default alignment to be overridden for individual flex items. 
- `justify-content` - Defines the alignment along the main axis and helps to distribute extra free space.
    - `flex-start` - This default option packs items toward the start of the flex-direction
    - `flex-end` - Packs items toward the end of the flex-direction
    - `start` - Packs items toward the start of the `writing-mode` direction
    - `end`- Packs items toward the end of the `writing-mode` direction
    - `left` - Packs items toward the left edge of the container
    - `right` - Packs items toward the right edge of the container
    - `center` - Centers items along the line
    - `space-between` - Evenly distributes items on the line
    - `space-around` - Distributes items so the spacing between any two items is equal
- `align-items` - Unlike `justify-content` which defines the alignment on the main axit, `align-items` defines how flex items are laid out along the cross axis. 
    - `stretch` - Stretches items to fill the container with respect to min-width and max-width
    - `flex-start`/`start`/ `self-start` - Places items at the start of the cross axis
    - `flex-end`/`end`/ `self-end` - Places items at the end of the cross axis
    - `center` - Centers items on the cross-axis
    - `baseline` - Items are aligned to reflect their baselines 
- `align-content` - Similar to `justify-content`, this property aligns a flex containers lines within when there is extra space.


## Sources:
 [Sherylynn Tan](https://1sherlynn.medium.com/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)
 
 [Chris Coyier](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
