**\*\*TOOLS USED --\*\***

Wireshark, VS Code, and an Online Hex to ASCII Converter



**\*\*Steps taken to solve --\*\***

First opened the given PCAP file in Wireshark and examined the network traffic.



Checked the TCP conversations and compared the normal industrial-control packets to find anything unusual.



Noticed that most packets contained normal communication, while one packet appeared only once and contained unusual data starting with \*\*`Hacker\_alert=`\*\*.



Copied the hexadecimal data from the suspicious packet and used an \*\*online Hex to ASCII converter\*\* to decode it.



The decoded text gave the \*\*FLAG\*\*:



\*\*`wired{1ndu5trial\_e5pinoage\_detect3d}`\*\*



