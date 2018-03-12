# Guidelines for Making Applications Accessible

## Level 1: What must be done
This level is defined as measures that are required for an application to be considered accessible. 

### Common Sense Navigation is Key
- Give your site a navigable hierarchy. The more orderly your content is, the easier it is to navigate with a keyboard and screen reader.
  - Use proper heading tags (`<h1>`, `<h2>`, etc) to structure your page, and don't break that hierarchy!
- Use descriptive links.
  - Links should make sense when read out of context. Don't label links "click here." Use descriptive language: "borrowing from the Libraries", "search the online catalog", etc.
- Provide a description of all images in an `alt` attribute.
  - The `alt` attribute allows you to convey to all users the content and meaning of your page. For example: `<img src="vanpelt.jpg" alt="Van Pelt Library">`
  - For images that don't contain content (such as decorative images and visual flourishes), leave the `alt` attribute empty so screen readers won't notice it.
- Indicate your content's language with the HTML `lang` attribute, otherwise screen readers might read in the wrong language. Read more here: [Using the HTML lang attribute](https://www.paciellogroup.com/blog/2016/06/using-the-html-lang-attribute/)

### Don't Re-Invent the Wheel! (And when you do, _do it right!_)
- Use semantic HTML whenever possible. Native HTML elements are accessible by default, so use them instead of reinventing the wheel.
  - Read more: [HTML5 Accessibility Chops: Just use a (native HTML) button](https://www.paciellogroup.com/blog/2011/04/html5-accessibility-chops-just-use-a-button/)
- But, sometimes we have custom components that don't exist natively. When this happens, we need to take extra care in making sure we build that component accessibly; ARIA roles can help with this.
  - Make sure you're using ARIA roles correctly; check out 5 rules of ARIA use in [W3's Notes on Using ARIA in HTML](https://www.w3.org/TR/2015/WD-aria-in-html-20150521).
  
## Level 2: What should also be done
This level is defined as measures, on top of those taken in Level 1, that should be done to make an application accessible beyond baseline measures.

### Colors Galore
- Use high contrast text/background combinations with little or no pattern in background.
  - Avoid red/green backgrounds, and other combinations that are hard to see when colorblind. [Make sure your color combinations meet accessibility standards.](http://leaverou.github.io/contrast-ratio/)
- Don't rely solely on color to convey meaning. Make sure that charts, graphs, and other visualizations still make sense _without_ color as a guide.

## Level 3: What may be done
This level is defined as measures that may be taken to enhance accessibility of an application, but that are not a requirement for the application to be accessible.

### Test, Test, Test!
- There is no replacement for testing your site. Accessibility Validators will help you knock out low hanging fruit, but the only way to _really_ be sure your site works is to actually try using it. Hide your mouse, turn on JAWS, and try navigating your site. Give extra attention to custom components.
- Ideally, you should find actual end users and have them test your site out. A developer and an actual user have vastly different perspectives and will behave accordingly.