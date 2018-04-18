---
author:
- Somewha7
title: 'Title Here'
type: Activity
---

Summary
=======

Activity that teaches how to write a quicksort. Part of the Sorting Algorithm Series

Objective
=========
The worst has happened... After stopping Bubble Boy and Billy the Squid in the [previous exercise](https://github.com/junior-devleague/clutter-and-confusion/blob/master/readme.md), Dr. Monsoon has had enough. Now he's coming for Heroes Inc. in his oddly menacing whale-shaped zeppelin, and he means business. Ahead of him he's sent waves of his wily and watery minions, and they're wreaking havoc! All of the lists that you oh so carefully sorted have been unsorted, and they're in such a mess that a bubble or insertion just couldn't sort them quickly enough for Heroes Inc. to be able to use them to prepare before Dr. Monsoon gets here! Whatever shall you do? Fortunately, just in the nick of time, you found a sorting algorithm so powerful as to be inconceivable -- the [quicksort](https://en.wikipedia.org/wiki/Quicksort). This sorting algorithm is far faster than any that you'd heard of, and who knows? It may just be enough to save they day...

Prerequisites
=============

-   Basic usage of Python REPL


Requirements
============

-   Shell terminal or Python IDE
-   

Desired Outcomes
================

-   Understanding of the quicksort algorithm, and the development of the skills required to write one in python

Tasks
=====

1.   Start by definining a function with 1 argument -- the list to sort. This is your sort function, so call it something like quicksort(myList)
2.   Choose a random index value from your list, save it as pivotIndex. This is what you'll use as the pivot to split your list
3.   Create a variable that's equal to the value at the index value of your pivot, save it as pivotValue. This is what you'll use for comparisons
4.   Create 3 empty lists -- left, middle, and right. For every item in your list, if the value of that item is less than your pivotValue, append it to left. If it's equal to pivotValue, append it to middle (This is to account for multiple copies of the same number). If it's greater than pivotValue, append it to right.
5.   If the length of list left is greater than 1, set left as equal to a recursive call of the quicksort function on left
6.   If the length of list right is greater than 1, set right as equal to a recrursive call of the quicksort function on right
7.   Create another empty list, save it as outlist
8.   For each item in left, append that item to outlist
9.   For each item in middle, append that item to outlist
10.   For each item in right, append that item to outlist
11.   return the function as being equal to outlist

How It Works
============

Quicksort is similar to a merge sort in that it uses a [divide and conquer](https://en.wikipedia.org/wiki/Divide_and_conquer_algorithm) approach to sorting an input list. The way that our quicksort works is as follows:
1.   It chooses a pivot point
2.   It splits the list around the pivot point into left & right sublists
3.   It recursively calls itself on those lists when the length of the list is greater than 1 (a list of length 1 is, by definition, sorted. This is our base case) and sets the sublist as equal to that function call, as the function call will return a sorted version of the left/right sublist, running all the way down to the base case ( list length = 1)
4.   After the recursive calling, it creates an output list and appends the left & right sublists in order (along with however many instances with a value equal to the pivot there were between those two)
5.   It returns the output list, which for sublists gets set as being equal to the left/right sublist 1 step up, or for the final case is the actual output list
