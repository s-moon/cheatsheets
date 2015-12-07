# C&#35;

C# (pronounced "C-sharp") is an object-oriented programming language from 
Microsoft that aims to combine the computing power of C++ with the programming 
ease of Visual Basic. C# is based on C++ and contains features similar to 
those of Java. C# is designed to work with Microsoft's .Net platform -- 
[source](http://searchwindevelopment.techtarget.com/definition/C).

### @
```
string @class = "a variable with a keyword name";
string path = @"c:\normally\slashes\would\escape";
```

### using
```
using (StreamReader rdr = File.OpenText ("file.txt"))
{
    ...
}

is equivalent to:

StreamReader rdr = File.OpenText ("file.txt")
try 
{
    ...
}
finally
{
    if (rdr != null)((IDisposable)rdr).Dispose();
}
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
