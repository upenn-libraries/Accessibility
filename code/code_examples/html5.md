## Code samples for accessible HTML5 elements

HTML5 elements can make websites more accessible, as they provide informational wrappers for elements on the page, informing user agents what sort of content is in these containers, and potentially how they behave.  Examples include navigation elements, headers, footers, physical address information, supplemental information, and more.  See examples below.

### HTML5 `nav` elements
For elements that provide navigation on a page and/or across the site:
```html
<nav role="navigation">
  <ul>
    <li>Library Info</li>
    <li>Facilities</li>
    <li>Research</li>
    ...
  </ul>
</nav>
```

### HTML5 `footer` element
For elements that contain footer information, which occur in the footer of the page (appropriately near the end of source code).  More than one footer element can occur on a page if necessary:
```html
<div class="blog-post">
  ...
  <footer>Published 2:48PM, 9/18/17</footer>
</div>
...
<footer>
  <p>Powered by <a href="https://drupal.org">Drupal</a></p>
</footer>
```
