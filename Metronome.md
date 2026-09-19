**TOOLS USED --**

ZXing Decoder Online, Python, Online Hex/XOR tools, and a QR code online scanner.

**STEPS TAKEN --**

I couldn't install ZXing/Magic-bricks-type QR tools on my laptop, so I used an online QR decoder instead. ZXing Decoder Online supports uploading a QR image directly from the browser.



1. Scanned the QR code using an online QR decoder to check whether it could be decoded normally.

2 . The QR did not decode correctly, so I inspected the pattern/structure of the QR instead of only looking at the encoded data. AND FIXED THE READING SQUARES(FINDER PATTERNS) .

&#x20;   I noticed that the timing pattern of the QR should follow a regular alternating pattern:

&#x20;   101010101010...(TRIMMING LINES)



3\. I treated this broken rhythm as the clue/key, as suggested by the challenge description.

4\. I analyzed the QR structure and recovered the encoded hexadecimal data:

&#x20;  1e001b0c0d121a0a5d0736045a36000f3610591c360a5d0714

5\. I then used the recovered key from the timing-pattern disturbance and XOR'd it with the hexadecimal data.

&#x20; The resulting data produced the hidden message:

&#x20; wired{sc4n\_m3\_if\_y0u\_c4n}

