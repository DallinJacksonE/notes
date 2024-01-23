# Announcements
## Project 1 due Friday
Reading in bytes from a file and printing them in hex, binary, and as chars
~49 lines of code, 2-2.5 hrs. Hint: (Print out a hex with a leading 0, use the %02x formatting string)
Lab prep is about the project, and yeah, don't drop the ball

### Pop Quiz
1. How many bits in a byte? `A: 8`
2. How many bytes in a char, int, short, long? `A: 1 4 2 8`
3. How many bytes does int i[4] take up? `A: 16`
4. long g[5] if &g[0] = 0x100, what is &g[1]? `A: 0x108`
**For this class we assume we are working with a 64-bit computer**

# Lecture
## Going back to first grade
### How Do we know the value of a number?
105624
What does the 5 mean?
Is the zero important? Yes

- 4 is 4 ones
- 2 is 2 tens
- 6 is 6 hundreds
- 5 is 5 thousands
- etc.

Place determines value in decimal, **Base 10**
In base 10, the i-th place has a value of 10<sup>i</sup>

### In class we will use:
- Binary (base 2)
- Hexadecimal (base 8)

### Binay
- Each place i is 2<sup>i</sup>
`110` - 2+4=6
`10111` - 16+4+2+1 = 23
> Learn binary, practice by hand and practice reading the values

### Hexadecimal
- Each place i is 16<sup>i</sup> X character value
> **Remember A = 10, B = 11, C = 12, D = 13, E = 14, F = 15**

#### Why Use Hexadecimal
It lines up with nibbles (four bits)

## Converting Binary to Hexadecimal
- Every four digits becomes a hex digit (start from right, least significant)
`01001011101101010010 ` -> `0100 1011 1011 0101 0010` -> `4 B B 5 2` -> `0x4bb52`
`1110100100001` -> `1 1101 0010 0001` -> `1 D 2 1` -> `0x1d21`

`51a4b` -> `0101 0001 1010 0100 1011`
`42ff` -> `0100 0010 1111 1111`

## Converting Decimal to Binary
- To convert n to binary:
  ```
  1. remainder is least significant digit (n%2)
  2. integer division n = n/2
  3. repeat until n = 0
  ```
Example 43
- 43 % 2 = `1`
- 43/2 = 21
- 21 % 2 = `1`
- 21/2 = 10
- 10 % 2 = `0`
- 10/2 = 5
- 5 % 2 = `1`
- 5/2 = 2
- 2 % 2 = `0`
- 2/2 = 1
- 1 % 2 = `1`
- 1/2 = 0
- 0 % 2 = `0`
- Result: `1101010`

