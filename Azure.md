
Microsoft Azure /ˈæʒər/ is a cloud computing platform and infrastructure created by Microsoft for building, deploying, and managing applications and services through a global network of Microsoft-managed data centers.

It provides both PaaS and IaaS services and supports many different programming languages, tools and frameworks, including both Microsoft-specific and third-party software and systems.

Azure was announced in October 2008 and released on 1 February 2010 as Windows Azure, before being renamed to Microsoft Azure on 25 March 2014. Along with Amazon Web Services, Azure is considered a leader in the IaaS field.

### Create a VM
```
> az vm create --resource-group azure-mol-chapter4 --name storagevm --image UbuntuLTS --size Standard_B1ms --admin-username azuremol --generate-ssh-keys --data-disk-sizes-gb 64

{
  "fqdns": "",
  "id": "/subscriptions/XXXX/resourceGroups/azure-mol-chapter4/providers/Microsoft.Compute/virtualMachines/storagevm",
  "location": "eastus",
  "macAddress": "XX-XX-XX-XX-XX-XX",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.4",
  "publicIpAddress": "40.XX.169.XX",
  "resourceGroup": "azure-mol-chapter4",
  "zones": ""
}
```

### Add a disk to a VM (same for Linux or Windows)
```
> az vm disk attach --resource-group azure-mol-chapter4 --vm-name storagevm --disk datadisk1 --size-gb 64 --sku Premium_LRS --new
```

### Open a port on a VM
```
> az vm open-port -n name-of-vm -g resource-group --port port-number
```

### Create resource group
```
> az group create --name azure-mol-chapter4 --location eastus
```

### Remove entire resource group
```
> az group delete -n name-of-resource-group
```

### VMs available in a region
```
> az vm list-sizes --location eastus --output table
MaxDataDiskCount    MemoryInMb    Name                    NumberOfCores    OsDiskSizeInMb    ResourceDiskSizeInMb
------------------  ------------  ----------------------  ---------------  ----------------  ----------------------
2                   2048          Standard_B1ms           1                1047552           4096
2                   1024          Standard_B1s            1                1047552           2048
4                   8192          Standard_B2ms           2                1047552           16384
4                   4096          Standard_B2s            2                1047552           8192
...
```
