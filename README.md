﻿# Timer-VHDL

This project is written in VHDL language, designed in Vivado software suite.

The timer has four 7-segments displays. The first two screens are for the minutes, while 
the other two are destined to show the seconds. So, the maximum value that can be displayed on 
the screens is: 99 minutes and 59 seconds.  

The device has three buttons: START/STOP, M (for minutes) and S (for seconds). 
Considering that the initial state is IDLE (00:00), if the START/STOP button is pressed, 
the timer starts counting in ascending mode. If the START/STOP button is pressed again, the timer 
stops at the current value displayed on the screens. Then, at the third press of the START/STOP 
button, the timer continues its counting. If it reaches 99 minutes and 59 seconds, it returns to the 
initial state. If the buttons M and S are pressed simultaneously, the device resets (goes to state 
IDLE).  

In any state, if the button M is pressed, the value of minutes will be incremented and 
displayed. This function is also applied to the button S. After the value is incremented for minutes 
and/or seconds, when the START/STOP button is pressed, the timer starts counting in descending 
mode, until it reaches state IDLE. After count-down, at the initial state, an alarm is issued, which 
in our case means lighting up a led. 
It is considered available a periodic signal with frequency of 1Hz.
