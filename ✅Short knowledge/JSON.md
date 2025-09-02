# JSON

**JSON** (JavaScript Object Notation) is a **lightweight data-interchange format** that's easy for humans to read and write, and easy for machines to parse and generate.

### 🔧 Core Purpose:

Used to **structure and transmit data** between a server and a client (commonly in web APIs).

### 📌 Basic Structure:

- Based on two structures:
    
    1. **Objects** (key-value pairs) → like Python dictionaries
    
    2. **Arrays** (ordered lists) → like Python lists

### 🧱 Example:

```json
{
	"name": "Sankho",
	"age": 20,
	"isStudent": true,
	"skills": ["Python", "JavaScript", "C++"],
	"profile": {
    	"goal": "Super Software Engineer",
    	"trait": "Hardworking"
	}
}
```

### ✅ Key Features:

- Language-independent (not just for JavaScript)

- Common in REST APIs and web development

- Supported by nearly all programming languages (Python: `json` module, JS: `JSON.parse()`, `JSON.stringify()`)

### 💡 Use Cases:

- API responses (e.g., from a backend to frontend)

- Configuration files (`package.json`, `tsconfig.json`, etc.)

- Storing structured data (e.g., in NoSQL databases like MongoDB)

---
