# PHP

PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used 
open source general-purpose scripting language that is especially suited 
for web development and can be embedded into HTML 
-- [source](http://php.net/manual/en/intro-whatis.php).

### Creating timestamps
```
// make a timestamp for Jan 17 2012 at 9.34pm
$ts = mktime(21, 34, 1, 17, 2012);
echo date("d/m/y G:i:s e", $ts);
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
