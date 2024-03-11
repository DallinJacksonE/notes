3/11/24

Homework 14
1. Problem 1
	power set is the set of all subset
	empty set is always a member of a power set
	use cardinality to find expected lengths
2. Problem 2
	bit strings
	U = {a, b, c}
	X = {a, b}  1 1 0
	Y = {b, c}  0 1 1
		    ------
		    0 1 0 and (n looking one)
		    1 1 1 or (U looking one: X U Y)
		    0 0 1 xor (~X)
		    1 0 0 X-Y


## Binary Relations

A binary relation is a representation of the relationships between members of two sets

A binary relation from A to B is a set of pairs, where the first element of each pair comes from A and the second element comes from B

A subset of the cartiesian product of two sets

Ex. We have a set of people, and we put a **cousins** realation on it and get:
```cousins = { (Jim, Bob), (Bob, Jim), (ann, Sue), (Sue, ann)}```

We have a 


## Reflexive Relation

Contains (x, x) for every x in the domain
Every member in the domain is related to itself


## Symmetric Relation

If the relation contains (x, y)
then the relation must contain (y, x)

### Antisymmetric

If the relation contains (x, y),
then the relation must not contain (y, x),

unless x and y are the same value i.e (1, 1)

## Transitive Relation

if the relation contains (x, y) and (y, z), the realtion must contain (x, z)


