---
layout:     post
title:      Range Queries
date:       2020-07-13 00:00:00
summary:    
categories: algo
tags: [algo, progress]
comment: true

green: "#d5e9dd"
red: "#ddafb6"
yellow: "#FCF4A3"
---

This post is just for revising range queries. Have highlighted the topics and problems. Might write solutions (my approach) for these problems as well for future reference. 

_to do : create collapsible for solutions + also to put the same in DP post_
 

#### Table of Contents (segment tree)
Link: [cp-algorithms - Segment tree](https://cp-algorithms.com/data_structures/segment_tree.html)

* Simplest form of a Segment Tree ✔️
    * Structure of the Segment Tree ✔️
    * Construction ✔️
    * Sum queries ✔️
    * Update queries ✔️
    * Implementation ✔️
    * Memory efficient implementation ✔️
* Advanced versions of Segment Trees
    * More complex queries ✔️
    * Saving the entire subarrays in each vertex ✔️ 
    * Range updates (Lazy Propagation) ✔️
    * Generalization to higher dimensions 📝
    * Preserving the history of its values (Persistent Segment Tree) 
    * Implicit segment tree 



#### Table of Contents (fenwick tree or BIT)
Link: [cp-algorithms - Fenwick tree](https://cp-algorithms.com/data_structures/fenwick.html)
* Description
    * Overview ✔️
    * Definition of g(i) ✔️
* Implementation
    * Finding sum in one-dimensional array ✔️
    * Finding minimum of [0,r] in one-dimensional array ✔️
    * Finding sum in two-dimensional array ✔️
    * One-based indexing approach ✔️
* Range operations
    1. Point Update and Range Query ✔️
    2. Range Update and Point Query 📝
    3. Range Updates and Range Queries 📝


###### CSES.fi problemSet (Range Queries)

1.  <a href="https://cses.fi/problemset/task/1646">Range Sum Queries I ✔️</a>
2.	<a href="https://cses.fi/problemset/task/1646">Range Sum Queries I ✔️</a>
3.	<a href="https://cses.fi/problemset/task/1647">Range Minimum Queries I ✔️</a>
4.	<a href="https://cses.fi/problemset/task/1648">Range Sum Queries II ✔️</a>
5.	<a href="https://cses.fi/problemset/task/1649">Range Minimum Queries II ✔️</a>
6.	<a href="https://cses.fi/problemset/task/1650">Range Xor Queries ✔️</a>
7.	<a href="https://cses.fi/problemset/task/1651">Range Update Queries ✔️</a>
8.	<a href="https://cses.fi/problemset/task/1652">Forest Queries ✔️</a>
9.	<a href="https://cses.fi/problemset/task/1143">Hotel Queries ✔️</a>
10.	<a href="https://cses.fi/problemset/task/1749">List Removals ✔️</a>
11.	<a href="https://cses.fi/problemset/task/1144">Salary Queries</a>
12.	<a href="https://cses.fi/problemset/task/1190">Subarray Sum Queries</a>
13.	<a href="https://cses.fi/problemset/task/1734">Distinct Values Queries</a>
14.	<a href="https://cses.fi/problemset/task/1739">Forest Queries II</a>
15.	<a href="https://cses.fi/problemset/task/1735">Range Updates and Sums</a>
16.	<a href="https://cses.fi/problemset/task/1736">Polynomial Queries</a>
17.	<a href="https://cses.fi/problemset/task/1737">Range Queries and Copies</a>
