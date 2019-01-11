# Styling images & styling with Images
---
The mysterious gap

<pre><code class="liveCoding xml" data-livecoding-id="css-gap" contenteditable>&lt;img src="images/captain-marvel-comic.png" 
  width="300" 
  height="400"&gt;</code></pre>

<pre><code class="liveCoding css" data-livecoding-id="css-gap" contenteditable>img{
  margin: 10px;
}</code></pre>

<div id="css-gap" style="background: #fff; border: 1px solid #000"></div>
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
Make images fit [⚡](snippets/replace-imgs-with-divs.txt)

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

<pre><code class="liveCoding xml" data-livecoding-id="css-image-focus">&lt;div&gt;&lt;/div&gt;</code></pre>

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

