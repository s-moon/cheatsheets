# C&#35;

C# (pronounced "C-sharp") is an object-oriented programming language from 
Microsoft that aims to combine the computing power of C++ with the programming 
ease of Visual Basic. C# is based on C++ and contains features similar to 
those of Java. C# is designed to work with Microsoft's .Net platform -- 
[source](http://searchwindevelopment.techtarget.com/definition/C).

### Naming conventions for identifiers
* PascalCase - public
* camelCase - private, protected
* Public classes, methods and properties - PascalCase
* Private helper methods, input parameters - camelCase
* Locally scoped variables - camelCase
* Private field - camelCase prefixed w/ underscore: _firstName
 
Choose long, memorable, understandable names that convey meaning / intent

###Static versus instance members
Static members - no instance of the class required to call method.
 
Instance member - must create an instance w/ new keyword to call
methods and properties.
 
Can mix both in the same class, but can't reference instance
members from inside of static members.
 
Classes can be decaoted w/ static keyword...all members
must be static, can't create a new instance of that class.

### Casting
Implicit conversions - smaller type to larger type without data loss, "upcasting"
 
Explicit conversions - require developer intervention, possibility of data loss, "downcasting", either in the form of cast or using a helper method.
 
#### Casting numbers
```
int myInteger = (int)myDouble;
```
 
#### Numbers to strings
```
string myString = myInteger.ToString();
```
 
#### String to numbers
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
#### Creating new DateTime objects
```
DateTime myDateTime = DateTime.Now;
DateTime myDateTime = DateTime("12/7/1969");
```

#### Formatting ... many options
```
myDateTime.To_____()
```

#### Retrieving Parts
```
myDateTime.Year // int
myDateTime.Hour // int
myDateTime.DayOfWeek // "Monday"
myDateTime.DayOfYear // int 175
```

#### DateTime Math
```
myDateTime.AddHours(3)
myDateTime.AddMinutes(-5)
```

#### "Chaining" = using multiple helper methods together with the dot . operator
```
myDateTime.AddHours(3).AddMinutes(-5).ToString() 
```

### Time
#### Create and initialize new TimeSpans
````
// Days.Hours:Minutes:Seconds.Milliseconds
TimeSpan myTimeSpan = TimeSpan.Parse("1.2:3:30.5");
DateTime myBirthday = DateTime.Parse("12/7/1969");
TimeSpan myAge = DateTime.Now.Subtract(myBirthday);
````

#### Get individual parts
```
myAge.Hours
myAge.Seconds
```

#### Fractional amounts
```
myTimeSpan.TotalDays // double
myTimeSpan.TotalHours // double 
```

### Conditional ternary operator
Shortcut for evaluating an expression and returning a result.
```
result = (a == b) ? "Equal" : "Not Equal";
```

### Formatting strings
#### Concatenate strings
```
+ +=
```
 
#### Format strings
```
String.Format("Hello {0}.  You are from {1}", "Bob", "Chicago")
```
 
#### Format numbers
```
String.Format("Reference Code: {0:000_000-0}", 1234567)
123_456-7
```
 
#### Formatting dates
```
String.Format("REference Date: {0:ddd - d, MM, yyyy}", someDate)
Tue - 5, 07, 2014
```

#### Formatting currency
```
String.Format("Total: {0:C}", totalAmount);
$50,000.00
```

### Single dimensional arrays
Indices are zero based.
 
#### Declaring arrays
```
string[] myArray = new string[3];
```
 
#### Declaring and initializing arrays
```
string[] myArray = new string[3] { "Moe", "Larry", "Curly" };
```
 
#### Setting / getting values
```
string myString = myArray[1]; // Retrieve the second element
myArray[0] = myString; // Sets first element
```

### Multi-dimensional arrays
```
double[,] myArray = new double[2,3]; // contains 6 elements
int[,,] rubicsCube = new int[3,3,3] // contains 27 elements

rubicsCube[0,1,2] = 42;
myInteger = rubicsCube[0,1,2];
``` 

### Changing the length of an array
Arrays are immutable = cannot be changed in memory.
.NET does provide helper functions which allow you to modify them, though.

```
Array.Resize(ref myArray, myArray.Length + 1);
 
// Get the highest index:
int highestIndex = myArray.GetUpperBound(0);

// 0 = dimension we want to retrieve the upper boundary for
 
// Arrays have other helper methods 
myArray.Sum()
myArray.Min()
myArray.Max()
myArray.Average()
 
Array.Sort(myArray)
Array.Reverse(myArray)
```

### Formatted output (C# 6)
```
int x = 5;
System.Console.WriteLine($"{x} is a lovely number.");
```

Written by Stephen Moon (stephen@logicalmoon.com), 2016
