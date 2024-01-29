# Week 4
## Announcements
- Project 1 due tuesday
- Homework 5 due wednesday
- read 1.3 equivalents (fist 6 pages) for class wednesday

## Review Recursive descent
A recursive descent parser tries to ID a token and pick the correct output for it 
```
S -> if E then S
S -> E=E
E -> 2 | x

E() {
  IF TOKEN IS 2
    MATCH(2)
  ELSE IF TOKEN IS X
    MATCH(X)
  ELSE
    ERROR
}

S() {
  IF TOKEN IS 'IF'
    MATCH(IF)
    E()
    MATCH(THEN)
    S()
  ELSE IF TOKEN IS 2 OR X
    E()
    MATCH(=)
    E()
  ELSE
    ERROR
}
```

## Project 2 comments

Our data log gives us an input of Schemes, Facts, Rules, and Queries like:
```
Schemes:
  snap(S,N,A,P)
  HasSameAddress(X,Y)

Facts:
  snap('12345','C. Brown','12 Apple','555-1234').
  snap('33333','Snoopy','12 Apple','555-1234').

Rules:
  HasSameAddress(X,Y) :- snap(A,X,B,C),snap(D,Y,B,E).

Queries:
  HasSameAddress('Snoopy',Who)?
```
and returns:
```
Success!
Schemes(2):
  snap(S,N,A,P)
  HasSameAddress(X,Y)
Facts(2):
  snap('12345','C. Brown','12 Apple','555-1234').
  snap('33333','Snoopy','12 Apple','555-1234').
Rules(1):
  HasSameAddress(X,Y) :- snap(A,X,B,C),snap(D,Y,B,E).
Queries(1):
  HasSameAddress('Snoopy',Who)?
Domain(6):
  '12 Apple'
  '12345'
  '33333'
  '555-1234'
  'C. Brown'
  'Snoopy'
```
Use the vector class to avoid memory leaks, and use pointers to look for things, don't use new and delete.

## Logical Arguments (ch. 1)
does a conclusion follow the premises?
```
PREMISES: IF IT SNOWS, I'LL GO SKIING
          IT'S SNOWING
CONCLUSION: I'LL GO SKIIING
```
Yes, because we have the premise which matches the conclusion
The conclusion needs to be the reslut of the predicate. It does not mean that if it were to not snow, you couldn't go skiing.


