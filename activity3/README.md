# Activities

## Task 1:

- Refer to the following link. Discuss how Stacks based on linked lists works:
  https://www.cs.usfca.edu/~galles/visualization/StackLL.html
  the answer: there is a pointer connected to each cell, as well as some value.
  and since the structure is stack - it means that when we "pop" one unit from the array - it "pops" from the end of the array.

## Task 2:

The following snippet is from `./src/stack.cpp` lines 25-31.

```cpp
void push(StackNode **root, int new_data)
{
    StackNode *stackNode = newNode(new_data);
    stackNode->next = *root;
    *root = stackNode;
    cout << new_data << endl;
}
```

- Discuss in groups how the code works?
- Why do we need to use double pointers?

the answer: ??

## Task 3: Individual (At home)

Practice: Asymptotic Analysis and Upper Bounds. Refer to the following link:
https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/AlgAnal/UpperBoundsSumm.html

the answer: DONE
