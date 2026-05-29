# 🎮 Real-Time Festival Prize Mini Game Platform

ยินดีต้อนรับสู่โปรเจกต์ **แพลตฟอร์มมินิเกมงานวัดและระบบสุ่มรางวัลแบบ Real-Time** ส่วนนี้เป็นซอร์สโค้ดหลักของตัวแอปพลิเคชัน (Core Application) ที่รวมการทำงานแบบ Full-Stack ระหว่างระบบหน้าบ้านและหลังบ้านเข้าด้วยกัน

---

## 📂 โครงสร้างภายในโฟลเดอร์ (Project Structure)

*   `Frontend/` - ซอร์สโค้ดฝั่งหน้าจอผู้เล่นและมินิเกมงานวัดทั้งหมด พัฒนาด้วย **Phaser 3 (JavaScript)**
*   `backend/` - ระบบหลังบ้านสำหรับจัดการห้องพักคอยและควบคุมสถานะเกม พัฒนาด้วย **ภาษา Go**
    *   `controllers/` - ส่วนควบคุมตรรกะ (Game Logic) และเงื่อนไขการรับรางวัล
    *   `routes/` - ส่วนจัดการ API Endpoint
    *   `ws/` - ส่วนควบคุมระบบ Real-Time Lobby และสตรีมข้อมูลผู้เล่นผ่าน **WebSocket**

---

## 🛠️ เทคโนโลยีที่เลือกใช้ (Tech Stack)

*   **Game Engine:** Phaser 3 (JavaScript)
*   **Backend Server:** Go (Golang)
*   **Real-Time Communication:** WebSockets
*   **Database Management:** Prisma ORM (เชื่อมโยงกับระบบสุ่มรางวัล)
*   **UI/UX Design:** Figma

---

## 🕹️ ฟีเจอร์หลักของระบบ (Key Features)

1.  **Lobby System:** หน้าพักคอยสำหรับรวมกลุ่มผู้เล่น ตรวจสอบความพร้อม และทำการยืนยันตัวตนก่อนเริ่มเกม
2.  **Sequential Gameplay:** ระบบควบคุมรอบการแข่งขัน โดยผู้เล่นทุกคนในห้องจะเล่นมินิเกมเดียวกันตามลำดับขั้นที่ระบบกำหนดไว้พร้อมๆ กัน
3.  **Mini Games:** รวบรวมมินิเกมงานวัดทั้งหมด 10 กิจกรรมหลัก เช่น:
    *   **เกมตักปลา (Fish Scooping)**
    *   **เกมจับคู่มวยไทย (Muay Thai Matching)**
    *   **เกมปาลูกโป่ง (Balloon Pop)** - ระบบ Multi-hit (ลูกโป่งอึด ต้องยิง 2 นัดถึงจะแตก)

---

## 🚀 วิธีการติดตั้งและเริ่มใช้งาน (Getting Started)

กรุณาตรวจสอบว่าเครื่องของคุณได้ทำการติดตั้ง [Node.js](https://nodejs.org/) และ [Go](https://go.dev/) เรียบร้อยแล้วก่อนเริ่มรันระบบ

### 1. การเปิดใช้งานระบบหลังบ้าน (Backend Setup)
```bash
# ดาวน์โหลด dependencies ของ Go
go mod download

# สั่งรัน Backend server
go run main.go
