## STEP 1 
In the default static positioning, the sidebar is fixed against the edge. But when you apply positioning, it moves depending on the directions you want. 
**TOP**: When given smaller pixel values, the sidebar moves UPWARD. 
**LEFT**: When given smaller pixel values, the sidebar would move LEFT. 

## STEP 2 
You cannot scroll a page when the position is fixed. The footer behaves differently from position relative since we applied **fixed.** When the position is fixed, it immediately puts the footer at the bottom since fixed adjusts to the whole page. 

## STEP 3 
When an element is in absolute position, the element gets adjusted to the page (like fixed). However, fixed makes the element stay in one place. Absolute allows us to scroll the page with the element. 

## STEP 4
Notice appears on top of the screen because in the html file, it's written as *div* which makes it a divider for the webpage. When the z-indexes are switched (from 1 to 2 and vice versa), nothing happens and notice still stays on top.
