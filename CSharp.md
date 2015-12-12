# C&#35;

C# (pronounced "C-sharp") is an object-oriented programming language from 
Microsoft that aims to combine the computing power of C++ with the programming 
ease of Visual Basic. C# is based on C++ and contains features similar to 
those of Java. C# is designed to work with Microsoft's .Net platform -- 
[source](http://searchwindevelopment.techtarget.com/definition/C).

### Casting

Implicit conversions - smaller type to larger type without data loss, "upcasting"
 
Explicit conversions - require developer intervention, possibility of data loss, "downcasting", either in the form of cast or using a helper method.
 
####Casting numbers
```
int myInteger = (int)myDouble;
```
 
####Numbers to strings
```
string myString = myInteger.ToString();
```
 
####String to numbers
```
int myInteger = int.Parse(myString);
```

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

### Dates
####Creating new DateTime objects
```
DateTime myDateTime = DateTime.Now;
DateTime myDateTime = DateTime("12/7/1969");
```

####Formatting ... many options
```
myDateTime.To_____()
```

####Retrieving Parts
```
myDateTime.Year // int
myDateTime.Hour // int
myDateTime.DayOfWeek // "Monday"
myDateTime.DayOfYear // int 175
```

####DateTime Math
```
myDateTime.AddHours(3)
myDateTime.AddMinutes(-5)
```

####"Chaining" = using multiple helper methods together with the dot . operator
```
myDateTime.AddHours(3).AddMinutes(-5).ToString() 
```

### Time
####Create and initialize new TimeSpans
````
// Days.Hours:Minutes:Seconds.Milliseconds
TimeSpan myTimeSpan = TimeSpan.Parse("1.2:3:30.5");
DateTime myBirthday = DateTime.Parse("12/7/1969");
TimeSpan myAge = DateTime.Now.Subtract(myBirthday);
````

####Get individual parts
```
myAge.Hours
myAge.Seconds
```

#### Fractional amounts
```
myTimeSpan.TotalDays // double
myTimeSpan.TotalHours // double 
```

Written by Stephen Moon stephen@logicalmoon.com, 2015
