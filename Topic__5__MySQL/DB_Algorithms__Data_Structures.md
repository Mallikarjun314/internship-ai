# 🔧 **Data Structures and Algorithms Used by MySQL**

## 🟩 **1. Storage Engines (Context Layer)**

MySQL supports multiple storage engines, primarily:

* **InnoDB** (default) – fully ACID-compliant
* **MyISAM** – legacy, read-heavy, no transactions

> We’ll focus mostly on **InnoDB**, as it’s used in production and exams.

---

# 🧱 **Core Data Structures in MySQL (Primarily InnoDB)**

## 🔹 1. **B+ Tree**

* Used for: **Primary and secondary indexes**
* Why B+ Tree?

  * Efficient range queries
  * Sorted structure
  * All values at leaf level = fast sequential access
* Applies to: Clustered (primary key) and non-clustered (secondary) indexes

## 🔹 2. **Hash Table**

* Used in:

  * **Adaptive Hash Index** (InnoDB)

    * Speeds up lookups by caching hot B+ Tree entries
  * **Join buffer** (for certain join operations)

## 🔹 3. **Double-Linked List**

* Used to manage:

  * **Buffer Pool pages** (for LRU eviction)
  * Tracks **recently used** and **dirty** pages

## 🔹 4. **Red-Black Tree / AVL Trees**

* Rare, but internal structures (e.g., temporary memory indexes) may use self-balancing binary trees.

## 🔹 5. **Bitmaps**

* Used in:

  * **Bitmap indexes** (in other engines, like MariaDB)
  * **Permissions, SET types**, and some optimizations in temporary tables

## 🔹 6. **Heaps / Priority Queues**

* Used in:

  * **ORDER BY / GROUP BY** operations in memory
  * Sorting large datasets with limited memory
