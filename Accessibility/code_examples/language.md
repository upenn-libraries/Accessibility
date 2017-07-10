## Human-readable language specification in HTML

* [IANA language tags registry](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry)

### Examples

#### Single language (document-wide, HTML only; sufficient in most cases)
```html
<html lang="en">
```

#### Single language (document-wide, XHTML & HTML)
```html
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
```

#### In-line language specification

##### Example 1
```html
<p>"<span lang="fr">Bonjour!</span>," the man said.</p>
```

##### Example 2
```html
<div>
<p>Translate this site into <span title="Spanish"><a lang="es" href="qa-html-language-declarations.es">Español</a></span></p>
</div>
```

