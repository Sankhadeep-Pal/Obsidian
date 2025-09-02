# API

An **API (Application Programming Interface)** is a set of rules and tools that allows different software applications to communicate with each other.

### Think of it like:

* A **menu in a restaurant**: The menu lists what you can order (functions), and when you place an order, the kitchen (the system behind the scenes) prepares it and gives you the result.

* You don’t need to know how the kitchen works — just what you can request and what you’ll get in return.

### Key Concepts:

* **Endpoints**: URLs that expose specific data or functionality.

* **Request**: You (the client) send a request to the API (like asking for data).

* **Response**: The API sends data back (usually in JSON or XML format).

* **HTTP Methods**:
	
	-  `GET`: Retrieve data
	
	-  `POST`: Send new data
	
	-  `PUT`: Update existing data
	
	-  `DELETE`: Remove data

### Example:

You want to show weather info in your app:

* Use a weather API (like OpenWeatherMap).

* You send a GET request to:
  `https://api.weather.com/current?city=Tokyo`

* API returns:

  ```json
  {
    "city": "Tokyo",
    "temperature": 28,
    "condition": "Clear"
  }
  ```

### Why APIs Matter:

* **Modularity**: Build apps by connecting to other services (payment, maps, chat, etc.).

* **Automation**: Enable systems to talk to each other without human input.

* **Innovation**: APIs are the backbone of mobile apps, web services, AI integration, etc.

> An **API is a contract** between two software systems: one asks, the other delivers — all without knowing each other's internal code.

---

