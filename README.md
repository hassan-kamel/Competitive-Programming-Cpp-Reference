# Complete C++ STL & Data Structures Reference for Competitive Programming

## Table of Contents

### 1. [Sequence Containers](#sequence-containers)

- [vector<T>](#1-vector) - Dynamic array with automatic resizing
- [deque<T>](#2-deque) - Double-ended queue
- [list<T>](#3-list) - Doubly linked list
- [forward_list<T>](#4-forward_list) - Singly linked list
- [array<T, N>](#5-array) - Fixed-size array

### 2. [Associative Containers](#associative-containers)

- [set<T>](#1-set) - Ordered unique elements (Red-Black Tree)
- [multiset<T>](#2-multiset) - Ordered elements with duplicates
- [map<K, V>](#3-map) - Ordered key-value pairs
- [multimap<K, V>](#4-multimap) - Ordered key-value pairs with duplicate keys

### 3. [Unordered Containers](#unordered-containers)

- [unordered_set<T>](#1-unordered_set) - Hash table for unique elements
- [unordered_multiset<T>](#2-unordered_multiset) - Hash table with duplicates
- [unordered_map<K, V>](#3-unordered_map) - Hash table for key-value pairs
- [unordered_multimap<K, V>](#4-unordered_multimap) - Hash table with duplicate keys

### 4. [Container Adaptors](#container-adaptors)

- [stack<T>](#1-stack) - LIFO container adapter
- [queue<T>](#2-queue) - FIFO container adapter
- [priority_queue<T>](#3-priority_queue) - Max/Min heap implementation

### 5. [Algorithms](#algorithms)

- [Sorting Algorithms](#1-sorting-algorithms) - sort, stable_sort, partial_sort, nth_element
- [Binary Search](#2-binary-search) - binary_search, lower_bound, upper_bound
- [Heap Operations](#3-heap-operations) - make_heap, push_heap, pop_heap, sort_heap
- [Permutations](#4-permutations) - next_permutation, prev_permutation
- [Numeric Algorithms](#5-numeric-algorithms) - accumulate, partial_sum, gcd, lcm
- [Modifying Algorithms](#6-modifying-algorithms) - fill, generate, transform, replace, remove
- [Non-modifying Algorithms](#7-non-modifying-algorithms) - find, count, search, min_element
- [Set Operations](#8-set-operations) - set_union, set_intersection, set_difference

### 6. [Iterators](#iterators)

- [Iterator Types](#iterator-types) - Forward, Bidirectional, Random Access
- [Iterator Operations](#iterator-operations) - advance, distance, next, prev

### 7. [Utility Classes](#utility-classes)

- [pair<T1, T2>](#1-pair) - Two-element tuple
- [tuple<T1, T2, ...>](#2-tuple) - Multi-element tuple

### 8. [Advanced Data Structures](#advanced-data-structures)

- [Segment Tree](#1-segment-tree-manual-implementation) - Range query and update
- [Fenwick Tree (BIT)](#2-fenwick-tree-binary-indexed-tree) - Efficient prefix sums
- [Disjoint Set Union (DSU)](#3-disjoint-set-union-dsuunion-find) - Union-Find operations
- [Trie (Prefix Tree)](#4-trie-prefix-tree) - String prefix operations

### 9. [String Algorithms](#string-algorithms)

- [String Class Methods](#1-string-class-methods) - Basic string operations
- [String Stream](#2-string-stream) - String parsing and formatting
- [KMP Algorithm](#3-kmp-algorithm-pattern-matching) - Pattern matching
- [Rolling Hash](#4-rolling-hash) - String hashing for fast comparison

### 10. [Bit Manipulation](#bit-manipulation)

- [Basic Operations](#1-basic-operations) - Set, clear, toggle bits
- [Subset Generation](#2-subset-generation) - Generate all subsets

### 11. [Mathematical Functions](#mathematical-functions)

- [Built-in Math Functions](#1-built-in-math-functions) - pow, sqrt, log, trigonometric
- [Combinatorics](#2-combinatorics) - Factorial, combinations, Pascal's triangle

### 12. [Advanced STL Features](#advanced-stl-features)

- [Custom Comparators](#1-custom-comparators) - Custom sorting and ordering
- [Lambda Functions](#2-lambda-functions) - Anonymous functions and closures
- [Function Objects](#3-function-objects-and-functors) - Standard functors and binding

### 13. [Memory Management & Performance](#memory-management--performance-tips)

- [Memory Optimization](#1-memory-optimization) - Reserve, emplace, shrink_to_fit
- [Fast I/O](#2-fast-io) - Optimized input/output
- [Compiler Optimizations](#3-compiler-optimizations) - Pragma directives and inlining

### 14. [Common Patterns](#common-patterns)

- [Two Pointers](#1-two-pointers) - Two pointers technique
- [Sliding Window](#2-sliding-window) - Fixed and variable size windows
- [Prefix Sums](#3-prefix-sums) - 1D and 2D prefix sum arrays
- [Binary Search Patterns](#4-binary-search-patterns) - Different binary search variations
- [Graph Algorithms](#5-graph-algorithms) - DFS, BFS, Dijkstra
- [Dynamic Programming](#6-dynamic-programming-patterns) - 1D, 2D, and space-optimized DP
- [Utility Functions](#7-common-utility-functions) - Fast I/O, modular arithmetic, prime checking

### 15. [Contest-Specific Tips](#contest-specific-tips)

- [Template Structure](#1-template-structure) - Competitive programming template
- [Debugging Macros](#2-debugging-macros) - Debug output macros
- [Common Edge Cases](#3-common-edge-cases) - Things to watch out for
- [Time Complexity Guidelines](#4-time-complexity-guidelines) - Constraint-based complexity selection

---

## Sequence Containers

### 1. vector<T>

**Dynamic array with automatic resizing**

```cpp
#include <vector>
vector<int> v;
```

**Methods & Big O:**

- `push_back(val)` - O(1) amortized
- `pop_back()` - O(1)
- `insert(pos, val)` - O(n)
- `erase(pos)` - O(n)
- `size()` - O(1)
- `empty()` - O(1)
- `clear()` - O(n)
- `resize(n)` - O(n)
- `reserve(n)` - O(n)
- `operator[]` - O(1)
- `at(i)` - O(1)
- `front()` - O(1)
- `back()` - O(1)
- `begin()`, `end()` - O(1)

**Space Complexity:** O(n)

### 2. deque<T>

**Double-ended queue**

```cpp
#include <deque>
deque<int> dq;
```

**Methods & Big O:**

- `push_front(val)` - O(1)
- `push_back(val)` - O(1)
- `pop_front()` - O(1)
- `pop_back()` - O(1)
- `insert(pos, val)` - O(n)
- `erase(pos)` - O(n)
- `operator[]` - O(1)
- `at(i)` - O(1)
- `size()` - O(1)

**Space Complexity:** O(n)

### 3. list<T>

**Doubly linked list**

```cpp
#include <list>
list<int> lst;
```

**Methods & Big O:**

- `push_front(val)` - O(1)
- `push_back(val)` - O(1)
- `pop_front()` - O(1)
- `pop_back()` - O(1)
- `insert(pos, val)` - O(1)
- `erase(pos)` - O(1)
- `remove(val)` - O(n)
- `sort()` - O(n log n)
- `merge(other)` - O(n + m)
- `splice(pos, other)` - O(1) or O(n)
- `size()` - O(1)

**Space Complexity:** O(n)

### 4. forward_list<T>

**Singly linked list**

```cpp
#include <forward_list>
forward_list<int> fl;
```

**Methods & Big O:**

- `push_front(val)` - O(1)
- `pop_front()` - O(1)
- `insert_after(pos, val)` - O(1)
- `erase_after(pos)` - O(1)
- `remove(val)` - O(n)
- `sort()` - O(n log n)

**Space Complexity:** O(n)

### 5. array<T, N>

**Fixed-size array**

```cpp
#include <array>
array<int, 100> arr;
```

**Methods & Big O:**

- `operator[]` - O(1)
- `at(i)` - O(1)
- `front()` - O(1)
- `back()` - O(1)
- `size()` - O(1)
- `fill(val)` - O(n)

**Space Complexity:** O(n)

---

## Associative Containers

### 1. set<T>

**Ordered unique elements (Red-Black Tree)**

```cpp
#include <set>
set<int> s;
```

**Methods & Big O:**

- `insert(val)` - O(log n)
- `erase(val)` - O(log n)
- `find(val)` - O(log n)
- `count(val)` - O(log n)
- `lower_bound(val)` - O(log n)
- `upper_bound(val)` - O(log n)
- `equal_range(val)` - O(log n)
- `size()` - O(1)
- `empty()` - O(1)
- `clear()` - O(n)

**Space Complexity:** O(n)

### 2. multiset<T>

**Ordered elements with duplicates allowed**

```cpp
#include <set>
multiset<int> ms;
```

**Same methods as set with same complexities**

- `count(val)` can return > 1

### 3. map<K, V>

**Ordered key-value pairs (Red-Black Tree)**

```cpp
#include <map>
map<int, string> m;
```

**Methods & Big O:**

- `insert({key, val})` - O(log n)
- `erase(key)` - O(log n)
- `find(key)` - O(log n)
- `operator[key]` - O(log n)
- `at(key)` - O(log n)
- `count(key)` - O(log n)
- `lower_bound(key)` - O(log n)
- `upper_bound(key)` - O(log n)
- `size()` - O(1)

**Space Complexity:** O(n)

### 4. multimap<K, V>

**Ordered key-value pairs with duplicate keys**

```cpp
#include <map>
multimap<int, string> mm;
```

**Same methods as map with same complexities**

---

## Unordered Containers

### 1. unordered_set<T>

**Hash table for unique elements**

```cpp
#include <unordered_set>
unordered_set<int> us;
```

**Methods & Big O:**

- `insert(val)` - O(1) average, O(n) worst
- `erase(val)` - O(1) average, O(n) worst
- `find(val)` - O(1) average, O(n) worst
- `count(val)` - O(1) average, O(n) worst
- `size()` - O(1)
- `bucket_count()` - O(1)
- `load_factor()` - O(1)
- `rehash(n)` - O(n)

**Space Complexity:** O(n)

### 2. unordered_multiset<T>

**Hash table with duplicate elements**

```cpp
#include <unordered_set>
unordered_multiset<int> ums;
```

**Same methods as unordered_set**

### 3. unordered_map<K, V>

**Hash table for key-value pairs**

```cpp
#include <unordered_map>
unordered_map<int, string> um;
```

**Methods & Big O:**

- `insert({key, val})` - O(1) average, O(n) worst
- `erase(key)` - O(1) average, O(n) worst
- `find(key)` - O(1) average, O(n) worst
- `operator[key]` - O(1) average, O(n) worst
- `at(key)` - O(1) average, O(n) worst
- `count(key)` - O(1) average, O(n) worst

**Space Complexity:** O(n)

### 4. unordered_multimap<K, V>

**Hash table with duplicate keys**

```cpp
#include <unordered_map>
unordered_multimap<int, string> umm;
```

**Same methods as unordered_map**

---

## Container Adaptors

### 1. stack<T>

**LIFO container adapter**

```cpp
#include <stack>
stack<int> st;
```

**Methods & Big O:**

- `push(val)` - O(1)
- `pop()` - O(1)
- `top()` - O(1)
- `empty()` - O(1)
- `size()` - O(1)

**Space Complexity:** O(n)

### 2. queue<T>

**FIFO container adapter**

```cpp
#include <queue>
queue<int> q;
```

**Methods & Big O:**

- `push(val)` - O(1)
- `pop()` - O(1)
- `front()` - O(1)
- `back()` - O(1)
- `empty()` - O(1)
- `size()` - O(1)

**Space Complexity:** O(n)

### 3. priority_queue<T>

**Max heap by default**

```cpp
#include <queue>
priority_queue<int> pq;                    // max heap
priority_queue<int, vector<int>, greater<int>> min_pq; // min heap
```

**Methods & Big O:**

- `push(val)` - O(log n)
- `pop()` - O(log n)
- `top()` - O(1)
- `empty()` - O(1)
- `size()` - O(1)

**Space Complexity:** O(n)

---

## Algorithms

### 1. Sorting Algorithms

```cpp
#include <algorithm>

// Sort
sort(v.begin(), v.end());                    // O(n log n)
sort(v.begin(), v.end(), greater<int>());    // O(n log n) descending

// Stable sort
stable_sort(v.begin(), v.end());             // O(n log n)

// Partial sort
partial_sort(v.begin(), v.begin()+k, v.end()); // O(n log k)

// Nth element
nth_element(v.begin(), v.begin()+k, v.end()); // O(n) average

// Is sorted
is_sorted(v.begin(), v.end());               // O(n)
```

### 2. Binary Search

```cpp
// Binary search
binary_search(v.begin(), v.end(), val);      // O(log n)

// Lower/Upper bound
lower_bound(v.begin(), v.end(), val);        // O(log n)
upper_bound(v.begin(), v.end(), val);        // O(log n)
equal_range(v.begin(), v.end(), val);        // O(log n)
```

### 3. Heap Operations

```cpp
// Make heap
make_heap(v.begin(), v.end());               // O(n)

// Push/Pop heap
push_heap(v.begin(), v.end());               // O(log n)
pop_heap(v.begin(), v.end());                // O(log n)

// Sort heap
sort_heap(v.begin(), v.end());               // O(n log n)

// Is heap
is_heap(v.begin(), v.end());                 // O(n)
```

### 4. Permutations

```cpp
// Next/Previous permutation
next_permutation(v.begin(), v.end());        // O(n)
prev_permutation(v.begin(), v.end());        // O(n)

// Is permutation
is_permutation(v1.begin(), v1.end(), v2.begin()); // O(n²) or O(n)
```

### 5. Numeric Algorithms

```cpp
#include <numeric>

// Accumulate
accumulate(v.begin(), v.end(), 0);           // O(n)

// Partial sum
partial_sum(v.begin(), v.end(), result.begin()); // O(n)

// Adjacent difference
adjacent_difference(v.begin(), v.end(), result.begin()); // O(n)

// Inner product
inner_product(v1.begin(), v1.end(), v2.begin(), 0); // O(n)

// GCD/LCM (C++14)
gcd(a, b);                                   // O(log min(a,b))
lcm(a, b);                                   // O(log min(a,b))
```

### 6. Modifying Algorithms

```cpp
// Fill
fill(v.begin(), v.end(), val);               // O(n)
fill_n(v.begin(), n, val);                   // O(n)

// Generate
generate(v.begin(), v.end(), rand);          // O(n)

// Transform
transform(v.begin(), v.end(), result.begin(), func); // O(n)

// Replace
replace(v.begin(), v.end(), old_val, new_val); // O(n)

// Remove
remove(v.begin(), v.end(), val);             // O(n)
remove_if(v.begin(), v.end(), predicate);    // O(n)

// Unique
unique(v.begin(), v.end());                  // O(n)

// Reverse
reverse(v.begin(), v.end());                 // O(n)

// Rotate
rotate(v.begin(), v.begin()+k, v.end());     // O(n)

// Random shuffle
random_shuffle(v.begin(), v.end());          // O(n)
shuffle(v.begin(), v.end(), rng);            // O(n)
```

### 7. Non-modifying Algorithms

```cpp
// Find
find(v.begin(), v.end(), val);               // O(n)
find_if(v.begin(), v.end(), predicate);      // O(n)

// Count
count(v.begin(), v.end(), val);              // O(n)
count_if(v.begin(), v.end(), predicate);     // O(n)

// Search
search(v1.begin(), v1.end(), v2.begin(), v2.end()); // O(nm)

// Min/Max
min_element(v.begin(), v.end());             // O(n)
max_element(v.begin(), v.end());             // O(n)
minmax_element(v.begin(), v.end());          // O(n)

// Equal
equal(v1.begin(), v1.end(), v2.begin());     // O(n)

// Mismatch
mismatch(v1.begin(), v1.end(), v2.begin());  // O(n)
```

### 8. Set Operations (on sorted ranges)

```cpp
// Set union
set_union(v1.begin(), v1.end(), v2.begin(), v2.end(), result.begin()); // O(n+m)

// Set intersection
set_intersection(v1.begin(), v1.end(), v2.begin(), v2.end(), result.begin()); // O(n+m)

// Set difference
set_difference(v1.begin(), v1.end(), v2.begin(), v2.end(), result.begin()); // O(n+m)

// Set symmetric difference
set_symmetric_difference(v1.begin(), v1.end(), v2.begin(), v2.end(), result.begin()); // O(n+m)

// Includes
includes(v1.begin(), v1.end(), v2.begin(), v2.end()); // O(n+m)
```

---

## Iterators

### Iterator Types

```cpp
// Forward iterator
forward_list<int>::iterator

// Bidirectional iterator
list<int>::iterator, set<int>::iterator, map<int,int>::iterator

// Random access iterator
vector<int>::iterator, deque<int>::iterator, array<int,N>::iterator
```

### Iterator Operations

```cpp
// Advance
advance(it, n);                              // O(1) for random access, O(n) otherwise

// Distance
distance(first, last);                       // O(1) for random access, O(n) otherwise

// Next/Prev
next(it, n);                                 // O(1) for random access, O(n) otherwise
prev(it, n);                                 // O(1) for random access, O(n) otherwise
```

---

## Utility Classes

### 1. pair<T1, T2>

```cpp
#include <utility>
pair<int, string> p = {1, "hello"};
pair<int, string> p = make_pair(1, "hello");

// Access
p.first, p.second

// Compare: lexicographically
p1 < p2, p1 == p2
```

### 2. tuple<T1, T2, ...> (C++11)

```cpp
#include <tuple>
tuple<int, string, double> t = make_tuple(1, "hello", 3.14);

// Access
get<0>(t), get<1>(t), get<2>(t)

// Tie
int x; string s; double d;
tie(x, s, d) = t;

// Structured bindings (C++17)
auto [x, s, d] = t;
```

---

## Advanced Data Structures

### 1. Segment Tree (Manual Implementation)

```cpp
class SegmentTree {
    vector<int> tree;
    int n;

public:
    SegmentTree(vector<int>& arr) {
        n = arr.size();
        tree.resize(4 * n);
        build(arr, 1, 0, n - 1);
    }

    void build(vector<int>& arr, int node, int start, int end) {
        if (start == end) {
            tree[node] = arr[start];
        } else {
            int mid = (start + end) / 2;
            build(arr, 2*node, start, mid);
            build(arr, 2*node+1, mid+1, end);
            tree[node] = tree[2*node] + tree[2*node+1];
        }
    }

    void update(int node, int start, int end, int idx, int val) {
        if (start == end) {
            tree[node] = val;
        } else {
            int mid = (start + end) / 2;
            if (idx <= mid) {
                update(2*node, start, mid, idx, val);
            } else {
                update(2*node+1, mid+1, end, idx, val);
            }
            tree[node] = tree[2*node] + tree[2*node+1];
        }
    }

    int query(int node, int start, int end, int l, int r) {
        if (r < start || end < l) {
            return 0;
        }
        if (l <= start && end <= r) {
            return tree[node];
        }
        int mid = (start + end) / 2;
        return query(2*node, start, mid, l, r) +
               query(2*node+1, mid+1, end, l, r);
    }

    void update(int idx, int val) { update(1, 0, n-1, idx, val); }
    int query(int l, int r) { return query(1, 0, n-1, l, r); }
};
```

**Time Complexity:**

- Build: O(n)
- Update: O(log n)
- Query: O(log n)
- Space: O(n)

### 2. Fenwick Tree (Binary Indexed Tree)

```cpp
class FenwickTree {
    vector<int> tree;
    int n;

public:
    FenwickTree(int size) : n(size), tree(size + 1, 0) {}

    void update(int idx, int val) {
        for (++idx; idx <= n; idx += idx & -idx) {
            tree[idx] += val;
        }
    }

    int query(int idx) {
        int sum = 0;
        for (++idx; idx > 0; idx -= idx & -idx) {
            sum += tree[idx];
        }
        return sum;
    }

    int range_query(int l, int r) {
        return query(r) - (l > 0 ? query(l - 1) : 0);
    }
};
```

**Time Complexity:**

- Update: O(log n)
- Query: O(log n)
- Space: O(n)

### 3. Disjoint Set Union (DSU/Union-Find)

```cpp
class DSU {
    vector<int> parent, rank;

public:
    DSU(int n) : parent(n), rank(n, 0) {
        iota(parent.begin(), parent.end(), 0);
    }

    int find(int x) {
        if (parent[x] != x) {
            parent[x] = find(parent[x]); // path compression
        }
        return parent[x];
    }

    bool unite(int x, int y) {
        int px = find(x), py = find(y);
        if (px == py) return false;

        if (rank[px] < rank[py]) swap(px, py);
        parent[py] = px;
        if (rank[px] == rank[py]) rank[px]++;

        return true;
    }

    bool connected(int x, int y) {
        return find(x) == find(y);
    }
};
```

**Time Complexity:**

- Find: O(α(n)) amortized (α is inverse Ackermann)
- Union: O(α(n)) amortized
- Space: O(n)

### 4. Trie (Prefix Tree)

```cpp
class Trie {
    struct TrieNode {
        TrieNode* children[26];
        bool is_end;

        TrieNode() : is_end(false) {
            fill(children, children + 26, nullptr);
        }
    };

    TrieNode* root;

public:
    Trie() { root = new TrieNode(); }

    void insert(string word) {
        TrieNode* node = root;
        for (char c : word) {
            int idx = c - 'a';
            if (!node->children[idx]) {
                node->children[idx] = new TrieNode();
            }
            node = node->children[idx];
        }
        node->is_end = true;
    }

    bool search(string word) {
        TrieNode* node = root;
        for (char c : word) {
            int idx = c - 'a';
            if (!node->children[idx]) return false;
            node = node->children[idx];
        }
        return node->is_end;
    }

    bool starts_with(string prefix) {
        TrieNode* node = root;
        for (char c : prefix) {
            int idx = c - 'a';
            if (!node->children[idx]) return false;
            node = node->children[idx];
        }
        return true;
    }
};
```

**Time Complexity:**

- Insert: O(m) where m is word length
- Search: O(m)
- StartsWith: O(m)
- Space: O(ALPHABET_SIZE _ N _ M) where N is number of words

---

## Common Patterns

### 1. Two Pointers

```cpp
// Two pointers from both ends
int left = 0, right = n - 1;
while (left < right) {
    if (condition) {
        left++;
    } else {
        right--;
    }
}

// Two pointers same direction
int slow = 0, fast = 0;
while (fast < n) {
    if (condition) {
        arr[slow++] = arr[fast];
    }
    fast++;
}
```

### 2. Sliding Window

```cpp
// Fixed size window
int window_sum = 0;
for (int i = 0; i < k; i++) {
    window_sum += arr[i];
}

int max_sum = window_sum;
for (int i = k; i < n; i++) {
    window_sum += arr[i] - arr[i - k];
    max_sum = max(max_sum, window_sum);
}

// Variable size window
int left = 0, right = 0;
while (right < n) {
    // Expand window
    add_to_window(arr[right]);

    // Contract window if needed
    while (window_invalid()) {
        remove_from_window(arr[left]);
        left++;
    }

    // Update result
    update_result();
    right++;
}
```

### 3. Prefix Sums

```cpp
// 1D prefix sum
vector<int> prefix(n + 1, 0);
for (int i = 0; i < n; i++) {
    prefix[i + 1] = prefix[i] + arr[i];
}

// Range sum query
int range_sum(int l, int r) {
    return prefix[r + 1] - prefix[l];
}

// 2D prefix sum
vector<vector<int>> prefix(m + 1, vector<int>(n + 1, 0));
for (int i = 1; i <= m; i++) {
    for (int j = 1; j <= n; j++) {
        prefix[i][j] = matrix[i-1][j-1] + prefix[i-1][j] +
                       prefix[i][j-1] - prefix[i-1][j-1];
    }
}
```

### 4. Binary Search Patterns

```cpp
// Standard binary search
int binary_search(vector<int>& arr, int target) {
    int left = 0, right = arr.size() - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == target) return mid;
        if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1;
}

// Lower bound (first >= target)
int lower_bound(vector<int>& arr, int target) {
    int left = 0, right = arr.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] < target) left = mid + 1;
        else right = mid;
    }
    return left;
}

// Upper bound (first > target)
int upper_bound(vector<int>& arr, int target) {
    int left = 0, right = arr.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] <= target) left = mid + 1;
        else right = mid;
    }
    return left;
}
```

### 5. Graph Algorithms

```cpp
// DFS
void dfs(vector<vector<int>>& adj, vector<bool>& visited, int u) {
    visited[u] = true;
    for (int v : adj[u]) {
        if (!visited[v]) {
            dfs(adj, visited, v);
        }
    }
}

// BFS
void bfs(vector<vector<int>>& adj, int start) {
    vector<bool> visited(adj.size(), false);
    queue<int> q;

    q.push(start);
    visited[start] = true;

    while (!q.empty()) {
        int u = q.front();
        q.pop();

        for (int v : adj[u]) {
            if (!visited[v]) {
                visited[v] = true;
                q.push(v);
            }
        }
    }
}

// Dijkstra's Algorithm
vector<int> dijkstra(vector<vector<pair<int, int>>>& adj, int start) {
    int n = adj.size();
    vector<int> dist(n, INT_MAX);
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;

    dist[start] = 0;
    pq.push({0, start});

    while (!pq.empty()) {
        int d = pq.top().first;
        int u = pq.top().second;
        pq.pop();

        if (d > dist[u]) continue;

        for (auto& edge : adj[u]) {
            int v = edge.first;
            int w = edge.second;

            if (dist[u] + w < dist[v]) {
                dist[v] = dist[u] + w;
                pq.push({dist[v], v});
            }
        }
    }

    return dist;
}
```

### 6. Dynamic Programming Patterns

```cpp
// 1D DP
vector<int> dp(n + 1, 0);
dp[0] = base_case;
for (int i = 1; i <= n; i++) {
    dp[i] = transition(dp[i-1], dp[i-2], ...);
}

// 2D DP
vector<vector<int>> dp(m + 1, vector<int>(n + 1, 0));
// Initialize base cases
for (int i = 1; i <= m; i++) {
    for (int j = 1; j <= n; j++) {
        dp[i][j] = transition(dp[i-1][j], dp[i][j-1], ...);
    }
}

// Space-optimized DP
vector<int> prev(n + 1, 0), curr(n + 1, 0);
for (int i = 1; i <= m; i++) {
    for (int j = 1; j <= n; j++) {
        curr[j] = transition(prev[j], curr[j-1], ...);
    }
    swap(prev, curr);
}
```

### 7. Common Utility Functions

```cpp
// Fast I/O
ios_base::sync_with_stdio(false);
cin.tie(NULL);

// Modular arithmetic
const int MOD = 1e9 + 7;
long long mod_pow(long long base, long long exp, long long mod) {
    long long result = 1;
    while (exp > 0) {
        if (exp % 2 == 1) result = (result * base) % mod;
        base = (base * base) % mod;
        exp /= 2;
    }
    return result;
}

// GCD/LCM
int gcd(int a, int b) {
    return b ? gcd(b, a % b) : a;
}

int lcm(int a, int b) {
    return a / gcd(a, b) * b;
}

// Check if number is prime
bool is_prime(int n) {
    if (n <= 1) return false;
    if (n <= 3) return true;
    if (n % 2 == 0 || n % 3 == 0) return false;
    for (int i = 5; i * i <= n; i += 6) {
        if (n % i == 0 || n % (i + 2) == 0) return false;
    }
    return true;
}

// Sieve of Eratosthenes
vector<bool> sieve(int n) {
    vector<bool> is_prime(n + 1, true);
    is_prime[0] = is_prime[1] = false;
    for (int i = 2; i * i <= n; i++) {
        if (is_prime[i]) {
            for (int j = i * i; j <= n; j += i) {
                is_prime[j] = false;
            }
        }
    }
    return is_prime;
}

// All divisors of a number
vector<int> get_divisors(int n) {
    vector<int> divisors;
    for (int i = 1; i * i <= n; i++) {
        if (n % i == 0) {
            divisors.push_back(i);
            if (i != n / i) {
                divisors.push_back(n / i);
            }
        }
    }
    sort(divisors.begin(), divisors.end());
    return divisors;
}

// Prime factorization
vector<pair<int, int>> prime_factors(int n) {
    vector<pair<int, int>> factors;
    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            int count = 0;
            while (n % i == 0) {
                n /= i;
                count++;
            }
            factors.push_back({i, count});
        }
    }
    if (n > 1) {
        factors.push_back({n, 1});
    }
    return factors;
}
```

---

## String Algorithms

### 1. String Class Methods

```cpp
#include <string>
#include <algorithm>
#include <cctype>
string s = "hello";
```

**Basic Operations - O(1)**

```cpp
// Length and size
s.length(), s.size()                    // Returns string length
s.empty()                              // Check if string is empty
s.clear()                              // Remove all characters

// Examples
string str = "hello world";
cout << str.length() << endl;          // Output: 11
cout << str.size() << endl;            // Output: 11
cout << str.empty() << endl;           // Output: 0 (false)

str.clear();
cout << str.empty() << endl;           // Output: 1 (true)
```

**Access Operations - O(1)**

```cpp
// Element access
s[i], s.at(i)                          // Access character at index (at() throws exception if out of range)
s.front(), s.back()                    // Access first/last character

// Examples
string str = "hello";
cout << str[0] << endl;                // Output: h
cout << str.at(1) << endl;             // Output: e
cout << str.front() << endl;           // Output: h
cout << str.back() << endl;            // Output: o

// str.at(10) would throw std::out_of_range exception
```

**Capacity Operations - O(1)**

```cpp
// Capacity information
s.capacity()                           // Current allocated capacity
s.reserve(n)                           // Reserve space for at least n characters
s.resize(n)                            // Resize string to n characters
s.resize(n, c)                         // Resize string to n characters, fill with c
s.shrink_to_fit()                      // Reduce capacity to match size

// Examples
string str = "hi";
cout << str.capacity() << endl;        // May vary (implementation dependent)
cout << str.size() << endl;            // Output: 2

str.reserve(100);
cout << str.capacity() << endl;        // Output: 100 or more

str.resize(5, '!');
cout << str << endl;                   // Output: hi!!!

str.shrink_to_fit();
cout << str.capacity() << endl;        // Reduced to match size
```

**Modification Operations - O(n) for insertion/deletion**

```cpp
// Append operations
s.push_back(c)                         // Add character to end
s.append(str)                          // Append string
s.append(str, pos, len)                // Append substring
s += str                               // Concatenate strings
s += c                                 // Append character

// Insert operations
s.insert(pos, str)                     // Insert string at position
s.insert(pos, str, len)                // Insert substring
s.insert(pos, n, c)                    // Insert n copies of character

// Erase operations
s.erase(pos, len)                      // Erase substring
s.erase(it)                           // Erase character at iterator
s.erase(first, last)                   // Erase range
s.pop_back()                          // Remove last character

// Replace operations
s.replace(pos, len, str)              // Replace substring with string
s.replace(first, last, str)           // Replace range with string

// Examples
string str = "hello";

// Append operations
str.push_back('!');
cout << str << endl;                   // Output: hello!

str.append(" world");
cout << str << endl;                   // Output: hello! world

str += "!";
cout << str << endl;                   // Output: hello! world!!

// Insert operations
str.insert(5, " beautiful");
cout << str << endl;                   // Output: hello beautiful! world!!

// Erase operations
str.erase(5, 11);                      // Remove " beautiful"
cout << str << endl;                   // Output: hello! world!!

str.pop_back();
cout << str << endl;                   // Output: hello! world!

// Replace operations
str.replace(0, 5, "Hi");
cout << str << endl;                   // Output: Hi! world!
```

**Substring Operations - O(n)**

```cpp
// Substring extraction
s.substr(pos, len)                     // Get substring starting at pos with length len
s.substr(pos)                         // Get substring from pos to end

// Examples
string str = "hello world";
string sub1 = str.substr(0, 5);        // "hello"
string sub2 = str.substr(6);           // "world"
string sub3 = str.substr(6, 3);        // "wor"
```

**Search Operations - O(n*m) where n is string length, m is pattern length**

```cpp
// Find operations
s.find(str, pos)                      // Find first occurrence of str starting from pos
s.rfind(str, pos)                     // Find last occurrence of str starting from pos
s.find_first_of(chars, pos)           // Find first character from chars starting from pos
s.find_last_of(chars, pos)            // Find last character from chars starting from pos
s.find_first_not_of(chars, pos)       // Find first character not in chars starting from pos
s.find_last_not_of(chars, pos)        // Find last character not in chars starting from pos

// Return value: string::npos if not found, otherwise the position

// Examples
string str = "hello world, hello universe";
string pattern = "hello";

// Find operations
size_t pos1 = str.find(pattern);       // Position of first "hello" (0)
size_t pos2 = str.find(pattern, 5);    // Position of second "hello" (13)
size_t pos3 = str.rfind(pattern);      // Position of last "hello" (13)
size_t pos4 = str.find("xyz");          // string::npos (not found)

cout << pos1 << " " << pos2 << " " << pos3 << " " << pos4 << endl;

// Character set operations
string vowels = "aeiou";
size_t pos5 = str.find_first_of(vowels);      // Position of first vowel (1 - 'e')
size_t pos6 = str.find_first_not_of("helo wrd,"); // Position of first non-matching char (11 - 'u')

cout << pos5 << " " << pos6 << endl;
```

**Comparison Operations - O(n)**

```cpp
// Comparison
s.compare(str)                        // Compare strings lexicographically
s.compare(pos, len, str)              // Compare substring with string
s.compare(pos, len, str, pos2, len2)  // Compare substrings

// Operators
s == str, s != str, s < str, s <= str, s > str, s >= str

// Examples
string str1 = "apple";
string str2 = "banana";
string str3 = "Apple";

cout << (str1 < str2) << endl;         // Output: 1 (true) - 'a' < 'b'
cout << (str1 == str3) << endl;        // Output: 0 (false) - case sensitive
cout << str1.compare(str2) << endl;    // Negative value - str1 < str2

int result = str1.compare(0, 3, str3, 0, 3);  // Compare "app" vs "App"
cout << result << endl;                // Positive value - 'a' > 'A' in ASCII
```

**Case Conversion Operations**

```cpp
// Case conversion (C++11, requires <algorithm> and <cctype>)
transform(s.begin(), s.end(), s.begin(), ::toupper);  // Convert to uppercase
transform(s.begin(), s.end(), s.begin(), ::tolower);  // Convert to lowercase

// Check character cases
isupper(c), islower(c), isalpha(c), isdigit(c), isalnum(c), isspace(c)

// Examples
string str = "Hello World!";
cout << str << endl;                   // Output: Hello World!

// Convert to uppercase
string upper = str;
transform(upper.begin(), upper.end(), upper.begin(), ::toupper);
cout << upper << endl;                 // Output: HELLO WORLD!

// Convert to lowercase
string lower = str;
transform(lower.begin(), lower.end(), lower.begin(), ::tolower);
cout << lower << endl;                 // Output: hello world!

// Check characters
cout << isupper('A') << endl;          // Output: 1 (true)
cout << islower('a') << endl;          // Output: 1 (true)
cout << isdigit('5') << endl;          // Output: 1 (true)
cout << isspace(' ') << endl;          // Output: 1 (true)
```

**Iterator Operations - O(1)**

```cpp
// Iterator access
s.begin(), s.end()                    // Iterator to beginning/end
s.rbegin(), s.rend()                  // Reverse iterator to beginning/end
s.cbegin(), s.cend()                  // Const iterator to beginning/end
s.crbegin(), s.crend()                // Const reverse iterator to beginning/end

// Examples
string str = "hello";

// Forward iteration
for (auto it = str.begin(); it != str.end(); ++it) {
    cout << *it << " ";
}
cout << endl;                          // Output: h e l l o

// Reverse iteration
for (auto it = str.rbegin(); it != str.rend(); ++it) {
    cout << *it << " ";
}
cout << endl;                          // Output: o l l e h

// Range-based for loop
for (char c : str) {
    cout << c << " ";
}
cout << endl;                          // Output: h e l l o
```

**Numeric Conversions**

```cpp
// String to number
stoi(s), stol(s), stoll(s)             // String to int/long/long long
stoul(s), stoull(s)                   // String to unsigned long/unsigned long long
stof(s), stod(s), stold(s)            // String to float/double/long double

// Number to string
to_string(num)                        // Convert any numeric type to string

// Examples
string num_str = "12345";
int num = stoi(num_str);
cout << num << endl;                   // Output: 12345

string float_str = "3.14159";
double pi = stod(float_str);
cout << pi << endl;                    // Output: 3.14159

int number = 42;
string str_num = to_string(number);
cout << str_num << endl;               // Output: "42"

double decimal = 3.14159;
string str_decimal = to_string(decimal);
cout << str_decimal << endl;           // Output: "3.141590"
```

**Common String Manipulation Patterns**

```cpp
// Remove all occurrences of a character
string remove_char(string s, char c) {
    s.erase(remove(s.begin(), s.end(), c), s.end());
    return s;
}

// Check if string is palindrome
bool is_palindrome(string s) {
    string rev = s;
    reverse(rev.begin(), rev.end());
    return s == rev;
}

// Count words in a string
int count_words(string s) {
    stringstream ss(s);
    string word;
    int count = 0;
    while (ss >> word) count++;
    return count;
}

// Examples
string str = "hello world!!";
cout << remove_char(str, '!') << endl; // Output: "hello world"

string pal = "radar";
cout << is_palindrome(pal) << endl;    // Output: 1 (true)

**String Concatenation and Merging**

```cpp
// Multiple ways to merge/combine strings

// Method 1: Using += operator
string str1 = "Hello";
string str2 = " World";
str1 += str2;                          // str1 becomes "Hello World"
str1 += "!";                           // str1 becomes "Hello World!"

// Method 2: Using append()
string str3 = "Hello";
str3.append(" World");                 // str3 becomes "Hello World"
str3.append("!");                      // str3 becomes "Hello World!"

// Method 3: Using + operator (creates new string)
string str4 = "Hello";
string str5 = " World";
string result = str4 + str5;           // result = "Hello World"
result = result + "!";                 // result = "Hello World!"

// Method 4: Using stringstream for complex merging
stringstream ss;
ss << "Hello" << " " << "World" << "!";
string merged = ss.str();              // merged = "Hello World!"

// Method 5: Using insert() to merge at specific position
string base = "Hello!";
base.insert(5, " Beautiful");          // base = "Hello Beautiful!"

// Method 6: Using replace() to merge by replacing
string target = "Hello";
target.replace(0, 0, "Hi ");          // target = "Hi Hello"

// Examples
string first = "Hello";
string second = "World";

// Multiple concatenation methods
cout << first + " " + second << endl;  // Output: Hello World
cout << (first += second) << endl;     // Output: HelloWorld

// Merging with separators
vector<string> words = {"Hello", "World", "C++"};
string sentence;
for (size_t i = 0; i < words.size(); i++) {
    sentence += words[i];
    if (i < words.size() - 1) {
        sentence += " ";
    }
}
cout << sentence << endl;              // Output: Hello World C++

// Complex merging with stringstream
stringstream complex_ss;
complex_ss << "Number: " << 42 << ", String: " << "Hello" << ", Float: " << 3.14;
cout << complex_ss.str() << endl;      // Output: Number: 42, String: Hello, Float: 3.14
```

### 2. String Stream

```cpp
#include <sstream>

// String to stream
stringstream ss(str);
string word;
while (ss >> word) {
    // process word
}

// Stream to string
stringstream ss;
ss << "Hello " << 123 << " World";
string result = ss.str();

// Reset stringstream
ss.str("");
ss.clear();
```

### 3. KMP Algorithm (Pattern Matching)

```cpp
vector<int> compute_lps(string pattern) {
    int m = pattern.length();
    vector<int> lps(m, 0);
    int len = 0;
    int i = 1;

    while (i < m) {
        if (pattern[i] == pattern[len]) {
            len++;
            lps[i] = len;
            i++;
        } else {
            if (len != 0) {
                len = lps[len - 1];
            } else {
                lps[i] = 0;
                i++;
            }
        }
    }
    return lps;
}

vector<int> kmp_search(string text, string pattern) {
    int n = text.length();
    int m = pattern.length();
    vector<int> lps = compute_lps(pattern);
    vector<int> result;

    int i = 0; // index for text
    int j = 0; // index for pattern

    while (i < n) {
        if (pattern[j] == text[i]) {
            i++;
            j++;
        }

        if (j == m) {
            result.push_back(i - j);
            j = lps[j - 1];
        } else if (i < n && pattern[j] != text[i]) {
            if (j != 0) {
                j = lps[j - 1];
            } else {
                i++;
            }
        }
    }
    return result;
}
```

**Time Complexity:** O(n + m)

### 4. Rolling Hash

```cpp
class RollingHash {
    const int MOD = 1e9 + 7;
    const int BASE = 31;
    vector<long long> hash, pow_base;

public:
    RollingHash(string s) {
        int n = s.length();
        hash.resize(n + 1, 0);
        pow_base.resize(n + 1, 1);

        for (int i = 0; i < n; i++) {
            hash[i + 1] = (hash[i] * BASE + (s[i] - 'a' + 1)) % MOD;
            pow_base[i + 1] = (pow_base[i] * BASE) % MOD;
        }
    }

    long long get_hash(int l, int r) {
        long long result = hash[r + 1] - (hash[l] * pow_base[r - l + 1]) % MOD;
        return (result % MOD + MOD) % MOD;
    }
};
```

**Time Complexity:**

- Preprocessing: O(n)
- Query: O(1)

---

## Bit Manipulation

### 1. Basic Operations

```cpp
// Check if i-th bit is set
bool is_set = (n >> i) & 1;
bool is_set = n & (1 << i);

// Set i-th bit
n |= (1 << i);

// Clear i-th bit
n &= ~(1 << i);

// Toggle i-th bit
n ^= (1 << i);

// Clear lowest set bit
n &= (n - 1);

// Get lowest set bit
int lowest = n & (-n);

// Count set bits
int count = __builtin_popcount(n);      // for int
int count = __builtin_popcountll(n);    // for long long

// Count trailing zeros
int zeros = __builtin_ctz(n);           // for int
int zeros = __builtin_ctzll(n);         // for long long

// Count leading zeros
int zeros = __builtin_clz(n);           // for int
int zeros = __builtin_clzll(n);         // for long long
```

### 2. Subset Generation

```cpp
// Generate all subsets
void generate_subsets(vector<int>& arr) {
    int n = arr.size();
    for (int mask = 0; mask < (1 << n); mask++) {
        vector<int> subset;
        for (int i = 0; i < n; i++) {
            if (mask & (1 << i)) {
                subset.push_back(arr[i]);
            }
        }
        // Process subset
    }
}

// Iterate through all subsets of a mask
void iterate_subsets(int mask) {
    for (int submask = mask; submask > 0; submask = (submask - 1) & mask) {
        // Process submask
    }
}
```

---

## Mathematical Functions

### 1. Built-in Math Functions

```cpp
#include <cmath>

// Power and roots
pow(base, exp)                  // O(log exp) if exp is integer
sqrt(x)                         // O(1)
cbrt(x)                         // cube root - O(1)

// Logarithms
log(x)                          // natural log - O(1)
log10(x)                        // base 10 log - O(1)
log2(x)                         // base 2 log - O(1)

// Trigonometric
sin(x), cos(x), tan(x)          // O(1)
asin(x), acos(x), atan(x)       // O(1)

// Rounding
floor(x), ceil(x)               // O(1)
round(x)                        // O(1)
trunc(x)                        // O(1)

// Absolute value
abs(x)                          // for integers
fabs(x)                         // for floating point

// Min/Max
min(a, b), max(a, b)            // O(1)
min({a, b, c, d})               // O(n)
max({a, b, c, d})               // O(n)
```

### 2. Combinatorics

```cpp
// Factorial
long long factorial(int n) {
    long long result = 1;
    for (int i = 2; i <= n; i++) {
        result *= i;
    }
    return result;
}

// Combination nCr
long long combination(int n, int r) {
    if (r > n - r) r = n - r;  // Take advantage of symmetry
    long long result = 1;
    for (int i = 0; i < r; i++) {
        result *= (n - i);
        result /= (i + 1);
    }
    return result;
}

// Pascal's triangle for combinations
vector<vector<int>> pascal_triangle(int n) {
    vector<vector<int>> triangle(n + 1);
    for (int i = 0; i <= n; i++) {
        triangle[i].resize(i + 1, 1);
        for (int j = 1; j < i; j++) {
            triangle[i][j] = triangle[i-1][j-1] + triangle[i-1][j];
        }
    }
    return triangle;
}

// Modular combination
class ModularCombinatorics {
    const int MOD = 1e9 + 7;
    vector<long long> fact, inv_fact;

    long long mod_pow(long long base, long long exp, long long mod) {
        long long result = 1;
        while (exp > 0) {
            if (exp % 2 == 1) result = (result * base) % mod;
            base = (base * base) % mod;
            exp /= 2;
        }
        return result;
    }

public:
    ModularCombinatorics(int n) {
        fact.resize(n + 1);
        inv_fact.resize(n + 1);

        fact[0] = 1;
        for (int i = 1; i <= n; i++) {
            fact[i] = (fact[i-1] * i) % MOD;
        }

        inv_fact[n] = mod_pow(fact[n], MOD - 2, MOD);
        for (int i = n - 1; i >= 0; i--) {
            inv_fact[i] = (inv_fact[i + 1] * (i + 1)) % MOD;
        }
    }

    long long nCr(int n, int r) {
        if (r > n || r < 0) return 0;
        return (fact[n] * inv_fact[r] % MOD) * inv_fact[n - r] % MOD;
    }
};
```

---

## Advanced STL Features

### 1. Custom Comparators

```cpp
// For sorting
sort(v.begin(), v.end(), [](const auto& a, const auto& b) {
    return a.first > b.first;  // Sort by first element descending
});

// For priority queue
auto cmp = [](const auto& a, const auto& b) {
    return a.first > b.first;  // Min heap based on first element
};
priority_queue<pair<int,int>, vector<pair<int,int>>, decltype(cmp)> pq(cmp);

// For set/map
auto cmp = [](const auto& a, const auto& b) {
    return a < b;
};
set<int, decltype(cmp)> s(cmp);
```

### 2. Lambda Functions

```cpp
// Basic lambda
auto add = [](int a, int b) { return a + b; };

// Capture by value
int x = 10;
auto func = [x](int y) { return x + y; };

// Capture by reference
auto func = [&x](int y) { x += y; return x; };

// Capture all by value/reference
auto func = [=](int y) { return x + y; };  // capture all by value
auto func = [&](int y) { x += y; return x; };  // capture all by reference

// Mutable lambda
auto func = [x](int y) mutable { x += y; return x; };
```

### 3. Function Objects and Functors

```cpp
#include <functional>

// Standard function objects
plus<int>(), minus<int>(), multiplies<int>(), divides<int>()
greater<int>(), less<int>(), greater_equal<int>(), less_equal<int>()
logical_and<bool>(), logical_or<bool>(), logical_not<bool>()

// Using with algorithms
transform(v.begin(), v.end(), v.begin(), [](int x) { return x * 2; });

// Binding
auto add5 = bind(plus<int>(), placeholders::_1, 5);
int result = add5(10);  // result = 15
```

---

## Memory Management & Performance Tips

### 1. Memory Optimization

```cpp
// Reserve memory for vector to avoid reallocations
vector<int> v;
v.reserve(1000000);  // Reserve space for 1M elements

// Use emplace instead of push for better performance
vector<pair<int, string>> v;
v.emplace_back(1, "hello");  // Better than v.push_back(make_pair(1, "hello"))

// Shrink to fit to reduce memory usage
vector<int> v(1000000);
v.resize(100);
v.shrink_to_fit();  // Reduce capacity to match size
```

### 2. Fast I/O

```cpp
// Disable synchronization with C I/O
ios_base::sync_with_stdio(false);

// Untie cin from cout
cin.tie(NULL);
cout.tie(NULL);

// Use '\n' instead of endl for better performance
cout << "Hello\n";  // Better than cout << "Hello" << endl;
```

### 3. Compiler Optimizations

```cpp
// Pragma for loop optimization
#pragma GCC optimize("O3")
#pragma GCC target("avx2")

// Inline functions for small frequently called functions
inline int add(int a, int b) {
    return a + b;
}

// Use register keyword for frequently used variables (rarely needed)
register int i;
```

---

## Contest-Specific Tips

### 1. Template Structure

```cpp
#include <bits/stdc++.h>
using namespace std;

typedef long long ll;
typedef pair<int, int> pii;
typedef vector<int> vi;
typedef vector<ll> vll;

#define pb push_back
#define mp make_pair
#define fi first
#define se second
#define sz(x) ((int)(x).size())
#define all(x) (x).begin(), (x).end()
#define rep(i, a, b) for (int i = (a); i < (b); i++)
#define per(i, a, b) for (int i = (b) - 1; i >= (a); i--)

const int MOD = 1e9 + 7;
const int INF = 1e9;
const ll LINF = 1e18;

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    // Your code here

    return 0;
}
```

### 2. Debugging Macros

```cpp
#ifdef LOCAL
#define debug(x) cerr << #x << " = " << x << endl
#define debug2(x, y) cerr << #x << " = " << x << ", " << #y << " = " << y << endl
#else
#define debug(x)
#define debug2(x, y)
#endif

// Usage
debug(variable);
debug2(a, b);
```

### 3. Common Edge Cases

```cpp
// Always check:
// - Empty input (n = 0, empty string)
// - Single element (n = 1)
// - All elements same
// - Negative numbers
// - Integer overflow
// - Array bounds
// - Division by zero
// - Invalid input format

// Use long long when needed
ll result = (ll)a * b;  // Prevent overflow

// Check for integer overflow
if (a > LLONG_MAX / b) {
    // Overflow will occur
}
```

### 4. Time Complexity Guidelines

- **n ≤ 10**: O(n!), O(n^6)
- **n ≤ 20**: O(2^n), O(n^5)
- **n ≤ 50**: O(n^4)
- **n ≤ 200**: O(n^3)
- **n ≤ 1000**: O(n^2)
- **n ≤ 100,000**: O(n log n)
- **n ≤ 1,000,000**: O(n)
- **n ≤ 10^9**: O(log n), O(sqrt(n))
