чтобы поднять виртуалку необходимо выполнить команду
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

где userdata.yaml - cloud-init файл ( доки по его заполнению: https://cloudinit.readthedocs.io/en/stable/reference/examples.
tml


