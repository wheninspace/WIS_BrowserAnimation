# WIS_BrowserAnimation
Create animated icons and text for the LiveCode browser widget

### Version 1.0.5
<ul>
<li>Added possibility to copy the code when running the web application (note that a urlDecode() must be done on the pasted text in LiveCode before using it)</li>
<li>Added possibility to enter an RGB value into the color field (works in the web application too)</li>
</ul>

### Version 1.0.4
<ul>
<li>More efficient CSS code handling - only CSS code needed for the chosen animations is now included</li>
<li>Added the possibility to animate text</li>
</ul>

### Version 1.0.3 
<ul>
<li>Added the possiblity to set the duration of animations.</li>
</ul>

Works well on Mac, possibly slightly unstable on Windows (may cause LC crash)

To see the browser animations work in a web deployment (now with more fish!), see:

https://wheninspace.com/browseranimation/

### What?
This stack lets you create html code for displaying an image in a browser widget, with nifty animations.

### Why?
The point of using a browser widget for animation is e.g. to create spinners that keep spinning through lockScreen and database/web data fetches. 

The LC spinner widget and animated gifs freeze during blocking processes or when lockScreen is true, giving the impression that the process has stopped or that the screen has frozen. The browser widget operates on another level of reality (or something), and keeps running the animation.

Naturally, the feature can be used for any kind of animation effect needed. The only drawback is that the browser widget always shows at top layer. 
As of LC 10, it can be transparent though, which makes it easier to integrate into any app layout.

### How?
The html code that is created is completely self-sufficient, meaning that you can copy the browser widget to another stack and it will keep working. Image data is imported and stuffed right into the html code, so access to the original image file is not necessary after code creation.

### Which images?
The types of images currently supported are:
- "Built-in" css icons
- SVG, PNG, JPG

By default, the stack looks for image files in the folder where the stack is located. You can choose another folder by clicking the folder icon.

### How do animations work?
The animations are css coded. You can choose one animation or combine two of them, for various results ranging from nice to disturbing... 
For more documentation on the css code, go to loading.io/animation/

### Does this browser trick still work in a standalone?
Yes! Tested both as web deployment (LC 10 dp 5) and as Mac standalone (LC 9.6.8).

### What does not work (yet)?
- Resizing SVGs. The svg path must be transformed to the new size, and I don't know how to do that. Research in progress! But you can try resizing the browser widget, sometimes that works...
- Using LC default SVGs. Just using the iconPath is not enough, apparently. Research in progress!
- Changing the color of multi-colored SVG files. That's too complex. Use the color chooser only with mono-colored SVGs.
- On Windows, handling multiple browser widgets on one card seems a bit unstable. 
