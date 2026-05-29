# 🎪 All-Projects: Real-Time Event & Academic Management Ecosystem

ยินดีต้อนรับสู่คลังซอร์สโค้ดรวม (Monorepo) สำหรับการพัฒนาระบบนิเวศทางซอฟต์แวร์ที่หลากหลาย โปรเจกต์นี้เป็นการรวบรวม 3 แพลตฟอร์มหลักที่แสดงถึงทักษะการพัฒนาซอฟต์แวร์แบบ Full-Stack ทั้งในส่วนของระบบเว็บเกมแบบเรียลไทม์ (Real-Time Web Platform) แดชบอร์ดบริหารจัดการข้อมูลขั้นสูง (Data Administration Dashboard) และแอปพลิเคชันบนมือถือ (Cross-Platform Mobile Application)

---

## 📂 โครงสร้างและการแยกส่วนประกอบของโปรเจกต์ (Project Components)

ภายใน Repository นี้ถูกแบ่งออกเป็น 3 ส่วนหลักตามสถาปัตยกรรมซอฟต์แวร์อย่างชัดเจน:

### 1. 🎮 [Real-Time Festival Prize Mini Game Platform](./Real-Time%20Festival%20Prize%20Mini%20Game%20Platform)
แพลตฟอร์มมินิเกมงานวัดแบบ Real-Time ที่มุ่งเน้นการรองรับผู้ใช้งานจำนวนมากพร้อมกัน (High Concurrency)
*   **Frontend (Game Engine):** พัฒนาด้วย **Phaser 3 (JavaScript)** มุ่งเน้นการจัดการทรัพยากรเกม, ระบบตรวจจับการชน (Collision) และการทำมินิเกมงานวัด เช่น เกมตักปลา, เกมจับคู่มวยไทย และเกมปาลูกโป่ง (ระบบยิง 2 นัดแตก)
*   **Backend (Real-Time Server):** พัฒนาด้วย **ภาษา Go (Golang)** ออกแบบสถาปัตยกรรมแบบ Event-driven ผ่าน **WebSocket** เพื่อควบคุมห้องพักคอย (Lobby System) และจัดลำดับการเล่นเกมพร้อมกันแบบเรียลไทม์
*   *👉 รายละเอียดเชิงลึกและวิธีรันระบบ: [อ่านต่อที่คู่มือ Mini Game Platform](./Real-Time%20Festival%20Prize%20Mini%20Game%20Platform/README.md)*

### 2. 🎲 [Reward Randomization System](./Reward%20Randomization%20System)
ระบบหลังบ้านและแดชบอร์ดบริหารจัดการห้องสุ่มรางวัลสำหรับงานเทศกาลระดับองค์กร (Enterprise Reward Engine)
*   **Backend (Clean Architecture):** พัฒนาด้วย **Go & Gin Framework** แยกเลเยอร์ชัดเจน (Controller, Service, Model) ร่วมกับ **Bun ORM** และ **PostgreSQL** เพื่อความถูกต้องแม่นยำของข้อมูลรางวัล
*   **Frontend (Dashboard):** พัฒนาด้วย **Nuxt 3 (Vue 3)**, **TypeScript** และ **Pinia** นำเสนอแอนิเมชันการสุ่มรางวัลที่น่าตื่นเต้นและแดชบอร์ดสรุปผลแบบเรียลไทม์
*   *👉 รายละเอียดเชิงลึกและวิธีรันระบบ: [อ่านต่อที่คู่มือ Reward System](./Reward%20Randomization%20System/README.md)*

### 3. 🏫 [Classroom Management System](./Classroom%20Management%20System)
แอปพลิเคชันบนมือถือแบบ Cross-Platform สำหรับบริหารจัดการชั้นเรียนและบันทึกเวลาเข้าเรียน
*   **Mobile Development:** พัฒนาด้วย **React Native** และ **Expo Managed Workflow** ร่วมกับ **TypeScript** 
*   **Key Highlights:** สถาปัตยกรรมแบบ File-based routing ด้วย **Expo Router**, การออกแบบ Modular UI Components และการจัดการ State ภายในแอปพลิเคชันที่มีประสิทธิภาพสูง รองรับทั้งระบบปฏิบัติการ iOS และ Android
*   *👉 รายละเอียดเชิงลึกและวิธีรันระบบ: [อ่านต่อที่คู่มือ Classroom Management](./Classroom%20Management%20System/README.md)*

---

## 🕹️ ไฮไลต์ฟีเจอร์ทางเทคนิค (Technical Core Features)

*   ⚡ **Real-Time Bidirectional Sync:** ใช้ WebSockets ในการสตรีมสถานะและควบคุมคิวการเล่นเกมของผู้เล่นในห้องพร้อมกันอย่างแม่นยำ
*   🔒 **Secure Draw Engine:** อัลกอริทึมสุ่มรางวัลขั้นสูงที่มีระบบตรวจสอบสิทธิ์ ป้องกันการชนกันของข้อมูล (Anti-collision) และระบบบล็อกการสุ่มซ้ำเพื่อความโปร่งใส
*   📊 **Asynchronous Bulk Data Parsing:** ระบบฝั่ง Nuxt 3 รองรับการนำเข้าข้อมูลผู้เข้าร่วมจำนวนมากผ่านไฟล์ Excel (`.xlsx`, `.xls`) และ CSV เพื่อลดภาระการทำงานของเครือข่าย
*   📱 **Native Component Rendering:** การพัฒนา Mobile App ที่คงความสม่ำเสมอของ UI/UX บนอุปกรณ์ที่แตกต่างกัน และการวางโครงสร้าง Custom Hooks เพื่อแยก Business Logic

---

## 🛠️ ภาพรวมเทคโนโลยีที่เลือกใช้ทั้งหมด (Total Tech Stack)

### Client & Game Engineering
*   **Web Frameworks:** Nuxt 3 (Vue 3), TypeScript, Pinia (State Management)
*   **Mobile Framework:** React Native, Expo Router, EAS (Expo Application Services)
*   **Game Development:** Phaser 3 (JavaScript)
*   **Styling Ecosystem:** Tailwind CSS, DaisyUI, Nuxt UI

### Server & Infrastructure
*   **Backend Languages:** Go (Golang), Gin Gonic Framework, Node.js
*   **Database & ORM:** PostgreSQL, Bun ORM, Prisma ORM
*   **Cloud Cloud Services:** Cloudinary API (สำหรับระบบฝากรูปภาพของรางวัล), Render
*   **DevOps:** Docker, Docker Compose, Linux Environments

---

## 👥 ข้อมูลผู้พัฒนา (Developer Profiles)

*   **Ammikaamy** — Full-Stack Software Engineer
    *   *บทบาทหลัก:* ออกแบบโครงสร้างระบบหลังบ้านด้วยภาษา Go, พัฒนาระบบ Real-time WebSockets, พัฒนาแกนหลักของมินิเกมด้วย Phaser 3 และจัดการฐานข้อมูลสุ่มรางวัลร่วมกับสถาปัตยกรรมแบบจัดโครงสร้างสะอาดยืดหยุ่น
    *   [GitHub Profile](https://github.com/Ammikaamy)
