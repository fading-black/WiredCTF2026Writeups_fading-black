**TOOLS USED --**
Wireshark, VS Code, and an Online Decimal to ASCII Converter

**Steps taken to solve --**
First opened the given PCAP file in Wireshark and examined the network traffic.

Noticed that most packets had a normal **TTL value of 64**, while a small number of packets had a different TTL value of **23**.

Since the hint mentioned counting how far each packet traveled, filtered the packets based on the unusual TTL value and inspected those packets.

The suspicious packets contained decimal numbers at the end of their data.

Copied these decimal values in the same order as they appeared in the packets and used an **online Decimal to ASCII converter** to convert them into characters.

The converted characters formed the FLAG:

**`wired{tt1_wh1sp3rs_th3_s3cr3t}`**
