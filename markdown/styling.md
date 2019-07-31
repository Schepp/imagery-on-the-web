<br><br><br><br><br><br>
# Styling images & styling with Images
---
## The mysterious gap

<pre><code class="liveCoding xml" data-livecoding-id="css-gap" contenteditable>&lt;img src="images/captain-marvel-comic.png" 
  width="300" 
  height="400"&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-gap" contenteditable>img {
  margin: 10px;
}</code></pre>

<div id="css-gap" style="background: #fff; border: 1px solid #000"></div>
---
## Styling broken images [⚡](snippets/broken-image-styling.txt)

<style>
#css-broken-image img { vertical-align: bottom; }
</style>

<div class="flex-row">
<pre><code class="liveCoding css" data-livecoding-id="css-broken-image" contenteditable>img {
}</code></pre>

<div>
<pre><code class="liveCoding xml" data-livecoding-id="css-broken-image" contenteditable>&lt;img src="images/iron-man.jpg"
alt="Iron Man energizing up for battle"&gt;</code></pre>

<div id="css-broken-image" style="width: 800px; padding: 10px; background: #fff; border: 1px solid #000; text-shadow: none; font-size: 30px; line-height: 1.3; color: #000"></div>
</div>
</div>
</div>
---
## Positioning backgrounds

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
## Generating backgrounds

<style>
#css-background-gradients div {
width: 100%;
height: 100%;
}
</style>

<pre><code class="liveCoding css" data-livecoding-id="css-background-gradients" contenteditable>div {
}</code></pre>

<div id="css-background-gradients" style="width: 400px; height: 400px; padding: 10px; background: #fff; border: 1px solid #000"><div></div></div>
---
## Animating gradients

<style>
#css-animated-backgrounds div {
width: 100%;
height: 100%;
}
</style>

<div class="flex-row" style="width:78%">

<pre><code>CSS.registerProperty({
  name: '--multiply',
  syntax: '<number>',
  inherits: false,
  initialValue: '0'
});</code></pre>

<pre><code>@keyframes chart-open {
  from { 
    --multiply: 0; }
  to   { 
    --multiply: 1; }
}</code></pre>

</div>

<pre><code class="liveCoding css" data-livecoding-id="css-animated-backgrounds" contenteditable>div {
  animation: chart-open 1000ms infinite;
  background-image: conic-gradient(
    blue calc(var(--multiply) * 40%), 
    red calc(var(--multiply) * 40%), 
    red calc(var(--multiply) * 70%), 
    yellow calc(var(--multiply) * 70%), 
    yellow calc(var(--multiply) * 90%), 
    transparent calc(var(--multiply) * 90%)
  );
  border-radius: 50%;
  filter: drop-shadow(10px 10px 10px #000);
}</code></pre>

<div id="css-animated-backgrounds" style="position: absolute; top: 0; right: 0; width: 400px; height: 400px; padding: 10px; background: #fff; border: 1px solid #000"><div></div></div>
---
Masking  [⚡](snippets/masks.txt)

<style>
#css-masks div {
width: 100%;
height: 100%;
}
</style>

<pre><code class="liveCoding css" data-livecoding-id="css-masks" contenteditable>div {
  animation: chart-open 1000ms infinite;
  background-color: #ddd;
  background-image: conic-gradient(
    blue calc(var(--multiply) * 40%), 
    red calc(var(--multiply) * 40%), 
    red calc(var(--multiply) * 70%), 
    yellow calc(var(--multiply) * 70%), 
    yellow calc(var(--multiply) * 90%), 
    transparent calc(var(--multiply) * 90%)
  );
  border-radius: 50%;
}</code></pre>

<div id="css-masks" style="position: absolute; top: 0; right: 0; width: 400px; height: 400px; padding: 10px; background: #fff; border: 1px solid #000"><div></div></div>
---
## Build your own Instagram

<style>
#css-instagram div,
#css-instagram img {
    display: block;
    width: 100%;
    vertical-align: bottom;
}
</style>

<pre><code class="liveCoding xml" data-livecoding-id="css-instagram" contenteditable>&lt;div&gt;
  &lt;img src="images/captain-marvel-scene.jpg"&gt;
&lt;/div&gt;</code></pre>

<div class="flex-row">
<pre><code class="liveCoding css" data-livecoding-id="css-instagram" contenteditable>div {
  position: relative;
}
img {
  filter: sepia(1);
}
div::after {
  content: '';
  position: absolute;
  top: 0; right: 0; bottom: 0; left: 0;
  background-image: radial-gradient(
    circle at center, #f000, #f00c);
  mix-blend-mode: overlay;
}</code></pre>

    <div id="css-instagram" style="width: 800px; padding: 10px; background: #fff; border: 1px solid #000"></div>
</div>
---
Make images fit [⚡](snippets/replace-imgs-with-divs.txt)

<style>
#css-background-size .flex {
  display: flex;
  width: 70vw;
  height: 70vh;
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

<div id="css-background-size" style="position: absolute; right: 0; top: 200px; background: #fff; border: 1px solid #000"></div>
---
Art direction via focal point

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
---
## Parallax [⚡](snippets/parallax.txt)

<style>
#parallax div {
width: 100%;
height: 100%;
}
</style>

<pre style="margin-left: 0"><code class="liveCoding xml" data-livecoding-id="parallax">&lt;div class="parallax"&gt;
  &lt;div class="background"&gt;&lt;/div&gt;
  &lt;div class="foreground"&gt;&lt;/div&gt;
&lt;/div&gt;</code></pre>

<pre style="margin-left: 0"><code class="liveCoding css" data-livecoding-id="parallax" contenteditable>.parallax {
  position: relative; overflow-x: hidden; overflow-y: scroll;
}
.background {
  background: center/cover url('images/parallax-city.jpg');
}
.foreground {
  position: absolute;
  top: 0; right: 0; bottom: 0; left: 0;
  background: center/cover url('images/parallax-iron-man.webp');
}</code></pre>

<div id="parallax" style="position: absolute; right: 0; top: 0; width: 600px; height: 1000px; padding: 10px; background: #fff; border: 1px solid #000"><div></div></div>
---
## Slideshow

<style>
#slideshow div {
  width: 800px; 
  height: 400px;
}
</style>

<pre style="margin-left: 0"><code class="js">CSS.registerProperty({
  name: '--cross-fade',
  syntax: '<number>',
  inherits: false,
  initialValue: '0'
});</code></pre>

<pre style="margin-left: 0"><code class="css">@keyframes cross-fade {
  0% { --cross-fade: 0 }
  50% { --cross-fade: 1 }
  100% { --cross-fade: 0 }
}
.slideshow {
  background-image: -webkit-cross-fade(
    url('../images/iron-man.jpg'),
    url('../images/hawkeye.jpg'),
    calc(100% * var(--cross-fade)));
  background-size: cover;
  animation: cross-fade 10000ms infinite;
}</code></pre>

<div id="slideshow" style="position: absolute; right: 0; width: 820px; top: 250px; border: 10px solid #fff; background: #fff; outline: 1px solid #000"><div></div></div>
---
<!-- .slide: data-state="canvas" -->

## Procedural backgrounds (Safari only)

```js
const ctx = document.getCSSCanvasContext('2d', 'snow', 1000, 1000);
/* draw in the canvas */
```

```html
<div></div>
```

```css
div {
  background-image: -webkit-canvas(snow);
}
```

<div style="width: 600px; height: 400px; margin: 0 auto; padding: 10px; background: #fff; border: 1px solid #000"><canvas id="canvas"></canvas></div>
---
## Inception!   

`-moz-element()`

[Demo](https://codepen.io/iamvdo/pen/vOwaWz)
---
.css {}