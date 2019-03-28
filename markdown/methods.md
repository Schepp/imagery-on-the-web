<br><br><br><br><br><br>
# JavaScript Methods
---
## Getting the current responsive SRC

`img.currentSrc`

<div class="fragment">

<pre><code>&lt;picture&gt;
 &lt;source type="image/svg+xml" srcset="images/captain-marvel-illustration.svg"&gt;
 &lt;img src="images/captain-marvel-illustration.png" 
         srcset="images/captain-marvel-illustration.png 2x"
         width="450"
         height="600"&gt;
&lt;/picture&gt;</code></pre>


even within a &lt;picture&gt; element, the &lt;img&gt; is to be addressed

</div>
---
## Loading images

the old fashioned way of loading images:

```js
const img = new Image();
img.onload = () => {
  document.body.appendChild(img); // decode and insert  
};
img.src = '...'; // triggers loading
```
---
## Loading images 2.0

the new way of loading images:

```js
const img = new Image();
img.src = '...';
img.decode().then(function() {
  // This is guaranteed to paint the image without flicker 
  // or decoding jank.
  document.body.appendChild(img);
});
```
---
## Feature test

The modern image format feature test

```js
const image = new Image();
image.src = 'image.webp';
image
  .decode()
  .then(() => {
    console.info('Supports WebP');
  })
  .catch(() => {
    console.warn('No WebP support');
  });
```
---
&lt;/script&gt;