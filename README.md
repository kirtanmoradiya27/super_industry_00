# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh



# Use the all command

npm create vite@latest
cd name_your
npm i
npm run dev

# Install the tailwindcss

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# tailwind.config.js

/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}


# index.css

@tailwind base;
@tailwind components;
@tailwind utilities;

# Mui

npm install @mui/material @emotion/react @emotion/styled
npm install @mui/material @mui/styled-engine-sc styled-components
npm install @mui/icons-material
npm install @mui/lab
npm install @mui/x-data-grid
npm install @mui/x-date-pickers
npm install @mui/x-data-grid-pro
npm install @mui/x-date-pickers-pro

# Mui tailwindcss

npm install @mui/styled-engine-sc styled-components