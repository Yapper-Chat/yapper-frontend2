# 💬 Chat System Frontend (React + Tailwind)

This is the frontend of the real-time chat system, built with ReactJS and Tailwind CSS.
It provides the user interface for authentication, messaging, and real-time updates, while communicating with the Laravel backend API.

## 🚀 Features
🔐 User authentication (login/register/logout)
💬 One-to-one messaging between users
⚡ Real-time updates with Laravel Echo + Pusher / WebSockets
🎨 Responsive UI with TailwindCSS
🔄 API integration with Laravel backend

## 🛠️ Tech Stack
Frontend Framework: React 18
Styling: TailwindCSS
State Management: React Context / Redux (your choice)
Real-time: Laravel Echo + PusherJS
Backend API: Laravel + MySQL (see backend repo)

## ⚙️ Setup Instructions
1. Clone the repo
git clone https://github.com/yourusername/chat-frontend.git
cd chat-frontend

2. Install dependencies
npm install

3. Configure environment

Create a .env file in the root with:

REACT_APP_API_URL=http://localhost:8000/api
REACT_APP_PUSHER_KEY=your-pusher-key
REACT_APP_PUSHER_CLUSTER=mt1

4. Start the dev server
npm run dev

## React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
