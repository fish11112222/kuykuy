# Thai Chat App (TERN Stack)

**Repository**: https://github.com/fish11112222/isus

แชทแอปพลิเคชันที่เขียนด้วย TypeScript + Express.js + React + Node.js

## 🚀 วิธีการ Deploy บน Vercel

### 1. เตรียมไฟล์โปรเจค

```bash
# Clone หรือ download โปรเจคนี้
git clone <your-repo-url>
cd thai-chat-app
```

### 2. สร้าง Repository บน GitHub

1. ไปที่ [GitHub.com](https://github.com)
2. สร้าง repository ใหม่
3. Upload โค้ดขึ้น GitHub:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

### 3. Deploy บน Vercel

1. **สมัครสมาชิก**: ไปที่ [Vercel.com](https://vercel.com) และสมัครด้วย GitHub

2. **เชื่อมต่อ Repo**: คลิก "New Project" → เลือก repository จาก GitHub

3. **ตั้งค่า Build**: 
   - Framework Preset: **Other**
   - Root Directory: `./` (ค่า default)
   - Build Command: ปล่อยว่างไว้ (ใช้ vercel.json)
   - Output Directory: ปล่อยว่างไว้ (ใช้ vercel.json)
   - Install Command: ปล่อยว่างไว้

4. **Deploy**: คลิก "Deploy" และรอ 2-3 นาที

5. **หากมี Error**: ดู logs และแก้ไขใน GitHub แล้วจะ auto-deploy ใหม่

### 4. ตั้งค่าหลัง Deploy

หลังจาก deploy สำเร็จ:
1. Vercel จะให้ URL แบบ: `https://your-app-name.vercel.app`
2. ทดสอบการใช้งาน: สมัครสมาชิก → เข้าสู่ระบบ → แชท
3. แชร์ URL ให้เพื่อนๆ ใช้งาน

## 🔧 สำหรับ Development

```bash
# ติดตั้ง dependencies
npm install

# รันในโหมด development
npm run dev

# เปิดเบราว์เซอร์ไปที่ http://localhost:5000
```

## 📁 โครงสร้างโปรเจค

```
thai-chat-app/
├── client/           # React frontend
│   ├── src/         # โค้ด React
│   ├── dist/        # Build output
│   └── package.json # Dependencies สำหรับ frontend
├── api/             # Vercel Functions (Serverless API)
│   ├── auth.ts      # Authentication API
│   ├── messages.ts  # Messages API
│   ├── users.ts     # Users API
│   └── chat/        # Chat related APIs
├── shared/          # Shared types และ schemas
├── vercel.json      # Vercel configuration
└── README.md        # คู่มือนี้
```

## 🌟 ฟีเจอร์

- ✅ แชทแบบเรียลไทม์
- ✅ ระบบสมาชิก (สมัคร/เข้าสู่ระบบ)
- ✅ อัปโหลดรูปภาพ และ GIF
- ✅ อิโมจิ
- ✅ แก้ไข/ลบข้อความ
- ✅ ระบบธีม (เปลี่ยนสีพื้นหลัง)
- ✅ โปรไฟล์ผู้ใช้
- ✅ แสดงคนออนไลน์
- ✅ Responsive design (ใช้งานได้ทั้งมือถือและคอม)

## 🔒 Security Notes

- ในเวอร์ชัน production ควรใช้ database จริง (PostgreSQL, MongoDB)
- ควรเพิ่มระบบ authentication ที่แข็งแกร่งกว่านี้
- ควรเพิ่มการ hash password
- ควรเพิ่ม rate limiting สำหรับ API

## 🔧 แก้ไขปัญหา Deploy

**ปัญหาที่พบบ่อย:**

1. **"Function Runtimes must have" Error**:
   - ตรวจสอบว่า vercel.json ถูกต้อง
   - ลองลบ cache: Settings → General → Clear Cache

2. **"Build failed" Error**:
   - ตรวจสอบใน Build Logs
   - มักเป็นปัญหาจาก dependencies ขาดหาย

3. **API ไม่ทำงาน**:
   - ตรวจสอบว่า API files อยู่ในโฟลเดอร์ `api/` 
   - ตรวจสอบ routes ใน vercel.json

**วิธีแก้ไข:**
1. ดู logs ใน Vercel dashboard
2. แก้โค้ดใน GitHub 
3. Vercel จะ auto-deploy ใหม่

---

**สร้างด้วย ❤️ โดยใช้ TERN Stack (TypeScript + Express.js + React + Node.js)**