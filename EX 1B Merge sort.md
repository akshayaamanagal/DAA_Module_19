# EX 1B Merge Sort
## DATE: 22.02.2025
## AIM:
To write a python program to implement merge sort using iterative approach on the given list of values.

## Algorithm
1. Define a function `Merge_Sort(S)` to sort a list `S` using the merge sort algorithm.  
2. If the length of `S` is greater than 1, find the middle index to divide the list into two halves.  
3. Split the list `S` into `left_arr` and `right_arr` at the middle index.  
4. Recursively call `Merge_Sort(left_arr)` and `Merge_Sort(right_arr)` to sort both halves.  
5. Initialize three pointers `i`, `j`, and `k` to 0 for traversing `left_arr`, `right_arr`, and `S`, respectively.  
6. Compare elements from `left_arr` and `right_arr` and merge the smaller element into `S`.  
7. Copy any remaining elements from `left_arr` into `S`.  
8. Copy any remaining elements from `right_arr` into `S`.  
9. Take an integer input `n` for the number of elements and store it.  
10. Use a loop to input `n` elements into the list `S`.  
11. Print the original array `S`.  
12. Call `Merge_Sort(S)` to sort the list.  
13. Print the sorted array `S`.  

## Program:
```
/*
Program to implement Merge Sort
Developed by: AKSHAYAA M
Register Number:  212222230009
*/
```
```python
def Merge_Sort(S):
    
    size = len(S);
    if size>1:
        middle = size // 2
        left_arr = S[:middle]
        right_arr = S[middle:]
        Merge_Sort(left_arr)
        Merge_Sort(right_arr)
        left_size = len(left_arr)
        right_size = len(right_arr)
        i=0
        j=0
        k=0
        
        while i<left_size and j<right_size:
            if left_arr[i]<right_arr[j]:
                S[k] = left_arr[i]
                i += 1
            else:
                S[k] = right_arr[j]
                j += 1
            k +=1
            
        while i<left_size:
            S[k] = left_arr[i]
            i +=1
            k+=1
        while j<right_size:
            S[k] = right_arr[j]
            j +=1
            k+=1
            
            
S=[]
n=int(input())
for i in range(n):
    S.append(int(input()))
print("The Original array is: ",S)
Merge_Sort(S)
print("Array after sorting is: ",S)
```

## Output:

![Screenshot 2025-04-29 110050](https://github.com/user-attachments/assets/1dd0b9d4-666c-4aa3-9e1b-1bf26ea89f84)


## Result:
The program successfully implemented by using merge sort for the given list of values in an iterative approach. 
