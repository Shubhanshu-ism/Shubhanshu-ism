<h1 align="center">Hi 👋, I'm Shubhanshu Jain</h1>
<h3 align="center">Full Stack Engineer @ GoPaisa | Node.js · React · PostgreSQL · LLM Agents | IIT (ISM) Dhanbad '25</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/shubhanshu-jain-iit-ism">LinkedIn</a> •
  <a href="https://shubhanshu-portfolio-one.vercel.app">Portfolio</a> •
  <a href="mailto:shubhanshujain2233@gmail.com">Email</a> •
  <a href="https://folio-green-omega.vercel.app">Folio (live)</a>
</p>

---

## 📌 Summary

**Shubhanshu Jain** — Full Stack Engineer at **GoPaisa** (fintech, Noida, India) since Jan 2026; B.Tech, **IIT (ISM) Dhanbad** (2021–2025). Works on production backend performance, data pipelines and internal tooling with **Node.js, React, PostgreSQL and MongoDB**, and builds LLM agents with **LangGraph, Gemini and OpenAI APIs**. Open to **SDE / Full Stack / Agentic AI Engineer** roles (Noida, relocation or remote).

**Experience at a glance**
- **GoPaisa** — Full Stack Engineer (Jan 2026 – Present): transaction-filter query **2+ min → <3 s**; CSV export memory **2.5 GB → 400 MB** and TTFB **70 s → 0.35 s** (253K rows, streaming + batching); campaign analytics platform for Policybazaar over **1.2M+ clicks**; CSV ingestion pipeline with SSE progress; SSE-based API failure monitor.
- **TableSprint** — Full Stack Developer Trainee (Nov – Dec 2025): responsive UI fixes on a MERN CRM.
- **IncNut Digital** — AI Intern, LLM Application Developer (Jul – Oct 2025): LangGraph/Flowise agents for Vedix & SkinKraft; **35.7%** fewer order-cancellation blockers, **60%** lower support workload.

---

## 🔥 Projects

### [Folio](https://github.com/Shubhanshu-ism/folio) — no-code portfolio builder · [live](https://folio-green-omega.vercel.app)
**Stack:** Next.js 16, TypeScript, PostgreSQL, Drizzle ORM, Better Auth, Turborepo, Zod
- Live-preview editor with draft autosave and **zero-deploy publishing** to permanent public URLs.
- Turborepo monorepo with **pluggable themes** and colour "Looks" (light/dark palettes).
- Content can be imported as **AI-generated JSON**, validated with Zod schemas.
- **Immutable versioned snapshots** of published portfolios for instant rollback.

### [Phoenix — PM2 Auto Recovery Alerts](https://github.com/Shubhanshu-ism/pm2-auto-recovery-alerts) — self-hosted health monitoring & auto-recovery
**Stack:** Node.js, Express 5, MongoDB (Mongoose), node-ssh, PM2, Winston, Helmet, Docker Compose
- Catches **application-level "zombie" states** PM2 can't see — blocked event loop, DB deadlocks, memory leaks — where the process shows `online` but requests time out.
- Poller runs every ~30 s with jitter, checking targets in **priority → sequence order**; each check sends an `x-health-token` with per-target timeouts.
- Distinguishes **healthy (200)**, **dependency down (503 → alert only)** and **down (timeout/unreachable → failure count)**.
- After `sshFailureThreshold` consecutive failures, **SSHs into the host** (key or password), runs `pm2 describe` to choose start vs restart, then **re-polls to verify recovery** and writes telemetry back to MongoDB.
- Recovery locks prevent duplicate restarts; failure state is in-memory, so it runs as a single process by design.
- **Pluggable alerting:** Flock (FlockML), Slack or Telegram, selected via `NOTIFICATION_PROVIDER`.
- **Secured target-management CRUD API:** API-key auth with `crypto.timingSafeEqual`, input validation, PM2 app-name allowlist regex and **path-traversal protection** on SSH key filenames.
- Ships with Dockerfile, docker-compose, CONTRIBUTING guide and full technical docs.

### [AI Compare](https://github.com/Shubhanshu-ism/AI-Compare) — side-by-side LLM comparison chat
**Stack:** React (Vite), Google Generative AI SDK (Gemini 2.5 Flash-Lite), OpenAI SDK via OpenRouter (DeepSeek V3), react-markdown + remark-gfm
- Sends one prompt to **Gemini and DeepSeek in parallel** and **streams both responses token-by-token** into separate panes.
- Each model runs independently, so one provider failing or rate-limiting doesn't block the other; errors are tagged by source.
- Keeps **per-model multi-turn conversation history**, with prompts and history persisted to localStorage.
- OpenRouter's OpenAI-compatible endpoint makes adding **other providers a config change**.
- Markdown/GFM rendering for code blocks and tables.

### [URL Shortener](https://github.com/Shubhanshu-ism/URL-shortner) — server-rendered link shortener with analytics
**Stack:** Node.js, Express 5, MongoDB (Mongoose), EJS, JWT
- Short IDs generated server-side; every redirect logs a timestamp to `visitHistory` for **click analytics**.
- **JWT auth in cookies**, with **role-based access** through a curried `restrictTo(roles)` middleware that guards an admin view of all users' links.
- MVC layout: routes, controllers, models, middlewares and an auth service.

### [MegaBlog](https://github.com/Shubhanshu-ism/MegaBlog) — blogging platform
**Stack:** React (Vite), Redux Toolkit, React Router, React Hook Form, TinyMCE, Appwrite, Tailwind CSS
- Auth (signup/login/logout), protected routes via an `AuthLayout` guard, and post CRUD with **slug-based URLs** and draft/active status.
- TinyMCE rich-text editor with image and code support, plus featured-image uploads to Appwrite Storage.
- Appwrite access wrapped in **service classes** (`auth`, `config`), so the backend can be swapped without touching UI code.
- Skeleton/shimmer loading states.

### [StickIt](https://github.com/Shubhanshu-ism/trello-clone) — Trello-style task board
**Stack:** React (Vite), react-beautiful-dnd, Tailwind CSS
- Drag-and-drop **cards across lists**, add/edit lists and cards, and a card detail modal.
- Board state persists to **localStorage**, with one-click reset to seed data.

### In progress
- **AI GitLab Coding Agent** (team of 4) — Next.js 14 + TypeScript agent that clones a GitLab repo into a Docker workspace, runs a read/edit/test tool loop, opens an MR and auto-repairs CI failures. Supports BYOK models (OpenAI, Anthropic, OpenRouter).
- **AI Coaching Agent** — voice-enabled AI tutor built with Next.js, Convex, Gemini, Web Speech API and Stack Auth.
- A from-scratch **dnd-kit-style drag-and-drop** library.

---

## 🛠️ Skills

- **Backend:** Node.js, Express.js, FastAPI, REST APIs, WebSockets, Server-Sent Events, PM2, JWT / OAuth
- **Databases:** PostgreSQL, MongoDB, Drizzle ORM, Sequelize, Mongoose, query optimization
- **Frontend:** React.js, Next.js, TypeScript, Redux Toolkit, Tailwind CSS, Material UI, React Virtuoso
- **AI / LLM:** LangGraph, LangChain, Flowise, Google Gemini API, OpenAI API, OpenRouter, DeepSeek, Multi-Agent RAG, n8n
- **DevOps & Tools:** Docker, Kubernetes, Nginx, CI/CD, Linux, Git, Postman, Turborepo, Vercel
- **Languages:** JavaScript (ES6+), TypeScript, Python, C, C++, SQL, HTML5, CSS3
- **CS fundamentals:** Data structures & algorithms, system design, OOP and design patterns, DBMS, operating systems

---

## 🏆 Competitive Programming

- **CodeChef:** 5★ (2029) — Starters 204: Rank 22 / 35K+ · Starters 199: Rank 14 / 32K
- **LeetCode:** Knight (2010) — Weekly 463: Rank 77 / 31K+ · Weekly 461: Rank 464 / 34K+
- **Codeforces:** Specialist (1527) — Round 1054 (Div. 3): Rank 483 / 19.7K+ · Round 1060 (Div. 2): Rank 1480 / 14.2K+
- **AtCoder:** 1393 — ABC 421: Rank 66 / 12.8K+ · ABC 418: Rank 334 / 16.1K+
- **JEE:** Main 99 percentile · Advanced top 0.7%

---

## 📈 GitHub Stats

<p align="center">
  <img height="170" src="https://github-readme-stats.shion.dev/api?username=Shubhanshu-ism&theme=dark&hide_border=false&include_all_commits=false&count_private=false&show_icons=true" alt="GitHub stats for Shubhanshu-ism" />
  <img height="170" src="https://github-readme-stats.shion.dev/api/top-langs/?username=Shubhanshu-ism&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact" alt="Top languages for Shubhanshu-ism" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Shubhanshu-ism&theme=dark&hide_border=false" alt="GitHub streak for Shubhanshu-ism" />
</p>

---

## 📫 Contact

- **Email:** shubhanshujain2233@gmail.com
- **LinkedIn:** [shubhanshu-jain-iit-ism](https://www.linkedin.com/in/shubhanshu-jain-iit-ism)
- **Portfolio:** [shubhanshu-portfolio-one.vercel.app](https://shubhanshu-portfolio-one.vercel.app)
- **Coding profiles:** LeetCode `sj_33` · Codeforces `Tanjiro_cp` · CodeChef `shubh_jain_1`
