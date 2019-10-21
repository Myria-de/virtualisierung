# Virtualisierung
Scripts &amp; Tipps zu Virtualbox &amp; Co

**Skripte/Konfiguration herunterladen:**

Klicken Sie die gewünschte Datei an, kopieren Sie den Text in einen Editor und speichern Sie die Datei.

Oder Sie klicken auf "RAW" und speichern die Datei dann vom Browser aus, in Firefox beispielsweise über die Tastenkombination Strg-S.

Dateien und Skripte müssen Sie unter Linux im Terminalfenster ausführbar machen:

`chmod +x [Skript-Datei]`

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
