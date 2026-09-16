**\*\*TOOLS USED --\*\***

VS Code, Online CAN Bus Analyzer/DBC Decoder, Online Hex XOR Calculator



**\*\*Steps taken to solve --\*\***

First opened the given CAN log file in \*\*VS Code\*\* and inspected the CAN messages.



Since I couldn't install the required CAN analysis tool on my laptop, I used an \*\*online CAN bus analyzer/DBC decoder\*\* to inspect the CAN IDs and message data.



While going through the log, I noticed the CAN ID \*\*1107\*\* appearing multiple times. I checked the Infiniti G37 CAN database and found that \*\*0x1107 corresponds to the LIGHTS message\*\*, which contains signals such as the \*\*LEFT\_BLINKER\*\*.



The clues mentioned \*\*"looking the wrong way"\*\*, \*\*"where you go"\*\*, and especially \*\*"left turn"\*\*, which indicated that the left-blinker messages were important.



I filtered the `1107` messages and looked at the frames where the left-blinker indicator was active. The relevant messages contained:



```text

1107#010000006F716A7D

1107#010000007C63742B

1107#010000007E2F476A

1107#01000000292E702F

1107#0100000047742B7E

1107#010000002F650000

```



I noticed that the first four bytes were being used for the CAN signals, while the \*\*last four bytes changed between the suspicious messages\*\*.



I extracted the last four bytes:



```text

6F716A7D

7C63742B

7E2F476A

292E702F

47742B7E

2F650000

```



The clue \*\*"0x18 steps away"\*\* suggested that `0x18` was being used as the key. I used an \*\*online Hex XOR calculator\*\* to XOR the extracted hexadecimal data with `0x18`. Online hex XOR tools can perform hexadecimal bitwise XOR directly in the browser.



The decoded data produced readable text:



```text

wired{l3f7\_r16h7\_l3f7}

```



Therefore, the \*\*FLAG\*\* was:



```text

wired{l3f7\_r16h7\_l3f7}

```



