# Validators

The outputs and the code of an application can be validated.

## XML validation

Applications that work with or produce XML should ensure XML validity. For
simple XML, this may be well-formedness. Often XML documents need to conform
to one or more schema defintions.

There are online, command-line and graphical tools that support validation.

On-line tools are often good for fast testing of XML.

Most tools will verify that an XML file is well-formed. Your environment,
programming language, and schema format will be determine the best tool.
Common schema formats are DTD, XSD, RNG (Relax NG), RNC (Relax NG compressed),
or Schematron.

### Online XML validators

#### <http://www.xmlvalidation.com>

Supports DTD and XSD validation

#### W3CSchools XML validators

- <https://www.w3schools.com/xml/xml_validator.asp>

Validate well-formedness.

- <https://www.w3schools.com/xml/xml_dtd.asp>

Validate against a DTD.

- <https://www.w3schools.com/xml/xml_schema.asp>

Validated against an XSD.

### Command-line/library XML validators

#### `xmllint` (Unix/Linux)

Formats: well-formedness, XSD, DTD

`Xmllint` is included with libxml2. On recent Ubuntu systems (all Debian
distros?) you must install libxml2-utils to get `xmllint`. It can be run as
follows:

    $ xmllint some_file.xml  --noout

#### Saxon (Java, .Net)

Formats: well-formedness, XSD, Schematron

Products:

- <http://www.saxonica.com/products/products.xml>

Saxon is a Java or .Net library that can be run from the command line or used
in code.

- <http://www.saxonica.com/html/documentation/schema-processing/commandline.html>

#### jing (Java)

Formats: RNG, RNC (Java)

Command-line and API.

- <http://www.thaiopensource.com/relaxng/>

#### Other languages

Most languages have libraries available for validating xml:

* Ruby gems
    - Nokgiri - well-formedness, XSD; depends on libxml2
    - lbxml-ruby - XSD, DTD, RNG; depends on libxml2

* Python
    - lxml - XSD, others???; depends on libxml2

## HTML

HTML validation is fraught. Very often HTML validators will treat valid HTML
as invalid. Anyway, if you must, here's an HTML validator:

- <https://validator.w3.org>
