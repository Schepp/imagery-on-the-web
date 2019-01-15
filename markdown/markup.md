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

<pre style="width: 60%; float: right"><code class="liveCoding xml" data-livecoding-id="markup-picture-3" contenteditable>&lt;picture&gt;
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
