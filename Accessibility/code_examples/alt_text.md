##Alt text best practices

High quality alt text should adhere to the following guidelines:
* Provide an accurate, short description of the contents of the image, including only pertinent information about the image to the user.
* Not contain extraneous, repetitive phrases such as "image of," "photo of," "portrait of," etc.  In the case of logo images, alt text indicating that the image is a logo (for example ``` alt="Apache logo" ```) may be deemed appropriate at the discretion of the creator.
* If the image is purely decorative, it should be included in the CSS rather than embedded as an ``` <img> ``` tag on the page.  If this is not possible, the alt attribute must be explicitly set to an empty string (see code examples below) in order for screen readers and other assistive devices to ignore it.
* If the image is of text, the alt text for the image should be the value of the text, without any additional information about its physical presentation unless this is pertinent to understanding the meaning of the image.

## Code Examples

Descriptive alt text
```html
<img src="apple_tree.jpg" alt="an apple tree" />
```

Empty alt attribute (image will be ignored by screen readers)

```html
<img src="apache_logo.png" alt="" />
```