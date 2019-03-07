What I learned about Imagery on the Web
======

Talk Slides: [https://schepp.github.io/imagery-on-the-web/](https://schepp.github.io/imagery-on-the-web/)

---

Using images on a website is pretty straightforward, right? It's using an `<img>` element or a CSS background and then have them display a JPG, PNG or SVG. And that's it. Or is there more to it than that? Well, yes, there is. And it's a truckload full of possibilities. I'll take you on a trip starting with uncommon HTML markup, then looking at new image object methods, after which we're gonna a have a closer look at different file formats. And finally I'll cover a bunch of nice CSS tricks for generating and controlling imagery all without the help of JavaScript (or almost).

> Christian Schaefer (https://twitter.com/derSchepp), known as "Schepp", is a freelance frontend developer from Düsseldorf, Germany. Instead of hacking around with JS-Frameworks as almost every other frontend developer currently does, he works on traditional server-rendered component-based systems, uses bleeding edge CSS, has an eye on accessibility as well as the loading and runtime performance of a site. And then he also organizes a meetup (https://www.meetup.com/Webworker-NRW/) and co-hosts a podcast (https://workingdraft.de/).

---

Bilder im Web sind eine einfache Sache, oder? Man verwendet entweder ein `<img>`-Element oder aber einen CSS Hintergrund, referenziert darin ein JPG, PNG oder SVG, und fertig ist die Laube. Oder ist da doch mehr? Natürlich ist da noch mehr! Und zwar endlos viel. Was genau, das zeige ich Euch bei einer Rundreise durch das Thema, bei der ich mit weniger bekanntem Markup beginne, ich Euch dann verschiedene interessante Methoden des Image Objekts zeigen werde, und wir uns anschließend mit den verwendbaren Dateiformaten beschäftigen werden. Zu guter Letzt zeige ich Euch noch allerhand CSS-Tricks, mit denen man Bildwelten generieren und kontrollieren kann - und (fast) ohne JavaScript.  

> Christian Schaefer (https://twitter.com/derSchepp), auch "Schepp" genannt, ist freiberuflicher Frontend-Entwickler aus Düsseldorf. Anstatt mit hippen JavaScript-Frameworks herumzuspielen wie gefühlt sonst fast jeder, arbeitet er an traditionellen, serverseitig gerenderten Komponenten-Bibliotheken und nutzt dabei modernstes CSS, achtet auf Barrierefreiheit und eine rasend schnelle Ladezeit. Außerdem organisiert er ein Meetup (https://www.meetup.com/Webworker-NRW/) und podcastet über Frontend-Themen (https://workingdraft.de/).

---

![Avatar Picture](https://s.gravatar.com/avatar/7096dcb1690ef7418c4e94518f2fed31?s=200) 
 
