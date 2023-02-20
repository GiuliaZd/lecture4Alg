# Activities

## Task 1

- Refer to the following link. Discuss how Merge-sort works:
  https://opendsa-server.cs.vt.edu/OpenDSA/AV/Sorting/mergesortAV.html
  answers: DONE in class
- Merge-sort Practice. Refer to the following link. Merge the two sub-arrays into the larger array.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Sorting/MergesortMergePRO.html
  answers: DONE

## Task 2

- Refer to the following link. Discuss how Quick-sort works:  
  https://opendsa-server.cs.vt.edu/OpenDSA/AV/Sorting/quicksortAV.html
  answers:DONE
- Quick-sort Practice. Refer to the following link. Partition the array using quicksort.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Sorting/QuicksortPartitPRO.html
  answers:DONE, understood

## Task 3

- The following snippet is from `./src/quicksort.cpp` lines 32-43. Discuss in groups how the code works:

`````cpp
void quickSort(int arr[], int low, int high)
{
    if (low < high)
    {
        //partition the array
        int pivot = partition(arr, low, high);

        //sort the sub arrays independently
        quickSort(arr, low, pivot - 1);
        quickSort(arr, pivot + 1, high);
    }
}
the answer: First if low less than high, there is a partition to define the pivot. Later there are 2 quicksorts for both parts of the array. if low is more or equal to high - the rest of the code will not be resolved.

- The following snippet is from `./src/quicksort.cpp` line 27. Discuss in groups how ìt works:

```cpp
swap(&arr[i + 1], &arr[high]);
````the answer: here after all the checking we swap the elements to make the partition of the elements of the array

## Task 4: Individual (at home)

1. Merge-sort has better worst case performance than quicksort. So why Quick-sort is considered better than Merge-sort? Refer to the following article
   https://www.geeksforgeeks.org/quicksort-better-mergesort/
   the answer:
   1. QS needs less space than MS;
      2.the worst case of QS can be easlily avoided;
   2. QS is faster due to the locality of reference;
   3. MS is better for large data structures
2. Refer to the following article. Analyze the complexity of the Merge-sort algorithm.
   https://www.softwaretestinghelp.com/merge-sort/
   the answer:The time complexity for merge sort is the same in all three cases (worst, best and average) as it always divides the array into sub-arrays and then merges the sub-arrays taking linear time. and it equals to O(n*log n).
Merge sort always takes an equal amount of space as unsorted arrays. Hence when the list to be sorted is an array, merge sort should not be used for very large arrays. However, merge sort can be used more effectively for linked lists sorting.
conclusion:Merge sort uses the “divide and conquer” strategy which divides the array or list into numerous sub arrays and sorts them individually and then merges into a complete sorted array.
Merge sort performs faster than other sorting methods and also works efficiently for smaller and larger arrays likewise.
3. Refer to the following article. Analyze the complexity of the Quick-sort algorithm.
   https://www.softwaretestinghelp.com/quick-sort/
the answer:
Given below are the various complexities for Quicksort technique:

Worst case time complexity	O(n 2 )
Best case time complexity	O(n*log n)
Average time complexity	O(n*log n)
Space complexity	O(n*log n)
`````
