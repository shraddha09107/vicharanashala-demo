<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6EE7B7,100:3B82F6&height=200&section=header&text=CrowdFAQ&fontSize=72&fontColor=ffffff&fontAlignY=38&desc=Vicharanashala%20×%20IIT%20Ropar%20Internship%20Knowledge%20Hub&descAlignY=60&descSize=16" width="100%"/>

<br/>

```
  ╔═══════════════════════════════════════════════════════════════╗
  ║   Interns ask.  Community answers.  Admins curate.           ║
  ║   Knowledge compounds — one question at a time.              ║
  ╚═══════════════════════════════════════════════════════════════╝
```

[![React](https://img.shields.io/badge/React_18-%2320232A.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)](https://jwt.io/)
[![Vite](https://img.shields.io/badge/Vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

<br/>

> **The problem every intern faces:**
> 300 new interns join. They all ask the same 40 questions.
> Answers drown in Slack. WhatsApp explodes. Emails pile up.
>
> **CrowdFAQ fixes this** — questions asked once, answered well,
> voted on, AI-moderated, and preserved forever.

<br/>

</div>

---

## 🗺️ How It Works

```
┌──────────────────────────────────────────────────────────────────────┐
│                                                                      │
│   INTERN                  COMMUNITY                    ADMIN         │
│                                                                      │
│   💬 Has a question       👥 Sees the post             🛡️ Reviews    │
│        │                       │                           │         │
│        ▼                       ▼                           ▼         │
│   🤖 NLP checks          ✍️ Answers +               ✅ Approve       │
│   for duplicates          votes roll in              → FAQ saved     │
│        │                       │                      ━━━━━━━━━━    │
│   📌 "Does this           🏆 Best answer             ❌ Reject       │
│   answer you?"            gets verified               → discarded    │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

Questions that pass NLP → posted to discussion board → community votes → admin promotes best answer → **permanent FAQ** ✨

---

## ⚡ Quick Start

### 🐳 Option A — Docker (zero config, recommended)

```bash
git clone https://github.com/your-org/Vicharanshala-FAQ-Generation.git
cd Vicharanshala-FAQ-Generation
docker-compose up
```

> Open `http://localhost:5173` — you're in.

---

### 🛠️ Option B — Manual Setup

<details>
<summary><b>Click to expand step-by-step instructions</b></summary>

**① Install dependencies**

```bash
cd server && npm install
cd ../client && npm install
```

**② Configure environment — create `server/.env`**

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/faqDB
JWT_SECRET=your_super_secret_key_here
JWT_EXPIRES_IN=7d
NODE_ENV=development
```

**③ Seed the database**

```bash
cd server

# Creates test accounts + sample categories + questions
npx ts-node src/scripts/seed.ts

# Optional: load real Vicharanashala FAQs
npx ts-node src/scripts/seed-vins-faqs.ts
```

**④ Start both servers**

```bash
# Terminal 1 — backend  →  http://localhost:5000
cd server && npm run dev

# Terminal 2 — frontend →  http://localhost:5173
cd client && npm run dev
```

</details>

---

## 🔑 Default Test Accounts

| Role | Email | Password | Access Level |
|:----:|-------|----------|-------------|
| 👑 **Admin** | `admin@faq.com` | `admin123` | Moderate · Approve · Analytics · Announce |
| 👤 **User** | `student1@faq.com` | `test123` | Ask · Answer · Vote · Comment |
| 👤 **User** | `student2@faq.com` | `test123` | Ask · Answer · Vote · Comment |

---

## ✨ Features

### 🎓 For Interns

| Feature | What it does |
|---------|-------------|
| 🔍 **Smart Search** | Full-text search across all FAQs and discussions |
| 💬 **Ask Questions** | NLP duplicate check runs first — "Does this already answer you?" |
| 🗳️ **Vote System** | Upvote helpful, downvote irrelevant — "Most Helpful FAQs" ranked live |
| 🌙 **Dark / Light Theme** | Toggle anytime; preference remembered across sessions |
| 🌐 **Multi-Language** | AI auto-translates FAQs — pick your preferred language |
| 🔔 **Notifications** | Alerted when your question gets answered or promoted to FAQ |
| 🤖 **AI Chatbot** | Ask anything in plain English — chatbot retrieves or generates answers instantly |
| 📚 **Learning Paths** | FAQs linked in sequences: `What is Python?` → `Install` → `Variables` → `Functions` |

### 🛡️ For Admins

| Feature | What it does |
|---------|-------------|
| 📥 **Moderation Queue** | Filter all pending posts by category or status |
| ✅ **Verify + Approve** | Mark best answer verified → one-click promotes to FAQ, archives discussion |
| ❌ **Reject** | Discard off-topic or low-quality threads |
| 📢 **Announcements** | Broadcast program-wide updates instantly |
| 📊 **Analytics Dashboard** | FAQ count · active users · top questions · unanswered search terms |
| 🧠 **Knowledge Gap Analyzer** | Surfaces "Top Missing FAQs" from unanswered searches — grow the knowledge base on real demand |

### 🤖 AI-Powered (Unique Features)

| Feature | How it works |
|---------|-------------|
| 🔁 **NLP Duplicate Detection** `✨` | Semantic similarity search before posting — stops duplicate questions at the gate |
| 🚨 **Auto Content Moderation** `✨` | Backend flags spam, malicious links, and inappropriate language before it goes live |
| ⚡ **AI FAQ Summary** `✨` | "Quick Summary" button on long answers — AI extracts key points in seconds |
| 🧩 **Personalized Recommendations** | Browsing history + search patterns → FAQs surfaced just for you |
| 📈 **Trending Score** | `trendingScore` = recency + votes + search clicks — always fresh, always relevant |

### 🏆 Community & Transparency (Unique Features)

| Feature | How it works |
|---------|-------------|
| 📜 **Version History + Diffs** `✨` | Every edit is tracked. Click "Edited" to see exactly what changed — transparent, tamper-evident |
| 🥇 **Community Heroes** | Weekly leaderboard · answers given · helpfulness score · 🥇 Gold / 🥈 Silver / 🥉 Bronze badges |
| ⏳ **Unanswered Queue** | Dedicated section: "Asked 3 hours ago — no answers yet" — contributors know where to go |
| 🗂️ **Smart Category Cards** | Shows question count · active discussions · trending topics · last activity — not just a label |
| 🎓 **Related Learning Paths** | Questions chained into guided sequences — FAQ becomes a mini-course |
| 🏅 **Expert Verified Badge** | Trusted admins badge critical answers — users know what to trust |

---

## 🗂️ Project Structure

```
Vicharanshala-FAQ-Generation/
│
├── 🐳 docker-compose.yml        ← one command to rule them all
├── 🚀 start.sh                  ← local dev shortcut
│
├── 📦 client/                   ← React 18 + Vite + Tailwind
│   └── src/
│       ├── components/
│       │   ├── answers/         ← AnswerForm
│       │   ├── auth/            ← AuthModal (login / signup)
│       │   ├── layout/          ← Navbar · Footer · PageLayout
│       │   ├── questions/       ← QuestionCard
│       │   ├── search/          ← SearchBar
│       │   └── votes/           ← VoteButtons ↑ ↓
│       │
│       ├── pages/
│       │   ├── HomePage.tsx           ← Hero + Popular + Most Voted
│       │   ├── QuestionsPage.tsx      ← Browse + filter
│       │   ├── QuestionDetailPage.tsx
│       │   ├── SearchPage.tsx         ← Full-text results
│       │   ├── AskQuestionPage.tsx
│       │   ├── CategoriesPage.tsx
│       │   ├── CommunityPage.tsx      ← Leaderboard + Heroes
│       │   ├── ProfilePage.tsx
│       │   └── AdminDashboard.tsx     ← Full moderation panel
│       │
│       ├── services/            ← Axios clients (questions · answers · search · admin)
│       ├── store/               ← authStore · uiStore (Zustand)
│       └── types/               ← Shared TypeScript interfaces
│
└── 🖥️  server/                  ← Node.js + Express + TypeScript
    └── src/
        ├── models/
        │   ├── User.ts
        │   ├── Question.ts      ← trendingScore · searchClickCount
        │   ├── Answer.ts        ← versionHistory []
        │   ├── Vote.ts
        │   ├── Category.ts      ← activeDiscussions · trendingTopics
        │   ├── SearchLog.ts     ← UnansweredSearch model
        │   └── Notification.ts
        │
        ├── modules/             ← controller + routes per feature
        │   ├── auth/
        │   ├── questions/       ← getMostSearched · recordSearchClick
        │   ├── answers/
        │   ├── votes/
        │   ├── search/
        │   ├── admin/
        │   └── recommendations/
        │
        └── scripts/
            ├── seed.ts              ← users · categories · sample Qs
            └── seed-vins-faqs.ts    ← domain FAQ seed
```

---

## 🔌 API Reference

> All protected routes require: `Authorization: Bearer <your_jwt_token>`

<details>
<summary><b>🔐 Authentication — /api/auth</b></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|:----:|-------------|
| `POST` | `/register` | — | Create new account |
| `POST` | `/login` | — | Login → signed JWT |

</details>

<details>
<summary><b>📚 FAQs — /api/faqs</b></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|:----:|-------------|
| `GET` | `/` | — | All approved FAQs; `?search=keyword` |
| `GET` | `/trending` | — | Top 10 by vote + search score |
| `GET` | `/recent` | — | 10 newest |
| `GET` | `/:id` | — | Single FAQ |
| `POST` | `/` | Admin | Create FAQ |
| `PATCH` | `/:id/approve` | Admin | Approve |
| `PATCH` | `/:id/upvote` | User | Upvote |
| `DELETE` | `/:id` | Admin | Delete |

</details>

<details>
<summary><b>💬 Discussions — /api/discussions</b></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|:----:|-------------|
| `GET` | `/` | — | List; `?category=` `?search=` `?sort=` |
| `GET` | `/:id` | — | Full thread with answers + comments |
| `POST` | `/` | User | Post new question |
| `POST` | `/:id/answers` | User | Submit answer |
| `POST` | `/:id/comments` | User | Add comment |
| `PATCH` | `/:id/upvote` | User | Upvote |
| `PATCH` | `/:id/downvote` | User | Downvote |
| `DELETE` | `/:id` | User | Delete own post |

</details>

<details>
<summary><b>📢 Announcements — /api/announcements</b></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|:----:|-------------|
| `GET` | `/` | — | All announcements |
| `POST` | `/` | Admin | Create |
| `DELETE` | `/:id` | Admin | Delete |

</details>

<details>
<summary><b>🛡️ Admin Panel — /api/admin</b></summary>

| Method | Endpoint | Auth | Description |
|--------|----------|:----:|-------------|
| `GET` | `/discussions` | Admin | All; filter `?category=` `?status=` |
| `GET` | `/analytics` | Admin | Dashboard stats |
| `PATCH` | `/discussions/:id/verify-answer` | Admin | Verify best answer |
| `PATCH` | `/discussions/:id/approve` | Admin | Promote → FAQ |
| `PATCH` | `/discussions/:id/reject` | Admin | Reject |
| `DELETE` | `/discussions/:id` | Admin | Hard delete |

</details>

---

## 🧱 Tech Stack

| Layer | Technology | Why we chose it |
|-------|-----------|-----------------|
| 🖼️ Frontend | React 18 + Vite | Blazing fast HMR, component-based architecture |
| 🎨 Styling | Tailwind CSS | Utility-first, no CSS bloat |
| 🗃️ State | Zustand | Tiny bundle, zero boilerplate global state |
| ⚙️ Backend | Node.js + Express + TypeScript | Type-safe API, flexible routing |
| 🍃 Database | MongoDB + Mongoose | Schema flexibility for evolving FAQ structures |
| 🔐 Auth | JWT + bcrypt | Stateless, scalable, industry standard |
| 📡 HTTP | Axios | Clean interceptors for auth headers |
| 🕷️ Scraping | Cheerio | Pull seed FAQs from samagama.in |

---

## 🗺️ Roadmap

```
PHASE 1 — FOUNDATION          PHASE 2 — AI LAYER           PHASE 3 — COMMUNITY
━━━━━━━━━━━━━━━━━━━           ━━━━━━━━━━━━━━━━━━           ━━━━━━━━━━━━━━━━━━━
✅ Community Q&A               📋 NLP Duplicate Check        📋 Version History + Diffs
✅ Voting system               📋 Auto Moderation            📋 Community Heroes Board
✅ Admin pipeline              📋 AI FAQ Summary             📋 Expert Verified Badge
✅ Full-text search            📋 AI Chatbot Assistant       📋 Smart Category Cards
✅ JWT Auth (RBAC)             📋 Personalized Recs          📋 Learning Paths
✅ Trending scores             📋 Knowledge Gap Analyzer     📋 Unanswered Queue
✅ Announcements               📋 Multi-Language Support     📋 Dark / Light Theme
✅ Categories + Filters
```

**Extended research features (Phase 4):**
- 📋 Completion meter — unsupervised model to estimate when a speaker will finish
- 📋 FLN-style multi-level engineering courses — data structures track, 100 levels
- 📋 BPS: Exploration vs Exploitation — smart placement decision engine
- 📋 Crowd-sourced confusion patterns + wording feedback loop

---

## 🤝 Contributing

We welcome contributions from all Vicharanashala interns and beyond.

```bash
# Fork → Clone → Branch → Code → PR

git clone https://github.com/your-username/Vicharanshala-FAQ-Generation.git
git checkout -b feature/your-feature-name
git commit -m "feat: describe what you built"
git push origin feature/your-feature-name
# → open a Pull Request on GitHub
```

**Commit message convention:**

| Prefix | Use for |
|--------|---------|
| `feat:` | New feature |
| `fix:` | Bug fix |
| `docs:` | Documentation update |
| `refactor:` | Code cleanup, no behaviour change |
| `chore:` | Dependency updates, config changes |

---

## 📄 License

```
MIT License — free to use, modify, and distribute.
Built with ♥ by the Vicharanashala × IIT Ropar Internship Cohort.
```

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:3B82F6,100:6EE7B7&height=100&section=footer" width="100%"/>

</div>
