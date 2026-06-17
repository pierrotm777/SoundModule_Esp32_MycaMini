# EXAMPLE OF CONFIGURATION IN PUSH-BUTTON MODE
![10 buttons board](https://github.com/pierrotm777/SoundModule_Teensy4.0-version/blob/main/10buttons_sch.png)  

Control in Push-Button mode for the Sound Module is simply obtained by upload the Buttons hex file.  

In this command mode, the keyboard can be of type:  
- DIY (homemade) keyboard with assembly of 10 push buttons and resistors.  
- Kingpad keyboard from Pistenking.  
- Steuerpad from Kraftwerk.  
-  Virtual touch keyboard (LUA script) for FrSky Ethos transmitters (X20 or X20S).  
- Virtual touch keyboard (LUA script) for EdgeTx transmitters (LCD Color screen).  

When using a physical or virtual KingPad keyboard from Pistenking or a physical Steuerpad keyboard from Kraftwerk, only 8 keys out of the 12 available are used by the Sound Module.
If using a DIY keypad, wire 10 push buttons, 8 for 8 sound and 2 for change the volume of sounds.  

Each press of a push button generates a different voltage at the input of the transmitter channel,
this will therefore generate an RC pulse of different width which will be found on the reception side on the associated channel.  

It is therefore necessary for Sound Module to know the channel pulse width associated with each push button.  

To do this, simply switch to calibration mode by sending the command via the serial terminal: (this calibration only needs to be carried out once)  
**T and RETURN** in Calibration mode.  
**C and RETURN** (Push Buttons = Calibration).

The display becomes:  
BP1:  
While holding **Push Button No. 1 pressed**, press the **Enter key** on the Serial Terminal keyboard.  
The pulse width measured for BP1 will then be displayed (and automatically stored) and BP2 will be displayed:  
BP1:0988  
BP2:  
While holding **Push Button No. 2 pressed**, press the **Enter key** on the Serial Terminal keyboard.  
Repeat the operation until BP10.  

Once the pulse width associated with the BP10 is displayed, the calibration is complete.
**T and RETURN** quit Calibration mode.  
It is possible to display the 10 pulse widths associated with BP1 to BP10 using the command:
**B and RETURN**.  
B=0988;1100;1228;1320;1672;1768;1888;2016;BT9;BT10  

There must be at least 65 µs difference between 2 "near" pulse widths.  
In the event of a false manipulation or error, it is obviously possible to redo a calibration by resending the command:
T and RETURN and C and RETURN for start a new calibration.  
B and RETURN will you return the new buttons values.  

Note:  
All modified parameters are automatically saved in the EEPROM memory of Teensy.  
This means that the next time you power it on, the new settings will not be lost.  
The user manual provides and details all the commands supported by the Sound Module.  