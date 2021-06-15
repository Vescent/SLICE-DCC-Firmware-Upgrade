# SLICE-DCC-Firmware-Upgrade
Repository for the latest released firmware for the SLICE-DCC
## Requires 
   Vescent SLICE_Firmware_Upgrade_Utility available at:
  
  https://github.com/Vescent/SLICE-FFC_Firmware_Upgrade_Utility:

## Instructions
  Left click on SLICE_Firmware_Update_Instructions-V1-11.pdf and then click 'Download' to download the instructions for use.  
   
  Left click on SLICE_firmware_update.docx and then click 'Download' to download the instructions for use.

  Left click on the upgrade package (Sx-xx-CCx-xx.zip) and then click 'Download' to download the firmware package to your hard drive.
  
  The two files in the .zip file need to be placed in the folder described in the instructions. DO NOT RENAME THEM!
# Change Log (Most Recent First)
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
 6. Fixes the lack of Interlock Warning display when the device is pwered on while the interlock switch is in an open position

## S1.69 CC1.52 
 1. Revises EEPROM reload function to fix a problem of overrunning RAM on startup which sometimes resulted in a Grey Screen.
 2. Adds a reset line hold to the startup sequence to hold ICE2 boards in reset until power is stable
## S1.68 CC1.51 (Initial Release)
 
