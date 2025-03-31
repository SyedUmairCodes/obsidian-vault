# Sets in Python

An unordered collection of distinct elements (members).  No duplicates are allowed.  Because sets are unordered, you cannot access elements by an index (like you can with lists).

* **Distinct Elements:** Each element in a set must be unique. Duplicates are automatically removed upon insertion or creation.
 * **Efficient Membership Testing:** Quickly check if an element exists in a set using optimized data structures (hash tables).  This allows for near-instant lookups, regardless of the set's size.
* **Elimination of Duplicates:** Ensures data cleanliness and conciseness.

## Set Operations

* **Union:** Combines all unique elements from two or more sets. Analogy: merging customer lists from different sources without duplicates.  Use case: aggregating data from different sources, ensuring comprehensive coverage without redundancy.
* **Intersection:** Identifies elements common to two or more sets. Analogy: comparing skills required for different job roles to find overlapping skills. Use case: market analysis (finding customers who buy from multiple categories)
