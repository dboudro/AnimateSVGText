Animate Text with SVG Paths
=======
This technique allows you to animate the drawing of text via converting text to SVG paths.

Preview:

![Example](http://i.imgur.com/JMPn7ir.gif)


####**[Live Demo](http://dboody.com/port-projects/SVG-text/index.html)**



### Whats this all about?

  SVG path animation is a trending technique in web-design allowing designers to draw simple and elegant icons (as seen [here](http://www.essential-icons.com/)).  Now, designers can easily apply SVG animations to text. 

How to
=====

Step 1: General Setup and Implementation
----
1. Download and Install  the vector graphics editor, [Inkscape](http://www.inkscape.org/en/download/).
2. Open a new Inkscape Document.
3. Create your desired Text in the Top-left corner of the document ![Text Placement](http://i.imgur.com/lA7ti6n.png?1).
4. Select your text with selection tool.
5. From the Path menu, select Object --> Path
6. Save as SVG
7. Open SVG in a text-editor and remove extraneous code (seen below)![Extraneous Code](http://i.imgur.com/AWe6FjH.png?1).  

*See index.html for an example of what SVG code is needed.  There is A LOT so cleaning it up makes life easier.*

Step 2: CSS Implementation
----
1. Make a div that wraps the SVG element.  Give the div an id and add the following CSS to your div:

 ```
 		#YOUR-SVG-CONTAINER { //ADJUST NAME TO MATCH YOUR ID
			position: relative;
			width: 360px;   //ADJUST WIDTH TO MATCH WIDTH OF YOUR TEXT
			height: 110px;  //ADJUST HEIGHT TO MATCH HEIGHT OF YOUR TEXT
			margin: 40vh auto 0 auto;
		}
 ```
 
2. Give your SVG element an id and add the following CSS to your SVG element 

 ```
 #svg-canvas { //ADJUST NAME TO MATCH YOUR ID
			position: relative;
			width: 360px; //ADJUST WIDTH TO MATCH WIDTH OF YOUR TEXT
			height: 110px; //ADJUST HEIGHT TO MATCH HEIGHT OF YOUR TEXT
		}
 ```
 
3.  Make each path element look like: 

 ```
 <path class="title" fill-opacity="0" stroke="#000" stroke-width="1.5"
 ```
 
4. Add the following CSS to your stylesheet:  This CSS will take care of animating the text being drawn.  A concise but thorough explanation of this code can be found [here](http://css-tricks.com/snippets/css/keyframe-animation-syntax/)
```
.title {
		stroke-dasharray: 500;
				stroke-dashoffset: 500;
		animation: draw 5s linear forwards;
		-webkit-animation: draw 8s linear forwards;
		-moz-animation: draw 8s linear forwards;
		-o-animation: draw 8s linear forwards;
		font-weight: bold;
		font-family: Amatic SC;
		-inkscape-font-specification: Amatic SC Bold"
		}
		@keyframes draw {
		to {
			stroke-dashoffset: 0;
			}
		}
		@-webkit-keyframes draw {
		to {
			stroke-dashoffset: 0;
			}
		}
		
		@-moz-keyframes draw {
		to {
			stroke-dashoffset: 0;
			}
		}
		@-o-keyframes draw {
		to {
			stroke-dashoffset: 0;
			}
		}
```

Solutions to Common Problems
=======


***Please*** email me with any questions, comments, or examples where you used this technique!  I will try my best to respond to emails addressed to DylanRBoudro@gmail.com within 24 hours.



### Trouble Installing Inkscape?
[this link](http://www.inkscape.org/en/download/mac-os/) will help you install Inkscape on **Mac OS X**.





 
 

