# Unit 4 Pointers
### Announcements
- Lab 4 due Friday, quiz style project
- Next week Project 2 is due BMP Filter. Black and white filter for pictures. Iterating through memory (~3hrs)
- Readings this week: **Sections 2.2** & **2.3**

### Unsigned Numbers
All of our types can be unsigned (except for flout/double/pointers)
- unsigned char, short, int, long

Values encoded in these cannot be negative, so they can go higher than signed values
_Ranges for the unsigned types are on pg 61_

### Signed Numbers
Signed numbers can store a negative value, but the range of how much data I can store is cut in half

**How is this done?**
- First try: have a sign bit
```The first bit of the number becomes the indicator of whether the number is positive or negative```

- Second Try (How we actually do it)
** 2's Complement!**
![Chart for 22's Complement](https://miro.medium.com/v2/resize:fit:401/1*Pt_CXz1ycPFFvVjc7X-DpQ.png)

_Ranges for signed numbers are on pg 61_

