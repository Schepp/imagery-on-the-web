<br><br><br><br><br><br>
# Image Formats
---
<h2 class="image-grid-headline">Still Images</h2>
<div class="image-grid">
  <div class="image"></div>
  <div class="image"></div>
  <div class="image"></div>
</div>
---
## Format Battle: Handdrawn vs. Illustration vs. Photo
 
<div class="flex-row">
   <div><img src="images/captain-marvel-drawing.png" class="comic-border"></div>
   <div><img src="images/captain-marvel-comic.png" class="comic-border"></div>
   <div><img src="images/captain-marvel-movie.png" class="comic-border"></div>
</div>
---
## Handdrawn

<img src="images/captain-marvel-drawing.png" width="300" height="400" class="comic-border" style="position: absolute; right: 0; top: -100px">

<canvas data-chart="bar">
<!-- 
{
 "data": {
  "labels": ["SVGZ","OptiPNG","MozJPEG","WebP"],
  "datasets": [
   {
    "data": [32.1,4,5.6,10.4],
    "label": "Filesize for 150x200 in KB","backgroundColor":"rgba(75,65,117,1)"
   },
   {
    "data": [32.1,17,24.6,43.7],
    "label": "Filesize for 450x600 in KB","backgroundColor":"rgba(21,103,174,1)"
   },
   {
    "data": [32.1,38.5,62.5,100],
    "label": "Filesize for 900x1200 in KB","backgroundColor":"rgba(200,56,44,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>
---
## Illustration

<img src="images/captain-marvel-comic.png" width="300" height="400" class="comic-border" style="position: absolute; right: 0; top: -100px">

<canvas data-chart="bar">
<!-- 
{
 "data": {
  "labels": ["SVGZ","OptiPNG","MozJPEG","WebP"],
  "datasets": [
   {
    "data": [840.4,64.1,8.2,8.5],
    "label": "Filesize for 150x200 in KB","backgroundColor":"rgba(75,65,117,1)"
   },
   {
    "data": [840.4,510,55.8,55.7],
    "label": "Filesize for 450x600 in KB","backgroundColor":"rgba(21,103,174,1)"
   },
   {
    "data": [840.4,1710,166,139],
    "label": "Filesize for 900x1200 in KB","backgroundColor":"rgba(200,56,44,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>
---
## Photo

<img src="images/captain-marvel-movie.png" width="300" height="400" class="comic-border" style="position: absolute; right: 0; top: -100px">

<canvas data-chart="bar">
<!-- 
{
 "data": {
  "labels": ["SVGZ","OptiPNG","MozJPEG","WebP"],
  "datasets": [
   {
    "data": [1171,48.5,5.5,4.4],
    "label": "Filesize for 150x200 in KB","backgroundColor":"rgba(75,65,117,1)"
   },
   {
    "data": [1171,361,30.2,21.7],
    "label": "Filesize for 450x600 in KB","backgroundColor":"rgba(21,103,174,1)"
   },
   {
    "data": [1171,1110,85.1,51.3],
    "label": "Filesize for 900x1200 in KB","backgroundColor":"rgba(200,56,44,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>
---
## Animated image formats

<img src="images/judge-dread-cinemagraph.gif" class="comic-border">
---
Animated GIFs have your back! 

<pre><code class="liveCoding xml" data-livecoding-id="format-agif" contenteditable>&lt;img src="images/explosion/explosion.gif"&gt;</code></pre>

<div id="format-agif"></div>
---
But at the same time they are pretty shitty... 💩

<ul>
  <li class="fragment">Only 256 colors supported</li>
  <li class="fragment">Only 1 bit of transparency supported (just on / off)</li>
  <li class="fragment">Huge file sizes</li>
  <li class="fragment">_</li>
</ul>
---
How about using Animated PNG instead? 

<pre><code class="liveCoding xml" data-livecoding-id="format-apng" contenteditable>&lt;img src="images/explosion/explosion.png"&gt;</code></pre>

<div id="format-apng"></div>
---
APNG is supported in every browser!

<ul>
  <li class="fragment">24 bit of colors supported!</li>
  <li class="fragment">8 bit of transparency supported!</li>
  <li class="fragment">Even more humongous file sizes... 💩 (4x GIF)</li>
  <li class="fragment">_</li>
</ul>
---
Motion-JPEG! Old, but gold.

<pre><code class="xml">&lt;img src="http://localhost/
imagery-on-the-web/explosion.mjpeg"&gt;</code></pre>

<div id="format-mjpeg" class="comic-border"><img src="http://localhost/imagery-on-the-web/explosion.mjpeg"></div>
---
Motion-JPEG is supported in every browser!

<ul>
  <li class="fragment">24 bit of colors supported!</li>
  <li class="fragment">No transparency</li>
  <li class="fragment">Okayish file sizes... (a little smaller than GIF)</li>
  <li class="fragment">Needs to be streamed as multipart JPEG-sequence from a server... 💩</li>
  <li class="fragment">_</li>
</ul>
---
Woah, WebP can be animated, too!?!?

<pre><code class="liveCoding xml" data-livecoding-id="format-webp" contenteditable>&lt;img src="images/explosion/explosion.webp"&gt;</code></pre>

<div id="format-webp"></div>
---
WebP is soon to be supported in almost every browser!

<ul>
  <li class="fragment">24 bit of colors supported!</li>
  <li class="fragment">8 bit of transparency supported!</li>
  <li class="fragment">Okayish file sizes... (a little smaller than GIF)</li>
  <li class="fragment">Not supported in Safari 💩</li>
  <li class="fragment">_</li>
</ul>
---
We might have a winner here...

<p class="fragment">Stop! Not so soon.</p>
---
We've forgotten about videos!

```html
<img src="images/explosion/explosion-h264.mp4">
```

<video src="images/explosion/explosion-h264.mp4" data-autoplay loop muted class="comic-border"></video>

<p class="fragment">Sadly, this only works in Safari</p>
---
<ul>
  <li class="fragment">24 bit of colors supported!</li>
  <li class="fragment">No transparency supported</li>
  <li class="fragment">Small file sizes</li>
  <li class="fragment">Using video in `<img>` only supported in Safari 💩</li>
  <li class="fragment">_</li>
</ul>
---
Last but not least...

<img src="images/AV1_logo.svg" width="1390" height="771" class="fragment">
---
AV1 is the next generation video format

```html
<img src="images/explosion/explosion-av1.mp4">
```

<video src="images/explosion/explosion-av1.mp4" data-autoplay loop muted class="comic-border"></video>
---
<ul>
  <li class="fragment">Backed by all of the browser vendors</li>
  <li class="fragment">40-50% better compression than H.264!</li>
  <li class="fragment">Supported by Chrome and Firefox, but not yet Safari 💩</li>
  <li class="fragment"><a href="https://www.singhkays.com/blog/av1-ecosystem-update-july-2019/" target=_blank">There is a polyfill for Safari</a>, though</li>
  <li class="fragment">_</li>
</ul>
---
## Animated format size comparison

<canvas data-chart="bar">
<!-- 
{
 "data": {
  "labels": ["Animated GIF","APNG","WebP","MJPEG","H.264","AV1"],
  "datasets": [
   {
    "data": [10105,39459,9387,8920,2562,1278],
    "label": "Filesize in KB","backgroundColor":"rgba(21,174,25,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>
---
## Bringing it all together

```html
<picture>
  <source type="video/av1" 
    src="images/explosion/explosion-av1.mp4">
  <source type="video/mp4" 
    src="images/explosion/explosion-h264.mp4">
  <source type="image/webp" 
    src="images/explosion/explosion.webp">
    <img src="images/explosion/explosion.gif">
</picture>
```
type="chapter/done"
