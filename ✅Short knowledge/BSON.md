# [BSON](https://www.mongodb.com/resources/basics/json-and-bson)

## What is BSON?
**BSON (Binary JSON)** is a **binary-encoded serialization format** used to store and transmit data. It was designed to extend JSON (JavaScript Object Notation) but with improvements that make it more efficient for storage, transport, and query execution in databases — most notably **MongoDB**, where it’s the underlying data format.

## Core Idea
JSON is great for human readability but inefficient for machines:

- It’s text-based, so parsing is slower.

- It lacks support for certain data types (e.g., binary data, date types).

- Storing large datasets in plain JSON leads to unnecessary overhead.

BSON solves this by being **binary, fast to parse, and supporting more types.**

## Key Features of BSON

1. **Binary Representation**
    
    - Unlike JSON (plain text), BSON uses binary encoding.
    
    - Makes reading/writing faster for machines.

2. **Rich Data Types**  
    BSON supports all JSON types **plus extras** like:
    
    - **Date** (proper datetime type, not just string)
    
    - **32-bit & 64-bit integers**
    
    - **Floating-point numbers**
    
    - **Decimal128** (high precision decimal for financial data)
    
    - **ObjectId** (unique IDs used in MongoDB)
    
    - **Binary data** (e.g., images, files)
    
    - **Regular expressions**
    
    JSON would have to fake these as strings.

2. **Efficient Traversal**
    
    - BSON is designed so the database can skip through fields quickly without parsing everything.
    
    - This speeds up queries and indexing in databases like MongoDB.

3. **Lightweight but Not Always Small**
    
    - BSON is faster but not necessarily smaller.
    
    - For example, a simple integer in JSON might be `"5"` (1 char + quotes = 3 bytes), while in BSON it’s 8 bytes (for int64).
    
    - BSON trades storage size for **speed and type richness**.


## Structure of BSON

Every BSON document is made up of:

- **Field name** (as a string, null-terminated)

- **Type identifier** (1 byte, tells what kind of value it is)

- **Value** (binary encoded, depending on type)

**Example:**  
JSON:

```json
{
  "name": "Sankho",
  "age": 21,
  "isStudent": true
}
```

BSON internally:

```
\x16\x00\x00\x00          // total document size
\x02 name \x00 Sankho\x00 // type=string, field="name"
\x10 age \x00 15\x00\x00\x00  // type=int32, field="age"
\x08 isStudent \x00 \x01  // type=boolean, field="isStudent"
\x00                      // end of object
```

## Advantages of BSON

- **Machine efficiency:** Faster parsing and traversal than JSON.

- **Rich data types:** Handles real-world data better (dates, binary, decimals).

- **Query performance:** Databases like MongoDB can index and retrieve fields directly.

- **Cross-language support:** BSON libraries exist for many programming languages.

## Disadvantages of BSON

- **Larger storage size** compared to plain JSON for simple data.

- **Not human-readable** (binary format).

- **Tied to MongoDB ecosystem:** While libraries exist elsewhere, its popularity is mostly because of MongoDB.

## Real-World Usage

- **MongoDB** → stores and transfers all documents in BSON format internally, but when you query, you usually see JSON.

- **GridFS** → stores large files (like images or videos) in MongoDB using BSON chunks.

- **Data transfer** → can be used wherever a binary format is needed, but mostly tied to databases.

---

✅ **In short:** BSON is “JSON for machines” — binary, faster, richer in data types, and built for efficient database operations.

---

