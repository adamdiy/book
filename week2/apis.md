#Web APIs, AJAX, JSON and jQuery

###Constructing a Web page

As we have already discussed, Web pages are increasingly constructed from disparate resources: images, video, stylesheets, JavaScript and data all served from different servers and pulled into the page with single-line calls from within the HTML source of the page.

###AJAX applications

The term AJAX, which  stands for _Asynchronous JavaScript And XML_, (XML: Extensible Markup Language)   was [coined in 1995](http://www.adaptivepath.com/ideas/ajax-new-approach-web-applications/) to describe the approach to building web applications pioneered by companies like Google.

In an AJAX application, a web page can be populated with content even after the page has loaded, often in response to user input. It can greatly speed up the interaction between browser and server by allowing complex applications to be run on a single page which updates incremementally. 

Instead of responding to browser requests by sending pages of HTML, a server can send XML--or increasingly JSON--containing just the data required.

JSON (JavaScript Object Notation), is an easy-to-read format for reading and writing data, developed by JavaScript guru Doug Crockford and derived from the syntax for a JavaScript object.

This is all part of a fundamental change in the way the Web is being put together. Many online publishers and service providers are now developing sites based around small well-defined Web services each with their own API. For a wonderful description of how Amazon is developing a service-oriented architecture, read this [great rant by well-known developer and blogger, Steve Yegge](https://plus.google.com/+RipRowan/posts/eVeouesvaVX).

[Here is example](http://api.openweathermap.org/data/2.5/weather?q=london) of some JSON delivered via a Web API (ApplicationPprogramming Interface).

###Using jQuery

jQuery's main uses are for manipulating the DOM and for requesting and parsing JSON.

To make a request, try adding this inside your jQuery event loop:

    $.ajax({
        url: "http://api.openweathermap.org/data/2.5/weather?q=london",
        success: function( data ) {
            $( "#weather" ).html( data.name + " is enjoying " + data.weather[0].description);
        }
    });

And add this somewhere on your blog:

    <div id="weather">Loading weather...</div>

With luck, your page will show the current weather in London.

