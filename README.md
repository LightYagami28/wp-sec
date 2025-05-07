# WordPress Plugin Vulnerability Scanner 🔍🔐

[![License](https://img.shields.io/github/license/Hiutaky/wp-sec?style=flat-square)](LICENSE)
[![Bun](https://img.shields.io/badge/Bun-%3E%3D1.2.13-yellow?style=flat-square&logo=bun)](https://bun.sh)
[![Status](https://img.shields.io/badge/status-active-brightgreen?style=flat-square)](#)

> A powerful tool to detect vulnerable WordPress plugins by parsing HTML and checking against public vulnerability databases.

---

## ✨ Features

- Detects installed WordPress plugins from public HTML
- Extracts plugin versions from `<script>`, `<link>` tags and readme files
- Cross-checks with known CVEs and WPScan data
- Displays vulnerability severity (CVSS) and descriptions
- Fast, responsive UI built with Tailwind CSS

---

## 🖼️ Screenshots

### Main Interface

![Main View](/public/screen-1.png)

### Vulnerability Details

![Vulnerabilities Dialog](/public/screen-2.png)

---

## ⚙️ Getting Started

### ✅ Prerequisites

- [Bun](https://bun.sh) ≥ **v1.2.13** (Canary recommended)

### 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/Hiutaky/wp-sec.git
cd wp-sec

# Install backend dependencies
bun install

# Install frontend dependencies
cd frontend
bun install
cd ..

# Run the development server
bun run dev
```

Then open your browser at [http://localhost:3000](http://localhost:3000)

---

## 🧪 Usage

1. Enter the target WordPress site URL.
2. Click **Scan** to initiate the scan.
3. View detected plugins and their vulnerabilities.

---

## 🧠 Technical Overview

- **Backend:** [Elysia.js](https://elysiajs.com) – lightweight & high-performance
- **Frontend:** React + Tailwind CSS
- **Scanner Engine:** HTML parser + version extractor + CVE/WPScan integration

---

## 📡 API

### `POST /scan`

**Request Body:**

```json
{
  "url": "https://example.com"
}
```

**Response Example:**

```json
{
  "plugins": [
    {
      "name": "elementor",
      "version": "3.10.2",
      "vulnerabilities": [
        {
          "title": "Authenticated RCE",
          "severity": "Critical",
          "cvss": 9.8,
          "cve_id": "CVE-2024-XXXX",
          "description": "..."
        }
      ]
    }
  ]
}
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## ✉️ Contact

Created by [Hiutaky](https://github.com/Hiutaky) – feedback and collaboration welcome!
