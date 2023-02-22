# Activities

> The [modulo-calculator](#links) might be handy in these exercises.

## Task 1

- Refer to the following link. Discuss how open hashing works.
  https://www.cs.usfca.edu/~galles/visualization/OpenHash.html
  the answer: first it finds modulo of the inserted integer by the length of the array, and assigned this integer to the corresponding to the remaindor of modulo place in the array.
- Open Hashing Practice. Refer to the following link. Move each record on the left to the appropriate bin on the right.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/OpenHashPRO.html
  the answer: done
- Given the following input (`4322, 1334, 1471, 9679, 1989, 6171, 6173, 4199`) and the hash function `x mod 10`, which of the following statements are true?
- [x] `9679, 1989, 4199` hash to the same value
- [x] `1471, 6171` hash to the same value
- [] All elements hash to the same value
- [] Each element hashes to a different value

## Task 2

- Bucket Hashing Practice. Refer to the following [link](https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Hashing/HashBucketPRO.html).
  the answer: done
- The keys `12, 18, 13, 2, 3, 23, 5 and 15` are inserted into an initially empty hash table of length `10` using open addressing with hash function `h(k) = k mod 10` and **linear probing**. What is the resultant hash table?
  the answer: 12,2;
  13,3,23;
  5,15;
  18

## Task 3:

- What is the [Birthday Paradox](http://en.wikipedia.org/wiki/Birthday_problem)?
  the answer: in other words it's "If you have a group of more than twenty-four people, the odds are better than even that two of them have the same birthday."
  but in theory it sounds like: "In probability theory, the birthday problem asks for the probability that, in a set of n randomly chosen people, at least two will share a birthday. The birthday paradox refers to the counterintuitive fact that only 23 people are needed for that probability to exceed 50%.
  The birthday paradox is a veridical paradox: it seems wrong at first glance but is, in fact, true. While it may seem surprising that only 23 individuals are required to reach a 50% probability of a shared birthday, this result is made more intuitive by considering that the birthday comparisons will be made between every possible pair of individuals. With 23 individuals, there are
  23 × 22
  /
  2
  = 253 pairs to consider, far more than half the number of days in a year.
- Why is it generally discussed with hashing?
  the answer: Because when proving and calcultaing, they build the probability table with hashes.
- In a hash table of 9658 slots, what is the smallest number of records that must be inserted for the probability of a collision to be 61% or more? Use the calculator at this [link](https://opendsa-server.cs.vt.edu/ODSA/AV/Hashing/Birthday.html)
  the answer: 136 records at least.
- Discuss in groups how the following program works `./src/birthday.cpp`?
  the answer: ??

## Task 4: Individual (at home)

- Difference between `Separate Chaining` and `Open Addressing` collision handling techniques?

  https://www.geeksforgeeks.org/open-addressing-collision-handling-technique-in-hashing/

  https://www.geeksforgeeks.org/separate-chaining-collision-handling-technique-in-hashing/
  the asnwer:
  The idea behind separate chaining is to implement the array as a linked list called a chain. Separate chaining is one of the most popular and commonly used techniques in order to handle collisions.
  Advantages of SC:
  Simple to implement.
  Hash table never fills up, we can always add more elements to the chain.
  Less sensitive to the hash function or load factors.
  It is mostly used when it is unknown how many and how frequently keys may be inserted or deleted.
  Disadvantages:
  The cache performance of chaining is not good as keys are stored using a linked list. Open addressing provides better cache performance as everything is stored in the same table.
  Wastage of Space (Some Parts of the hash table are never used)
  If the chain becomes long, then search time can become O(n) in the worst case
  Uses extra space for links

In Open Addressing, all elements are stored in the hash table itself. So at any point, the size of the table must be greater than or equal to the total number of keys (Note that we can increase table size by copying old data if needed). This approach is also known as closed hashing. This entire procedure is based upon probing. the types of probing :
Insert(k): Keep probing until an empty slot is found. Once an empty slot is found, insert k.
Search(k): Keep probing until the slot’s key doesn’t become equal to k or an empty slot is reached.
Delete(k): Delete operation is interesting. If we simply delete a key, then the search may fail. So slots of deleted keys are marked specially as “deleted”.
The insert can insert an item in a deleted slot, but the search doesn’t stop at a deleted slot.

- (Bonus) Run the following program and comment on the code `./src/hashtable.cpp`
  the answer: ??

## Link(s)

- [modulo-calculator](https://www.calculators.org/math/modulo.php)
- [Practice Problems on Hashing](https://www.geeksforgeeks.org/practice-problems-on-hashing/)
