# Notes for Digital Logic
Converting to and from binary decimal and hexidecimal 
  - Repeatedly subtract largest power of 2 you can the powers subtract 
  - or divide by 2 and take the remainder(gives you binary digits right to left). 
Binary to decimal 
  - Add up the powers of 2 based on place value 
  -   674 = 6x10^2 + 7x10^1+4x10^0
  -   1 0 1 1 1 = 1x16+0x8+1x4+1x2+1x1
       2^4 2^3 2^2 2^1 2^0 = 23!
Binary to Hexidecmimal 
- Group digits in groups of 4 from right to left. Convert each group of 4 bits to a single hex digit.
  - 1101 0001 1001
  - 8421 8421 8421
  -  13   1    9 

Hexidecimal to Binary 
- Reverse the process each hex digit expands to 4 binary digits 
