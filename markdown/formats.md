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
</ul>
---
Motion-JPEG! Old, but gold.

<pre><code class="liveCoding xml" data-livecoding-id="format-mjpeg" contenteditable>&lt;img src="http://mjpeg.sanford.io/count.mjpeg"
  width="200"
  height="200"&gt;</code></pre>

<div id="format-mjpeg" class="comic-border"></div>
---
Motion-JPEG is supported in every browser!

<ul>
  <li class="fragment">24 bit of colors supported!</li>
  <li class="fragment">No transparancy</li>
  <li class="fragment">Okayish file sizes... (a little smaller than GIF)</li>
  <li class="fragment">Needs to be streamed as multipart JPEG-sequence from a server... 💩</li>
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
</ul>
---
We might have a winner here...

<p class="fragment">Stop! Not so soon.</p>
---
We've forgotten about videos!

<pre><code class="liveCoding xml" data-livecoding-id="format-mp4" contenteditable>&lt;video src="images/explosion/explosion-h264.mp4" 
  autoplay 
  muted&gt;</code></pre>

<div id="format-mp4"></div>

<p class="fragment">Since recently, you can use MP4 video in IMG elements in safari as well!</p>
---
