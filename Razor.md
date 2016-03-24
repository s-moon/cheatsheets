# Razor

Razor is an ASP.NET programming syntax used to create dynamic web pages with the C# or Visual Basic .NET programming languages.-- 
[source](https://en.wikipedia.org/wiki/ASP.NET_Razor). Some of this has come from [here](http://haacked.com/archive/2011/01/06/razor-syntax-quick-reference.aspx/). 

### Code Blocks
```
@{ 
  int x = 1; 
  string s = "test";
}
```

### Expression (Html Encoded)	
```
<span>
    @model.Message
</span>
```

###Expression (Unencoded)	
```
<span>
    @Html.Raw(model.Message)
</span>
```

###Combining Text and Markup 
```
@foreach(var item in items) {
  <span>@item.Prop</span> 
}
```
 
###Mixing Code and Plain Text 
```
@if (foo) {
  <text>Plain Text</text> 
}
```

###Using Block 
```
@ using (Html.BeginForm()) {
  <input type="text" value="input here">
}
```

###Mixing Code and Plain Text (alternate)	
```
@if (foo) {
  @:Plain Text is @bar
}
```

###Email Addresses	
```
Hi philha@example.com
Razor recognizes basic email format and is smart enough not to treat the @ as a code delimiter
```

###Explicit Expression	
```
<span>
  ISBN@(isbnNumber)
</span>
```

###Escaping the @ sign
```
<span>
  In Razor, you use the 
  @@foo to display the value 
  of foo
</span>
```

###Server side Comment	
```
@*
This is a server side 
multiline comment 
*@
```

###Calling generic method	
```
  @(MyClass.MyMethod<AType>())
```

###Creating a Razor Delegate	
```
@{
  Func<dynamic, object> b = 
   @<strong>@item</strong>;
}
@b("Bold this")
```

###Mixing expressions and text	
```
Hello @title. @name.
```
Written by Stephen Moon, 2016
