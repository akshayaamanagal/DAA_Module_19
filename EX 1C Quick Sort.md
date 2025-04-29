# EX 1C Quick Sort
## DATE: 25.02.2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of integers.

## Algorithm  
1. Define the `quickSort(alist, start, end)` function to recursively sort the list using Quick Sort.  
2. If the sublist length is greater than 1, partition the list and get the pivot index `p`.  
3. Recursively apply `quickSort` to the left sublist (`start` to `p`) and right sublist (`p+1` to `end`).  
4. Define the `partition(alist, start, end)` function to rearrange elements around a pivot.  
5. Select the first element as the pivot and initialize pointers `i` and `j` to traverse the sublist.  
6. Move `i` forward until an element greater than the pivot is found.  
7. Move `j` backward until an element smaller than the pivot is found.  
8. If `i` is still less than or equal to `j`, swap elements at `i` and `j`.  
9. If `i > j`, swap the pivot with the element at `j` and return `j` as the pivot index.  
10. Take an integer input `n` for the number of elements in the list.  
11. Read `n` integers from the user and store them in the list `arr`.  
12. Call `quickSort(arr, 0, n)` to sort the entire list.  
13. Print the sorted array elements one by one.  

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of integers.
Developed by: AKSHAYAA M
Register Number: 212222230009 
*/
```
```python
def quickSort(alist,start,end):
    if end-start>1:
        p=partition(alist,start,end)
        quickSort(alist,start,p)
        quickSort(alist,p+1,end)
def partition(alist,start,end):
    pivot=alist[start]
    i=start+1
    j=end-1
    while True:
        while(i<=j and alist[i]<=pivot):
            i=i+1
        while(i<=j and alist[j]>=pivot):
            j=j-1
        if i<=j:
            alist[i],alist[j]=alist[j],alist[i]
        else:
            alist[start],alist[j]=alist[j],alist[start]
            return j
arr=[]
n=int(input())
for i in range(n):
    arr.append(int(input()))
quickSort(arr,0,n)
print("Sorted array is:")
for i in arr:
    print(i)
```

## Output:

![image](https://github.com/user-attachments/assets/5ceb9ce3-5c77-433b-9749-0013261e2a45)


## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
