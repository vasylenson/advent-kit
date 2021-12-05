# Design concept

## Overview: what do you need for AoC

- Short variables names
- Utils
  - Basic dir structure setup
  - pulling down input and submission
  - (rapid testing, test generation - probably not gonna be done, unless we get into decorators and contracts)
- input parsing
  - lists
  - matrices
  - csv
  - skip empty lines
- debugging
  - formatting data structures
- working with matrices
  - checking row/column conditions
  - searching (in the matrix space, number of the matrix, row, col)
  - emilination (set to None)
  - operator lifting (like numpy)
- algorithms?
  - sorting?
  - pathfinding?
  - i dunno
- custom logic support, performance
  - hand tuning
  - tabulation or memoisation
  - get first, last

## Appendix

### Algorithm examples

Rough and ambiguous, but very compact verbal descriptions of AoC solutions. We should try to model the framework to match them.

#### Day 1

1. get list with newlines to ints
2. collect `list[2..n] - list[1..n]`
3. **count positive**

#### Day 2

1. get list of (cmd, value)
2. match cmd, accumulate conditinally
3. **multiply**

#### Day 3

1. get matrix
2. map most common to cols
3. **invert and multiply**
4. repeat for each col
5. divide by col value
6. keep the bigger list. prefer value 1
7. O2 <- repeat until 1 remains
8. CO2 <- same, but choose smaller, prefer 0
9. **O2 * CO2**

#### Day 3.2 alt

Just as many steps on paper, but probably easier to code. May sacrifice some performance too, but not complexity.

1. for each col
2. cmp <- most common or 1
3. filter rows on (col == cmp)
4. oxy <- repeat until left with 1 row
5. carb <- same but cmp <- least common or 0
6. **oxy * carbon**

#### Day 4

1. get csv (moves)
2. get list of 5x5 matrices
3. for each move
4. find in matrices, eliminate, store positions
5. for each position if the whole row of column is eliminated -> save score, eliminate the matrix
6. **get the first score**
7. **get the last score**

#### Day 5

1. get array of "int,int -> int,int"