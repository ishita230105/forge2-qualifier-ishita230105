# Taskflow

Taskflow is a premium, beautifully designed Kanban board built with a **Laravel API (SQLite)** backend and a **React (Vite)** frontend. It features a clean, light-mode aesthetic inspired by modern macOS design principles, prioritizing smooth interactions and soft typography.

Built for the Forge 2 Qualifier.

## Features
- **Full Kanban Functionality**: Boards → Lists → Cards.
- **Drag & Drop**: Smooth reordering of cards between lists using `@dnd-kit`.
- **Card Details**: Edit titles, descriptions, and assign colorful tags.
- **Member Assignment**: Assign team members to specific tasks.
- **Due Dates**: Set and track deadlines with visual indicators.
- **Premium UI**: Soft shadows, rounded corners, and micro-animations for a high-end feel.

## Models Used & Routing Rationale
- **Hermes (Brain/Planning)**: `gpt-oss-120b` (via Groq). Used for its massive context window and deep reasoning capabilities to architect the database schema and React component hierarchy.
- **OpenClaw (Hands/Coding)**: `llama-3.3-70b-versatile` (via Groq). Chosen for its lightning-fast inference speed and robust code-generation abilities to churn out the Tailwind components and Laravel controllers efficiently.

## Local Run Instructions

### 1. Backend (Laravel API)
```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
php artisan serve
```
The API will run at `http://127.0.0.1:8000`.

### 2. Frontend (React UI)
```bash
cd frontend
npm install
npm run dev
```
The UI will run at `http://localhost:5173`.

---
*Developed by Ishita Modi.*
