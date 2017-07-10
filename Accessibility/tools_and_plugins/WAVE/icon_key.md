
![Label missing icon](images/label_missing.png)

| WAVE Icon | What It Means | What To Do | Code Example | 
| --- | --- | --- | --- |
| ![Label missing icon](images/label_missing.png) | A form field without an accessible label is present. | Add a form label with appropriate descriptive text associated with the form field, using the "for" attribute on the label and the "id" attribute on the form field. | ```html
<label for="firstname">First name:</label> 
<input type="text" name="firstname" id="firstname" />
``` |