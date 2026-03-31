# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="Alpha Celestine J. Jimenez" />
  <meta name="revised" content="March 27, 2026" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

**ANSWER:** 
In the default static positioning, the sidebar is fixed against the edge. But when you apply relative positioning, it moves a small distance from the header and the edge. There will be spacing between the sidebar from the header and the left edge. 

However, when we change **top** and **left** to **bottom** and **right**, the opposite happens. The sidebar will be very sticked to the header and edge to the point that it's overlapping them. 

__TOP__: When given smaller pixel values, the sidebar moves UPWARD. 

__LEFT__: When given smaller pixel values, the sidebar would move LEFT.



### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

**ANSWER**:
When we scroll the page, the footer scrolls along with it. The footer behaves differently from position relative since fixed makes it adjust to the user. While relative makes the footer position itself in the webpage, fixed makes it position with respect to the computer.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

**ANSWER**:
The absolute position makes elements adjust to the ENTIRE webpage. It will move the elements to occupy different spaces of the webpage, so that the size of the webpage is maximized and not just in one portion. 

Absolute is different from fixed as it only stayes in one place for the webpage, whereas fixed moves with respect to the computer. 

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?

**ANSWER:** 
Notice appears on top of the content because of its z-index being **greater** than that of content. When the z-index values are swapped, the layers change. 

__Z-index value 2__: The element will be on top 

__Z-index value 1__: The element will be at the bottom
- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    **ANSWER:**
    The different position values determine how an element sits on the page and how it reacts to other elements. 

    __Static__: The default. Elements will follow the normal flow of the page and stay where they are put in the HTML. 

    __Relative__: Element stays in normal flow, but you can move it using top/bottom/right/left without affecting the elements around it. 

    __Absolute__: Element is removed from the normal flow. It positions itself relative to the whole page and other elements act like it's not there. 

    __Fixed__: Element is stayed stuck to your browser window. 

    b. How does absolute positioning depend on its parent element?

    **ANSWER:**
    Absolute positioning looks for a parent. If a parent element has a position of ``relative``, ``absolute``, or ``fixed``, the child element will stay inside that parent's boundaries when you give it coordinates. 

    If no parents are there, the element will just use the entire webpage as its reference point. 

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    While both can stay visible when scrolling, they behave differently depending on the scroll position. 

    __Fixed__: It is always stuck to the screen from the very start. It doesn't care about its containers and stays in the same spot no matter where you are on the page. 

    __Sticky__: It acts like relative positioning until you scroll past it. Once it hits a certain point (like the top of the screen), it sticks there, but only within its parent container. Once you scroll past that parent container, the element disappears with it. 


    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    **ANSWER:**
    Positioning helps make sure the most important details don't get lost as the user explores the site. 

    __Example 1 (Fixed)__: I would use the fixed position for a "Register Now" button at the bottom of the screen so students can sign up instantly no matter how far down they scroll. 

    __Example 2 (Absolute)__: I would use the absolute postion to place a "sold Out" or "New" badge diagonally over the corner of an event poster image to catch the eye. 

<<<<<<< HEAD
    __Example 3 (Sticky)__: I would use the sticky position for event schedule headers (like "Day 1" or "Day 2" so they stay at the top of the screen while the user reads through the activities for that specific day. 
=======
    __Example 3 (Sticky)__: I would use the sticky position for event schedule headers (like "Day 1" or "Day 2" so they stay at the top of the screen while the user reads through the activities for that specific day. 
>>>>>>> e4eb921f9ce10d5e2c9cccdf6aaa9d618b3d5d9b
