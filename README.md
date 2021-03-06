wordpress-pco-api
=================

Provides a WordPress framework for the Planning Center Online API, and includes useful example scripts.

See it in action: [http://beltway.org/worship/what-were-singing/](http://beltway.org/worship/what-were-singing/)

Requirements
------------

You'll need the [PECL OAuth module](http://pecl.php.net/package/oauth) installed on your server.

Usage
-----

When you enable this plugin in WordPress, you'll be able to access a page in the WordPress admin (under Settings > PCO Connection) where you can connect WordPress with your PCO account. Simply enter your Consumer Key and Consumer Secret and you're good to go.

This plugin was really built to provide a very specific feature for my church. If you want to customize it very much, you'll need to edit the underlying code.

The included shortcode pulls the two most recent PCO Plans from a PCO Service and displays all the songs from these plans. I made this functionality in order to build a "What We're Singing" page for our church website that displays the songs from the most recent two Sunday Mornings. It will also display handy links to iTunes, Spotify, or Amazon if visitors would like to donwload those songs (note that the songs and their arrangements must be linked to each third-party service inside PCO).

Here's the shortcode to use the sample script:
`[whatwearesinging servicetype="12345" showauthor="true" showcopyright="false" showmedialinks="true"]`

*servicetype* is the ID of the service you'd like to pull plans from. You can get this number by logging into PCO and looking at the URL of the service type you'd like to pull from.

The other parameters are fairly self-explanatory once you load up the page. Any of the *showXXX* parameters can be either `true` or `false`.
