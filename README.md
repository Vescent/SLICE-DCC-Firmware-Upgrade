# SLICE-DCC-Firmware-Upgrade
Repository for the latest released firmware for the SLICE-DCC
## Requires 
   Vescent SLICE_Firmware_Upgrade_Utility available at:
  
  https://github.com/Vescent/SLICE-FFC_Firmware_Upgrade_Utility:

## Instructions
  Follow the link above to download the latest version of the SLICE Firmware Upgrade Utility.

  Left click on SLICE_Firmware_Update_Instructions-V1-42.pdf and then click 'Download' to download the instructions for use.  

  Follow the instructions in the PDF to use the Auto-Download functionality of the SLICE Firmware Upgrade Utility.

### If you do not wish to use Auto-Download:
  Left click on the upgrade package (Sx-xx-CCx-xx.zip) and then click 'Download' to download the firmware package to your hard drive.
  
  The two files in the .zip file need to be placed in the following location on your computer: **C:\Vescent\SLICE\UPGRADE\**.
  DO NOT RENAME THEM!

  Now, run the SLICE Firmware Upgrade Utility, and choose to use the files when they are detected by the program.

# Change Log (Most Recent First)
## S1.109 CC1.72
 1. Adds polarity setting to Trigger In and Trigger Out functionality
 2. Adds Input Trigger Option that latches the operating mode in an OFF state
 3. Fixes 24V power good fault handling to correctly disable channels, capture and report the power output at the moment of the fault
 ## S1.106 CC1.69
 1. Enhanced safety features to assure no current is output from the SLICE-DCC when the GUI indicates an OFF state
 2. Adds “Possible Fault Detected” message if current output is continuously detected after corrective steps have been taken
 3. Fixes Constant Power Mode lack of output current
 4. Fixes Incorrect Enabled state if INTERLOCK button is rapidly touched and then dismissed after closing the interlock circuit.
 5. Changes startup sequence to delay modulation enable until current has ramped up to the setpoint.
 6. Fixes de-shunting of inactive channel
 7. Fixes Trigger In functionality to correct cross channel shunting / de-shunting
 8. Fixes momentary appearance of polarity change when settings are locked.
 9. Changes wording on Trigger In menu to reflect the actual function:
    “Enable / Disable Current Shunt”
 10. Fixes DCC Compliance voltage on unused channel while the other channel is enabled
 11. Adds I2C failure triggered system reset an warning message

## S1.98 CC1.59
 1. GUI responsiveness improved.
 2. USB Device Descriptor now includes Serial Number, to make devices more easily distinguishable in software.
**Note: On Windows PCs, this may cause your device to appear as a different COM Port than it did previously.**
 3. The unit's serial number (as written on the rear panel) is now displayed on the General Settings screen.
 4. Assorted bugfixes.

## S1.82 CC1.58
 1. Changes behavior of I/O Trigger In Enable/Disable Channel functionality to use interrupt driven shunting to control output based on the following when enabled in I/O menu:  
###    Channel Enabled  
       Trigger In Low -> No output shunting (Current flows to load)  
       Trigger In High -> Output shunted (No current flows to load)  
       Trigger In Disconnected -> No output shunting (Current flows to load)  
###    Channel Disabled  
       Trigger In Low -> No output shunting (No current flows to load)  
       Trigger In High -> Output shunted (No current flows to load)  
       Trigger In Disconnected -> No output shunting (No current flows to load)  
 2. Fixes Current surge when channel is enabled just before current ramps up 
 3. Fixes random values and lockups when using the rotary knob to adjust values
 4. Removes the ability to enable a channel through the API CONTROL command when the channel is in an error state
 5. Turns off modulation selection when channels are disabled
 6. Fixes the lack of Interlock Warning display when the device is powered on while the interlock switch is in an open position

## S1.69 CC1.52 
 1. Revises EEPROM reload function to fix a problem of overrunning RAM on startup which sometimes resulted in a Grey Screen.
 2. Adds a reset line hold to the startup sequence to hold ICE2 boards in reset until power is stable
## S1.68 CC1.51 (Initial Release)
 
