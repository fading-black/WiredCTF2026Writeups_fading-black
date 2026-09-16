**\*\*TOOLS USED --\*\***

VS Code, Online Hex to ASCII Converter, and Online Base64 Decoder



**\*\*Steps taken to solve --\*\***

First opened the given CAN log file in VS Code and observed that it contained multiple entries with \*\*Timestamp, ID, and Data\*\* fields.



The Data values were in \*\*hexadecimal format\*\*, so I used an online \*\*Hex to ASCII converter\*\* to decode them into readable text.



After converting the Data values, I noticed that the \*\*CAN IDs were not in sequential order\*\*, so I arranged the decoded entries according to their IDs.



After arranging them, the decoded text formed a meaningful string and also contained a section that looked like \*\*Base64 encoded data\*\*.



I copied the Base64-looking portion into an online \*\*Base64 decoder\*\*, which revealed the final readable message.



The decoded message gave the FLAG:



\*\*`wired{c4n\_y0u\_h34r\_m3}`\*\*



