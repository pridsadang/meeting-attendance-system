# 🎯 ระบบเซ็นชื่อเข้าร่วมประชุม v2.0

> ระบบบันทึกการรับทราบเอกสารและลายเซ็นออนไลน์ที่ทันสมัยและใช้งานง่าย

## ✨ ฟีเจอร์หลัก

- 🔐 **Admin Mode** - แก้ไขข้อมูลเอกสารได้เฉพาะผู้ดูแลระบบ
- ✍️ **ลายเซ็นดิจิทัล** - เซ็นชื่อบน Canvas รองรับทั้ง Mouse และ Touch
- 📊 **Firebase Integration** - บันทึกข้อมูล Real-time ลง Firestore
- 📄 **PDF Export** - ส่งออกเป็น PDF พร้อมลายเซ็นทั้งหมด
- 💾 **Auto-save** - บันทึกอัตโนมัติทุก 30 วินาที
- 📱 **Responsive Design** - ใช้งานได้บนทุกอุปกรณ์
- 🌐 **Offline Support** - ทำงานได้แม้ไม่มีอินเทอร์เน็ต
- 🚀 **Vercel Ready** - พร้อม deploy ทันที

## 🛠️ เทคโนโลยีที่ใช้

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Database**: Firebase Firestore
- **Canvas API**: สำหรับลายเซ็นดิจิทัล
- **PDF Generation**: jsPDF
- **Hosting**: Vercel
- **Version Control**: GitHub

## 📦 โครงสร้างไฟล์

```
meeting-attendance-system/
├── index.html              # ไฟล์หลักของระบบ
├── README.md              # คู่มือการใช้งาน
├── vercel.json            # การตั้งค่า Vercel (แก้ไข Error แล้ว)
├── .gitignore             # ไฟล์ที่ไม่ต้อง commit
├── package.json           # ข้อมูล Project
├── firebase-setup.md      # คู่มือตั้งค่า Firebase
└── DEPLOY.md             # คำแนะนำการ Deploy
```

## 🚀 การติดตั้งและ Deploy

### 1. ⚡ Quick Start (5 นาที)

1. **Download ไฟล์ทั้งหมด** จาก artifacts
2. **อัปเดต Firebase Config** ในไฟล์ `index.html`
3. **Upload ไป GitHub** Repository
4. **Deploy ด้วย Vercel** (auto-deploy)
5. **เพิ่ม Domain** ใน Firebase Authorized domains

### 2. 🔧 ขั้นตอนละเอียด

ดูคู่มือครบชุดใน:
- 📖 `firebase-setup.md` - ตั้งค่า Firebase
- 🚀 `DEPLOY.md` - Deploy ไป Vercel

## ⚙️ การตั้งค่า

### Firebase Configuration
แก้ไขในไฟล์ `index.html` บรรทัดที่ 398:

```javascript
const firebaseConfig = {
    apiKey: "ใส่ API Key ของคุณ",
    authDomain: "your-project.firebaseapp.com",
    projectId: "your-project-id",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "123456789",
    appId: "your-app-id"
};
```

### Admin Password
เปลี่ยนรหัสผ่าน Admin ที่บรรทัดที่ 420:
```javascript
const ADMIN_PASSWORD = 'P@ssw0rd2024';
```

### รายชื่อผู้เข้าร่วม
แก้ไขรายชื่อที่บรรทัดที่ 430:
```javascript
let participants = [
    'นายศักดิ์ไชย ไชยปัญญา',
    'นายศิริพงศ์ คงวิเศษ',
    // เพิ่มหรือแก้ไขชื่อที่นี่
];
```

## 🎯 การใช้งาน

### สำหรับผู้เข้าร่วมประชุม
1. เปิดเว็บไซต์
2. เลือกวิธีการรับทราบเอกสาร
3. เซ็นชื่อในช่องลายเซ็น
4. เลือกวันที่ลงนาม
5. ระบบจะบันทึกอัตโนมัติ