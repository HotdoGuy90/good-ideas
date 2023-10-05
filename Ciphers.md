# Ciphers

Im sure everyone knows what a cipher is, and [DCODE](https://dcode.fr) makes a pretty good documentation. (It's in French idk why) So, I thought about making a new one.

## ASCII-Roman Cipher

The ASCII-Roman Cipher is very easy to run. It adds the use of ASCII and Roman Numerals. I can't remember the actual conversion list for ASCII, but you can look it up by typing `man ascii` on the command line, then press down until it shows "The decimal set:" and then the characters after. (press q to exit) Roman Numerals work like so:

1. I = 1
2. V = 5
3. X = 10
4. L = 50
5. C = 100
6. D = 500
7. M = 1000

When a character goes before a character with smaller or the same value, they become added.
**eg.** VI = 6, and XV = 15

When a character goes before a character with *larger* value, the become subtracted.
**eg.** IV = 4, and XC = 90

NOTE: This only works for some characters. You can only do it if all of the following statements are true:

- only one of the characters in front has a less value **eg.** IVX ≠ 6; VI does
- the character with more value has to be 5 times or 10 times the value that the lower character has **eg.** IC ≠ 99; XCIX does (its weird but the romans were stingy)
- You cannot put 4 of the same symbol together except 4000 or on clocks where they write 4 as IIII (the romans may be stingy but galileo was stingier)
- i forgot
- i forgot
- i forgot
- i forgot (doesnt matter though)

Now I had an idea to combine both Roman Numberals and ASCII, and create a cipher called The ASCII-Roman Cipher (Just rolls off the tounge doesn't it?) 
### How to use it

Well, say you had the letter "H" and, you wanted it to be encoded into the ASCII-Roman Cipher. Well, you could type find out that the ASCII for that, is 72. Now, convert it into Roman Numerals, and *Viola*, (vy-OLE-uh) you got the numeral LXXII.
Example: "HotdoGuy" becomes "LXXII CXI CXVII C CXI LXXIII CXVIII CXXI"
Ask me any questions, comments, or concerns using [issues](https://github.com/HotdoGuy90/good-ideas/issues).
