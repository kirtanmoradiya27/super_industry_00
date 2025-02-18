Here’s a setup for a React project with Vite, TailwindCSS, and MUI (downgraded to v5). I’ll provide you with the initial structure, including ready-to-use folders: `common`, `components`, `store`, `pages`, and `api`.

---

### **Step 1: Initialize React + Vite Project**
Run these commands to create a new React project with Vite and navigate into the directory:
```bash
npm create vite@latest my-app --template react
cd my-app
npm install
```

---

### **Step 2: Install TailwindCSS**
Install TailwindCSS and its dependencies:
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Update your `tailwind.config.js`:
```javascript
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
```

Add Tailwind directives in `index.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### **Step 3: Install MUI (v5)**
```
"@mui/icons-material": "^5.15.5",
    "@mui/lab": "^5.0.0-alpha.99",
    "@mui/material": "^5.15.5",
    "@mui/x-date-pickers": "^5.0.4",
    "@mui/styles": "^5.15.5",
    "@mui/styled-engine-sc": "^5.15.5",
```
Install MUI v5 and related packages:
```bash
npm install @mui/material@^5.15.5 @emotion/react @emotion/styled
npm install @mui/icons-material@^5.15.5 @mui/lab@^5.0.0-alpha.99
npm install @mui/x-data-grid@^5.17.4 @mui/x-date-pickers@^5.0.4
npm install @mui/styled-engine-sc styled-components
```

---

### **Step 4: Folder Structure**
Create the following folders inside the `src` directory:

```
src
├── api
│   └── apiClient.js
├── common
│   └── constants.js
├── components
│   ├── Navbar.jsx
│   ├── Footer.jsx
│   └── Button.jsx
├── pages
│   ├── Home.jsx
│   ├── About.jsx
│   └── Contact.jsx
├── store
│   └── store.js
└── App.jsx
```

---

### **Step 5: File Contents**

#### `api/apiClient.js`
```javascript
import axios from 'axios';

const apiClient = axios.create({
  baseURL: 'https://api.example.com',
  headers: {
    'Content-Type': 'application/json',
  },
});

export default apiClient;
```

#### `common/constants.js`
```javascript
export const APP_NAME = 'My React App';
export const API_URL = 'https://api.example.com';
```

#### `components/Navbar.jsx`
```javascript
import React from 'react';
import { AppBar, Toolbar, Typography } from '@mui/material';

const Navbar = () => {
  return (
    <AppBar position="static">
      <Toolbar>
        <Typography variant="h6">
          Navbar
        </Typography>
      </Toolbar>
    </AppBar>
  );
};

export default Navbar;
```

#### `components/Footer.jsx`
```javascript
import React from 'react';

const Footer = () => {
  return (
    <footer className="text-center p-4 bg-gray-100">
      <p>&copy; 2025 My React App</p>
    </footer>
  );
};

export default Footer;
```

#### `components/Button.jsx`
```javascript
import React from 'react';
import { Button as MuiButton } from '@mui/material';

const Button = ({ label, onClick, color = 'primary', variant = 'contained' }) => {
  return (
    <MuiButton color={color} variant={variant} onClick={onClick}>
      {label}
    </MuiButton>
  );
};

export default Button;
```

#### `pages/Home.jsx`
```javascript
import React from 'react';
import Navbar from '../components/Navbar';

const Home = () => {
  return (
    <div>
      <Navbar />
      <main className="p-4">
        <h1 className="text-2xl font-bold">Welcome to My App</h1>
        <p>This is the home page.</p>
      </main>
    </div>
  );
};

export default Home;
```

#### `store/store.js`
```javascript
import { configureStore } from '@reduxjs/toolkit';

const store = configureStore({
  reducer: {},
});

export default store;
```

#### `App.jsx`
```javascript
import React from 'react';
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import Home from './pages/Home';
import About from './pages/About';
import Contact from './pages/Contact';

const App = () => {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;
```

#### `pages/About.jsx`
```javascript
import React from 'react';

const About = () => {
  return (
    <div>
      <h1>About Page</h1>
      <p>This is the about page of the app.</p>
    </div>
  );
};

export default About;
```

#### `pages/Contact.jsx`
```javascript
import React from 'react';

const Contact = () => {
  return (
    <div>
      <h1>Contact Page</h1>
      <p>Reach out to us at contact@myapp.com</p>
    </div>
  );
};

export default Contact;
```

---

### **Step 6: Install React Router**
Install `react-router-dom` for routing:
```bash
npm install react-router-dom
```

---

### **Step 7: Run the Project**
Start the development server:
```bash
npm run dev
```

---

Let me know if you need any additional customization!






# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# Use the all command

```
npm create vite@latest
cd name_your
npm i
npm run dev
```

# Install the tailwindcss

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

# tailwind.config.js

```
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
```

# index.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

# Mui

```
npm install @mui/material @emotion/react @emotion/styled
npm install @mui/material @mui/styled-engine-sc styled-components
npm install @mui/icons-material
npm install @mui/lab
npm install @mui/x-data-grid
npm install @mui/x-date-pickers
npm install @mui/x-data-grid-pro
npm install @mui/x-date-pickers-pro
```

# Mui tailwindcss

```
npm install @mui/styled-engine-sc styled-components
```
