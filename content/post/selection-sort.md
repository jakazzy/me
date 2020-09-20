---
title: "Linked List and Array"
date: 2020-09-20T06:13:09Z
draft: false
description: "Notes from Grokking Algorithm as part of Learning in Public"
linktitle: Notes from Grokking Algorithm
lead: "Notes from Grokking Algorithm as part of Learning in Public" # Lead text
categories:
  - "Algorithm and Datastructures"
tags:
  - "Linkedlist"
  - "Arrays"
---

These notes from Grooking Algorithm by Aditya Y Bhargava seeks to understand/ explain the follwing questions:
1. What is an array?
2. What is a linked list?
3. What are the differences between the two
4. What are the pros and cons?
5. Based on the above, when do i use each?

## Array:
Most algorithms require the data to be sorted(eg the Binary search Algorithm). Hence it is necessary to understand the sorting algorithm. Array and Linked list are used for storing data linearly but they have their differences. Array is a data structure in which items in the list are stored contiguosly. Elements are stored in an index Even though items in an array are kept sequential, it breeds couple of challenges. 

### PROS:
-- It is easy to randomly access an element.
### CONS:
-- The size of an array is fixed hence leads to wasting memory especially when spaces are empty.
-- Inserting or deleting an item in an array is slow

## Linkedlist:
This is a linear data structure and its items are unordered. The elements in a linkedlists stores the address of the next item in memory making it possible to traverse a linkedlist from the head down to the last element. Elements in a linkedlist are referred to as nodes.
### PROS: 
-- It is dynamic hence they can easily expand
-- It is easy to perform operations such as insertion and deletion on a linkedlist


### CONS:
-- It is difficult to randomly access an item in a linkedlist(it uses sequential access)
-- Every node consumes extra memory space to contain the address of the next item in sequence.





