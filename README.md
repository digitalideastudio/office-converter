# Office Converter
#### PHP Wrapper for LibreOffice

Convert offices files to PDF and HTML using LibreOffice or OpenOffice.
Supported conversion formats include:

* pptx => pdf
* ppt => pdf
* pdf => pdf, html
* html => txt
* docx => pdf, odt, html
* doc => pdf, odt, html
* xlsx => pdf
* xls => pdf
* png => pdf
* jpg => pdf
* jpeg => pdf
* tiff => pdf
* tif => pdf
* pps => pdf
* ppsx => pdf

### Installation

It is recommended to install OfficeConverter through [Composer](http://getcomposer.org/).

Run this command within your project directory

```shell
composer require digitalideastudio/office-converter
```

### Dependencies
In order to use OfficeConverter, you need to install [LibreOffice](http://www.libreoffice.org/).

Example for Ubuntu 18.04.2 LTS:

```
apt-get update
apt-get install --no-install-recommends -y ghostscript openjdk-11-jre-headless:amd64 libreoffice
```

### Usage

Here are some samples.

```php
<?php
// if you are using composer, just use this
use NcJoes\OfficeConverter\OfficeConverter;

$converter = new OfficeConverter('test-file.docx');
$converter->convertTo('output-file.pdf'); //generates pdf file in same directory as test-file.docx
$converter->convertTo('output-file.html'); //generates html file in same directory as test-file.docx

//to specify output directory, specify it as the second argument to the constructor
$converter = new OfficeConverter('test-file.docx', 'path-to-outdir');
?>
```

### License
The OfficeConverter package is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

### Feedback & Contribute

Notify me of any issues, bugs, or improvements. Thanks :+1:
