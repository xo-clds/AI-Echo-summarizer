# 🎬 Echo Summarizer — AI Video Intelligence & Learning Platform

Transform any YouTube video into structured knowledge with AI-powered summaries, chapters, insights, concept maps, and interactive chat.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Backend-3FCF8E?logo=supabase&logoColor=white)

---

## ✨ Features

- **🎯 AI Video Summarization** — Paste any YouTube URL and get an instant AI-generated summary
- **📑 Auto Chapters** — Automatically generated chapter breakdowns with timestamps
- **💡 Key Insights** — Extracts key concepts, important commands, and notable moments
- **🗺️ Concept Map** — Visual concept map generated from video content
- **💬 Chat with Video** — Ask questions about the video and get AI-powered answers with timestamp references
- **🔖 Save Videos** — Authenticated users can save analyzed videos to their library
- **🔐 Authentication** — Email-based signup/login with password reset support
- **📱 Responsive Design** — Works seamlessly on desktop and mobile

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| **React 18** | UI framework |
| **TypeScript** | Type safety |
| **Vite** | Build tool & dev server |
| **Tailwind CSS** | Utility-first styling |
| **shadcn/ui** | Component library (Radix UI primitives) |
| **Framer Motion** | Animations |
| **React Router** | Client-side routing |
| **TanStack React Query** | Server state management |
| **React Markdown** | Markdown rendering |
| **Recharts** | Charts & data visualization |
| **Sonner** | Toast notifications |

### Backend (Supabase / Lovable Cloud)
| Technology | Purpose |
|---|---|
| **Supabase Auth** | User authentication |
| **Supabase Database (PostgreSQL)** | Data persistence |
| **Supabase Edge Functions (Deno)** | Serverless backend logic |
| **Google Gemini AI** | Video analysis, chat, concept maps (via Lovable AI Gateway) |

---

## 📁 Project Structure

```
├── src/
│   ├── components/          # React components
│   │   ├── ui/              # shadcn/ui base components
│   │   ├── ChaptersTab.tsx   # Chapter breakdown view
│   │   ├── ChatTab.tsx       # Chat with video interface
│   │   ├── ConceptMapTab.tsx  # Visual concept map
│   │   ├── ExplainDialog.tsx  # AI explanation dialog
│   │   ├── InsightsTab.tsx    # Key insights view
│   │   ├── LoadingAnalysis.tsx # Loading state
│   │   ├── SavedVideos.tsx    # Saved videos list
│   │   ├── SummaryTab.tsx     # Summary view
│   │   ├── UrlInput.tsx       # YouTube URL input
│   │   └── VideoPlayer.tsx    # Embedded YouTube player
│   ├── hooks/               # Custom React hooks
│   │   ├── use-auth.tsx      # Authentication hook
│   │   ├── use-youtube-player.ts # YouTube player control
│   │   └── use-mobile.tsx    # Responsive detection
│   ├── integrations/
│   │   └── supabase/        # Auto-generated Supabase client & types
│   ├── lib/
│   │   ├── types.ts         # TypeScript interfaces
│   │   ├── utils.ts         # Utility functions
│   │   └── youtube.ts       # YouTube helpers
│   ├── pages/
│   │   ├── Index.tsx        # Main app page
│   │   ├── Auth.tsx         # Login/Signup page
│   │   ├── ResetPassword.tsx # Password reset
│   │   └── NotFound.tsx     # 404 page
│   ├── App.tsx              # App root with routing
│   ├── main.tsx             # Entry point
│   └── index.css            # Global styles & design tokens
├── supabase/
│   ├── functions/
│   │   ├── analyze-video/    # Video analysis edge function
│   │   ├── chat-with-video/  # Chat AI edge function
│   │   ├── explain-timestamp/ # Timestamp explanation edge function
│   │   └── generate-concept-map/ # Concept map generation edge function
│   └── config.toml          # Supabase configuration
├── tailwind.config.ts       # Tailwind configuration
├── vite.config.ts           # Vite configuration
└── package.json
```

---

## 🗄️ Database Schema

| Table | Description |
|---|---|
| `saved_videos` | Stores analyzed video data (title, summary, chapters, insights, transcript) per user |
| `profiles` | User profile information (display name, avatar, username) |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ & npm
- A Supabase project (or use Cloud)

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/echo-summarizer.git

# Navigate to the project
cd echo-summarizer

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Add your VITE_SUPABASE_URL and VITE_SUPABASE_PUBLISHABLE_KEY

# Start the dev server
npm run dev
```

The app will be available at `http://localhost:8080`.

### Environment Variables

| Variable | Description |
|---|---|
| `VITE_SUPABASE_URL` | Your Supabase project URL |
| `VITE_SUPABASE_PUBLISHABLE_KEY` | Your Supabase anon/public key |

Edge functions require `LOVABLE_API_KEY` for AI capabilities.

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
