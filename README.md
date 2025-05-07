# WordPress Plugin Vulnerability Scanner 🔍🔐

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Bun Version](https://img.shields.io/badge/Bun-≥1.2.13-yellow.svg)](https://bun.sh/)
[![Status](https://img.shields.io/badge/Project-Active-brightgreen.svg)](#)

> A powerful scanner to detect vulnerable WordPress plugins by parsing HTML and checking against public vulnerability databases (CVEs & WPScan).

---

## ✨ Features

- **Auto-detects installed WordPress plugins**
- **Extracts plugin versions** from HTML `<script>`/`<link>` tags and readme files
- **Cross-references vulnerabilities** using public databases (CVE/WPScan)
- **Displays detailed reports** with severity scores and vulnerability descriptions
- **Clean, responsive web interface** built with Tailwind CSS

---

## 🖼️ Screenshots

<p align="center">
  <img src="https://camo.githubusercontent.com/9f40e8d7f54b65b9d96feeb7a3787e4dc3a9f442cc27932f3fc238bcd1c93e17/68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f48697574616b792f77702d7365632f6d61696e2f7075626c69632f73637265656e2d312e706e67" alt="Main View" width="600"/>
  <br/>
  <em>Main Interface</em>
</p>

<p align="center">
  <img src="https://camo.githubusercontent.com/6db030dc7dc51175a093b33dc1fc2eddb58aa4524ceaf24c8a88234cb8c6a33d/68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f48697574616b792f77702d7365632f6d61696e2f7075626c69632f73637265656e2d322e706e67" alt="Vulnerability Dialog" width="600"/>
  <br/>
  <em>Vulnerability Details Dialog</em>
</p>

---

## ⚙️ Getting Started

### ✅ Prerequisites

- [Bun Runtime](https://bun.sh/) ≥ v1.2.13 (Canary recommended)

### 🚀 Installation


# 1. Clone the repository
git clone https://github.com/Hiutaky/wp-sec.git
cd wp-sec

# 2. Install backend dependencies
bun install

# 3. Install frontend dependencies
cd frontend
bun install
cd ..

# 4. Run the development server
bun run dev


Open http://localhost:3000 in your browser to use the app.

⸻

🧪 Usage
	1.	Enter a WordPress site URL in the input field.
	2.	Click “Scan” to start analyzing the site.
	3.	View the plugin list and see any known vulnerabilities.

⸻

🧠 Technical Overview
	•	Backend: Elysia.js (high-performance TypeScript framework)
	•	Frontend: React + Tailwind CSS
	•	Core Scanner Module: Parses HTML, extracts plugin names/versions, checks against CVE/WPScan

⸻

 📡 API

 POST /scan

 Request Body:

{
  "url": "https://example.com"
}

Response:

{
  "plugins": [
    {
      "name": "elementor",
      "version": "3.10.2",
      "vulnerabilities": [
        {
          "title": "Authenticated Remote Code Execution",
          "severity": "Critical",
          "cvss": 9.8,
          "cve_id": "CVE-2024-XXXX",
          "description": "..."
        }
      ]
    }
  ]
}


⸻

📄 License

This project is licensed under the MIT License.

⸻

🙌 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

⸻

✉️ Contact

Created by Hiutaky – feel free to reach out for feedback or collaboration!