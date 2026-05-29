# 🎪 Real-Time Event Platform: Mini-Games & Advanced Reward Systems

A production-ready Monorepo showcasing a full-stack, real-time festival platform. This project integrates micro-features across two major systems: a high-concurrency real-time mini-game environment and an enterprise-grade reward randomization engine.

---

## 🚀 System Architecture Overview

This repository is structured as a **Monorepo** to demonstrate clean separation of concerns, modern API design, and robust database architectures.

### 1. 🎮 [Real-Time Mini-Game Platform](./Real-Time%20Festival%20Prize%20Mini%20Game%20Platform)
A high-engagement, real-time gaming core built for concurrent festival environments.
*   **Frontend (Game Engine):** Built with **Phaser 3 (JavaScript)** to deliver low-latency, interactive visual assets and smooth multi-hit game mechanics.
*   **Backend (Real-Time Service):** Developed using **Go (Golang)** with an event-driven **WebSocket** architecture to handle state synchronization across player lobbies.
*   **Key Highlights:** Real-time synchronized room management (Lobby), sequential game state control, and complex collision/interaction scoring.

### 2. 🎲 [Reward Randomization System](./Reward%20Randomization%20System)
An enterprise-grade administration dashboard and backend engine designed for high-integrity reward distribution.
*   **Backend (Clean Architecture):** Built with **Go & Gin Framework**, implementing a structured layer pattern (Controller, Service, Model) with **Bun ORM** and **PostgreSQL**.
*   **Frontend (SPA/SSR):** Developed using **Nuxt 3 (Vue 3)**, **TypeScript**, and **Pinia** for efficient state management and optimized rendering.
*   **Key Highlights:** Anti-collision draw mechanics (preventing duplicate winners), dynamic condition-based matching, bulk data handling, and structured logging.

---

## 🛠️ Production-Grade Tech Stack

### Frontend & Game Engineering
*   **Core & Frameworks:** Nuxt 3 (Vue 3), TypeScript, Phaser 3, Pinia, Vue Router
*   **UI/UX Component Ecosystem:** Tailwind CSS, DaisyUI, Nuxt UI, SweetAlert2
*   **Data Parsing & Assets:** XLSX (Excel data processing), QRCode.vue, Axios

### Backend & Cloud Infrastructure
*   **Languages & Frameworks:** Go (Golang), Gin Gonic
*   **Databases & ORM:** PostgreSQL, Bun ORM, Prisma ORM
*   **Storage & Deployment:** Cloudinary (Asset Storage), Docker & Docker Compose, Linux (Fedora/Rocky environments), Render

---

## 🕹️ Technical Deep Dive & Key Features

### 🔹 High-Concurrency Real-Time Synchronization
*   **WebSocket State Machine:** The Go-based backend manages independent room sessions (`ws/`) ensuring real-time bidirectional messaging for interactive user verification and lobbies.
*   **Sequential Gameplay Logic:** Implemented rigid state sync across distributed clients so all participants experience identical game stages and rules concurrently.

### 🔹 Advanced Randomization Logic & Data Management
*   **Data Ingestion Pipeline:** Supports asynchronous bulk imports of participant rosters via Excel (`.xlsx`, `.xls`) and CSV format parsing.
*   **Secure Draw Engine:** Implemented condition-based filtering and strict constraints to guarantee deterministic reward caps, automated item exhaustion, and zero-duplicate draw histories.
*   **Media & CDN Management:** Integrated Cloudinary API to dynamically stream and manage visual assets for prize carousels seamlessly.

---

## 📁 Repository Structure

```text
├── Real-Time Festival Prize Mini Game Platform/   # Core App (Game + Real-time WebSockets)
│   ├── Frontend/                                 # Phaser 3 Client
│   └── backend/                                  # Go (Lobby & Game State Server)
└── Reward Randomization System/                  # Reward Engine (Nuxt 3 + Gin + Postgres)
    ├── frontend/                                 # Dashboard & Animation Client
    └── backend/                                  # Go Clean Architecture Server
