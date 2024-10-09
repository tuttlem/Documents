# UniVerse Database Engineer

## Files and Design

### What are some of the different file types?

| File type | Type         | Description                                                                 |
|-----------|--------------|-----------------------------------------------------------------------------|
| 1 & 19    | directory     | Represents directories.                                                     |
| 2         | static        | Keys end with numbers.                                                      |
| 3         | static        | Keys end mainly with numbers.                                               |
| 4         | static        | Keys end with letters.                                                      |
| 5         | static        | Keys end with a full range of ASCII characters.                             |
| 6         | static        | Keys begin with numbers.                                                    |
| 7         | static        | Keys begin mainly with numbers.                                             |
| 8         | static        | Keys begin with letters.                                                    |
| 9         | static        | Keys begin with a full range of ASCII characters.                           |
| 10        | static        | Keys are numbers.                                                           |
| 11        | static        | Keys are mainly numbers.                                                    |
| 12        | static        | Keys are letters.                                                           |
| 13        | static        | Keys are the full range of ASCII characters.                                |
| 14        | static        | Entire keys are numbers.                                                    |
| 15        | static        | Entire keys are mainly numbers.                                             |
| 16        | static        | Entire keys are letters.                                                    |
| 17        | static        | Entire keys are the full range of ASCII characters.                         |
| 18        | static        | Entire keys are of arbitrary form.                                          |
| 30        | dynamic       | A dynamic file type with modifiable characteristics based on usage patterns.|

### Why would you use a particular file type over another?
Discuss specific use cases where a static file is more efficient versus when a dynamic file is better suited, especially as it relates to data size, access patterns, and expected future growth.

### Explain the terms "modulo" and "separation"
- **Modulo** refers to the number of groups (or partitions) the file has, which affects how data is distributed and retrieved from disk. 
- **Separation** defines how many 512-byte disk frames are allocated to each group, affecting data storage efficiency and performance.

### What are some of the common fields of a dictionary record?

| Field           | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| Conversion      | Specifies a format for data representation. For example, `D DMY[2,A3,4]` would store `01` for `01 JAN 1968`. |
| Column Header   | Title that appears at the head of a report or query result column.           |
| Format          | Specifies how many characters are displayed and how they are aligned (e.g., `10R` for 10 characters, right-aligned). |
| Single or Multi | Defines whether the field holds a single value (S) or multiple values (M).  |

---

## Support

### Describe some of the ways that you'd relieve database processing pressure on poorly performing files?
* **Resize files**: Adjusting the modulo and separation settings to optimize the data distribution.
* **File splitting or sharding**: For very large files, consider splitting them to improve access time.
* **Reorganizing**: Perform file reorganizations to reduce fragmentation.
* **Indexing**: Consider adding indices for fields used frequently in queries.
* **Archiving**: Move historical or less-used data to secondary storage.

---

## General

### Describe the difference between named and unnamed common in UniVerse
- **Named Common**: A shared memory area where variables can be stored and accessed across different programs using explicit names.
- **Unnamed Common**: A memory area without named access, where variables are implicitly shared among programs in the same execution context.

### What is a recursive subroutine, and when might it be used?
- A recursive subroutine is a function or procedure that calls itself in order to solve a problem. It is typically used in situations such as navigating hierarchical structures (e.g., trees or file systems) or solving problems that can be broken down into smaller sub-problems (e.g., calculating factorials).
  
### What special considerations are needed when coding a recursive subroutine?
- **Base Case**: Always ensure there is a clear exit condition to avoid infinite recursion.
- **Stack Usage**: Recursion consumes stack memory for each call, so deep recursion may cause stack overflow if not handled properly.
- **Performance**: Evaluate whether recursion or iteration is the more efficient solution for the problem.

### Describe the concepts behind transaction processing and how UniVerse implements it
- **Transaction Processing**: Refers to the management of changes in the database in a way that ensures data integrity, especially during multiple operations. In UniVerse, transactions are controlled with **BEGIN TRANSACTION** and **COMMIT** or **ROLLBACK**, allowing for atomicity of operations and consistency in case of failures.
  
### Describe the pessimistic and optimistic approaches to database locking
- **Pessimistic Locking**: Locks data when read to prevent other users from modifying it until the lock is released. This reduces conflicts but can reduce concurrency.
- **Optimistic Locking**: Allows multiple users to read data without locking it but verifies at the time of update if the data has been changed. If it has, a conflict resolution is required.

### Describe the difference between SQL NULL and an empty string in UniVerse
- **SQL NULL**: Represents the absence of a value. It indicates "unknown" or "missing" data.
- **Empty String**: A valid value, meaning the string exists but contains no characters. It differs from NULL in that it explicitly means "nothing" rather than "unknown."

### Describe the hashed file concept used by the UniVerse database
- **Hashed Files**: UniVerse uses hashed files to store and retrieve data quickly. The hashing algorithm distributes data across various "groups" (buckets), which allows fast retrieval based on the key. Each group holds multiple records in a linked-list-like structure.
  
### Describe the Type 30 file concept used by the UniVerse database
- **Type 30 Files**: These are dynamic files that adjust their size and distribution characteristics based on the data being inserted or modified. They are designed for scalability and to handle large volumes of data without manual intervention.

### Why should file separations never be an odd number?
- Odd-numbered separations can cause misalignment between UniVerse’s group boundaries and the host system’s disk block boundaries, potentially degrading performance.

### What is the difference between Type 1 and Type 19 files in UniVerse?
- **Type 1**: Basic file type used in UniVerse. They are static and suited for small, unchanging datasets.
- **Type 19**: Directory-based files, typically used for system files and internal UniVerse data structures.

### What is the difference between a 32-bit and 64-bit file in UniVerse?
- **32-bit Files**: Have a maximum size limit of 2GB.
- **64-bit Files**: Can exceed the 2GB limit, supporting much larger datasets, which is increasingly important for modern applications with large amounts of data.

### Why does the UniVerse database support multiple "flavors"?
- To maintain compatibility with application software written for other variants of PICK-style databases, minimizing migration and upgrade challenges.

### How does the wide zero mechanism work in UniVerse?
- **Wide Zero**: When UniVerse compares two numbers, it uses the wide zero configuration to determine the tolerance for treating small differences between numbers as zero. If the difference is smaller than the configured threshold, the numbers are considered equal.

