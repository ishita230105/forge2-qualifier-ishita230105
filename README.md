# 🚀 Taskflow(The KanBan Board)

Taskflow is a premium, beautifully designed Kanban board built with a **Laravel API (SQLite)** backend and a **React (Vite)** frontend. It features a clean, modern aesthetic focusing on smooth interactions, intuitive design, and seamless task management.

🎯 **Built for the Forge 2 · Edition 2 Qualifier.**

---

## ✨ Features
- **Full Kanban Functionality**: Create Boards, Lists, and Cards seamlessly.
- **Drag & Drop**: Smooth reordering of cards between lists using `@dnd-kit`.
- **Card Details**: Edit titles, descriptions, and assign colorful tags.
- **Member Assignment**: Assign team members directly to specific tasks.
- **Due Dates**: Set and track deadlines with visual indicators.
- **Premium UI**: Soft shadows, rounded corners, and micro-animations for a high-end, native feel.

---

## 🤖 The Two-Agent System
This project was built and refined using a 100% free-stack, dual-agent architecture wired entirely through Slack Socket Mode, strictly adhering to the Forge 2 Qualifier handbook.

### 🧠 Hermes (The Brain)
- **Role**: Orchestrator, planning, and high-level architectural reasoning.
- **Model**: `gemini-2.5-flash` (via Google AI Studio).
- **Function**: Planned the database schema, broke down the React component hierarchy, and guided the hands based on the Forge handbook requirements.

### 🦞 OpenClaw (The Hands)
- **Role**: High-speed code generation and terminal execution.
- **Model**: `llama3-70b-8192` (via Groq).
- **Function**: Executed terminal commands, scaffolded the Laravel backend, and rapidly built the Tailwind CSS UI components with blazing-fast inference.

---

## 💻 Local Run Instructions

### 1. Backend (Laravel API)
```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
php artisan serve
```
*The API will run at `http://127.0.0.1:8000`.*

### 2. Frontend (React UI)
```bash
cd frontend
npm install
npm run dev
```
*The UI will run at `http://localhost:5173`.*

---

🎓 *Developed by Ishita Modi.*
