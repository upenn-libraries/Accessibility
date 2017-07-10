## Links
Link text should adhere to the following guidelines:
* The text of the link should describe the link target (the ```href``` attribute value).  Some assistive technologies allow users to navigate by cycling through all of the links on a page, so nondescriptive, repetetive link text such as "click here" or "learn more" is insufficient and should not be used. 
* If the link behaves differently than a standard HTML link (for example, opening in a new tab or opening an email client), this must be indicated either in the text of the link or in the "title" attribute.
* If the link target a non-web document (for example, a PDF, Word document, or Powerpoint presentation), this must be indicated in the link text, the title and/or title attribute.  Ideally, an icon next to the linked document indicating the type of document being linked to should also be included.

## Examples

### Appropriate link text

```html
<a href="about_vp.html">About Van Pelt Library</a>
```
### Opens in a new tab

#### Example 1 (title attribute)

```html
<a href="larger_view.html" target="_blank" title="opens in a new tab">View larger image</a>
```

#### Example 2 (link text)

```html
<a href="larger_view.html" target="_blank">View larger image (opens in a new tab)</a>
```

### Linking to a PDF

#### Example 1 (title attribute)

```html
<a href="annual_report.pdf" title="PDF document">Annual Report</a>
```

#### Example 2 (link text)

```html
<a href="annual_report.pdf">Annual Report (PDF)</a>
```