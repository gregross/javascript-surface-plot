# 3D Surface Plotting in JavaScript`!` #

created by Greg Ross

---



## The first and original, freely available, JavaScript surface plot. ##

This library allows one to plot 3D surfaces. Download the code and take a look at test.html to see how.

Tested in Chrome, Firefox, Opera, Safari and Internet Explorer 6. **Works in IE via use of [excanvas](http://code.google.com/p/explorercanvas/).** (See test.html in the download.)

Performs best in Safari and Chrome.

## See [here](http://www.grvisualisation.50webs.com/javascript_surface_plot.html) for a working example, or play around with the plot on [jsFiddle](http://jsfiddle.net/gregross/vTBv3/). ##

## See [here](http://javascript-surface-plot.googlecode.com/svn/trunk/googleVizApi.html) for API details. ##

Need Sans-GoogleVis? See [here](http://jsfiddle.net/gregross/3fcvQ/32/) for a version that does not rely on the GoogleVis API.


Want some WebGL slickness? [See here](http://code.google.com/p/webgl-surface-plot/).

[![](http://javascript-surface-plot.googlecode.com/svn/trunk/images/screenshot1.png)](http://www.grvisualisation.50webs.com/javascript_surface_plot.html)

z = cos(x) `*` cos(y)
<br><br>

<img src='http://javascript-surface-plot.googlecode.com/svn/trunk/images/screenshot2.png' />

z = sin(x) <code>*</code> cos(y)<br>
<br><br>

<img src='http://javascript-surface-plot.googlecode.com/svn/trunk/images/screenshot3.png' />

z = cos(x) <code>*</code> cos(y) + sin(x)<br>
<br><br>

<img src='http://javascript-surface-plot.googlecode.com/svn/trunk/images/screenshot4.png' />

a wire frame is rendered when the "fillPolygons:" option is set to false<br>
<br><br>


<h2>Features</h2>

<ul><li><b>pure JavaScript</b> implementation. <b>No need for Flash</b>.<br>
</li><li><b>rotation</b> - left-click and drag the mouse to rotate the surface<br>
</li><li><b>scaling</b> - hold down the shift key and drag the mouse to scale<br>
</li><li>hover the mouse over the surface to see values<br>
</li><li>custom axis titles<br>
</li><li>customisable <b>colour gradients</b>
</li><li>works in all popular browsers<br>
</li><li>wrapped in the <b>Google Visualization API</b>. See <a href='http://javascript-surface-plot.googlecode.com/svn/trunk/googleVizApi.html'>here</a>.</li></ul>



<h2>Applications</h2>

<ul><li>visualise correlation surfaces<br>
</li><li>plot trigonometric functions<br>
</li><li>chart financial volatilities in 3D</li></ul>

<br>

<h2>Implementation</h2>

In all browsers with the exception of IE, everything is rendered on the HTML-5 Canvas element. In IE, <a href='http://code.google.com/p/explorercanvas/'>excanvas</a> is used for VML rendering.<br>
<br>
Each segment on the graph is a polygon and its geometric centroid is used in measuring distance from the 'camera' so that we can determine the order in which to render all segments. This is a simple implementation of <b><a href='http://en.wikipedia.org/wiki/Painter%27s_algorithm'>Painter's algorithm</a></b>.<br>
<br>
Rotation and scaling are achieved by simple matrix manipulation.<br>
<br>
Colour gradients are defined by the <a href='http://code.google.com/p/javascript-surface-plot/source/browse/trunk/javascript/ColourGradient.js'>ColourGradient class</a>. This is a utility I wrote a while ago to create gradients through any path in RGB space using any number of colours. Each colour defines a point in the space and when traveling from the start colour to the end colour we obtain a path. The start and end colours are mapped to given min and max numerical bounds.  When provided with a number within those bounds, a new colour is obtained by linearly interpolating along the path in RGB space. Simples!<br>
<br>
<br>

<hr />

Other projects by Greg Ross...<br>
<br>
<h3><i><b><a href='http://code.google.com/p/webgl-surface-plot/'>WebGL surface plot</a>.</b></i></h3>

<b>3D surface plotting in JavaScript via WebGL</b>


<br>


<h3><i><b><a href='http://www.grvisualisation.50webs.com/visi_scroll.html'>Visi-Scroll</a>.</b></i></h3>

<b>An HTML scrollbar with highligting for easy access to information</b>


<br>

<h3><i><b><a href='http://www.grvisualisation.50webs.com/excelrangefinder.html'>Excel RangeFinder</a>.</b></i></h3>

<b>An overview+detail visualisation for navigation in Excel spreadsheets</b>


<br>

<h3><i><b><a href='http://www.grvisualisation.50webs.com/'>Magic Table</a>.</b></i></h3>

<b>A JavaScript library that allows you to see more in your data by applying some simple visual techniques to transform a table.</b>


<br>

<h3><i><b><a href='http://www.grvisualisation.50webs.com/javascript_voronoi.html'>JavaScript voronoi</a>.</b></i></h3>

<b>A pure JavaScript implementation of a Voronoi tessellation</b>

<br>
<hr />
<b>iPhone apps</b>

<a href='http://itunes.apple.com/gb/app/claptrax/id427145886?mt=8'><img src='http://www.grvisualisation.50webs.com/images/clapForMusic/SplashViewPhone.png' /></a>

<hr />

<a href='http://ax.itunes.apple.com/gb/app/peekaboo-3d/id380735126?mt=8'><img src='http://www.grvisualisation.50webs.com/images/peekaboo/PeekabooAd.png' /></a>