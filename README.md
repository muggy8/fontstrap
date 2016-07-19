# About Fontstrap
Fontstrap is a bootstrap plugin(?) that lets you adjust your font size. It is intended to be just that with literally nothing else but I think being able to fully control font-size responsively is just too powerful to not make use of elsewhere. After all em-units are really great for just about everything.

<h2>Documentations</h2>
<h3>How to use:</h3>
<p>class name convention: size-#em, size-#rem, "scale"-#em, "scale"-up-#em </p>
<p>for a flat adjustment of something to 1.5em for a "span" element you'd use class="size-150em" and same goes for rem units if you're using that</p>
<p>the scale-units have 2 parts, for example md-125em would make the font size only 1.25em when the screen fits the condition for md (see bootstrap) if you want the font size to be applied to all fonts and up like bootstrap use something like class="md-up-125em" of courese if you can chain them together like in bootstrap.</p>
<p>eg: class="col-xs-12 col-md-3 xs-200em sm-175em md-up-100em"</p>

<p>the numbers that are supported right now is 25, 50, 75, 100, 125, 150, 172, 200 which I feel is plenty to get you started. You are free to modify them as you wish.</p>

<h3>Additional stuff? (fontstrap-extended.css)</h3>
<p>Probably the most useful part of having adjustable font sizes is that you can adjust other parts of your site responsively wihtout adjusting the CSS rules. The first of this to get added is padding and margin (though padding is likely to be used more). The added classes are: pad-#em, pad-#rem, marg-#em and marg-#rem, pad-horiz-#em, pad-horiz-#rem, marg-horiz-#em and marg-horiz-#rem, pad-virt-#em, pad-virt-#rem, marg-virt-#em and marg-virt-#rem where number is again, 25 to 200 incrementing in 25s. The intended usage of the padding commands are like this: </p>
<p>class="size-100em sm-75em lg-75em pad-150em padless-horiz"</p>
<p>class="size-100em sm-75em lg-75em pad-virt-150em pad-horiz-75em marg-virt-75em"</p>
<p>After You completely messed up your em based heiarchy for your spacing needs, remember you can always redefine a new heiarchy somewhere down the line later with rem calls. As an example. if the above class belong to a section tag that contained some divs, you can then declare the following in the div tag for the rest of the stuff</p>
<p>class="size-100rem"</p>
<p>I understand that not everyone cares about controlling padding / margin and just want the font size adjustments and as a result, I have decided to split the code and added a second fontstrap css file into the src folder. If you want the addtional stuff grab the extended version if you just want basic font size control and really care about load times, then grab the non-extended version.</p>
<p>I have a custom cut of bootstrap that I like to use since it's increadibly small and has the most important bits (the grid) and that's about it. I usually just combine my custom cut of bootstrap and fontstrap in PHP and inline both bootstrap and fontstrap into my sites as part of the critical core css. You can feel free to do the same.</p>

<h3>Other Defaults</h3>
<p>Font sizes base are xs:20px, sm:18px, md:16px, lg:14px. These are the default font sizes but if you dont like them feel free to change them </p>
