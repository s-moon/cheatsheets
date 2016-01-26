# PHP

PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used 
open source general-purpose scripting language that is especially suited 
for web development and can be embedded into HTML 
-- [source](http://php.net/manual/en/intro-whatis.php).

### Accessing Substrings
```
$substring = substr($string,$start,$length);

If $start is negative, substr( ) counts back from the end of the string to determine where 
your substring starts: 
print substr('watch out for that tree', -6);
print substr('watch out for that tree', -17,5);
t tree
out f

$username = substr($_REQUEST['username'],0,8)
```

### Creating Timestamps
```
// make a timestamp for Jan 17 2012 at 9.34pm
$ts = mktime(21, 34, 1, 17, 2012);
echo date("d/m/y G:i:s e", $ts);
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
