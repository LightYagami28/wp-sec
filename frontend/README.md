# ⚛️ React + TypeScript + Vite ⚡

A minimal yet powerful starter template to kick off your **React** projects using **TypeScript** and **Vite**, with built-in **Hot Module Replacement** and **ESLint** integration.

---

## 🚀 Features

- **Lightning-fast** development with [Vite](https://vitejs.dev)
- Modern React setup with JSX and TypeScript
- Hot Module Replacement (HMR) for an optimized dev workflow
- Linting powered by ESLint and extendable configurations
- Easily customizable for production use

---

## 🔌 Supported React Plugins

Choose the rendering engine that fits your needs:

- [`@vitejs/plugin-react`](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) – powered by [Babel](https://babeljs.io/) ⚡  
- [`@vitejs/plugin-react-swc`](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) – powered by [SWC](https://swc.rs/) ⚡

---

## 🛠️ Expanding ESLint Configuration

For production-grade projects, we recommend enabling **type-aware** lint rules:

```js
export default tseslint.config({
  extends: [
    ...tseslint.configs.recommendedTypeChecked, // Balanced rules
    ...tseslint.configs.strictTypeChecked,      // Stricter codebase
    ...tseslint.configs.stylisticTypeChecked,   // Optional styling rules
  ],
  languageOptions: {
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})


⸻

🔍 Recommended ESLint Plugins for React

Improve your code quality and safety with:
	•	eslint-plugin-react-x
	•	eslint-plugin-react-dom

Plugin Integration Example:

// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config({
  plugins: {
    'react-x': reactX,
    'react-dom': reactDom,
  },
  rules: {
    ...reactX.configs['recommended-typescript'].rules,
    ...reactDom.configs.recommended.rules,
  },
})


⸻

📦 Quick Start

npm create vite@latest my-app -- --template react-ts
cd my-app
npm install
npm run dev

Then open http://localhost:5173 in your browser!

⸻

📁 Project Structure

├── src/
│   ├── App.tsx
│   ├── main.tsx
├── public/
├── index.html
├── tsconfig.json
├── vite.config.ts


⸻

❤️ Contributing

Pull requests, issues and ideas are welcome!

⸻

📝 License

MIT — feel free to use, modify and share.

⸻

Happy coding! ✨