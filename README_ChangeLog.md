# SLICE-DCC-Firmware-Upgrade
Repository for the latest released firmware for the SLICE-DCC
## Requires 
  Vescent SLICE-PC-GUI application available at:
  
  https://github.com/Vescent/SLICE-PC-GUI/blob/master/SLICE-GUI-Windows-1-17.zip
## Instructions
  Left click on SLICE_firmware_update.docx and then click 'Download' to download the instructions for use.

  Left click on the upgrade package (Sx-xx-DCCx-xx.zip) and then click 'Download' to download the firmware package to your hard drive.
  
  The two files in the .zip file need to be placed in the folder described in the instructions. DO NOT RENAME THEM!
# Change Log
## Configuration S1.69 DCC1.52
 1. Revises EEPROM reload function to fix a problem of overrunning RAM on startup which sometimes resulted in a Grey Screen.
 2. Adds a reset line hold to the startup sequence to hold ICE2 boards in reset until power is stable
## Configuration S1.68 DCC1.51
 1. Adds negative number blocking to rotary edit mode for all values limited to 0.0 minimum
 2. Adds two stage powerup to make sure digital circuit is stable before enabling 24V and +/- 14V power
 3. Remaps EEPROM to allow SLICE serial number to be stored in NV memory
 4. Adds API to allow production to set the serial number of the unit
 5. Implements ***IDN?** Serial API command
   
       Returns:
    
       __Vescent Photonics, SLICE-`<model>`, `<serial number>`, `<System Controller FW Version>`, `<ICE2 FW Version>`__
       
## Configuration S1.64 DCC1.50
 1. Changes API commands referencing current from [mA] to [A] units
 2. Removes choices 2 and 3 from AMODSEL and AMODSEL? API commands
## Configuration S1.64 DCC1.49
 1. Improves firmware upgradeability 
 2. Improves fault handling to use the ICE2 FAULT line to notify the system controller of an error. Corrects phantom error problems seen on earlier versions
 3. Fixes the possibility of entering a negative current setpoint
## Configuration S1.61 DCC1.47
 1. Adds Current Output Calibration capability
 2. Adds Power Limit Exceeded Warning, Shutdown, and Informational Table Display
 3. Adds PWR_GOOD pin monitoring to shut down 
## Configuration S1.54 DCC1.32 (Initial Release)
 1. Two Independent channels for controlling current
 2. Output current range current limit
  2.1. DCC-200  200 mA
  2.2. DCC 500  500 mA
  2.3. DCC 1000 1000 mA
  2.4. DCC 2000 2000 mA
 3. Current setpoint resolution:
  3.1. DCC-200  2 decimal places
  3.2. DCC 500  2 decimal places
  3.3. DCC 1000 2 decimal places
  3.4. DCC 2000 1 decimal place
 4. Each channel has a mode whereby the output current is controller via a feedback loop filter which maintains an externally-supplied input current at a constant value.
 5. External interlock disables all channels when the interlock is in the open position
 6. Each channel provides voltage protection to limit output voltage in the event of a sudden interruption in current flow to the driven device. (Open Circuit Protection)
 7. Detects internal component over temperature condition and shuts down when a threshold is exceeded.
 8. Detects inside case over temperature condition and shuts down when a threshold is exceeded.
 9. Stores the following in NV Storage during power off state:
  9.1. Constant current Setpoint
  9.2. Current Limit
  9.3. Detector Response
  9.4. Constant power setpoint
  9.5. Constant Power Gain [dB]
  9.6. Constant Power Polarity
  9.7. External Input Selection for each front panel input
  9.8. External Output Selection for each front panel output
  9.9. Input Trigger selection
  9.10. Output Trigger selection
 10. Allows setting and NV Storage of the following:
  10.1. Backlight and Audio Levels
  10.2. Input Impedance setting for each front panel input
  11. Provides Standard SLICE Lock / Unlock functionality
