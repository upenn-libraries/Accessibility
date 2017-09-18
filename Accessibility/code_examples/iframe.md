## Code sample for accessible iFrame inclusion

```html
<iframe src="http://hdl.handle.net/0000" title="HathiTrust Digital Library Search" scrolling="auto" />
```

NOTE: Many authoring tools do not specify a `scrolling` value for iFrames by default.  iFrames are inaccessible when the `scrolling` value (the attribute defining whether or not users can scroll within the iFrame) is set to `no`, as assistive devices may change the display of content across the page (for example, dramatically increasing font size on demand) which requires scrolling in order to perceive all included content.  If the value of `scrolling` is not defined, user agents will using the default value of `auto`, which allows scrolling if needed, and is, in most cases, the most accessible option. 
