# About Fontstrap
Fontstrap is a bootstrap plugin(?) that lets you adjust your font size. It is intended to be just that with literally nothing else but I think being able to fully control font-size responsively is just too powerful to not make use of elsewhere. After all em-units are really great for just about everything.

<h2>Versions:</h2>
<p>There are currently 2 versions of the style sheet. One set is produced by hand (I wrote it) and the other one is written in LESS and compiled into CSS. If you require a different increments/units or what not, I would suggest changing the configs in the LESS version. Additionally there's better support for different screen sizes in the less version as it has xl (extra large) and mc(micro) instead of just xs-lg that the current bootstrap standard. However if you do not require a different increment, wider scaling support, or smaller adjustments, I would suggest that you use the one I written by hand as that one is slightly cleaner and also much smaller (aka ships faster) which is found in the by-hand folder.</p>

<h2>Documentations</h2>
<h3>How to use:</h3>
<p>class name convention: font-#em, font-#rem, font-"scale"-#em, font-"scale"-up-#em </p>
<p>for a flat adjustment of something to 1.5em for a "span" element you'd use class="font-150em" and same goes for rem units if you're using that</p>
<p>the scale-units have 2 parts, for example md-125em would make the font size only 1.25em when the screen fits the condition for md (see bootstrap) if you want the font size to be applied to all fonts and up like bootstrap use the up class: class="md-up-125em" of courese if you can chain them together like in bootstrap.</p>
<p>eg: class="col-xs-12 col-md-3 xs-200em font-sm-175em font-md-up-100em"</p>

<p>the numbers that are supported in the by hand version is 0, 25, 50, 75, 100, 125, 150, 172, 200 which I feel is plenty to get you started. You are free to modify them as you wish. The base fontstrap.css is inline ready and is relatively small. You can safely inline it into your base HTML if you're into that kind of things, the rest of the addon is a bit large and you probably want to load that after the fold aka link it in the footer or something (if you're using it at all). If you require a different increment system (eg by 20s instead of 25s) please adjust according in the LESS file and recompile.</p>

<p>Simple compact view for possiable class names: font-[xs-/sm-/md-/lg-][up-](0/25/50/75/100/125/150/175/200)(em/rem)</p>
<p>[] = optional</p>
<p>() = manditory</p>
<p>"font-up-150em" is not a thing</p>
<p>"font-0" is a thing</p>
<h2>Additional uses for fonts</h2>
<p>font sizes can be used as a unit in CSS via <a href="http://zellwk.com/blog/rem-vs-em/">em and rem.</a> so if you try something like this: </p>

...<br>
&lt;style&gt;.image-wrapper{padding:1em}&lt;/style&gt;<br>
&lt;div class=&quot;image-wrapper font-75em md-up-50em&quot;&gt;&lt;img src=&quot;some-image.png&quot;&gt;&lt;/div&gt;<br>
...

<p>You would not need to write custome media queries for your image-wrapper class as it's padding will resize responsively based on the font size of your element. In conjunction with bootstrap, this lets you easily make minor adjustments to your layout. Where bootstrap lets you adjust large things like grids, fontstrap will let you adjust the smaller minor details. probably the most useful way of using this through the font-&lt;size&gt;-0 adjuster as you can use it to completely get rid of assets at spicific sizes assume they are sized to en em unit. In theory, you'd be able to have a main style sheet that does not contain any media queries and rely exclusively on bootstrap and fontstrap for adapting the layout for different views.</p>

<p><strong>The biggest advantage of this is that it allows you to keep all of your responsive design choices in one place: the HTML file.</strong></p>

<h3>fontstrap-addon.css?</h3>
<p>If you want to have some predefined classes for making these small adjustments then that's wehre fontstrap-addon comes in. The default fonstrap will only carry with it responsive font sizes. In the addon CSS you'll find a number of other tools at your disposal. such as adjusting margin and padding as well as letter space and so on. Here's a list of the classes that are defined and an example of how to get some desired effects. You are often better off just declareing custome classes. In most of these cases unless stated otherwise numbers that are supported are: 25/50/75/100/125/150/175/200. Incase you did not notice, the addon styles exists in the by-hand folder.</p>
<ul>
	<li>pad-#em</li>
	<li>pad-#rem</li>
	<li>pad-virt-#em</li>
	<li>pad-horiz-#rem</li>
	<li>padless</li>
	<li>padless-virt</li>
	<li>padless-horiz</li>
	<li>padless-right</li>
	<li>padless-left</li>
	<li>padless-top</li>
	<li>padless-bottom</li>
	<li>marg-#em</li>
	<li>marg-#rem</li>
	<li>marg-virt-#em</li>
	<li>marg-horiz-#rem</li>
	<li>marginless</li>
	<li>marginless-virt</li>
	<li>marginless-horiz</li>
	<li>marginless-right</li>
	<li>marginless-left</li>
	<li>marginless-top</li>
	<li>marginless-bottom</li>
	<li>lspace-0</li>
	<li>lspace-#em (letter spacing | additional numbers: 5/10/15/20)</li>
	<li>lspace-#rem (letter spacing | additional numbers: 5/10/15/20)</li>
	<li>weight-# (supported numbers: 100/200/300/400/500/600/700/800/900)</li>
	<li>font-# (supported numbers: 100/200/300/400/500/600/700/800/900)</li>
	<li>font-X (supported words: xlight/light,normal/bold/xbold)</li>
</ul>

<p>If you're using this, your HTML is gonna get really cluttered and would probably defeat the purpose of this framework. If you are just prototyping and would like easily adjustable things than ya maybe this is not that bad. Here's how you'd achieve some common desired results:</p>

<p>padding-left: 1 em -> pad-horiz-1em padless-right</p>

<p>so for your own sake, if you're messing with margins and paddings, just declare an extra class. As for the other classes, it's up to you what you want to do with them. They seem kind of useful but I haven't played around with them enough to say for sure.</p>

<h3>Other Defaults</h3>
<p>Font sizes base are xs:20px, sm:18px, md:16px, lg:14px. These are the default font sizes but if you dont like them feel free to change them </p>
