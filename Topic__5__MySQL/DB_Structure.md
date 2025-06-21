# 🧱 **Main Components of a Database System (DBMS)**

![DBMS_Components](https://d14qv6cm1t62pm.cloudfront.net/ccbp-website/Blogs/home/structure-of-dbms-image-1.png)

## 1. **Query Processor**

* **Role:** Translates and executes user queries (SQL).
* **Sub-components:**

  * **Parser:** Checks SQL syntax and builds internal structure (parse tree).
  * **Query Optimizer:** Chooses the most efficient execution plan (uses statistics and indexes).
  * **Query Executor:** Runs the query plan using the storage engine.

✅ **Think of it like a translator and planner.**

\
\
\
\
\
\
\
\


## 2. **Storage Manager**

* **Role:** Handles how data is stored, retrieved, and updated on disk.
* **Sub-components:**

  * **Buffer Manager:** Manages memory pages (caching, LRU).
  * **File Manager:** Manages space allocation and file I/O.
  * **Index Manager:** Handles B+ Trees, Hash Indexes, etc.
  * **Access Methods:** Scans, searches, and modifies records.

✅ **Think of it like the file system of the database.**

\
\
\
\
\
\
\
\


## 3. **Transaction Manager**

* **Role:** Ensures **ACID** properties (Atomicity, Consistency, Isolation, Durability).
* **Responsibilities:**

  * Concurrency control (locks, MVCC)
  * Deadlock detection
  * Transaction isolation (read committed, repeatable read, etc.)

✅ **Think of it like a supervisor for simultaneous users.**

\
\
\
\
\
\
\
\


## 4. **Recovery Manager**

* **Role:** Ensures data durability and crash recovery.
* **Mechanisms:**

  * **Undo Logs:** Roll back uncommitted changes.
  * **Redo Logs (WAL):** Reapply committed changes after crash.
  * Checkpointing

✅ **Think of it as the emergency backup system.**

\
\
\
\
\
\
\
\


## 5. **Catalog Manager (Data Dictionary)**

* **Role:** Stores metadata about the database schema.
* Stores:

  * Tables, columns, data types
  * Indexes, constraints, users, privileges

✅ **Think of it like the system’s address book and registry.**

\
\
\
\
\
\
\
\


## 6. **User Interface Layer (Front-End APIs)**

* **SQL Interface / API Layer:**

  * Accepts queries from applications, users, GUIs
  * Converts them into internal representations

✅ **Acts as the entry point for users and applications.**

## 🎓 **Simplified Diagram**

```
           +--------------------------+
           |    SQL Interface / API   |
           +------------+-------------+
                        |
           +------------v-------------+
           |      Query Processor     |
           +------------+-------------+
                        |
     +------------------+------------------+
     |     Transaction Manager             |
     |     Recovery Manager                |
     +------------------+------------------+
                        |
               +--------v--------+
               | Storage Manager |
               +--------+--------+
                        |
                +-------v-------+
                |  File System  |
                +---------------+
```
