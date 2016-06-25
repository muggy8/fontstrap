# About Fontstrap
Fontstrap is a bootstrap plugin(?) that lets you adjust your font size. There's literally nothing else other than a few extra auxiliary functions.

<h2>Documentations</h2>
<h3>How to use:</h3>
<p>class name convention: size-#em, size-#rem, "scale"-#em, "scale"-up-#em </p>
<p>for a flat adjustment of something to 1.5em for a "span" element you'd use class="size-150em" and same goes for rem units if you're using that</p>
<p>the scale-units have 2 parts, for example md-125em would make the font size only 1.25em when the screen fits the condition for md (see bootstrap) if you want the font size to be applied to all fonts and up like bootstrap use something like "md-up-125em"</p>
<p>the numbers that are supported right now is 25, 50, 75, 100, 125, 150, 172, 200 which I feel is plenty to get you started. You are free to modify them as you wish.</p>

<h3>Additional stuff?</h3>
<p>There really isn't much here. paddless, marginless, padless-horiz, paddless-virt, marginless-horiz, marginless-virt which pretty much does exactly what it sounds like, The last useful thing I added is that when you have a bunch of spans lined up, some of them lose their spacing, so there's a class called spacefix which adds padding equivilant to 0.25em (the size of a space normally) to the right of the span (mono-spacefix for monospace fonts). </p>
<p>I have a custom cut of bootstrap that I like to use since it's increadibly small and has the most important bits (the grid) and that's about it. I usually just combine my custom cut of bootstrap and fontstrap in PHP and inline both bootstrap and fontstrap into my sites as part of the critical core css. You can feel free to do the same.</p>

<h3>Other Defaults</h3>
<p>Font sizes base are xs:20px, sm:18px, md:16px, lg:14px. These are the default font sizes but if you dont like them feel free to change them </p>