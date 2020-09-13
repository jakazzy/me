---
title: "Algorithm"
date: 2020-09-13T06:18:14Z
draft: false
description: "Notes from Grokking Algorithm as part of Learning in Public"
linktitle: Notes from Grokking Algorithm
lead: "Notes from Grokking Algorithm as part of Learning in Public" # Lead text
categories:
  - "Algorithm and Datastuctures"
tags:
  - "Algorithm"
---

Algorithms refer to series of steps/instructions for achieving a task.

## Binary Search Algorithm:
This algorithm works when the input data or list is sorted inorder. It cuts down the nimner of steps to search for an element in a list. Imagine you are searching for a name, Adwoa in a phone book. The names of the contacts are sorted in alphabetical order

Searching for the names by flipping a page at a time for a phone book of 1000 pages means, it may take maximum 1000steps to find Grena.

Which is quite a lot. Binary search Algorithm on the other hand reduces the number of steps(operations) inorder to find the name Grena.

To use a Binary Search Algorithm, first you flip to the middle of the contact book, check the initial letter of the name in the middle and ask if the letter before or after the letter "G".
If the letter is  before G, taking the name as the lower half, divide the contact book into two again. Compare the initial letter of the middle name with the letter "G" of Grena. If the letter is  is after "G", now move the upper half to this middle letter and repeat the process.
When Grena is found, the algorithm returns the position of Grena in the contact book. If Grena cannot be found in the book, the algorithm returns  null.

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
Big O Notaion provides insight on the maximum number of operations an algorithm perform to run. The focus is on run time of an algorithm. This is not necessaril how fast an algorithm will run but rather how an increase in the size of input will increase an algorithm's run time.

The Common Big O Notation Runtimes include:

      1. O(log n)
      2. O(n)
      3. O(n log n)
      4. O(n2) //n squared
      5. O(n!) // n factorial

Big O Notation is most focused on the worst case scenario
