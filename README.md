# wp-sec

To install dependencies:

```bash
bun install
```

To run (CLI):

```bash
bun run index.ts
```

This project was created using `bun init` in bun v1.2.6. [Bun](https://bun.sh) is a fast all-in-one JavaScript runtime.

## Backend Server

To start the API server:

```bash
bun run server.ts
```

The server runs on port 3000 and provides the following endpoint:

- GET /api/scan?siteUrl=<URL>  Returns JSON with plugins and vulnerabilities.

## Frontend

The React frontend is located in the `frontend` directory.

1. Change to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   bun install
   ```

3. Start the development server:
   ```bash
   bun dev
   ```

Open http://localhost:5173 in your browser to access the UI.
