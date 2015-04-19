## testing-php
Composer package for PHP unit testing tools, using Phing for Jenkins or local development

### Includes: 
  - phploc
  - pdepend
  - phpmd
  - phpunit
  - phpcpd
  - phpdox
  - phpdoc2
  - phpcs / phpcbf

### Usage:
 - Require this package in your composer.json
 - Add it to your .gitattributes file, to keep the files out of production builds
 - Copy or include the build.xml into your project
 - Enjoy a convenient set of build tools!

Build targets can be run by calling: `phing <target>`
Review build.xml for the targets you can run against your code. 
