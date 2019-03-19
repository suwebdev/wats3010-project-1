# Project 1: Travel Blog  

## HTML  
1. Create files: index.html and css/style.css.  Use VS code to generate default html in the index.html file (hint: use !<tab> in VS Code.).  Link CSS file into the html.  Add a meta tag to specify you as the author `<meta name="author" content="<your name">`

2. You can find all content in the files located in the content directory.  Enter the title of the web pages into the titles tag in the head element.

3. Code the semantic html to provide document structure:
  header
  nav
  figure
  main
  ---- section
  ---- section
  footer

4. Add head tags to the `header` element and supply the title and subtitle
5. Add 2 div tags within the `nav` element. Add an unordered list tag (`ul`) inside each of the div elements. The list on the left should contain list items (`li`) with content and links (`a`) to "Home", "Recent Blogs", and "About".  These will be linked to internal links. The list items on the right should contain links to "Twitter", "Facebook" and "Github" and will be external links.
6. The figure element should contain and image (`img`) and a caption (`figcaption`).  The image source is "images/backlit-clouds-dark-831x200.jpg" and the caption is in the titles-captions.txt file.  
7. The Recent Blogs section will use a CSS Table layout using 1 row and 3 columns. First add a head tag with the word "Recent Blogs" to desribe the section. Add a div tag for the row and 3 child divs within the row to represent the 3 columns. Within each column add an image (`img`) and a paragraph (`p`).  The images can be found in the images directory and the content for paragraphs in the recent-blogs.txt file.  The order of the images is : "hudson-river..", "fort-point...", "prince-william...".
8. The About section will use a CSS Table layout using 1 row and 2 columns.  First add the a head tag with the word "About" to desribe the section.  Add a div tag for the row and and 2 child divs within the fow to represent the 2 coluns.  Within each column add an head tag with and a paragraph.  The head tags should contain the words "News" and "About".  The content for the news and about paragraphs are in the correpsonding content directory files.
9. Within the div tag representingn the column for "About" place a div tag that will by styled to be a call to action (CTA) area with a child button element and make it's content "Click to find out more".
10. In the footer section add 2 div tags to represent the left and right contents of the footer. The contents of the left should contain the copyright information `Copyright &copy; 2019-20` and the contents on the right should contain your name.
11. Internal Page Links: In order to support internal navigation add id attributes to head tag for the "recent blogs" section and the head tag for the "about" section.  Then use these id's in the page links section of the nav element by assigning the `#<id>` to the `href`.  You can leave the home link `href` empty to cause the page to refer to the start of the document. Test this out by clicking on these links.

## CSS
1. Normalize the styles (overrided default browser styles)
  - set body height to 100%
  - use the `*` selector and set box sizing to border box
  - set margin and padding to 0, line-height to 1.2 rem and text transform to uppercase on all `head` tags
  - set `ul` margin and padding to 0
  - set `main` margin top and bottom to 0 and left and right to 20px
  - set `p` padding top and bottom to 0 and left and right to 5px
2. Typography
  - set `h1` and `h2` font family to `Arial, Helvetica, sans-serif`
  - set `h1` and `h2` margin to 0
  - set `h1` font size to 3rem
  - set `h2` font size to 1rem 
  - set `h2` letter spacing to .2rem
  - set `h2` padding top to 0, right to 10px, bottom to 15px, and right to 10px
  - set `nav`, `div`, `a`, `figcaption` and `span` tages to font family `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`
3. Page Links
  - create a class called `page-links` and assign it to the `ul` that contains the navigation internal links. The `ul` overflow should be set to hidden to release the float after the element. Following the pattern establish in ** Skills 1-4 Layout Horizonal ** assignment, float the list items to the left, remove bullet points and give them a background color of `#333`. Make the `a` tags block and the text white. Align the text to the center, remove the underline from the link (`text-decoration:none`) and adding top and side padding.  On hover of the link set the backgorund color to gray and the text color to white. When the link is `active` set the background color to black and the text color to white.
4. Social links
  - create a class called `social-links` and assign it to the `ul` that contains the social linnks.  Use `display:inline-block` on the list items `li` to cause them to layout horizontally following a patter in the ** Skills 1-4 Layout Horizonal ** assignment.  Set list style type to none to remove bullet points and then set height and line-height in the `ul` to 48px, so that the text will center vertically.  The list items should all be equal in width (`5rem`) with a background color of `#ffbf00` and centered text alignment.  The social links `a` tags should have black text and remove the default underline with `text-decoration: none`.  On hovering the `a`'s the text should be white and hovering the `li`'s the text should be gray.
5. Positioning the Page Links and Social links to appear on the same line in the nav
  - use `position:relative` on the `nav` in order to apply absolute positioning on the children (page links and social links) See the ** Skills 1-4 Layout Horizontal ** assignment where the footer used absolute positioning to move contents to left and right for example
  - the nav should be 48px with a black background
  - assigne the `div` that contains the page links a class of `nav-left` and the `div` that contains the social links should be given a class of `nav-right`
  - apply `position: absolute` to both `nav-left` and `nav-right`
  - `nav-left` will be positioned at `right:0, top:0` and `nav-right` will be positioned at `left:0, top:0`
6. Big Image Figure: set the margin to 0 on the figure and set the width to 100% and height to auto. This ensures that the image covers the full width of the page no matter how big the window is.
7. Table layouts are used for both the Recent Blogs and About sections.  The table layout will be controlled by the number of rows and columns as well as the amount of content.
  - create a table class and assign it to sections containing **Recent Blogs** and **About**.  Create a table class selector in the style sheet and give it the following properties and values:

  ```
  {
    display: table;
    height: 100%;
    width: 100%;
    table-layout: fixed;
    border-collapse: separate;
    border-spacing: 10px;
  }
  ```

- create a row class and assign it to the divs that are direct children of the section elements and give them the rows the following style  

```
.row {
    display: table-row;
 }
```

- create a `col` class and add the `col` class to any `div`'s that are children of the `row` class and then style the cols and `p` children with the following
 
 ```
.col {
        display: table-cell;
        border: 1px solid lightgray;
        border-radius: 10px;
    }

    .col p {
        font-size: 1rem;
    }
 ```
8. Float the text in the **Recent Blogs** section around the images by adding a `wrapped` class to the images and set them to `display:block` and `float:left`.  Add 5px padding.
  
9. Call to action button styling 
  - assign a `cta` class to the div around the button and give it a width of `11rem`, `margin:auto` and center align the text
  - assign a `cta-button` class to the button and make it a block element with a heigth of `40px`, a line height of `40px`, a red backgound, white text and `border-radius` of `30px`
10. Footer
  - provide a background color of #333, height of 4rem and text color white
  - give it a padding of 20 and position relative with a width of 100%
  - create a `footer-left` and `footer-right` class and assign them to the 2 `div`'s nested in the `footer`
  - set absolute position for both `footer-right` and `footer-left`
  - set a property of `left: 0.50%` on `footer-left`
  - set a property of `right: 0.50%` on `footer-right`

## Test 
Bring up your page and test it 
