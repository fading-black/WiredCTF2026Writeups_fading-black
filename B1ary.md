**TOOLS USED --**
Visual Studio Code , Online Binary to ASCII Converter, and Online Text/ASCII Decoder

**Steps taken to solve --**
First opened the given binary dump file in VS Code and noticed that it contained multiple lines of binary data.

Since I couldn't install the required binary-analysis tool on my laptop, I used an online **Binary to ASCII converter** to decode the binary values.

I entered the binary data into the converter in **8-bit groups**, since each 8 bits represents one ASCII character.

After converting the binary to ASCII, most of the output appeared to be random or unreadable data. I searched through the decoded output for a recognizable flag format.

I noticed the string **`wired{`** appearing in the decoded data. I then checked the consecutive lines around it and found that they contained the remaining parts of the flag.
**DISCOVERED 2ND METHOD LATER**
can just use the "string" function in terminal and you will get all the diff text values in the particular file. 

The decoded parts were:

`wired{jU5t_@_3in`
`a3y_dUmp`
`1}`

Joining these parts together gave the final flag:

**`wired{jU5t_@_3ina3y_dUmp1}`**
