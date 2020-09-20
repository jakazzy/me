---
title: "Algorithm"
date: 2020-09-13T06:18:14Z
draft: false
description: "Notes from Grokking Algorithm as part of Learning in Public"
linktitle: Notes from Grokking Algorithm
lead: "Notes from Grokking Algorithm as part of Learning in Public" # Lead text
categories:
  - "Algorithm and Datastructures"
tags:
  - "Binary Search"
  - "Big O Notation"
---

Algorithms refer to series of steps/instructions for achieving a task.

## Binary Search Algorithm:
This algorithm works when the input data or list is sorted inorder. It reduces the number of steps to search for an element in a list. Imagine you are searching for a name, Grena in a phone book. The names of the contacts in the phone book are sorted in alphabetical order.

Searching for a name by flipping a page at a time for a phone book of 1000 pages means, it may take maximum 1000steps to find Grena.

Which is quite a lot steps(operations). Binary search Algorithm, on the other hand reduces the number of operations to be performed inorder to find the name Grena.

To use a Binary Search Algorithm, first you identify the middle of the contact book and flip to that position in the contact book. You identlify the name in that position(middle). Subsequently, you compare the name to the search name, Gren. Then you ask, does Gren come before or after this current middle name? If Gren comes before this current middle name,  mark this position as the highest point. Determine another middle position from the initial page of the book the current highest position(previous middle page). Determine a middle page between the two, compare with Gren, based on  the result shift either the lowest pointer or the highest pointer till Gren is identified. 
This algorithm will be explained in code below(in JavaScript following same proceedure as in the book Grokking algorithm)

If after the process Grena is found, the algorithm returns the position of Grena in the contact book. If Grena cannot be found in the book, the algorithm returns  null.

Demonstrated in code (JavaScript)
      // Binary search as understood from the Grokking Algorithm

      const binarySearch = (arr, item) => {
        let low = 0;
        let high = arr.length - 1;

        while (low <= high) {
          let mid = Math.floor((low + high) / 2);
          let guess = arr[mid];

          if (guess === item) {
            return mid;
          }
          if (guess < item) {
            low = mid + 1;
          }
          if (guess > item) {
            high = mid + 1;
          }
        }
        return null;
      };

      myList = [1, 3, 5, 7, 9];
      console.log(binarySearch(myList, 3)); 

## BIG O NOTATION
Big O Notaion provides insight on the maximum number of operations an algorithm can perform. The focus is on run time of an algorithm. This is not necessarily how fast an algorithm will run but rather how an increase in the size of input will increase an algorithm's run time.

The Common Big O Notation Runtimes include:

      1. O(log n)
      2. O(n)
      3. O(n log n)
      4. O(n2) //n squared
      5. O(n!) // n factorial

Big O Notation is most focused on the worst case scenario. Algorithm is therefore measured in growth.
