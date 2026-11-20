# bouquetAscii

A spinning bouquet of pink and white flowers drawn entirely from 0s and 1s, in a single HTML file. Hidden in the binary is a message you can reveal with the decode button.

Everything lives in one file, bouquet.html. Download it and open it in any browser. There is nothing to install or build.
<br>

<img width="600" height="700" alt="Screenshot 2026-11-19 at 7 01 32 PM" src="https://github.com/user-attachments/assets/d989e24c-cbfc-4af9-871d-d0e1d4b36cea" />

## How the encoding and decoding works
Computers store text as numbers. Every character has a code, and each code can be written in binary.

When you press decode, the page converts the binary groups back into letters one at a time, so you can watch the message appear. Press encode to turn it back into binary.

## How the bouquet is drawn
Each flower, leaf, and the wrapper is built from a cloud of colored 3D points.
Every frame the points are rotated around the vertical axis. That is the twirl.
The points are flattened onto a 56 by 64 grid. When several points land in the same cell, the nearest one wins, so front flowers hide the ones behind.

Each lit cell is drawn as a 0 or a 1, tinted with that point's color. The digits flip over time so the whole picture shimmers.

The page uses plain HTML, CSS, and JavaScript with a <canvas>, and no libraries. The pixel font loads from Google Fonts. If it can't load, the page falls back to a plain monospace font and still works.

## Make your own
- Open bouquet.html in a text editor and change these near the top of the script:
- Message shown under the bouquet	MESSAGE
- Message hidden in the binary	SECRET
- Flower, leaf, and wrapper colors (RGB, 0 to 255)	COL
- Which flower color goes where	ringA and ringB
- Flower center colors	TONES
- Background color	--ink in the CSS and INK in the script
- Keep SECRET to plain letters, numbers, and common punctuation. Characters like curly quotes or long dashes don't 
fit in 8 bits and will decode wrongly.

# Notes
- If a computer is set to reduce motion, the bouquet stays still.
- Built with help from Claude, made by me.
