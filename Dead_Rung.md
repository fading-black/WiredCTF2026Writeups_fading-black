**TOOLS USED --**

PLC Ladder Logic Viewer, Modbus Diagnostic Snapshot , Pen and Paper



**Steps taken to solve --**

1.First analyzed the given PLC ladder logic to understand the conditions required for the MOTOR coil.



2.Compared the live Modbus snapshot values with the ladder logic.



3.Understood how the ESTOP and DOOR\_CLOSED inputs affect the internal ESTOP\_OK and DOOR\_OK signals.



4.Traced the 3-second TON timer and identified the DRIVE\_READY condition required for SAFETY\_OK.



5.Finally, determined the minimum input changes required and submitted the flag in alphabetical order.




