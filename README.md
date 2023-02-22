EFI for HP Elitebook 850 G7 - Monterey 
=============


## How to use

Generate correct SMBIOS for `MacBookPro16,2` using this guide: [Generate a new Serial](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial)
and replace "YOUR_SERIAL", "YOUR_BOARD_SERIAL", and "YOUR_SMUUID" in the conflig.plist with your MLB, Serial, and SmUUID.

## Disabling sleep

To disable sleep run:

```bash
sudo pmset -a sleep 0
sudo pmset -a hibernatemode 0
sudo pmset -a disablesleep 1
```

## Color profile

By default the 850 G7 has an oversaturated colors. To fix it go to System Preferences -> Displays -> Color, uncheck the "Show profiles for this display only" checkbox and select the "sRGB IEC61966-2.1" display profile.

## Working:

- iGPU
- Video over USB-C (HDMI/DisplayPort)
- Intel Wifi
- Bluetooth (tested only Apple devices, other should work too)
- Audio
- Keyboard & touchpad
- FileVault
- iMessage and FaceTime
- Handoff, unlocking with Apple Watch etc (no AirDrop though)

If you can change your wifi to CS2 Macbook Wifi card (BCM94360CS2) , so you can able to use Airdrop too. Disable Bluetooth and Intel Wifi related kext if you encounter any problems when you change the card. 

## Not working:

- Camera (might work for you, depends on model/vendor)
- Microphone
- HDMI port (currently buggy)
