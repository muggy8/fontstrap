# About Fontstrap
Fontstrap is a bootstrap plugin(?) that lets you adjust your font size. There's literally nothing else in here other than a few extra auxiliary functions.

<h2>Documentations</h2>
<h3>How to use:</h3>
<p>class name convention: size-#em, size-#rem, "scale"-#em, "scale"-up-#em </p>
<p>for a flat adjustment of something to 1.5em for a "span" element you'd use class="size-150em" and same goes for rem units if you're using that</p>
<p>the scale-units have 2 parts, for example md-125em would make the font size only 1.25em when the screen fits the condition for md (see bootstrap) if you want the font size to be applied to all fonts and up like bootstrap use something like class="md-up-125em" of courese if you can chain them together like in bootstrap.</p>
<p>eg: class="col-xs-12 col-md-3 xs-200em sm-175em md-up-100em"</p>

<p>the numbers that are supported right now is 25, 50, 75, 100, 125, 150, 172, 200 which I feel is plenty to get you started. You are free to modify them as you wish.</p>

<h3>CSS3 Animations</h3>
<p>I really like CSS3 animations and as such I did a bunch with it. By default, everything will inherit from the parent element it's transition time (0.25s by default) and font size. This means that if a parent's font size changes because of a break point (say the doc root HTML element), the child elements will change anywhere from 1-4 seconds (depending on how deep into the doc nest it is) because all of it's parents are taking their sweet time transitioning.</p>

<p>If you have a really artsy website and want to have it dance around a bunch then this is totally fine but sometimes this isn't really desired... or well most of the time. This is when you can use the class "instant-em-pass" which will disable font size transitions for all of it's children. So if you want the transition to last 0.25s put this on the body, if you want it to last .5s put it on the next thing under the body and so on.</p>

<p>This of course means that other default transitions to font size might not work either and in that case there's the em-transition class where you can restore the default transition to that node only.</p>

<h3>Additional stuff?</h3>
<p>There really isn't much here. paddless, marginless, padless-horiz, paddless-virt, marginless-horiz, marginless-virt which pretty much does exactly what it sounds like, The last useful thing I added is that when you have a bunch of spans lined up, some of them lose their spacing, so there's a class called spacefix which adds padding equivilant to 0.25em (the size of a space normally) to the right of the span (mono-spacefix for monospace fonts). </p>
<p>I have a custom cut of bootstrap that I like to use since it's increadibly small and has the most important bits (the grid) and that's about it. I usually just combine my custom cut of bootstrap and fontstrap in PHP and inline both bootstrap and fontstrap into my sites as part of the critical core css. You can feel free to do the same.</p>

<h3>Other Defaults</h3>
<p>Font sizes base are xs:20px, sm:18px, md:16px, lg:14px. These are the default font sizes but if you dont like them feel free to change them </p>
