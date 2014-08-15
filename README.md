Animate Text via SVG
=======
This technique allows you to animate the drawing of text via converting text to SVG paths.

![Example ](http://i.imgur.com/JMPn7ir.gif "Example)](http://dboody.com)


Live Demo: [coming soon]

Setup and Implementation
=======
1. Download and Install  [Inkscape](http://www.inkscape.org/en/download/), a vector graphics editor.
2. Open a new Inkscape Document.
3. Create your desired Text in the Top-left corner of the document ![Text Placement ]](http://i.imgur.com/lA7ti6n.png?1).
4. Select your text with selection tool.
5. From the Path menu, select Object --> Path
6. Save as SVG
7. Open SVG in a text-editor and remove extraneous code ![Extraneous Code ]](http://i.imgur.com/AWe6FjH.png?1).  See index.html for an example of what SVG code is needed.  There is A LOT so cleaning it up makes life easier.
CSS Implementation
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
 #svg-canvas {
			position: relative;
			width: 360px; //ADJUST WIDTH TO MATCH WIDTH OF YOUR TEXT
			height: 110px; //ADJUST HEIGHT TO MATCH HEIGHT OF YOUR TEXT
		}
 ```
3.  Make each <path> element look like:
 ```
 <path class="title" fill-opacity="0" stroke="#000" stroke-width="1.5"
 ```
4. Add the following CSS to your stylesheet:  This CSS will take care of animating the text being drawn.
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

Help
=======
FAQ section coming soon.  Will update Readme to be more concise.

**Please** email me with any questions or comments.  DylanRboudro@gmail.com


 
 

