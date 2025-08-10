# Event Management & RSVP App (MVP)

This repository contains a minimal full-stack Event Management & RSVP application scaffold:
- Backend: Node.js, Express, PostgreSQL
- Frontend: React (Vite) + Tailwind (minimal)

## Quick start (local)

1. Create a Postgres DB and set DATABASE_URL in backend/.env
2. Run migrations: psql $DATABASE_URL -f backend/migrations/001_create_tables.sql
3. Backend:
   cd backend
   npm install
   cp .env.example .env   # edit values
   npm run dev
4. Frontend:
   cd frontend
   npm install
   cp .env.example .env   # edit VITE_API_BASE if needed
   npm run dev

## Demo checklist
- Register user (POST /api/auth/register) or use frontend /login
- Create event (POST /api/events) as host
- View public events on home
- RSVP (POST /api/events/:id/rsvp)
- Host sends reminder (POST /api/events/:id/reminder)

## Deployment
- Deploy frontend to Vercel
- Deploy backend to Render / Railway / Heroku
- Use managed Postgres for production

