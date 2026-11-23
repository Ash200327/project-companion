# Lovable Project Companion: Web IDE & Real-Time AI Workspace

[![React](https://img.shields.io/badge/React-18-blue.svg)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-blue.svg)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.4-purple.svg)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.4-38B2AC.svg)](https://tailwindcss.com/)
[![Radix UI](https://img.shields.io/badge/Radix%20UI-Shadcn-black.svg)](https://ui.shadcn.com/)
[![CodeMirror](https://img.shields.io/badge/CodeMirror-6-red.svg)](https://codemirror.net/)

The interactive web client and AI workbench for **Distributed Lovable**. Features a split-view IDE layout with real-time SSE chat streaming, syntax-highlighted code editor, file tree navigation, in-iframe runtime error interception, and instant live preview.

---

## ✨ Features

- **Split-View Web IDE**: Resizable panels powered by `react-resizable-panels` allowing simultaneous AI chat, code inspection, and live preview.
- **Real-Time SSE Parser**: Streams granular events directly from Spring AI:
  - 💡 **Thoughts**: Model thinking indicator with duration timing.
  - 🔍 **Tool Logs**: Badges detailing files read by the AI architect.
  - 📝 **File Edits**: Interactive badges showing files modified in real time.
  - 💬 **Markdown Message**: GitHub Flavored Markdown (GFM) streaming rendering.
- **In-Iframe Error Interceptor (`public/error-catcher.js`)**:
  - Automatically captures uncaught runtime errors, unhandled promise rejections, console errors, and Vite compile overlays from inside the preview iframe.
  - Posts messages to the parent window and presents an interactive **"Fix with AI"** alert that feeds error stack traces directly into the next prompt.
- **Multi-Tab Code Editor**: CodeMirror 6 with GitHub Dark theme and syntax highlighting for TypeScript, JavaScript, CSS, JSON, and HTML.
- **Project Collaboration**: Role-based access control (OWNER, EDITOR, VIEWER) with invitation modal.
- **Full ZIP Export**: One-click download of the entire project codebase.

---

## 🚀 Quickstart

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment
```bash
# Copy environment configuration
cp .env.example .env
```
Ensure `VITE_API_URL` points to your API Gateway (default: `http://localhost:8080`).

### 3. Start Development Server
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 📦 Tech Stack
- **Framework**: React 18, Vite, TypeScript
- **UI Components**: Radix UI, Shadcn UI primitives, Lucide Icons
- **Styling**: Tailwind CSS, Tailwind Animate
- **Editor**: `@uiw/react-codemirror` (v4)
- **Data Fetching**: `@tanstack/react-query` (v5)
- **Routing**: `react-router-dom` (v6)

---

## 📜 License
MIT License.
