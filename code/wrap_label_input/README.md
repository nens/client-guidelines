[<-- Back to Main](./../../README.md)  
  
[[] Open index.html](./index.html)  

# scale + wrap label and input depending on width

<table>

<tr><td>
  Title
</td><td>
  scale + wrap label and input depending on width
</td></tr>

<tr><td>
  Problem
</td><td>
If the space to show 2 elements next to each other becomes to small,  
then they can often be shown beneath each other.  
This is called wrapping and can happen automaticly with CSS based on the available space.   
Below is an example using flexbox to scale a input + label.  
  
Some elements can both be small or big.  
They should simply take up the available space.  
Below this is done for a input element using flexbox.  
</td></tr>


<tr><td>
  tags
</td><td>
  flexbox, scale, wrap, responsive, input, label, small-screen, align
</td></tr>

<tr><td>
  description
</td><td>
  Flexbox wrap is used to make responsive.
  <ul>
    <li>
    Label will show on top of input on small screens
    </li>
    <li>
    Label will show left of input on bigger screens
    </li>
    <li>
    input field will grow to fill rest of screen
    </li>
    <li>
    Several input label pairs below each other will scale exactly aligned to each other 
    </li>
  </ul>
</td></tr>

<tr><td>
  Source
</td><td>
  <a href="https://webdesign.tutsplus.com/tutorials/building-responsive-forms-with-flexbox--cms-26767">https://webdesign.tutsplus.com/tutorials/building-responsive-forms-with-flexbox--cms-26767</a>
</td></tr>

<tr><td>
  Date
</td><td>
  2019-July-23
</td></tr>

<tr><td>
  Explaination
</td><td>
   The flexbox makes it easy for elements to wrap to a new line. it also makes it easy for elements to grow according to the page size
</td></tr>

<tr><td>
  Advantages
</td><td>
   This approach is not dependent on:
   <ul>
    <li>
      media queries
    </li>
    <li>
      complicated css containers.
    </li>
    <li>
      libraries like bootstrap
    </li>
    <li>
      tables
    </li>
   </ul>
</td></tr>

<tr><td>
  Disadvantage
</td><td>
   <ul>
    <li>
      no use of media queries may be disadvantage if this is explicitly required
    </li>
    <li>
      I (Tom) found the flexbox api personally very difficult. It is not clear when to use min-widt versus flex-basis etc. Also I find the flex short-hand very confusing.
    </li>
    <li>
      When using table element one could get some of the functionality without hardcoding the max-width of the label.
    </li>
   </ul>
</td></tr>

<tr><td>
  Alternatives
</td><td>
   <ul>
    <li>
      Libraries like bootstrap. They are not the standard and will outdate every 2 year.
    </li>
    <li>
      Tables probably lack all sort of functionality like wrapping and scollable body.
    </li>
    <li>
      grid. Not yet supported everywhere and might actually more complicated to do this with grid.
    </li>
    <li>
      media query selectors. Creates more code and will be dependent on screensize (as opposed to parent element size) to work.
    </li>
   </ul>
</td></tr>

<tr><td>
  Emerging technologies
</td><td>
   Grid is for now NOT supported everywere, but may do a good job for this as well.
</td></tr>

<tr><td>
  Relation to our own architecture
</td><td>
   For our new apps we use flexbos alot and are no longer using CSS libraries like bootstrap.  
   Therefore this seems a good fit.  
</td></tr>

</table>


# Discussion

For now the flex-basis of the label is hardcoded in order for both items in the row to scale the same.  
If flex-basis was not hardcoded then both labels would get a different width.  
When using table elements this is not needed.  
Tables align automaticly, but will not wrap or scroll.  

Instead of using min-width, fles-basis is used.  
The only reason (known by me) for this is that this simply works.  
I do not understand the logic behind this and or if this is a bug.  

I preferred writing out all flex properties instead of using the flex short-hand,   
because I feel the flex short-hand is confusing.  
Anyway, writing out all properties is confusing too.   
Maybe we should just use whatever works.  

I used CSS child selectors, but this might be done with simply adding classes as well.  
Maybe this could be explained in another article under CSS / Selectors.  







