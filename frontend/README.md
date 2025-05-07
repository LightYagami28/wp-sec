# React + TypeScript + Vite ⚡️🧪

[![Vite](https://img.shields.io/badge/Vite-5.0+-blueviolet?style=flat-square&logo=vite)](https://vitejs.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18+-61dafb?style=flat-square&logo=react)](https://reactjs.org/)
[![License](https://img.shields.io/github/license/Hiutaky/react-ts-vite-template?style=flat-square)](LICENSE)

> Minimal yet flexible boilerplate to kickstart your React + TypeScript project with Vite, HMR, and modern linting.

---

## 🚀 Features

- ⚛️ React 18+ with TypeScript 5+
- ⚡️ Powered by [Vite](https://vitejs.dev) for lightning-fast builds
- ♻️ HMR (Hot Module Replacement) out of the box
- ✅ ESLint and Prettier configured
- 🔍 Recommended plugins and advanced type-aware linting

---

## 🔌 Plugin Options

You can choose between two official Vite React plugins:

- [`@vitejs/plugin-react`](https://github.com/vitejs/vite-plugin-react) — uses **Babel** for Fast Refresh
- [`@vitejs/plugin-react-swc`](https://github.com/vitejs/vite-plugin-react/tree/main/packages/plugin-react-swc) — uses **SWC** for better performance

---

## ✅ Advanced ESLint Setup

To enable stricter, type-aware linting for production:

```js
export default tseslint.config({
  extends: [
    // Recommended with type checking
    ...tseslint.configs.recommendedTypeChecked,
    
    // For stricter code rules
    ...tseslint.configs.strictTypeChecked,

    // Optional: stylistic rules
    ...tseslint.configs.stylisticTypeChecked,
  ],
  languageOptions: {
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

---

## 🧩 Recommended React ESLint Plugins

You can enhance React linting with:

- [`eslint-plugin-react-x`](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x)
- [`eslint-plugin-react-dom`](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom)

Example configuration:

```js
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
```

---

## 📦 Getting Started

```bash
npm create vite@latest my-app -- --template react-ts
cd my-app
npm install
npm run dev
```

---

## 📄 License

Licensed under the [MIT License](LICENSE)

---

## 🛠️ Maintained by [Hiutaky](https://github.com/Hiutaky)