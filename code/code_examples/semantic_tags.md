## Do use semantic tags to expose the structure of your document.  
## Do not use semantic tags as a shortcut for formatting.
Semantic tags often come with a default look. 
- If you don't like the default look, use CSS to get rid of it. Don't ditch or modify the tag!
- If you do want the look but the tag doesn't describe your content, use CSS to duplicate the look. Ditch the tag! 

### 1. Give screenreaders a quick outline of your page with H-tags
**H-tags are not a font size**
- A sighted user understands the  structural hierarchy of a page at a glance. A big title sits at the top, and a hierarchy of subtitles is sprinkled through the content. Tables of contents and side issues are often fenced off in columns and boxes.
- A person using a screen reader expects to get the same quick outline by jumping through the H-tags. So it's important to maintain the hierarchy.  
   **H1** should be the tag for the page title.  
   **H2** should be used for boxes or columns (if you have them). If you're using a content management system like LibGuides, these headings are already provided.  
   **H3** will usually be the top tag for your own content structure.  

- If you want your headings to be extra big or colorful, use CSS (note: 1rem = 10px):  
   ```html
       <h3 style="font-size: 3.5rem; color: red;">About Our Locations</h3>
   ```
- **_Advanced best practive:_** Use H-tags in addition to strong tags.
   Screen readers are usually set to ignore strong tags (and em tags) because their users find the default voice changes annoying. 
   Sighted users benefit from strong tags, but folks who use screen readers need something more. 
   Use an H-tag. Then preserve your look by providing css to keep it inline. Here's an example of a list with a header for each item:
   ```html
       <ul>
         <li><h3 style="display:inline; margin: 0;"><strong>List item header </strong></h3> and here's some more text</li>
         <li><h3 style="display:inline; margin: 0;"><strong>List item header </strong></h3> and here's some more text</li>
       <ul>
   ``` 

## 2. Provide a quick overview of actions and connections using a-tags, button tags, and form structure.
Actions and connections are the basis for the internet. Screen readers can give their users an overview - if you let them.
