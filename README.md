### чтобы поднять виртуалку необходимо выполнить команду
```
.\New-HyperVCloudImageVM.ps1 `
    -CustomUserDataYamlFile "userdata.yaml" `
    -VMProcessorCount 2 `
    -VMMemoryStartupBytes 2GB `
    -VHDSizeBytes 10GB `
    -VMName "debian2" `
    -ImageVersion "12" `
    -VMGeneration 2 `
    -ShowSerialConsoleWindow `
    -KeyboardLayout en `
    -ShowVmConnectWindow `
    -VMMachine_StoragePath "$env:ProgramData\hyperv-vm-provisioning"
```

где userdata.yaml - cloud-init файл ( доки по его заполнению: https://cloudinit.readthedocs.io/en/stable/reference/examples.
tml

```
.\New-HyperVCloudImageVM.ps1 `
    -VMProcessorCount 2 `
    -VMMemoryStartupBytes 2GB `
    -VHDSizeBytes 8GB `
    -VMName "debin-static" `
    -ImageVersion "12" `
    -VirtualSwitchName "SWBRIDGE" `
    -VMGeneration 2 `
    -VMMachine_StoragePath "D:\HyperV" `
    -NetAddress 192.168.2.22/24 `
    -NetGateway 192.168.2.1 `
    -NameServers "192.168.2.1" ` 
    -ShowSerialConsoleWindow 
    -ShowVmConnectWindow
```

