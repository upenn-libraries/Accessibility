## Code samples for accessible headings

While it is no longer considered inaccessible to have more than one h1 tag on the page, **the `h1` tag should generally be used once per page,** representing the title or heading of the main content of the page.  Using more than one instance per page will trigger warnings if not failures in most accessibility validators.

The page title in the **h1 tag** should duplicate the title in the **`html head`** of the page.
```html
<html>
  <head>
    <title>Title of page</title>
  </head>
  <body>
    <h1>Title of page</h1>
    <p>Content</p>
  </body>
</html>
```


Headings should occur in numerical order without skipping levels.  See examples below.

Accessible example:

```html
<h2>About Our Locations</h2>
  <h3>Van Pelt Library</h3>
    <h4>Mailing Address</h4>
    <h4>Hours of Operation</h4>
  <h3>Kislak Center</h3>
    <h4>Mailing Address</h4>
    <h4>Hours of Operation</h4>
```

Inaccessible examples:

Goes 1, 3, 4; skips level 2:
```html
<h1>About Our Locations</h1>
<h3>Van Pelt Library</h3>
  <h4>Mailing Address</h4>
  <h4>Hours of Operation</h4>
<h3>Kislak Center</h3>
  <h4>Mailing Address</h4>
  <h4>Hours of Operation</h4>
```
