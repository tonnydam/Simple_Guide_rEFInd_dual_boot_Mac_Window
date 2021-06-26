### Simple guide for rEFInd and Opencore
 - Why use rEFInd for dual boot? Avoid opencore apply ACPI on Window.
 - Best way to dual boot on same hard drive or on separate hard drives.
 - Step 1: Move EFI/BOOT/BOOTx64.efi to OC/BOOTx64.efi
 - Step 2: Overwrite this BOOT folder to EFI/BOOT
 - Step 3: Move Microsoft to EFI/Microsoft (if it's on other hard drivers, move to the same hard drives with rEFInd)
 - Step 4: Boot to Window, open cmd (windows command prompt) and type: bcdedit /set "{bootmgr}" path \EFI\BOOT\BOOTx64.efi (make sure "{bootmgr}" is inside quotes, otherwise it will not work)
 - Step 4-1: If you want to restore this step, type: bcdedit /set "{bootmgr}" path \WINDOWS\system32\winload.efi
 - That's all.
 - Auto boot to rEFInd and auto select OS, with mouse/keyboard support.


### Config rEFInd, edit refind.conf

 - timeout << change timeout
 - default_selection "Windows 10" << default boot to window, change to: default_selection "MacOS" if you want MACOS.
