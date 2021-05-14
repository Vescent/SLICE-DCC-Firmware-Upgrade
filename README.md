# SLICE-DCC-Firmware-Upgrade
Repository for the latest released firmware for the SLICE-DCC
## Requires 
   Vescent SLICE_Firmware_Upgrade_Utility available at:
  
  https://github.com/Vescent/SLICE-FFC_Firmware_Upgrade_Utility:

## Instructions
  Left click on SLICE_Firmware_Update_Instructions-V1-10.pdf and then click 'Download' to download the instructions for use.  
   
  Left click on SLICE_firmware_update.docx and then click 'Download' to download the instructions for use.

  Left click on the upgrade package (Sx-xx-CCx-xx.zip) and then click 'Download' to download the firmware package to your hard drive.
  
  The three files in the .zip file need to be placed in the folder described in the instructions. DO NOT RENAME THEM!
# Change Log (Most Recent First)
## S1.69 CC1.52 
 1. Revises EEPROM reload function to fix a problem of overrunning RAM on startup which sometimes resulted in a Grey Screen.
 2. Adds a reset line hold to the startup sequence to hold ICE2 boards in reset until power is stable
## S1.68 CC1.51 (Initial Release)
 
