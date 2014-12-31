Jade
====

A [Ghost](http://github.com/tryghost/ghost/) theme loosely based on a [Website](https://github.com/hxkclan/hxkclan.github.io) i made earlier.

#Design & features
- Loosely based on [Material Design principles](http://www.google.com/design/spec/what-is-material/environment.html); so simple, no fuss, it just works.
- No header image - it's just plain and simple
- Shows post date/tags in post header
- Shows author info at bottom of each post
- Shows pagination when available (aka when there are enough posts)
- Seperated parts of the code in 'partials', more on this later.

#Stuff used
Jade uses the following libraries;
- [Bootstrap](https://github.com/twbs/bootstrap)
- [jQuery](https://github.com/jquery/jquery) (included within Ghost)

#Preview
This theme is currently under (heavy) development. So it changes, stuff gets added etc. The master branch usually has a version that is at least usable. 

![Jade Preview v0.4.1 - Home](http://img.photobucket.com/albums/v385/hxkclan/github/Screenshotfrom2014-12-31001835.png)
![Jade Preview v0.4.1 - Author part within post](http://img.photobucket.com/albums/v385/hxkclan/github/Screenshotfrom2014-12-31002026.png)

#Use
- Download the package
- Place the jade theme folder inside your 'content/theme' folder
- Restart your Ghost instance to see the new theme and apply it.

#Customization - partials
##Disqus
To use disqus; create jade/partials/disqus.hbs. Parse the full 'disqus universal' code in there.

##Google Analytics
To use Google Analytics, please create a file (jade/partials/analytics.hbs) and parse your full script code in it. 

##Header 
The header.hbs partial (jade/partials/header.hbs) basically consists of two parts. The first p tag is the actual header with the blog title. The second line (about div) involves a call to the modal (question mark top right), so you could remove it, but i would appreciate it if you would keep it there for reference. 

##Modal
The actual modal is called from inside /jade/partials/default.hbs (infomodal). Which references the file jade/partials/infomodal.hbs. If you really want to remove the modal completely you can;
- remove jade/partials/infomodal.hbs
- remove the modal reference in default.hbs
- remove the question mark from jade/partials/header.hbs
