# Thai Chat App 🇹🇭

แอปแชทภาษาไทย สร้างด้วย TERN Stack (TypeScript + Express.js + React + Node.js)

## ✨ Features

- 💬 Real-time chat messaging
- 👥 User profiles with statistics
- 🎨 6 beautiful themes + custom theme creator
- 📱 Mobile-responsive design
- 🌙 Dark/Light mode support
- 🖼️ Background image themes

## 🚀 Deployment

### สำหรับ Vercel:

1. **Push ไฟล์เหล่านี้ไป GitHub repository:**
   - `vercel.json` (configuration สำคัญ)
   - `api/` folder (Backend Functions)
   - `client/` folder (React Frontend)
   - `shared/` folder (Shared Types)

2. **ไป Vercel.com:**
   - New Project
   - Import from GitHub
   - เลือก repository
   - Framework: **Other**
   - Deploy

3. **การตั้งค่า Environment:**
   - Root Directory: **ว่างไว้**
   - Build Command: `cd client && npm run build`
   - Output Directory: `client/dist`
   - Install Command: `cd client && npm install`

## 📂 Project Structure

```
├── api/                 # Vercel Functions (Backend)
│   ├── auth.ts         # Authentication API
│   ├── messages.ts     # Messages API
│   ├── users.ts        # Users API
│   └── chat/theme.ts   # Theme API
├── client/             # React Frontend
│   ├── src/
│   ├── package.json
│   └── dist/           # Build output
├── shared/             # Shared TypeScript types
│   └── schema.ts
└── vercel.json         # Vercel configuration
```

## 🛠️ Tech Stack

- **Frontend:** React 18, TypeScript, Vite, Tailwind CSS
- **Backend:** Vercel Functions (Node.js)
- **State Management:** TanStack Query
- **UI Components:** Radix UI + shadcn/ui
- **Routing:** Wouter
- **Styling:** Tailwind CSS + Custom CSS Variables

## 🎯 Key Features

### Chat System
- Real-time messaging with auto-refresh
- Message editing and deletion
- User avatars and timestamps

### User Profiles
- Complete profile system
- User statistics (days active, message count)
- Contact information
- Online status tracking

### Theme System
- 6 built-in themes
- Custom theme creator with image backgrounds
- Real-time theme preview
- Responsive theme selector

### Mobile Optimization
- Responsive header design
- Mobile-friendly buttons and spacing
- Touch-optimized interface

Made with ❤️ in Thailand