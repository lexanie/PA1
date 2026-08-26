## ECE 2112 - Experiment 1: Introduction to Python Programming
This repository contains my solution for Experiment 1: Introduction to Python Programming for ECE 2112: Advanced Computer Programming and Algorithms  

This notebook solves three problems that practice string indexing/slicing, string methods, and extended sequence unpacking — no loops, classes, or external libraries required.  

Author: DE LEON, Maria Nichole Lexanie C. Section: 2ECE-D  

### Experiment Overview
This experiment focuses on **basic Python programming**.
- Python functions
- String operations
- List manipulation

## A. Word Rotation Problem

The **rotate_word()** function moves the first character of a string to the end while keeping the remaining characters in their original order.

> ## Function
def rotate_word(text):  
    remaining = text[1:]  
    return remaining + text[0]  
> ## Test Cases
print(rotate_word("python"))  
print(rotate_word("logic"))  
print(rotate_word("Code"))  
print(rotate_word("A"))  
> ## Expected Output
ythonp  
ogicl  
odeC  
A  

## B. Username Builder Problem

The **make_username()** function creates a username by:
- Converting the names to lowercase
- Removing spaces
- Joining the first and last names with a period (.)
> ## Function
def make_username(first_name, last_name):  
    first_name = first_name.lower().replace(" ", "")  
    last_name = last_name.lower().replace(" ", "")  
    return first_name + "." + last_name  
> ## Test Cases
print(make_username("Ada", "Lovelace"))  
print(make_username("Alan", "Turing"))  
print(make_username("Ana Maria", "De Leon"))  
> ## Expected Output
ada.lovelace  
alan.turing  
anamaria.deleon  

## C. Bookend Swap Problem

The ** swap_bookends()** function swaps the first and last elements of a list while keeping the middle elements in their original order.  
It uses extended sequence unpacking:
first, *middle, last = items
> ## Function
def swap_bookends(items):  
    first, *middle, last = items  
    return [last] + middle + [first]  
> ## Test Cases
print(swap_bookends([1, 2, 3, 4, 5, 6]))  
print(swap_bookends(["red", "green", "blue"]))  
print(swap_bookends([8, 3]))  
> ## Expected Output
[6, 2, 3, 4, 5, 1]  
['blue', 'green', 'red']  
[3, 8]  
