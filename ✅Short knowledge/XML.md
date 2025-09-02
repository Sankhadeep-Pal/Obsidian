# XML

**XML (eXtensible Markup Language)** is a markup language used to store and transport data. It's both **human-readable** and **machine-readable**, designed to be **self-descriptive** — meaning the structure and the data are both encoded in a way that explains their meaning.

### ✅ Key Features:

- **Structured Data Format**: Similar to HTML but used for data, not presentation.

- **Custom Tags**: You define your own tags based on the needs of your application (e.g., `<student><name>John</name></student>`).

- **Hierarchical Structure**: Data is nested, making it ideal for representing tree structures.

- **Text-Based**: Plain text format makes it easy to parse and transmit over networks.

### ✒️ Example:

```xml
<book>
  <title>Clean Code</title>
  <author>Robert C. Martin</author>
  <year>2008</year>
</book>
```

### ☑️ Use Cases:

- Web services (SOAP)

- Configuration files

- Data exchange between systems (especially legacy systems)

- Document formats (e.g., Microsoft Office uses XML-based formats)

### 🟢 Strengths:

- Platform-independent

- Widely supported

- Can be validated with DTD or XML Schema

### 🔴 Weaknesses:

- Verbose (lots of tags = large files)

- Slower to parse compared to JSON

- Largely replaced by **JSON** in modern APIs (lighter and easier to work with)

### 🔥 Bottom Line:

**XML is like the granddaddy of structured data formats.** Still important for enterprise systems, but if you're building modern web or mobile apps, you'll mostly deal with JSON unless you're integrating with older services. Learn XML to understand the ecosystem — then move fast into JSON, REST, and GraphQL.

---
