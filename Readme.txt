Dell Vostro 3578 (macOS Ventura 13.7.7)
Original sources: https://github.com/winofwin292/hackintosh-dell-vostro-3578
OpenCore v1.0.6

Specs:
    - CPU: Intel Core i5-8250U
    - GPU: Intel UHD 620
    - Memory: 8GB DDR4 2400MT/s
    - Wireless/BT: Intel AX200

What's working:
    - Display (1366x768) with QE/CI
    - Brightness (Can be controlled by pressing Fn + F11/F12)
    - Battery Indicator
    - Sleep 
    - Trackpad (I2C, HID)
    - HDMI with 60Hz or higher with audio "Untested because my Monitor does not have speaker"
    - VGA Port
    - Webcam
    - Headphones, Microphone (Onboard)
    - Internet with cable
    - USB
    - Secure Digital Card (SDCard) "Untested because my SD Card slot has been broken :("
    - USB mapped

Issues:
    - Bluetooth does not work well
    - Cannot update to macOS Sonoma, Sequoia, Tahoe even use supported SMBIOS
    - Continuity features does not work due to Intel cards

Things to do after installed macOS:
    - Put EFI Folder to EFS Partition by using Opencore Configuration or OCAT
    - Re-generate SMBIOS: Serial Number, SMUUID, Board-ID and Broad Serial Number
    - Upgrade your Wifi card from DW1810 or Intel 3165 to Intel AX200 or AX210 "DW1810 does not work,  you must replace your wifi card"
    - If your laptop has dGPU you must disable it
    - Remove -v boot-args if you don't want verbose mode while booting
