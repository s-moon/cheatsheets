
Microsoft Azure /ˈæʒər/ is a cloud computing platform and infrastructure created by Microsoft for building, deploying, and managing applications and services through a global network of Microsoft-managed data centers.

It provides both PaaS and IaaS services and supports many different programming languages, tools and frameworks, including both Microsoft-specific and third-party software and systems.

Azure was announced in October 2008 and released on 1 February 2010 as Windows Azure, before being renamed to Microsoft Azure on 25 March 2014. Along with Amazon Web Services, Azure is considered a leader in the IaaS field.

### Open a port on a VM
```
az vm open-port -n name-of-vm -g resource-group --port port-number
```

### Remove entire resource group
```
az group delete -n name-of-resource-group
```

### VMs available in a region
```
stephen@Azure:~$ az vm list-sizes --location eastus --output table
MaxDataDiskCount    MemoryInMb    Name                    NumberOfCores    OsDiskSizeInMb    ResourceDiskSizeInMb
------------------  ------------  ----------------------  ---------------  ----------------  ----------------------
2                   2048          Standard_B1ms           1                1047552           4096
2                   1024          Standard_B1s            1                1047552           2048
4                   8192          Standard_B2ms           2                1047552           16384
4                   4096          Standard_B2s            2                1047552           8192
...
```
