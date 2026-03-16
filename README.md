# AI Resume Analyzer & Intelligent Job Match Platform

## 🚀 Live Demo

🔗 **Try the platform:** https://gvxxpt599a.youware.app

---

# AI Resume Analyzer & Intelligent Job Match Platform

## 📌 Project Overview

A fully production-ready **SaaS platform** that uses **AI to analyze resumes, match jobs, and help candidates land their dream jobs**.

The platform simulates a **real-world recruitment ecosystem** with three user roles:

* Candidates
* Recruiters
* Admins

It provides **AI-driven resume scoring, ATS compatibility analysis, job matching, and analytics dashboards** with a **premium Silicon Valley–level UI/UX design**.

---

# ✨ Key Features

## 👨‍💻 For Candidates

### AI Resume Analysis

* Upload **PDF or DOCX resumes**
* Get **instant AI score (0–100)**
* ATS compatibility analysis
* Skill extraction
* Resume improvement suggestions

### Job Matching

* Semantic job matching engine
* Compatibility score with job listings
* Smart skill overlap detection

### AI Resume Rewrite Tool

* AI-powered resume rewriting
* Professional bullet suggestions
* Optimized ATS wording

### Analytics Dashboard

* Skill gap radar charts
* Weekly activity analytics
* Resume score tracking

### Resume History

* Track multiple resume versions
* Compare resume scores over time

### Job Browser

* Browse job listings
* Filter jobs
* Save jobs
* One-click apply

---

# 🏢 For Recruiters

### Job Posting

* Post new job openings
* Define required skills
* Add experience requirements

### AI Candidate Ranking

* Automatically rank candidates
* Resume compatibility scoring

### Candidate Shortlisting

* Filter applicants
* Compare candidates
* Export candidate lists

### Recruitment Analytics

* Job posting performance
* Candidate pipeline tracking

---

# 🛠 For Admins

### User Management

* Manage platform users
* Moderate accounts

### AI Usage Monitoring

* Track AI scans
* Monitor API calls
* System health monitoring

### Revenue Analytics

* Monthly recurring revenue (MRR)
* Subscription plan tracking

### Platform Analytics

* Daily active users
* Conversion rates
* Platform performance metrics

---

# 🧑‍💻 Tech Stack

| Layer            | Technology                      |
| ---------------- | ------------------------------- |
| Framework        | React 18 + TypeScript           |
| Build Tool       | Vite 7                          |
| Styling          | Tailwind CSS 3                  |
| Animations       | Framer Motion 11 + GSAP         |
| Charts           | Recharts                        |
| State Management | Zustand                         |
| Routing          | React Router DOM v6             |
| Icons            | Lucide React                    |
| File Upload      | React Dropzone                  |
| 3D / Physics     | Three.js + Cannon.js (optional) |

---

# 🎨 Design System

## Colors

Primary: **Indigo**
`#6366f1 → #4f46e5`

Accent Colors

* Purple — `#a855f7`
* Cyan — `#22d3ee`
* Pink — `#ec4899`

Dark Theme

* Background — `#0a0a0f`
* Card — `#111118`
* Border — `#1e1e2e`

---

# 🎯 UI Components

* Glassmorphism cards
* Animated cursor with spring physics
* Particle background
* Tilt 3D cards
* Score ring progress indicators
* Toast notification system
* Skeleton loaders
* Radar skill charts
* Analytics charts
* Animated page transitions

---

# 📂 Project Architecture

```
src/
├── App.tsx
├── main.tsx
├── index.css
│
├── types/
│   └── index.ts
│
├── store/
│   ├── authStore.ts
│   ├── resumeStore.ts
│   └── jobStore.ts
│
├── components/
│   ├── ui/
│   │   ├── AnimatedCursor.tsx
│   │   ├── SharedComponents.tsx
│   │   └── Toast.tsx
│   │
│   ├── animations/
│   │   └── Backgrounds.tsx
│   │
│   └── layout/
│       ├── Navbar.tsx
│       ├── Footer.tsx
│       └── Sidebar.tsx
│
├── pages/
│   ├── LandingPage.tsx
│   │
│   ├── auth/
│   │   ├── LoginPage.tsx
│   │   └── RegisterPage.tsx
│   │
│   ├── candidate/
│   │   ├── CandidateDashboard.tsx
│   │   └── JobsPage.tsx
│   │
│   ├── recruiter/
│   │   └── RecruiterDashboard.tsx
│   │
│   ├── admin/
│   │   └── AdminPanel.tsx
│   │
│   └── shared/
│       ├── ProfilePage.tsx
│       └── NotFoundPage.tsx
```

---

# 🔑 Demo Accounts

| Role      | Email                                           | Password |
| --------- | ----------------------------------------------- | -------- |
| Candidate | [candidate@demo.com](mailto:candidate@demo.com) | any      |
| Recruiter | [recruiter@demo.com](mailto:recruiter@demo.com) | any      |
| Admin     | [admin@demo.com](mailto:admin@demo.com)         | any      |

You can also register a **new account** and choose your role.

---

# 🌐 Routes

| Route        | Access        | Description         |
| ------------ | ------------- | ------------------- |
| `/`          | Public        | Landing Page        |
| `/login`     | Public        | Login Page          |
| `/register`  | Public        | Register Page       |
| `/dashboard` | Candidate     | Candidate Dashboard |
| `/jobs`      | Authenticated | Job Browser         |
| `/profile`   | Authenticated | Profile Page        |
| `/recruiter` | Recruiter     | Recruiter Dashboard |
| `/admin`     | Admin         | Admin Panel         |
| `*`          | Public        | 404 Page            |

---

# 🤖 AI Engine (Mock Implementation)

The AI engine simulates real-world resume analysis.

Features include:

* Resume score **72–92**
* ATS issue detection
* Skill extraction
* Job compatibility scoring
* AI resume rewriting suggestions

To integrate **real AI APIs**, replace the mock function:

```
generateMockAnalysis()
```

with OpenAI or other AI APIs.

---

# 💎 Premium UI Features

1. Custom Animated Cursor
2. Particle Background
3. Glassmorphism UI
4. 3D Tilt Cards
5. SVG Score Rings
6. Toast Notifications
7. Framer Motion Animations
8. Radar Charts
9. Area Analytics Charts
10. Skeleton Loaders

---

# ⚙️ Development Setup

## Install Dependencies

```
npm install
```

## Run Development Server

```
npm run dev
```

## Production Build

```
npm run build
```

---

# 📦 Build Optimization

| Chunk         | Size    | Description      |
| ------------- | ------- | ---------------- |
| react-vendor  | ~53 KB  | React ecosystem  |
| charts        | ~118 KB | Recharts         |
| framer-motion | ~39 KB  | Animations       |
| icons         | ~6 KB   | Lucide icons     |
| state         | ~1 KB   | Zustand          |
| index         | ~57 KB  | Application code |

---

# 💰 Subscription Plans

| Plan      | Price     | Features               |
| --------- | --------- | ---------------------- |
| Free      | $0        | Basic analysis         |
| Pro       | $19/month | Advanced AI tools      |
| Recruiter | $49/month | Bulk candidate ranking |

---

# 🚀 Future Enhancements

* Real AI resume parsing
* AWS S3 file storage
* JWT authentication
* Email notifications
* LinkedIn resume import
* Multi-language resume support
* Chrome extension for job analysis
* Recruiter team accounts
* ATS integrations (Greenhouse, Lever, Workday)

---

# 🧠 Development Notes

* All state stored using **Zustand with localStorage persistence**
* Dark theme currently fully styled
* Animated cursor disabled on mobile
* Mock AI returns realistic randomized data
* Supported file formats: **PDF, DOCX**

---

# ⭐ Contributing

Contributions are welcome. Feel free to open issues or submit pull requests.

---

# 📜 License

MIT License

---

# 👩‍💻 Author

**Monali Pawar**
Computer Science Engineering Student
Passionate about **AI, Full Stack Development, and SaaS Platforms**








