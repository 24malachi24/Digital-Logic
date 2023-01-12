# Notes for Digital Logic
Converting to and from binary decimal and hexidecimal 
  - Repeatedly subtract largest power of 2 you can the powers subtract 
  - or divide by 2 and take the remainder(gives you binary digits right to left). 
 
Binary to decimal 
  - Add up the powers of 2 based on place value 
  -   674 = 6x10^2 + 7x10^1+4x10^0
  -   1 0 1 1 1 = 1x16+0x8+1x4+1x2+1x1
       2^4 2^3 2^2 2^1 2^0 = 23!

Binary to Hexidecmima
- Group digits in groups of 4 from right to left. Convert each group of 4 bits to a single hex digit.
  - 1101 0001 1001
  - 8421 8421 8421
  -  13   1    9 

Hexidecimal to Binary 
- Reverse the process each hex digit expands to 4 binary digits 
-  2 E 3 B 
- 8421 8421 8421 8421 
- 0010 1110  0011 1011

Convert 99 from decimal (base 10) to binary (base 2) and then to hexidecimal(base 16)

99 / 2 = 49 (remainder 1)
49 / 2 = 24 (remainder 1)
24 / 2 = 12 (remainder 0)
12 / 2 = 6 remainder (0)
6 /2 = 3 (remainder 0)
3 / 2 = 1 (remainder 1)
1 / 2 = 0 (remainder 1)

Or powers of 2 
so 128 64 32 16 8 4 2 1 
    0   1  1 0 0 0 1 1
    
    So then from binary to hexidecimal split into groups of 4 
    
   0 1 1 0 & 0 0 1 1
   
   8 4 2 1  8 4 2 1
   
   4+ 2 = 6     2+1 = 3
    hex 6        hex 3

Always need to know how many bits are available 
adding 4 bits 
1+1 in binary = 1 0
then cary the one so
0 1 1 1 + 1 0 1 0 = 0 0 0 1 with a carry out (1)

6 bits 
101101+010111 = 001000 with a carry out (1)

What about negative numbers?
 - use one bit to indicate sign.
 - 
 
 Advantages of 2's complement 
 - we can use the same hardware for addition adn subtraction
 - No magnitude comaprison is needed
 - No negative zero
 - Format also works for integer multiplication
 - Can cover the number range from -2^n to 2^n -1 for n bits
 - Chart shows 4-bit values from -8 to 7

5 bits 
-7 + 10 = 00011 (carry out 1) no over flow both equal 3. 
7 = 00111 flip and add 1
2's = 11001 = -7
10 = 01010

-8 + 3 = 11011 = -5 to make sure take 2's compliment 00100 +1 = 00101 = 5 so it holds
8 = 01000
2^s 10111 flip and add one 1
-8 = 11000
3 = 00011 

-15 + -3 = 14 overflow!
15 = 01111
2's = 10000 +1 = 10001
3 =00011
2's=11100 +1 = 11101
10001 + 11101 = 01110 (carry out 1) = 14

TO extend bits you just put zeros on the front so here is an example
5 bits      8 bits            5 bits              8 bits
00101=5       00000101=5      10001 = -15         11110001=-15
padd with zeros                 pad with 1's

Subtraction Example!

01010 -00011 

1. Take the 2's compliment of the second number and add instead.
- 11101 so 01010 + 11101 = 00111 (carry out 1)
 10 -3 = 7 
 
 10001 - 10011
 
 1. 01100 +1 = 01101 
 2. 10001 + 01101 = 11110 = 31
 3. 17-19 = -2 
4. unsigned has overflow 31=-2 signed has no overflow 

Rules to not forget 
11111 = -16+8+4+2+1

9     - 2 = 7
1001 - 0010
1. 1101 + 1 = 1110
2. 1001+1110 =   0111 carry out 1
3. 0111 = 7 
4. signed has overflow -9 =7
5. unsigned has no overflow 7=7

 
 Another number representation BCD (Binary coded decimal )
 9 2 6 
 8421 8421 8421 
 1001  0010 0110
