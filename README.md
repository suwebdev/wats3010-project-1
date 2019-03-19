# Project 1: Travel Blog  

## HTML  
1. Create files: index.html and css/style.css.  Use VS code to generate default html in the index.html file (hint: use !<tab> in VS Code.).  Link CSS file into the html.  Add an `author` tag with your name in the head section.

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
9. Within the div tag representingn the column for "About" place a div tag that will by styled to be a call for action button and make it's content "Click to find out more".
10. In the footer section add 2 div tags to represent the left and right contents of the footer. The contents of the left should contain the copyright information `Copyright &copy; 2019-20` and the contents on the right should contain your name.

## CSS




The left div should contain a class indicating `nav-left` and the right div tag should contain a class indicating `