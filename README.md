# Virtualisierung
Scripts &amp; Tipps zu Virtualbox &amp; Co
```
#!/bin/bash
# Code fuer die Konfiguration von Mac OS in Virtualbox
echo "Starte VM-Konfiguration MacOS"
vboxmanage modifyvm "MacOS" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
vboxmanage setextradata "MacOS" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac11,3"
vboxmanage setextradata "MacOS" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"
vboxmanage setextradata "MacOS" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"
vboxmanage setextradata "MacOS" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"
vboxmanage setextradata "MacOS" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1
vboxmanage setextradata "MacOS" "VBoxInternal2/EfiGraphicsResolution" "1024x786"
# oder beispielsweise # vboxmanage setextradata "MacOS" "VBoxInternal2/EfiGraphicsResolution" "1920x1080"
echo "VM-Konfiguration beendet"
```
