# 🧩 **Types of SQL (Structured Query Language)**

SQL commands are grouped into **five main categories** based on their purpose:

\
\
\
\
\
\
\
\
\
\
\
\

## 🟢 **1. DDL – Data Definition Language**

> Used to define and modify the structure of database objects (tables, schemas, etc.).

**Common DDL Commands:**

| Command    | Purpose                                             |
| ---------- | --------------------------------------------------- |
| `CREATE`   | Create a new table or object                        |
| `ALTER`    | Modify structure of an existing object              |
| `DROP`     | Delete an object (e.g., table)                      |
| `TRUNCATE` | Delete all rows from a table (faster than `DELETE`) |

✅ *Affects schema structure.*

\
\
\
\
\
\
\
\
\


## 🔵 **2. DML – Data Manipulation Language**

> Used to manage and modify data within tables.

**Common DML Commands:**

| Command  | Purpose                    |
| -------- | -------------------------- |
| `SELECT` | Retrieve data from a table |
| `INSERT` | Add new rows               |
| `UPDATE` | Modify existing rows       |
| `DELETE` | Remove rows                |

✅ *Affects the data, not the structure.*

\
\
\
\
\
\
\
\
\


## 🟡 **3. DCL – Data Control Language**

> Deals with **permissions** and **access control**.

**Common DCL Commands:**

| Command  | Purpose                  |
| -------- | ------------------------ |
| `GRANT`  | Give privileges to users |
| `REVOKE` | Take back privileges     |

✅ *Used by DBAs for security.*

\
\
\
\
\
\
\
\
\


## 🟠 **4. TCL – Transaction Control Language**

> Manages transactions and their behavior (commit, rollback, etc.).

**Common TCL Commands:**

| Command           | Purpose                             |
| ----------------- | ----------------------------------- |
| `COMMIT`          | Save changes made by a transaction  |
| `ROLLBACK`        | Undo changes since the last commit  |
| `SAVEPOINT`       | Create intermediate rollback points |
| `SET TRANSACTION` | Define properties of a transaction  |

✅ *Ensures ACID compliance.*

\
\
\
\
\
\
\
\
\


## 🔴 **5. DQL – Data Query Language**

> Sometimes considered a subset of DML, focusing **only on retrieving data**.

**Command:**

* `SELECT` – Retrieves data

✅ *Read-only command, essential for reporting and analysis.*


\
\
\
\
\
\
\
\
\



#  **Quick Summary Table**

| Type | Name                       | Example Commands             | Purpose             |
| ---- | -------------------------- | ---------------------------- | ------------------- |
| DDL  | Data Definition Language   | `CREATE`, `ALTER`, `DROP`    | Define structure    |
| DML  | Data Manipulation Language | `SELECT`, `INSERT`, `UPDATE` | Manage data         |
| DCL  | Data Control Language      | `GRANT`, `REVOKE`            | Control access      |
| TCL  | Transaction Control        | `COMMIT`, `ROLLBACK`         | Manage transactions |
| DQL  | Data Query Language        | `SELECT`                     | Query data          |
