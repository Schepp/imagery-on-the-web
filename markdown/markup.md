<br><br><br><br><br><br>
# Markup
---
## input[type="image"]

```html
<form action="images/raster.png" target="_blank">
  <input type="image" 
         src="images/raster.png"
         width="600" height="600">
</form>
```

<div style="display: inline-block; margin: 0 auto; padding: 10px; background: #fff; border: 1px solid #000">
<form action="images/raster.png" target="_blank">
  <input type="image" 
         src="images/raster.png"
         width="600"
         height="600" 
         style="vertical-align: bottom">
</form>
</div>

---
<!-- .slide: data-transition="none" -->
## The alt-tag
---
<!-- .slide: data-transition="none" -->
## The <del>alt-tag</del> alt-attribute
---
<!-- .slide: data-transition="none" -->
## The <del>alt-tag</del> alt-attribute

> Except where otherwise specified, the alt attribute must be specified and its value must not be empty;  
the value must be an appropriate replacement for the image.

[W3C HTML5 Spec](https://www.w3.org/TR/2011/WD-html5-author-20110809/the-img-element.html#alt)

<a href="https://html5.validator.nu/?doc=http%3A%2F%2Fschepp.github.io%2Fimagery-on-the-web%2Fdemos%2Falt.html&showsource=yes" target="validator" class="fragment">Validator example</a>

<a href="https://html5.validator.nu/?doc=http%3A%2F%2Fschepp.github.io%2Fimagery-on-the-web%2Fdemos%2Ftitle.html&showsource=yes" target="validator" class="fragment">A title-attribute works, too!</a>

<a href="https://html5.validator.nu/?doc=http%3A%2F%2Fschepp.github.io%2Fimagery-on-the-web%2Fdemos%2Ffigcaption.html&showsource=yes" target="validator" class="fragment">as does &lt;figcaption&gt;</a>
---
## generator-unable-to-provide-required-alt

> Markup generators may specify a <u>generator-unable-to-provide-required-alt</u> attribute on img elements for which they have been unable to obtain alternative text and for which they have therefore omitted the alt attribute.

<a href="https://html.spec.whatwg.org/multipage/images.html#guidance-for-conformance-checkers" target="_blank">WHATWG HTML Spec</a>

<a href="https://html5.validator.nu/?doc=http%3A%2F%2Fschepp.github.io%2Fimagery-on-the-web%2Fdemos%2Fgenerator-unable-to-provide-required-alt.html&showsource=yes" target="validator" class="fragment">What does the validator say?</a>
---
## &lt;image&gt; Alias

<pre><code class="liveCoding xml" data-livecoding-id="markup-alias" contenteditable>&lt;img src="images/batman-white.jpg"&gt;</code></pre>

<div id="markup-alias" style="max-width: 75%; padding: 10px; background: #fff; border: 1px solid #000"></div>
---
## &lt;image&gt; Alias

> The HTML &lt;image&gt; element is an obsolete remnant of an ancient version of HTML lost in the mists of time;  
In general, browsers will attempt to map this to &lt;img&gt;.  
However, that doesn't mean this is a good idea to use. It's not.

[MDN: &lt;image&gt;: The obsolete Image element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/image) 
---
## Format switching back in the days...

<pre><code class="liveCoding xml" data-livecoding-id="markup-svg-alias" contenteditable>&lt;svg width="450" height="600"&gt;
 &lt;image xlink:href="images/captain-marvel-illustration.svg"
        src="images/captain-marvel-illustration.png"
        width="450"
        height="600"&gt;
&lt;/svg&gt;</code></pre>

<div id="markup-svg-alias" style="padding: 10px; background: #fff; border: 1px solid #000"></div>
---
## Format switching today

<pre><code class="liveCoding xml" data-livecoding-id="markup-picture" contenteditable>&lt;picture&gt;
 &lt;source type="image/svg+xml" srcset="images/captain-marvel-illustration.svg"&gt;
 &lt;img src="images/captain-marvel-illustration.png" 
         width="450"
         height="600"&gt;
&lt;/picture&gt;</code></pre>

<div id="markup-picture" style="padding: 10px; background: #fff; border: 1px solid #000"></div>
---
## Format and resolution switching

<pre><code class="liveCoding xml" data-livecoding-id="markup-picture-2" contenteditable>&lt;picture&gt;
 &lt;source type="image/svg+xml" srcset="images/captain-marvel-illustration.svg"&gt;
 &lt;img src="images/captain-marvel-illustration.png" 
         srcset="images/captain-marvel-illustration.png 2x"
         width="450"
         height="600"&gt;
&lt;/picture&gt;</code></pre>

<div id="markup-picture-2" style="padding: 10px; background: #fff; border: 1px solid #000"></div>
---
## Art direction

<pre style="width: 75%; float: right"><code class="liveCoding xml" data-livecoding-id="markup-picture-3" contenteditable>&lt;picture&gt;
 &lt;source media="(max-width: 320px)" 
    srcset="images/black-widow-closeup.jpg 1x,
            images/black-widow-closeup2x.jpg 2x"&gt;
 &lt;img src="images/black-widow.jpg" 
    srcset="images/black-widow2x.jpg 2x"
    width="450"
    height="600"&gt;
&lt;/picture&gt;</code></pre>

<div class="resizable" style="position: absolute; top: 0; left: 0; width: 450px; height: 600px; margin: 0 auto; background: #fff; border: 10px solid #fff; outline: 1px solid #000">
<iframe id="markup-picture-3" src="about:blank" style="width: 100%; height: 100%; padding: 0; overflow: hidden; border: none;" scrolling="no"></iframe>
</div>
---
## Universal <br>resolution switching

<pre style="width: 75%; float: right"><code class="liveCoding xml" data-livecoding-id="markup-picture-4" contenteditable>&lt;style&gt; img { width: 100vw }
@media (min-width: 320px) {
  img { width: 50vw }
}&lt;/style&gt;    
&lt;img src="https://satyr.io/900x1200?text=fallback" 
    sizes="(min-width: 320px) 50vw, 100vw"
    srcset="
    https://satyr.io/300x400?text=300w 300w,
    https://satyr.io/450x600?text=450w 450w,
    https://satyr.io/600x800?text=600w 600w,
    https://satyr.io/900x1200?text=900w 900w"&gt;

</code></pre>

<div class="resizable" style="position: absolute; top: 0; left: 0; width: 450px; height: 600px; margin: 0 auto; background: #fff; border: 10px solid #fff; outline: 1px solid #000">
<iframe id="markup-picture-4" src="about:blank" style="width: 100%; height: 100%; padding: 0; overflow: hidden; border: none;" scrolling="no"></iframe>
</div>
---
## Flexible images

<style>
#markup-flexible img {
    max-width: none;
}
</style>

<pre style="float: right; width: 55%"><code class="liveCoding css" data-livecoding-id="markup-flexible" contenteditable>img {
  background-color: #333;
}
</code></pre>

<pre style="float: right; width: 55%"><code class="liveCoding xml" data-livecoding-id="markup-flexible" contenteditable>&lt;img src="https://satyr.io/
800x450?text=Flexible&delay=0"
  width="800"
  height="450"&gt;
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
</code></pre>

<div id="markup-flexible" class="resizable" style="position: absolute; left: 0; top: 150px; width: 820px; height: 820px; overflow: hidden; outline: 1px solid #000; background: #fff; border: 10px solid #fff; padding-bottom: 20px;"></div>
---
## Native lazy-loading

```html
<img src="whatever.jpg" loading="lazy">
```

<ul>
 <li class="fragment">`lazy`: defer fetching until content can be viewed</li>
 <li class="fragment">`eager`: fetch immediately</li>
 <li class="fragment">`auto`: let the browser decide</li>
 <li class="fragment">_</li>
</ul>

<p class="fragment">IE 11 and Edge also supported a `lazyload` attribute with values `0` and `1`</p>
---
# Force lazyloading for all images

Feature Policy Header

`Feature-Policy: lazyload 'self'(force)`

---
## Priority Hints

Telling the browser which image to load first via `importance` attribute

```html
<img src="whatever.jpg" importance="low">
<img src="hero.jpg" importance="high">
<img src="whatever.jpg" importance="low">
```

<p class="fragment">Or, if it's super critical to your life and business, use a Resource Hint:<br>
`<link rel="preload" href="hero.jpg" as="image">`</p>
---
## Non-blocking image decode

`<img src="whatever.jpg" async="on">`

<img src="images/image-decode.png" width="1200" height="394" style="width: 100%; height: auto">

`on`: Waits for when the browser has capacity  
`off`: Decodes the image right away, blocking the main thread 
---
## Hotlinking galore

If you are the bad girl/guy and want to use someone else's image:

`<img src="whatever.jpg" referrerpolicy="no-referrer">`

<p class="fragment">(and also good for privacy)</p>
---
# &lt;/html&gt;