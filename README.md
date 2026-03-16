# AI Resume Analyzer & Intelligent Job Match Platform

## Project Overview

A fully production-ready SaaS platform that uses AI to analyze resumes, match jobs, and help candidates land their dream jobs. Built with a premium Silicon Valley-level UI/UX.

## Key Features

### For Candidates
- **AI Resume Analysis** — Upload PDF/DOCX, get instant score (0–100), ATS analysis, skill extraction, and improvement suggestions
- **Job Matching** — Semantic matching with compatibility scores against curated job listings
- **AI Rewrite Tool** — GPT-powered resume rewrite suggestions
- **Analytics Dashboard** — Skill gap charts, radar charts, weekly activity
- **Resume History** — Track multiple resume versions and their scores
- **Job Browser** — Browse and save matched jobs with one-click apply

### For Recruiters
- **Post Jobs** — Define required skills and experience levels
- **AI Ranking** — Automatically rank candidates by resume compatibility
- **Candidate Shortlisting** — Filter, compare, and export candidates
- **Analytics** — Track posting performance and candidate pipeline

### For Admins
- **User Management** — View, manage, and moderate all users
- **AI Usage Monitoring** — Track API calls, scan counts, and system health
- **Revenue Analytics** — MRR, plan distribution, subscription management
- **Platform Analytics** — DAU, conversion rates, performance metrics

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | React 18 + TypeScript |
| Build | Vite 7 (with manual chunk splitting) |
| Styling | Tailwind CSS 3 + custom CSS |
| Animations | Framer Motion 11 + GSAP |
| Charts | Recharts |
| State | Zustand (with localStorage persistence) |
| Routing | React Router DOM v6 |
| Icons | Lucide React |
| File Upload | React Dropzone |
| 3D/Physics | Three.js + Cannon.js (optional) |

## Design System

### Colors
- **Primary**: Indigo (`#6366f1` → `#4f46e5`)
- **Accent Purple**: `#a855f7`
- **Accent Cyan**: `#22d3ee`
- **Accent Pink**: `#ec4899`
- **Dark BG**: `#0a0a0f`
- **Dark Card**: `#111118`
- **Dark Border**: `#1e1e2e`

### CSS Classes
- `.glass` — Glassmorphism card (low blur)
- `.glass-strong` — High-blur glassmorphism
- `.glass-card` — Subtle card background
- `.gradient-text` — Indigo→Purple gradient text
- `.btn-primary` — Primary CTA button with glow
- `.btn-secondary` — Secondary glass button
- `.badge-{success|warning|danger|info|primary}` — Color badges
- `.skeleton` — Loading skeleton with shimmer effect
- `.dropzone` / `.dropzone-active` — File upload zones
- `.sidebar-item` / `.sidebar-item-active` — Navigation items

### Tailwind Extensions
- `shadow-glow` — Blue glow shadow
- `shadow-glow-lg` — Large blue glow shadow
- `animate-float` — Slow floating animation
- `animate-pulse-glow` — Pulsing glow animation
- `animate-gradient-shift` — Gradient background shift

## Project Architecture

```
src/
├── App.tsx                    # Root with routes, ToastProvider, AnimatedCursor
├── index.css                  # Global styles, glassmorphism, custom CSS
├── main.tsx                   # Entry point
├── types/
│   └── index.ts               # All TypeScript types
├── store/
│   ├── authStore.ts           # Zustand auth + theme store (persisted)
│   ├── resumeStore.ts         # Resume analyses store (persisted)
│   └── jobStore.ts            # Job listings + matching engine
├── components/
│   ├── ui/
│   │   ├── AnimatedCursor.tsx # Custom cursor with spring physics
│   │   ├── SharedComponents.tsx # ScoreRing, ProgressBar, TiltCard, Badge, Skeleton, StatCard
│   │   └── Toast.tsx          # Toast notification system
│   ├── animations/
│   │   └── Backgrounds.tsx    # ParticleBackground, FloatingOrbs, GridBackground
│   └── layout/
│       ├── Navbar.tsx         # Landing page navbar with user menu
│       ├── Footer.tsx         # Landing page footer
│       └── Sidebar.tsx        # Dashboard sidebar (role-aware)
├── pages/
│   ├── LandingPage.tsx        # Full landing page (hero, features, pricing, testimonials)
│   ├── auth/
│   │   ├── LoginPage.tsx      # Login with demo account hints
│   │   └── RegisterPage.tsx   # Register with role selection
│   ├── candidate/
│   │   ├── CandidateDashboard.tsx # 4-tab dashboard (overview, analysis, jobs, rewrite)
│   │   └── JobsPage.tsx       # Job listings browser with filters
│   ├── recruiter/
│   │   └── RecruiterDashboard.tsx # Recruiter panel with job posting, candidate table
│   ├── admin/
│   │   └── AdminPanel.tsx     # Admin with user management, analytics, revenue
│   └── shared/
│       ├── ProfilePage.tsx    # Profile/Settings (profile, security, notifications, billing, privacy)
│       └── NotFoundPage.tsx   # 404 page
```

## Demo Accounts

| Role | Email | Password |
|------|-------|---------|
| Candidate | `candidate@demo.com` | any |
| Recruiter | `recruiter@demo.com` | any |
| Admin | `admin@demo.com` | any |

You can also register any new email and choose a role during signup.

## Routes

| Path | Access | Description |
|------|--------|-------------|
| `/` | Public | Landing page |
| `/login` | Public | Login page |
| `/register` | Public | Register page |
| `/dashboard` | Candidate | Main candidate dashboard |
| `/jobs` | Authenticated | Job browser |
| `/profile` | Authenticated | Profile & settings |
| `/recruiter` | Recruiter | Recruiter dashboard |
| `/admin` | Admin | Admin panel |
| `*` | Public | 404 Not Found |

## AI Engine (Mock)

The resume analysis and job matching engines are fully simulated but production-realistic:
- **Resume Score**: 72–92 range with randomized variation per upload
- **ATS Issues**: Detects tables, missing LinkedIn, lacks metrics
- **Skill Extraction**: 10 predefined skills across technical/soft/tool categories
- **Job Matching**: Semantic-style matching based on skill overlap %
- **AI Rewrite**: Template-based professional resume rewrite suggestions

To integrate real AI (OpenAI API), replace `generateMockAnalysis()` in `resumeStore.ts` with actual API calls.

## Premium UI Features

1. **Custom Animated Cursor** — Spring physics, scaling on hover, trail effect
2. **Particle Background** — 30 floating particles with opacity fade
3. **Glassmorphism** — Multi-level glass effects (`glass`, `glass-strong`, `glass-card`)
4. **TiltCard** — 3D perspective tilt on mouse move
5. **Score Rings** — SVG animated circular progress with color thresholds
6. **Toast Notifications** — Spring-animated toasts (success/error/info/warning)
7. **Framer Motion** — Page transitions, stagger animations, scroll-triggered reveals
8. **Radar Charts** — Skill visualization with recharts
9. **Area Charts** — Weekly activity analytics
10. **Skeleton Loaders** — Shimmer effect on loading states

## Build & Development

```bash
# Install dependencies
npm install

# Development server
npm run dev

# Production build
npm run build
```

## Build Output (Optimized)

| Chunk | Size (gzip) | Contents |
|-------|-------------|---------|
| react-vendor | ~53 KB | React, ReactDOM, Router |
| charts | ~118 KB | Recharts |
| framer-motion | ~39 KB | Framer Motion |
| icons | ~6 KB | Lucide React |
| state | ~1 KB | Zustand |
| index | ~57 KB | App code |

## Subscription Plans

| Plan | Price | Scans | Features |
|------|-------|-------|---------|
| Free | $0 | 3/month | Basic analysis, job matching |
| Pro | $19/mo | Unlimited | Advanced AI, resume rewriting, ATS breakdown |
| Recruiter | $49/mo | Unlimited | Bulk ranking, AI filtering, export |

## Future Enhancements

- [ ] Real OpenAI/Anthropic API integration for actual resume parsing
- [ ] AWS S3 for secure resume file storage
- [ ] Real authentication with JWT tokens
- [ ] Email notifications with SendGrid
- [ ] LinkedIn import integration
- [ ] Multi-language resume support
- [ ] Chrome extension for job page analysis
- [ ] Team/company accounts for recruiters
- [ ] ATS integration with Greenhouse, Lever, Workday

## Notes for Development

- All state is persisted to `localStorage` via Zustand `persist` middleware
- Theme switching (dark/light) is in `authStore.ts` — currently only dark is fully styled
- `AnimatedCursor` is hidden on mobile (`pointer-events: none` via CSS media query)
- The `mock AI engine` returns realistic but randomized data on each file upload
- All files accepted are `.pdf` and `.docx` (validation in CandidateDashboard)
