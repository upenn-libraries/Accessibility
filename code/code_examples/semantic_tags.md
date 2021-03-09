## Do use semantic tags to expose the structure of your document.  
## Do not use semantic tags as a shortcut for formatting.
Semantic tags often come with a default look. 
- If you don't like the default look, use CSS to get rid of it. Don't ditch the tag!
- If you do want the look but the tag doesn't describe your content, use CSS to duplicate the look. Ditch the tag! 

Note. The code snippets below measure screen content in rems. 1rem = 10px. Using rems benefits people with low eyesight if they magnify screen content.

### 1. Give screenreaders a quick outline of your page with H-tags
**H-tags are not a font size**
- A sighted user understands the  structural hierarchy of a page at a glance. A big title sits at the top, and a hierarchy of subtitles is sprinkled through the content. Tables of contents and side issues are often fenced off in columns and boxes.
- A person using a screen reader expects to get the same quick outline by jumping through the H-tags. So it's important to maintain the hierarchy.  
   **H1** should be the tag for the page title.  
   **H2** should be used for boxes or columns (if you have them). If you're using a content management system like LibGuides, these headings are already provided.  
   **H3** will usually be the top tag for your own content structure.  

- If you want your headings to be extra big or colorful, use CSS:  
   ```html
       <h3 style="font-size: 3.5rem; color: red;">My strident header</h3>
   ```
- **_Advanced best practive:_** Use H-tags in addition to strong tags.
   Screen readers are usually set to ignore strong tags (and em tags) because their users find the default voice changes annoying. 
   Sighted users benefit from strong tags, but folks who use screen readers need something more. 
   Use an H-tag. Then preserve your look by providing CSS to keep it inline. Here's an example of a list with a header for each item:
   ```html    
       <ul>
         <li><h3 style="display:inline; margin: 0;"><strong>List item header </strong></h3> and here's some more text</li>
         <li><h3 style="display:inline; margin: 0;"><strong>List item header </strong></h3> and here's some more text</li>
       </ul>
   ``` 

### 2. Provide a quick overview of actions and connections using a-tags, button tags, and form structure.
1. **Buttons and Links**  
Tim Berners Lee invented HTML to connect documents. Connections are the bones of the World Wide Web.    
Users often set screen readers to jump through a list of a-tags on a page. Along with the page title, that scan provides a sense of the page's context within the World Wide Web. If your most important a-tag is coded as a button, it will be missing from that overview.  

   **Use a button tag for an action:** “download,” “sign up,” “log out.”

   **Use an a-tag to link** to a new page or to a different target on the same page.

   **Do not use a button tag to make a link more strident for your sighted users.**   
   If you want to yell at sighted users, you can (you probably shouldn't) style your a-tag as a button:  
   ```html    
       <a href="some-url" style="-webkit-border-radius: .5rem; -moz-border-radius: .5rem; border-radius: .5rem; padding: .5rem 1rem; border: 1px solid #c00; background: red; color: white; text-decoration: none; text-align: center; font-weight: bold; width: 11rem;">About me!</a>
   ``` 
	 
    The snippet above styles an a-tag as a red button with bold white text. Change ```width: 11rem``` to fit your text.

2. **Accessible forms are not discussed here** because they're a subject by themselves. But Submit (or Search or the main form action) should be a button!

### 3. Use semantic tags to indicate inner structure. Again it's all about providing shortcuts to information that a sighted user gets at a glance.
1. **Use tables to present data.**  
   [See WebAIM's discussion of coding accessible tables](https://webaim.org/techniques/tables/data) 
   - It's desirable to provide a caption for a data table. It follows immediately after the table tag: 
   ```html
       <table>
         <caption>Brief description of table content</caption>
   ``` 
 
   - It's essential to provide table header tags (```<th>```). Without table headers, screen readers will give an awkward, annoying account of which data belongs to which column or row. Worse, they cannot indicate the significance of the column-row data structure. That's data without metadata!  
   - If your table has headers both across the top and down the left side, mark them up. 
   ```html
       <table>
           <tr>  
             <th>top header</th>  
             <th>top header</th>  
             <th>top header</th>  
           </tr>  
           <tr>  
             <th>side header</th>  
             <td>data</th>  
             <td>data</th>  
	   </tr>
           <tr>
             <th>side header</th>  
             <td>data</td>  
             <td>data</td>  
           </tr>		
       </table>
   ``` 
   **Do not use tables for layout.**    
   - CSS can provide any layout you desire. If you're at Penn Libraries, the  [Web Unit](mailto:webunit@lists.upenn.edu) will help.  
   - If you're absolutely desperate to use a table for layout, give your table tag the role presentation: 
   ```html
       <table role="presentation">
   ```  
3. **Use blockquote tags to indicate that your content is a quotation.**  
   **Do not use blockquote as a shortcut to indent ordinary text.**   
   Here's the CSS for indented text that matches the look of a blockquote:  
   ```html
       <p style="margin-left: 4rem;">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pharetra metus et ligula laoreet tincidunt. Suspendisse dignissim erat sed dui varius feugiat. Cras non risus quam. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus porttitor ante in neque eleifend, a venenatis turpis efficitur. Pellentesque sed lacus quis arcu mattis congue. Fusce mattis pharetra sodales.</p>
   ``` 
   
5. **Use HTML lists for lists.**  
   - Screen readers announce the list and tell the user how many items it has.   
   - Screen readers distinguish between ordered (numbered) lists and unordered (dotted) lists and so should we. Use numbers if the order is meaningful.  
     
   **If you don't like the default look of an html list, use CSS to dump the look. Don't dump the HTML list structure.**  
   The CSS goes in the ```<ul>``` tag.
   - List items in this ```<ul>``` tag will be indented and will display with no dots.   
     ```html
       <ul style="list-style-image: none; list-style-type: none;">list items inside</ul>
     ```   
   - List items in this ```<ul>``` tag will not be indented and will display no dots.   
     ```html
       <ul style="list-style-image: none; list-style-type: none; margin-left: 0; padding-left: .8rem;">list items inside</ul>
     ``` 

6. **Use the dl-dt-dd list structure for** 
   - **term: definition(s)**
   - **field: value(s)**
   - **FAQ question: answer(s)**
   
   You're not stuck with the default look. You can use CSS to display ```<dt>``` and ```<dd>``` on the same line:
      ```html
       <dl>
         <dt style="float: left; margin-right: 1rem;">Subjects:</dt>
         <dd>Aristotle</dd>
         <dt style="float: left; margin-right: 1rem;">OCLC:</dt>
         <dd>45031325</dd>
       </dl>
     ``` 
   **Don't use dl-dt-dd lists to format hanging indents.** 
   Here's the CSS for that look:
   ```html
       <p style="text-indent: -4rem; margin-left: 4rem;">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc pharetra metus et ligula laoreet tincidunt. Suspendisse dignissim erat sed dui varius feugiat.</p>
   ``` 

