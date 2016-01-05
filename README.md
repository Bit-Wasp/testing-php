## testing-php
Composer package for PHP unit testing tools, using Phing for Jenkins or local development
Includes: 
  - pdepend
  - phpmd
  - phpunit
  - phpcs / phpcbf

#### Installation:
This package should be installed via composer, which takes care of loading dependencies appropriate for
your build. 

`composer require bitwasp/testing-php`

or add it to your composer.json:
```...
    "require": {
        "bitwasp/testing-php": "@stable"
    }
...
```

### Usage:
Build targets can be run by calling: `phing <target>`
Review build.xml for the targets you can run against your code. 

#### Import this build script:
The simplest way to get started is to import this projects build.xml file in your own build.xml.
  The only thing you need to change here is YOUR-PACKAGE-NAME. 
  The rest of the file simply configures the binary tools directory, which you must change if you keep them somewhere other than the composer default (vendor/bin)
  The builddir should be kept the same.

```
<?xml version="1.0" encoding="UTF-8"?>

<project name="YOUR-PACKAGE-NAME" default="build">

    <property name="toolsdir" value="${project.basedir}/vendor/bin"/>
    <property name="builddir" value="${project.basedir}/build/"/>

    <import file="vendor/bitwasp/testing-php/build.xml" />
</project>
```

#### Or roll your own:
Refer to the build.xml, or the documentation of the respective tools. 
You can import the default build.xml and extend it with your own functionality as required, or take whatever interests you. 
