# Markup
---
## <image> Alias

<pre><code class="liveCoding xml" data-livecoding-id="markup-alias" contenteditable>&lt;img src="images/batman-white.jpg"&gt;</code></pre>

<div id="markup-alias" style="max-width: 75%; padding: 10px; background: #fff; border: 1px solid #000"></div>
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
