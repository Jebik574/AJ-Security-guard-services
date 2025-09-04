I cannot generate a real downloadable folder directly in this canvas. However, I can create all the individual files with their contents here so you can copy them into a folder named `aj_security_website` on your local machine. Once all files are copied, you can zip the folder and deploy it.

Here are the files you need:

---
**package.json**
```json
{
  "name": "aj-security-guard-services",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "vite": "^5.0.0",
    "@vitejs/plugin-react": "^4.0.0"
  }
}
```

---
**vite.config.js**
```js
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()]
});
```

---
**public/index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AJ Security Guard Services</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
```

---
**public/logo.svg**
```svg
<svg xmlns="http://www.w3.org/2000/svg" width="400" height="120">
  <rect width="400" height="120" rx="12" fill="#0ea5a4"/>
  <text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-family="Arial" font-size="22" fill="white">AJ Security Guard Services</text>
</svg>
```

---
**src/main.jsx**
```jsx
import React from 'react';
import { createRoot } from 'react-dom/client';
import App from './App';
import './index.css';

createRoot(document.getElementById('root')).render(<App />);
```

---
**src/App.jsx**
```jsx
import React from 'react';

export default function App() {
  const phone = '+971522019994';
  return (
    <div>
      <header>
        <h1>AJ Security Guard Services</h1>
        <a href={'tel:' + phone}>{phone}</a>
      </header>
      <main>
        <p>Professional security solutions in Ajman.</p>
      </main>
      <footer>
        <p>Address: Ecape Tower, Rashidya 3, Ajman</p>
        <p>PSBD Certified</p>
      </footer>
    </div>
  );
}
```

---
**src/index.css**
```css
body { margin: 0; font-family: Arial, sans-serif; background: #f8fafc; color: #0f172a; }
header, footer { padding: 16px; background: #e0f2fe; }
main { padding: 32px; }
```
