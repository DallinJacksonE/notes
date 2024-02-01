# Unit 4 Pointers
### Announcements
- Lab 4 due Friday, quiz style project
- Next week Project 2 is due BMP Filter. Black and white filter for pictures. Iterating through memory (~3hrs)
- Readings this week: **Sections 2.2** & **2.3**

### Unsigned Numbers
All of our types can be unsigned (except for flout/double/pointers)
- unsigned char, short, int, long
- just a binary representation

Values encoded in these cannot be negative, so they can go higher than signed values
_Ranges for the unsigned types are on pg 61_

### Signed Numbers
Signed numbers can store a negative value, but the range of how much data I can store is cut in half
Use 2's complement, so the binary pattern changes if the leading bit is a 1

**How is this done?**
- First try: have a sign bit
```The first bit of the number becomes the indicator of whether the number is positive or negative```

- Second Try (How we actually do it)
** 2's Complement!**
![Chart for 22's Complement](https://miro.medium.com/v2/resize:fit:401/1*Pt_CXz1ycPFFvVjc7X-DpQ.png)

_Ranges for signed numbers are on pg 61_

## Conversions
- If you convery between singed and unsigned, you lose a bit of data which is bad

## Using Signed and Unsigned values together in operations
- If either one of a data type is unsigned, then it is assumed the other value is unsigned, and the bytes are read differently than your intial value

## Conversions between Sizes
- expanding your type, going to more bits, you have the space to do so, but if your new bit is negative, then you need to use **sign extension** and make all your new bits a 1 so it holds its value

- If we are changing size and signed-ness, do we expand or change type first?
  1. Size is changed first
  2. now we change the sign


