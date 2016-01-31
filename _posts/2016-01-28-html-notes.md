---
layout: post
title:  "HTML NOTES"
date:   2016-01-24
categories: notes
permalink: html-notes
---

# [HTML5 Notes](http://creative.colorado.edu/~schaal/web/pdf/web-html5.pdf)

HTML, CSS and JavaScript are the core languages of the web - forming the backbone of all websites and web content. CSS controls how a page looks, JavaScript controls how a page behaves, and HTML provides the essential structure and content of a web page.


HTML is a markup language. It’s not a programming language because it doesn’t understand logic. HTML contains information about the structure, content and display of a document.

# HTML Tags
HTML is made up of tags. Tags are used to mark up the content and give the browser information about how to display the text. Tags are simply short pieces of text starting with the less-than sign `<` and ending with the greater-than sign `>`. Tags are used to mark up the start and end of an HTML element.

{% highlight html %}
<p></p>
{% endhighlight %}

For a complete list of all HTML tags, see the [w3school's HTML Element Reference](http://www.w3schools.com/tags/).

# HTML elements
An element represents some kind of structure or semantics and generally consists of a start tag, content, and an end tag. This is a paragraph element:

{% highlight html %}
<p>This is the content of the paragraph element.</p>
{% endhighlight %}

# HTML attributes
Some tags also have attributes associated with them, attributes define a property for an element. They appear in the start tag.

{% highlight html %}
<p lang='en'>This is the content of the paragraph element.</p>
{% endhighlight %}


# The Skeletal System
There are a few main tags that every web page must have - html, head, title, and body. The very simplest web page looks like this in text view:

{% highlight html %}
<!DOCTYPE HTML>
<html>
	<head>
 		<meta charset=”utf-8”>
		<title>The name of my page</title>
	</head>

	<body>
		<p>Some information here.</p>
	</body>
</html>
{% endhighlight %}


# URLs
Every page and every image on a website has a ***URL*** (or Uniform Resource Locator). <br>The URL is made up of the **domain name** such as `creative.colorado.edu` followed by the **path** to that page or image, like `/~identikey/my-page.html`. The complete URL would look like: `creative.colorado.edu/~identikey/my-page.html`

# Site Structure & Navigation
+ Every page and every image on a website has a URL
+ Every website is built inside directories on a web server
+ Each web page is a separate file on that web server (ending in .html or .js)
+ Sometimes when you go to a URL, there is no file listed in the URL 
+ For example, we type: `colorado.edu` instead of `colorado.edu/index.html`

# index.html
This is default HTML file that appears in a browser when a user invokes a URL, it is the main homepage of a site. Every directory should have an index.html page for usability and security purposes.

# Links
One of the most improtant tags, the `<a>` tag, defines a hyperlink, which is used to link from one page to another. The most important attribute of the `<a>` element is the href attribute, which indicates the link's destination.

Links are created using the `<a>` element; users can click on anything between the opening `<a>` tag and the closing `</a>` tag. You specify which page you want to link to using the `href=""` attribute.

{% highlight html %}
<a href="http://www.w3schools.com">Visit W3Schools.com!</a>
{% endhighlight %}

The `<a>` tag requires an attribute of ‘href’, which is short for hyperlink reference — this is where you put the URL of the link. You can link to a page on your own site or to an external page.

# Absolute Links
A hyperlink containing a full URL, which includes all the information needed to find a particular site, page or document or other addressable item on the Internet. This information includes the protocol to use, such as HTTP (Hypertext Transfer Protocol) or FTP (File Transfer Protocol).

{% highlight html %}
<a href="http://www.colorado.edu/">Colorado.edu</a>
{% endhighlight %}

# Relative Links
Used when linking to pages within your own website. they provide a shorthand way of telling the browser where to find your files. If you are linking to a page within your own site, it is best to use relative links rather than absolute links or qualified URLS.

{% highlight html %}
<a href="music/listings.html">Listings</a>
{% endhighlight %}

To move **IN** a directory, use a backslash `/` notation, the directory name and the file name:
{% highlight html %}
movies/cinema/listings.html
{% endhighlight %}

To move OUT a directory, use the following notation:  `../`
{% highlight html %}
../../index.html
{% endhighlight %}

# Google Web Fonts
Visit [google.com/fonts](https://www.google.com/fonts) and choose a font to use, then click the middle button (the quick use option). Follow their directions:

1. Choose the style you want
2. Choose the character set you want (you can usually skip this)
3. Add the link code inside the head tags of your html page
4. Integrate your css - either on an external stylesheet or within a style tag within the html code

On your .html page, you will have something like this in the `<head>` tag:
{% highlight html %}
<link href='https://fonts.googleapis.com/css?family=Open+Sans' rel='stylesheet' type='text/css'>
{% endhighlight %}

And you will add the css within a `<style>` tag on the html page or on an external .css stylesheet:
{% highlight html %}
<style>
	body {
		font-family: 'Open Sans', sans-serif;
	}
</style>
{% endhighlight %}

# Font Awesome Icons
Paste the following code into the `<head>` section of your site's HTML. This link can also be found on the [Get Started Page](http://fortawesome.github.io/Font-Awesome/get-started/) on Font Awesome.
{% highlight html %}
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
{% endhighlight %}

Then, choose what icon you want to use and just copy and paste the code in your html. It will look something like this:
{% highlight html %}
<i class="fa fa-fort-awesome"></i>
{% endhighlight %}

# HTML video tag
The `<video>` tag is a new addition in HTML5; prior to this, there was no standard for showing videos on a web page. Before HTML5, videos could only be played with a plug-in (like flash). The `<video>` element specifies a standard way to embed a video in a web page.

To use the video element, you should save a .mp4 and .ogg video file in the same directory where your .html page is saved. Then you can create a relative link to the file (like in the code below). 

{% highlight html %}
<video width="320" height="240" controls>
	<source src="my-video.mp4" type="video/mp4">
	<source src="my-video.ogg" type="video/ogg">
	Your browser does not support the video tag.
</video>
{% endhighlight %}

The **controls** attribute adds video controls, like play, pause, and volume.

It is a good idea to always include **width** and **height** attributes.

If height and width are not set, the browser does not know the size of the video. The effect will be that the page will change (or flicker) while the video loads.


# HTML audio tag
The `<audio>` tag is very similar to the video tag. To use this element, save an audio file (.mp3 and .ogg) to the same directory where your .html page is saved.


{% highlight html %}
<audio controls>
	<source src="audio.ogg" type="audio/ogg">
	<source src="audio.mp3" type="audio/mpeg">
	Your browser does not support the audio tag.
</audio>
{% endhighlight %}

