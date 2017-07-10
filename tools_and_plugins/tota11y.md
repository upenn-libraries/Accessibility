# [tota11y](http://khan.github.io/tota11y/) - an accessibility visualization toolkit

[tota11y](http://khan.github.io/tota11y/) is a free browser plugin that allows you to quickly visualize how your site performs with assistive technologies. It's essentially a beginner-friendly accessibility validator. It's great for doing quick checks because it's always available in your browser bookmarks.
You can play with a demo on tota11y's homepage: http://khan.github.io/tota11y/

## Installation
Getting started is easy; you don't even have to install anything. You simply add the plugin to your bookmarks. Bookmark the following link, or drag it up into your bookmarks toolbar:

<a class="bookmarklet" href="javascript:(function(){var%20tota11y=document.createElement('SCRIPT');tota11y.type='text/javascript';tota11y.src='//khan.github.io/tota11y/tota11y/build/tota11y.min.js';document.getElementsByTagName('head')[0].appendChild(tota11y);})();" onclick="javascript:return false;">tota11y</a>
<style>
.bookmarklet {
    border-radius: 5px;
    border: 3px solid #333;
    display: inline-block;
    font-weight: bold;
    margin: 10px 0;
    padding: 10px 25px;
    text-decoration: none;
}
</style>

## Usage
In your browser, open the page you want to visualize. Then, click on the tota11y bookmark. A small grey tab will appear in the bottom-left corner of the page; clicking that tab opens a toolbar.

The toolbar contains a self-explanatory list of tools; the tools are labeled with clear descriptions in case you forget what they do. Click a tool to toggle it on/off.

There are options to view heading structure, color contrast, link text, labels, alt-text, and ARIA landmarks. If there are problems with any of these on the page, tota11y will point out where and provide details about what is wrong.

There is also a "Screen Reader Wand" that allows you to hover over an element and preview how it would be seen by a screen reader. This is not as good as doing actual testing with a screen reader, but it's a low-barrier entry to such practices.
