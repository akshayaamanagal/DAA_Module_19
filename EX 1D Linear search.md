# EX 1D Linear search
## DATE: 01.03.2025
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.

## Algorithm  
1. Define the `search(List, n)` function to search for an element `n` in the list `List`.  
2. Loop through each element in `List` using a `for` loop and check if the element equals `n`.  
3. If a match is found, return the index of the element.  
4. If the loop completes without finding `n`, return `-1` to indicate that the element is not found.  
5. Read the input for the number of elements in the list and store it.  
6. Use a list comprehension to read `n` elements from the user and store them in `List`.  
7. Read the element `n` to be searched from the user.  
8. Call the `search(List, n)` function to search for the element in the list.  
9. If the result is not `-1`, print "Found"; otherwise, print "Not Found".  

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: AKSHAYAA M
Register Number:  212222230009
*/
```
```python
def search(List,n):
    for i in range(len(List)):
        if List[i]==n:
            return i
    else:
        return -1

List = [input() for _ in range(int(input()))]
n = input()
res = search(List,n)
if res != -1:
    print("Found")
else:
    print("Not Found")
```

## Output:

![image](https://github.com/user-attachments/assets/3a312939-2f1c-478e-81a3-5f3daa10d821)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
