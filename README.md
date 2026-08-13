# bengals-taekwondo-app
BENGALS Taekwondo
# Clone repo ลงมา
git clone https://github.com/YOUR_USERNAME/bengals-taewondo-app.git
cd bengals-taewondo-app

# Copy ไฟล์หลัก
cp taekwondo-supabase.jsx ./
cp *.md ./

# สร้าง package.json
cat > package.json << 'EOF'
{
  "name": "bengals-taewondo",
  "version": "1.0.0",
  "description": "BENGALS Taewondo Management System",
  "main": "index.js",
  "scripts": {
    "dev": "react-scripts start",
    "build": "react-scripts build",
    "start": "react-scripts start"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "lucide-react": "^latest"
  },
  "devDependencies": {
    "react-scripts": "5.0.0"
  },
  "browserslist": {
    "production": [">0.2%", "not dead", "not op_mini all"],
    "development": ["last 1 chrome version", "last 1 firefox version"]
  }
}
EOF

# สร้าง index.js
cat > index.js << 'EOF'
import React from 'react';
import ReactDOM from 'react-dom/client';
import Root from './taekwondo-supabase.jsx';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <Root />
  </React.StrictMode>
);
EOF

# สร้าง public/index.html
mkdir -p public
cat > public/index.html << 'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BENGALS Taewondo - Manager</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif; }
    #root { width: 100%; min-height: 100vh; }
  </style>
</head>
<body>
  <div id="root"></div>
</body>
</html>
EOF

# Push ไป GitHub
git add .
git commit -m "Initial commit: BENGALS Taewondo Manager"
git push origin main
