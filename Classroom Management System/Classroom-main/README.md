# 🏫 Classroom Management System

แอปพลิเคชันบนมือถือแบบ Cross-platform ที่ถูกพัฒนาขึ้นเพื่อเพิ่มประสิทธิภาพในการบริหารจัดการชั้นเรียน การเช็กชื่อเข้าเรียน (Attendance Tracking) และการสื่อสารภายในห้องเรียนระหว่างผู้สอนและผู้เรียน ตัวแอปพลิเคชันพัฒนาด้วยเทคโนโลยีหลักอย่าง **React Native**, **Expo (Router)** และ **TypeScript** เพื่อส่งมอบประสบการณ์การใช้งานที่ลื่นไหลและตอบสนองได้อย่างรวดเร็ว

---

## 📂 โครงสร้างสถาปัตยกรรมระบบ (Project Architecture)

โปรเจกต์นี้ได้รับการออกแบบโครงสร้างในรูปแบบ Modular ที่มีความสะอาดและเป็นระเบียบตามมาตรฐานของ Expo Router:

* `app/` - ส่วนควบคุมการจัดเส้นทาง (Routing) และ Layout หน้าจอหลักทั้งหมด โดยใช้ระบบ File-based routing ของ **Expo Router**
* `components/` - แหล่งรวม Atomic Components ที่สามารถนำกลับมาใช้ซ้ำได้ (เช่น Buttons, Inputs, Modals, Cards) เพื่อคงความสม่ำเสมอของ UI/UX
* `constants/` - ส่วนจัดเก็บค่าคงที่ส่วนกลางของระบบ เช่น Global Styles, การตั้งค่าธีมสี (Themes) และ API Endpoints
* `hooks/` - Custom React Hooks ที่แยกส่วนตรรกะทางธุรกิจ (Business Logic) และการจัดการ State ออกจากหน้า UI เพื่อให้ง่ายต่อการทดสอบและบำรุงรักษา
* `scripts/` - สคริปต์อัตโนมัติสำหรับช่วยสนับสนุนระบบการทำงานและการทดสอบในขั้นตอนการพัฒนา

---

## 🛠️ เทคโนโลยีที่เลือกใช้ในการพัฒนา (Mobile Engineering Tech Stack)

* **Framework Core:** React Native (Expo Managed Workflow)
* **Routing & Navigation:** Expo Router (Native Navigation)
* **Language:** TypeScript (Strict Type Safety)
* **Build Pipeline & Distribution:** EAS (Expo Application Services) สำหรับการทำ Cloud Builds
* **State Management:** React Hooks & Context API

---

## 🕹️ ฟีเจอร์เด่นของระบบ (Key Features)

* **Real-time Attendance Tracking:** ระบบเช็กชื่อและบันทึกเวลาเข้าเรียนของผู้เรียนแบบเรียลไทม์ พร้อมโครงสร้างที่รองรับการสรุปผลและส่งออกรายงานสำหรับผู้สอน
* **Classroom Management Dashboard:** ระบบแยกสิทธิ์การใช้งาน (Roles) ระหว่างผู้สอนและผู้เรียน เพื่อจัดการตารางเรียน บันทึกคะแนน และอัปเดตสถานะงานที่ได้รับมอบหมาย
* **Interactive Announcements:** โครงสร้างระบบรองรับการเชื่อมต่อกับระบบกระจายข่าวสารและประกาศสำคัญภายในห้องเรียน
* **Cross-Platform Uniformity:** การันตีการแสดงผลและประสิทธิภาพการทำงานที่สอดคล้องกันทั้งบนระบบปฏิบัติการ iOS และ Android ผ่านการเรนเดอร์ Native Components

---

## 🚀 ขั้นตอนการติดตั้งและเริ่มต้นใช้งาน (Local Installation)

กรุณาตรวจสอบว่าเครื่องของคุณได้ติดตั้ง Node.js และมีแอปพลิเคชัน Expo Go บนสมาร์ทโฟนก่อนเริ่มต้นรันระบบ

### 1. เข้าสู่ไดเรกทอรีของโปรเจกต์

```bash
cd "Classroom Management System"
```

### 2. ติดตั้ง Dependencies

```bash
npm install
```

### 3. เริ่มต้น Development Server

```bash
npx expo start
```

### 4. เปิดใช้งานผ่าน Expo Go

สแกน QR Code ที่แสดงบน Terminal หรือ Browser ผ่านแอป Expo Go เพื่อเริ่มต้นใช้งานระบบบนอุปกรณ์มือถือจริง

---

## 📦 Build & Deployment

ระบบรองรับการ Build แบบ Cloud Native ผ่าน Expo Application Services (EAS)

### Build Android

```bash
eas build -p android
```

### Build iOS

```bash
eas build -p ios
```

---

## 👨‍💻 แนวทางการพัฒนาในอนาคต (Future Enhancements)

* ระบบแจ้งเตือนแบบ Push Notification
* AI Analytics สำหรับวิเคราะห์พฤติกรรมการเข้าเรียน
* ระบบ Video Classroom Integration
* Offline Attendance Sync
* Multi-Classroom Management System
* Dashboard วิเคราะห์ผลการเรียนเชิงสถิติแบบ Real-time

---

## 📄 License

This project is developed for educational and portfolio purposes.
