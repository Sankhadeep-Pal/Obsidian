# DOM

The **DOM** stands for **Document Object Model**.

### 📘 In Simple Terms:

The **DOM is a programming interface** for web documents. It represents the structure of a web page as a **tree of objects** that you can interact with using JavaScript.

### 🧱 Example:

Take this simple HTML:

```html
<html>
  <body>
    <h1>Hello</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

The **DOM** turns it into a tree-like structure like this:

```
Document
└── html
    └── body
        ├── h1
        └── p
```

Each HTML element becomes a **node** in the DOM tree.

### 🔧 Why the DOM is Useful:

It allows JavaScript to:

- Access elements (`getElementById`, `querySelector`, etc.)

- Change content (`element.innerHTML = "new text";`)

- Add/remove elements

- Change styles dynamically

- Respond to user events (clicks, typing, etc.)

### 🧠 Think of the DOM as:

> A **live, dynamic representation** of the page that JavaScript can read from and write to.
