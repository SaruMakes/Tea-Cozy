#Tea Cozy - Codecademy HTML/CSS project

##Planning phase
    
<p>Looking at the Redline design specifications, I was wondering if it would be best to use a Reset.css stylesheet or something else. After doing some research, reading up on other developers' opinions and recommendations regarding resets as well as normalize.css, I've come to the conclusion that it would probably be best to use a normalize.css sheet. My reasoning is that, since the design specs specify h1-h6 header stylings for various paragraphs and headers, I would have to recreate the stylings by eye, if I decided to reset all of the stylings, as a reset will have all the headers be looking exactly the same.</p>

Other than that, I don't think there's all that much extra to this one. Since I've started getting more comfortable using flexboxes, and this is a fairly simple layout, I'm going to use flexboxes as much as seems logical.

If you want to have a look at the specsheet, then simply open "img-tea-cozy-redline.jpg" in the root folder.


##Creating the Header/Navbar

So, my plan for this one was pretty simple: I wanted to use a flexbox to nest the logo and the navbar list items in. Then I'd apply a "justify-content: space-between" to push the two containers out to either end of the header, pushing up against the 10px side padding. This worked fine. 

I had to play around with the settings a bit, until I got the Tea Cozy logo to resize itself to fit the parent container. I'd assumed that it would automatically resize as it was a flex-item, but it didn't and so I set it as its own flex-container as well, which fixed the problem.

I used the flex-grow property to adjust how much space the respective containers took up, to ensure that the navbar list didn't try to take up more space than the design specs indicated. I ended up with a 1-3 flex ratio between the logo and navbar containers. 

The rest of the work consisted of me adjusting the settings to achieve the desired result. Of note was me having an issue where the header kept pushing itself down from the top of the page, equal to the amount that I'd pushed the Main section down the page, to prevent the fixed header from overlapping everything else, when at the top of the page. I couldn't figure out why it was doing this, but I fixed it by setting its position to "top: 0;", to fix it to the top of the page.

- Overall I'm fairly happy with how the work on the header went. I'm still not quick at coding in CSS at all, but every new project is an opportunity to learn and get better and faster. I'm happy that all of my initial HTML structure didn't need to be changed, other than me deciding to make the navbar into actual links to the various sections on the page + making the logo a link to get to the top of the page. I had to refresh how to do this, but in doing so, I was also pleased to see that my structuring of the page in HTML meant, that it was very simple to do.


##Creating the Our Mission Section

My plan for this section was basically to create a container for the full vertical section and have that span the entire page width. Then within this, I would have a container, which would have the background image in it, and the set width and height from the specs. Inside this, I would have a container, with both paragraphs nested inside it and stacked vertically. I got the main setup sorted very quickly and it worked as expected.
    
However, I spent the majority of the time simply trying to get the horizontal black container, to decrease in size vertically and to have less padding around the paragraphs. In the end, the only thing that seemed to make a difference, was for me to set the line-height to something smaller than the actual height of the text, to decrease this padding/margin around the lines. This only worked to some extent, but didn't fully solve the issue.

- I'm not super pleased with the point that I left the section in. It looks just fine, but it irks me when something isn't doing what I'd like it to do, and I also don't understand why this is. I tried to troubleshoot it and the dev tools suggest that maybe it's something in the normalization css, which is causing the issue. However, I couldn't see what would cause it, while also ignoring the specificity of my code. I might return to this issue, to see if I can figure out the cause, but for now I've decided to move on, so as to not spend too much time on this with greatly diminishing returns.

- (EDIT) After revisiting the section and looking at the code with fresh eyes, I realised that there must've been some margins applied to my headers (since the specs use headers heavily for styling purposes), but after zeroing the margins, things worked in a much more predictable manner.


##Creating the Tea of the Month section 

This was one of the sections that I was thinking might end up causing me the most trouble, due to my past experiences creating similar layouts. My idea for this section was to, once again, have a man section that stretched the entire page width. Inside of this, I nested the main content section with the fixed width (which does shrink responsively as needed). It was then that I realised that I needed a separate container for the headlines and the images (incl. captions), as each needed different kinds of styling. So I made the new div-wrappers and got to work on setting up the styling. 

The styling didn't act exactly the way I wanted it to, to begin with, but through some quick trial-and-error I fixed the issues I was having. Among these issues was the sizing of the images, with me having accidentally limited the image container (incl. caption) to the size of the image, which then covered the text. Once I realised the error, I got it looking correctly very quickly.

- This section went better than I feared. I feel like the troubleshooting and resolutions came more easily than before, and, while I did see the same odd line-spacing behavior from the past section again, it caused less of an issue this time. I also was able to figure out that it seems related to having the text content in flexbox(es). I'm still not sure how to fix it though.


##Creating the Locations section

This section was a really difficult one for me. I'd decided to still go with Flexbox as my solution for spacing the location textboxes, but as soon as I added the "Locations" above the top box, it broke my layout. It kept pushing the boxes down, leaving them no longer centered vertically.

I also found that in order to match the image in the spec sheet, the listed container height had to be adjusted, so the image is not accurate to what the specification states. I opted to recreate the design so that it matches visually, rather than matching the stated height in pixels exactly.

- In hindsight, and after having looked at the Codecademy forums, to see what others had been discussing regarding this particular part of the site, I've come to the conclusion that I should try to recreate the section without using Flexbox. The current placement of the heading is to have it be "position: absolute" and then manually set the spacing from the bottom of the page, which is anything but responsive design.

- (EDIT) I went back to having a go at this section again, and after some experimentation, it dawned on me that I could still use Flexboxes, I simply needed to split the section into three horizontal boxes. The center one contains the location textboxes, the top one contains only the header, and the bottom one is a carbon copy of the top box, but without any content in it. The top and bottom boxes/containers are the same height, so they keep the textboxes nicely centered vertically. Meanwhile, I can align the text inside the top box, without messing with the overall layout. I set the 15px margin both to the top and bottom of the middle container, to keep it centered, and zeroed the margins of the H2 header.


##Creating the "The Tea Cozy" contacts section and footer

These two sections were very simple and quick for me to do. All that was required was some minor experimentation with padding, to achieve the look of the specification image, as the provided measurements were not detailed enough.

- I'm pleased that it only took me a very short amount of time to sort out these two sections, as it at least tells me that I have a good grasp of the basics, and that I can create simple layouts quite efficiently.