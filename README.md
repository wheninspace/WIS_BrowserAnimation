# WIS_BrowserAnimation
Create spinners and other animated icons and text for the LiveCode browser widget.
<br>
Primarily designed for use as a stack within the LiveCode IDE, but almost all the functionality can be tested in this web deployed version:
<br>
https://wheninspace.com/browseranimation/

### Version 2.0.1
<ul>
<li>Added possibility to set pure spinner colors on web</li>
<li>Improved possibility to copy spinner code and script on web (no more urlDecode needed)</li>
</ul>

### Version 2.0
#### A major update!
<ul>
<li>12 modern spinners have been added, adapted for even easier use in your LC projects</li>
<li>Ability to set the background color of the widget, to make it blend in with whatever background is below it, when transparency is not supported</li>
<li>The widget now contains script that can be called, for changing the color, after you have copied it to your own stack</li>
</ul>

### Version 1.0.6
<ul>
<li>The number of iterations can now be set. -1 means infinite.</li>
<li>Added possibility to enter a url. Link directly to an imagefile on the web to animate it. Or an entire site... <br>NB! If you use a widget animated by url in one of your apps, it must naturally have access to the url destination for it to work.</li>
</ul>

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

Works well on Mac, Win and iOS. Has been reported to work suboptimally on Android, because... Android...

### What?
This stack lets you create html code for displaying an image in a browser widget, with nifty animations.

### Why?
The point of using a browser widget for animation is e.g. to create spinners that keep spinning through lockScreen and database/web data fetches. 

The LC spinner widget and animated gifs freeze during blocking processes or when lockScreen is true, giving the impression that the process has stopped or that the screen has frozen. The browser widget operates on another level of reality (or something), and keeps running the animation.

Naturally, the feature can be used for any kind of animation effect needed. The only drawback is that the browser widget always shows at top layer. 
As of LC 10 dp5, it can be transparent though, which makes it easier to integrate into any app layout.

### How?
The html code that is created is completely self-sufficient, meaning that you can copy the browser widget to another stack and it will keep working. Image data is imported and stuffed right into the html code, so access to the original image file is not necessary after code creation, unless a url is used.

### Which images?
The types of images currently supported are:
- "Built-in" css icons
- SVG, PNG, JPG
- Any valid url to a file, or website

By default, the stack looks for image files in the folder where the stack is located. You can choose another folder by clicking the folder icon (on desktop, not web).

### How do animations work?
The animations are css coded. You can choose one animation or combine two of them, for various results ranging from nice to disturbing... 
For more documentation on the css code, go to loading.io/animation/

### Does this browser trick still work in a standalone?
Yes! Tested both as web deployment (LC 10 dp 5) and as Mac and Win standalones (LC 9.6.9).

### Planned development
- Better handling of adaptive resizing relative to browser rect
- Using LC default SVGs

### Acknowledgements
css/html code created by https://loading.io <br>
rgbToHex function created by https://github.com/Ferruslogic
