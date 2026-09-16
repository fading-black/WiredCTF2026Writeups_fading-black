**TOOLS USED --** 

Wireshark, VS Code, Python, XOR operation, and a hex-to-string converter.



**Steps taken to solve --**

1. Opened the provided PCAP file in Wireshark and examined the captured traffic.

2\.  Observed normal ARP and broadcast/discovery traffic.

3\. Used the filter: eth.type == 0x1337

&#x20; This displayed the unusual Ethernet frames mentioned in the clue.



4.Checked the Ethernet II section and noticed that the destination MAC address was repeatedly:



&#x20;    de:ad:be:ef:13:37



&#x20;  Inspected the packet bytes and found that each suspicious frame contained three important bytes:



&#x20;   The first byte represented the fragment index.



&#x20;   The next two bytes contained encoded data.



5\. The timestamps were not reliable for ordering, so I used the fragment index byte to arrange the packets from 00 to 11.

The clue said to “look at the address,” so I examined the source MAC address of each frame. The final byte of the source MAC was used as        the XOR key for that frame.



6 .XORed the two encoded data bytes with the final byte of the source MAC address.



&#x20; Converted the decoded hexadecimal values into ASCII characters and joined the fragments in the correct order to get the FAG.





