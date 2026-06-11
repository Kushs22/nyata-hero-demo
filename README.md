# Nyata API Hero Demo

A minimal HTML + JavaScript demo showing how to send a user message to the Nyata API and display the response using `fetch()`.

---

## Screenshot

![Working Demo](./screenshots/hero-demo-overview.png)

Expected output:

* User enters a message
* Request sent to Nyata API
* AI response displayed on page

---

## Prerequisites

Before running this demo you need:

* A Nyata API Key
* A modern web browser (Chrome, Safari, Edge, Firefox)
* Visual Studio Code
* Live Server extension (recommended)

---

## Project Structure

```text
nyata-hero-demo/
│
├── index.html
├── README.md
└── screenshots/
    └── hero-demo-overview.png
```

---

## Setup (3 Steps)

### Step 1 — Clone Repository

```bash
git clone https://github.com/Kushs22/nyata-hero-demo.git
cd nyata-hero-demo
```

---

### Step 2 — Add Your API Key

Open:

```text
index.html
```

Find:

```javascript
"X-API-Key":"YOUR_API_KEY"
```

Replace with:

```javascript
"X-API-Key":"nyata_xxxxxxxxx"
```

Save the file.

---

### Step 3 — Run Locally

Open `index.html` in VS Code.

Start Live Server:

```text
Right Click → Open with Live Server
```

Browser opens automatically:

```text
http://127.0.0.1:5500
```

Enter a message and press **Send**.

---

## Example Request

```javascript
const res = await fetch(
"https://ai.mottatracking.com/external_api.php",
{
method:"POST",
headers:{
"Content-Type":"application/json",
"X-API-Key":"YOUR_API_KEY"
},
body:JSON.stringify({
model:"ft:gpt-4.1-mini-2025-04-14:nyata:bristol:ChciyaQP",
messages:[
{
role:"user",
content:"Hello!"
}
]
})
}
)
```

---

## Example Response

```json
{
"id":"chatcmpl-xxx",
"choices":[
{
"message":{
"role":"assistant",
"content":"Hello!"
}
}
]
}
```

---

## API Documentation

Full Nyata API documentation:

https://nyataai.co.uk/playground.html

---

## Notes

* No frameworks used
* Under 100 lines of HTML/JS
* Built as a minimal integration example
* Intended to demonstrate how quickly a developer can adopt Nyata API

---

## Author

Kush Sharma
GitHub: https://github.com/Kushs22
