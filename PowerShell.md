# PowerShell Cheat Sheet

### List available verbs
```
> Get-Verb
Verb        Group         
----        -----         
Add         Common        
Clear       Common        
Close       Common
...
```
### Show commands that match a pattern
```
> Get-Command *ip*
Application     cscript.exe                                        5.812.1... C:\WINDOWS\system32\cscript.exe                     
Application     gpscript.exe                                       10.0.17... C:\WINDOWS\system32\gpscript.exe                    
Application     ipconfig.exe                                       10.0.17... C:\WINDOWS\system32\ipconfig.exe
...
```

### Getting help
```
> Get-Help Command
> Get-Help *Pattern*
> Get-Help Command -Detailed
> Get-Help Command -Examples
> Get-Help Command -Online
```

### Updating help
```
> Update-Help
```

### List available modules
```
> Get-Module -ListAvailable
```
