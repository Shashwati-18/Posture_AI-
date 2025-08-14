# Posture_AI-
#  Posture Analysis Web Application

An AI + computer vision powered **posture analysis and musculoskeletal (MSK) health tracking web application**.  
The app helps users monitor and improve their posture in real time using their device camera, provides personalized feedback, ergonomic tips, and mood tracking.  
It also tracks progress over time with beautiful visualizations. This project is an AI and AR-powered posture correction application designed to monitor, analyze, and improve a user’s posture in real-time. It aims to address musculoskeletal (MSK) health issues by detecting poor posture habits and providing instant feedback, making it ideal for students, professionals, and fitness enthusiasts.

---

## Features
- **Real-Time Posture Detection** using browser-based camera access
- **Personalized Feedback & Recommendations** for better posture
- **Mood Tracking** for holistic health monitoring
- **Progress Tracking** with historical data visualization
- **User Accounts** with login & signup functionality
- **Ergonomic Tips** tailored to posture results
- **Modern, Responsive UI** with dark mode-friendly design

---

## System Architecture

### **Frontend**
- **React 18** with functional components & hooks
- **TypeScript** for type safety
- **Wouter** for lightweight routing
- **TanStack Query** for server state management & caching
- **Tailwind CSS** with custom design system
- **shadcn/ui** components built on Radix UI primitives
- **React Hook Form** + **Zod** for type-safe forms & validation
- **Lucide React** icons for consistent UI

**Architecture Style:**  
Component-based, with clear separation of UI, business logic, and data fetching.  
Pages, reusable UI components, and feature-specific components are well-structured.

---

### **Backend**
- **Express.js** server with TypeScript
- RESTful API endpoints
- **In-memory storage** (can swap to PostgreSQL)
- **Zod schemas** for runtime validation (shared between client & server)
- **Session-based authentication** (email/password)
- **Middleware** for logging, error handling, and response formatting

**Storage Layer:**  
Interface pattern (`IStorage`) with an in-memory implementation (`MemStorage`), ready for database integration.

---

### **Database**
(Current: in-memory → Planned: PostgreSQL with Drizzle ORM)
- **Drizzle ORM** with PostgreSQL dialect
- **Neon Database** for serverless deployment
- Three main tables: `users`, `posture_scans`, `user_moods`
- Full type safety across database operations

---

### **Authentication**
- Email/password registration & login
- Session management with `localStorage`
- Protected routes on both client & server
- Passwords stored in plain text for development (⚠ Needs hashing in production)

---

### **Posture Analysis**
- **WebRTC** for live camera feed
- **Canvas API** for overlay & posture point visualization
- Simulated scoring algorithm for realistic feedback
- Real-time posture analysis overlay
- Structured feedback system with score + issue list

---

## 🛠️ Tech Stack

**Frontend:** React 18, TypeScript, Wouter, TanStack Query, Tailwind CSS, shadcn/ui, React Hook Form, Zod  
**Backend:** Express.js, TypeScript, Zod, Session Auth  
**Database:** Drizzle ORM, PostgreSQL (Neon)  
**Posture Analysis:** WebRTC, Canvas API, (Future: MediaPipe/OpenCV integration)  
**Dev Tools:** Vite, ESBuild, PostCSS, Path Aliases
