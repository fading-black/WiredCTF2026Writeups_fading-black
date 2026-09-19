**TOOLS USED --**
Audacity, Online DTMF Decoder, Online ASCII/Encoding Converter

**Steps taken to solve --**
First, I listened to the given audio file. At first, the sound seemed like random noise, but after listening carefully, I thought it could be **Morse code** because of the repeated short and long sounds.

I initially followed this idea, but it turned out to be a **misdirection**.

After listening to the audio again, I noticed that the sounds were similar to the tones produced when pressing numbers on a **normal mobile phone keypad**. This made me suspect that **DTMF tones** were being used.

I opened the audio in **Audacity** and modified the frequency range to approximately **0–1400 Hz** to make the keypad tones easier to identify.

After processing the audio, I used an **online DTMF decoder** to decode the different keypad tones.

The decoder gave me a sequence of encoded numbers. I then noticed that the numbers followed another encoding, so I converted them using an **online ASCII/decimal converter**.

After converting the values, the FLAG was revealed.
