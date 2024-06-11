<h1>Tea Cozy - Codecademy HTML/CSS project</h1>

<h2>Planning phase</h2>
    
    Looking at the Redline design specifications, I was wondering if it would be best to use a Reset.css stylesheet or something else. After doing some research, reading up on other developers' opinions and recommendations regarding resets as well as normalize.css, I've come to the conclusion that it would probably be best to use a normalize.css sheet. My reasoning is that, since the design specs specify h1-h6 header stylings for various paragraphs and headers, I would have to recreate the stylings by eye, if I decided to reset all of the stylings, as a reset will have all the headers be looking exactly the same.

    Other than that, I don't think there's all that much extra to this one. Since I've started getting more comfortable using flexboxes, and this is a fairly simple layout, I'm going to use flexboxes as much as seems logical.

    If you want to have a look at the specsheet, then simply open "img-tea-cozy-redline.jpg" in the root folder.


<h2>Creating the Header/Navbar</h2>

    So, my plan for this one was pretty simple: I wanted to use a flexbox to nest the logo and the navbar list items in. Then I'd apply a "justify-content: space-between" to push the two containers out to either end of the header, pushing up against the 10px side padding. This worked fine. 

    I had to play around with the settings a bit, until I got the Tea Cozy logo to resize itself to fit the parent container. I'd assumed that it would automatically resize as it was a flex-item, but it didn't and so I set it as its own flex-container as well, which fixed the problem.

    I used the flex-grow property to adjust how much space the respective containers took up, to ensure that the navbar list didn't try to take up more space than the design specs indicated. I ended up with a 1-3 flex ratio between the logo and navbar containers. 

    The rest of the work consisted of me adjusting the settings to achieve the desired result. Of note was me having an issue where the header kept pushing itself down from the top of the page, equal to the amount that I'd pushed the Main section down the page, to prevent the fixed header from overlapping everything else, when at the top of the page. I couldn't figure out why it was doing this, but I fixed it by setting its position to "top: 0;", to fix it to the top of the page.

- Overall I'm fairly happy with how the work on the header went. I'm still not quick at coding in CSS at all, but every new project is an opportunity to learn and get better and faster. I'm happy that all of my initial HTML structure didn't need to be changed, other than me deciding to make the navbar into actual links to the various sections on the page + making the logo a link to get to the top of the page. I had to refresh how to do this, but in doing so, I was also pleased to see that my structuring of the page in HTML meant, that it was very simple to do.


<h2>Creating the Our Mission Section</h2>
