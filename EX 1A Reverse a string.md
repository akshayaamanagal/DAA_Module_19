# EX 1A Reverse a String
## DATE: 18.02.2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm  
1. Define a function `reverse_string(s)` to reverse a string recursively.  
2. Check if the length of `s` is less than or equal to 1; if so, return `s` (base case).  
3. Otherwise, call `reverse_string` on `s[1:]` and append `s[0]` to the result (recursive step).  
4. Read a string from user input and store it in `input_string`.  
5. Call `reverse_string(input_string)` and print the result. 

## Program:
```
/*
Program to implement Reverse a String
Developed by: AKSHAYAA M
Register Number: 212222230009 
*/
```
```python
def reverse_string(s):
   
    if len(s) <= 1:
        return s
    
    return reverse_string(s[1:]) + s[0]


input_string = input()
print(reverse_string(input_string))
```

## Output:

![Screenshot 2025-04-29 104226](https://github.com/user-attachments/assets/d6bbd701-499e-4c87-9e62-470a06f39c5c)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
