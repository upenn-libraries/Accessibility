## Do use semantic tags to expose the structure of your document.  
   Do not use semantic tags as a shortcut for formatting.
Semantic tags often come with a default look. 
- If you don't like the default look, use CSS to get rid of it. Don't ditch the tag!
- If you do want the look but the tag doesn't describe your content, use CSS to duplicate the look. Ditch the tag! 

## Give screenreaders a quick outline of your page with H-tags and A-tags 
### H-tags are not a font size
- A sighted user understands the  structural hierarchy of a page with a glance at page titles.

- A person using a screen reader expects to get the same quick outline by jumping through the H-tags. So it's important to maintain the hierarchy. 
     ** H1** should be the tag for the page title.  
      **H2** should be used for boxes or columns (if you have them). If you're using a content management system like LibGuides, these headings are already provided.  
      **H3** will usually be the top tag for your own content structure.  

- If you want your headings to be extra big or colorful, it's easy. Use CSS:  
   ```html
<h3 style="font-size: 33px; color: red">About Our Locations</h3>
   ```
