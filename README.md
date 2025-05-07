# WordPress Plugin Vulnerability Scanner

A tool to scan WordPress sites for vulnerable plugins by analyzing HTML source code and checking against known vulnerability databases.

## Features

- Scans WordPress sites to detect installed plugins
- Identifies plugin versions from script/link tags and readme files
- Checks detected plugins against vulnerability databases
- Provides detailed vulnerability information including severity scores
- Simple and intuitive web interface

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) runtime environment min version 1.2.13 ( canary )

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/Hiutaky/wp-sec.git
   cd wp-sec
   ```

2. Install server dependencies

   ```bash
   bun install
   ```
3. Install frontend dependencies
   ```bash
   cd frontend && bun install && cd ..
   ```
3. Run the application
   ```bash
   bun run dev
   ```

4. Open your browser and navigate to `http://localhost:3000`

## Usage

1. Enter the URL of a WordPress site in the input field
2. Click "Scan" to analyze the site
3. View the results showing detected plugins and any vulnerabilities

## Technical Details

The application consists of:

- Backend API built with Elysia.js
- Frontend interface using React with Tailwind CSS
- Scanner module that extracts plugin information and checks for vulnerabilities

## API Endpoints

- `POST /scan` - Accepts a WordPress site URL and returns scan results

## License

[MIT](LICENSE)
