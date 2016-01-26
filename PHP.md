# PHP

PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used 
open source general-purpose scripting language that is especially suited 
for web development and can be embedded into HTML 
-- [source](http://php.net/manual/en/intro-whatis.php).

### Accessing Substrings
```
$substring = substr($string,$start,$length);

If $start and $length are positive, substr( ) returns $length characters in the string, 
starting at $start. The first character in the string is at position 0: 

print substr('watch out for that tree',6,5);
out f

If you leave out $length, substr( ) returns the string from $start to the end of the original string: 

print substr('watch out for that tree',17);
t tree

If $start plus $length goes past the end of the string, substr( ) returns all of the string from $start forward: 

print substr('watch out for that tree',20,5);
ree

If $start is negative, substr( ) counts back from the end of the string to determine where 
your substring starts: 

print substr('watch out for that tree', -6);
print substr('watch out for that tree', -17,5);
t tree
out f

If $length is negative, substr( ) counts back from the end of the string to determine 
where your substring ends: 

print substr('watch out for that tree',15, -2);
print substr('watch out for that tree', -4, -1);
hat tr
tre

$username = substr($_REQUEST['username'],0,8)
```

### Creating Timestamps
```
// make a timestamp for Jan 17 2012 at 9.34pm
$ts = mktime(21, 34, 1, 17, 2012);
echo date("d/m/y G:i:s e", $ts);
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
