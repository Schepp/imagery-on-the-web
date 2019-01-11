# Styling images & styling with Images
---
The mysterious gap

<pre><code class="liveCoding xml" data-livecoding-id="css-gap" contenteditable>&lt;img src="images/captain-marvel-comic.png" 
  width="300" 
  height="400"&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-gap" contenteditable>img {
  margin: 10px;
}</code></pre>

<div id="css-gap" style="background: #fff; border: 1px solid #000"></div>
---
Positioning backgrounds

<style>
#css-background-position div {
position: relative;
width: 100%;
height: 100%;
background-size: 50% 50%;
}

#css-background-position div::before,
#css-background-position div::after {
position: absolute;
top: 0;
right: 0;
bottom: 0;
left: 0;
width: 100%;
height: 100%;
background-image: linear-gradient(to bottom, black, black);
background-repeat: no-repeat;
background-position: inherit;
}

#css-background-position div::before {
background-size: 1px 100%;
}

#css-background-position div::after {
background-size: 100% 1px;
}
</style>

<pre><code class="liveCoding css" data-livecoding-id="css-background-position" contenteditable>div {
  background-image: url('images/transparent-red.png');
  background-repeat: no-repeat;
}</code></pre>

<div id="css-background-position" style="width: 400px; height: 400px; background: #fff; border: 1px solid #000"><div></div></div>
---
Generating backgrounds

<style>
#css-background-gradients div {
width: 100%;
height: 100%;
}
</style>

<pre><code class="liveCoding css" data-livecoding-id="css-background-gradients" contenteditable>div {
}</code></pre>

<div id="css-background-gradients" style="width: 400px; height: 400px; background: #fff; border: 1px solid #000"><div></div></div>
---
Make images fit [⚡](snippets/replace-imgs-with-divs.txt)

<style>
#css-background-size .flex {
  display: flex;
  width: 40vw;
  height: 30vh;
  border: 5px solid #fff;
}
#css-background-size .flex \> * {
  flex: 1 1 200px;
  min-width: 1px;
  border: 5px solid #fff;
}
</style>

<pre><code class="liveCoding xml" data-livecoding-id="css-background-size" contenteditable>&lt;div class="flex"&gt; 
  &lt;img src="images/thor.jpg"&gt;
  &lt;img src="images/iron-man.jpg"&gt;
  &lt;img src="images/hawkeye.jpg"&gt;
&lt;/div&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-background-size" contenteditable>* {
}</code></pre>

<div id="css-background-size" style="background: #fff; border: 1px solid #000"></div>
---
Art direction via image focus

<style>
#css-image-focus {
  width: 30vw;
  height: 40vh;
  padding: 10px;
  background: #fff;
  border: 1px solid #000;
}

#css-image-focus \> * {
  width: 100%;
  height: 100%;
}

#css-image-focus-setter {
  position: relative;
  cursor: crosshair;
}

#css-image-focus-setter::after {
  content: attr(data-coordinates);
  position: absolute;
  right: 0;
  bottom: 0;
  display: block;
  padding: 10px;
  background-color: rgba(0,0,0,.7);
  color: #fff;
  font-size: 20px;
  line-height: 1.3;
}
</style>

<pre><code class="liveCoding xml" data-livecoding-id="css-image-focus" contenteditable>&lt;div&gt;&lt;/div&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-image-focus" contenteditable>div {
  background-image: url('images/thor.jpg');
  background-size: cover;
}</code></pre>

<div class="inline-row">
  <div id="css-image-focus" class="resizable"></div>
  <div id="css-image-focus-setter" data-coordinates="0 0">
    <img src="images/thor.jpg" width="500" height="333">
  </div>
</div>
---
Art direction for Retina

<style>
#css-image-focus-2 {
  width: 30vw;
  height: 40vh;
  padding: 10px;
  background: #fff;
  border: 1px solid #000;
}

#css-image-focus-2 \> * {
  width: 100%;
  height: 100%;
}

#css-image-focus-2-setter {
  position: relative;
  cursor: crosshair;
}

#css-image-focus-2-setter::after {
  content: attr(data-coordinates);
  position: absolute;
  right: 0;
  bottom: 0;
  display: block;
  padding: 10px;
  background-color: rgba(0,0,0,.7);
  color: #fff;
  font-size: 20px;
  line-height: 1.3;
}
</style>

<pre><code class="liveCoding xml" data-livecoding-id="css-image-focus-2" contenteditable>&lt;img srcset="images/thor.jpg 1x, images/thor2x.jpg 2x"&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-image-focus-2" contenteditable>🤔</code></pre>

<div class="inline-row">
  <div id="css-image-focus-2" class="resizable"></div>
  <div id="css-image-focus-2-setter" data-coordinates="0 0">
    <img src="images/thor.jpg" width="500" height="333">
  </div>
</div>
---
Art direction for Responsive Images

<style>
#css-image-focus-3 {
  width: 30vw;
  height: 40vh;
  padding: 10px;
  background: #fff;
  border: 1px solid #000;
}

#css-image-focus-3 picture,
#css-image-focus-3 img {
  width: 100%;
  height: 100%;
}

#css-image-focus-3-setter {
  position: relative;
  cursor: crosshair;
}

#css-image-focus-3-setter::after {
  content: attr(data-coordinates);
  position: absolute;
  right: 0;
  bottom: 0;
  display: block;
  padding: 10px;
  background-color: rgba(0,0,0,.7);
  color: #fff;
  font-size: 20px;
  line-height: 1.3;
}
</style>

<pre><code class="liveCoding xml" data-livecoding-id="css-image-focus-3" contenteditable>&lt;picture&gt;
  &lt;source type="image/webp" srcset="images/thor.webp 1x, images/thor2x.webp 2x"&gt;
  &lt;source type="image/jpg" srcset="images/thor.jpg 1x, images/thor2x.jpg 2x"&gt;
  &lt;img src="images/thor.jpg"&gt;
&lt;/picture&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-image-focus-3" contenteditable></code></pre>

<div class="inline-row">
  <div id="css-image-focus-3" class="resizable"></div>
  <div id="css-image-focus-3-setter" data-coordinates="0 0">
    <img src="images/thor.jpg" width="500" height="333">
  </div>
</div>

