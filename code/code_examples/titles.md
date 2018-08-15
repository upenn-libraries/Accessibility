## Code sample for accessible titles

Titles are generally used to convey additional information about elements upon which they're used.  Title attributes should not be redundant with other information on the element, such as link text or image `alt` attributes.

### Accessible examples
The title attribute is used to convey information about the content of the link not otherwise indicated.

Linking to something other than a webpage:
```html
<a href="http://www.library.upenn.edu/publications/a_to_z.pdf" title="PDF document">The Penn Libraries from A to Z</a>
```

Link behaves in a way not predictable by the link text or other adjacent information (opening in a new tab):
```html
<a href="http://hdl.handle.net/0001" target="_blank" title="Opens in a new tab">See this resource in the catalog</a>
```

### Inaccessible examples
The value of title is redundant with the link text:
```html
<a href="search_results.html" title="View search results">View search results</a>
```

The value of title is meaningless:
```html
<a href="login.html" title="click here">Log into My Account</a>
```
