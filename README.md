<h1 align="center">Hi 👋, I'm Shubhanshu Jain</h1>
<h3 align="center">Full Stack Engineer @ GoPaisa · Node.js · React · PostgreSQL · LLM Agents · IIT (ISM) Dhanbad '25</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/shubhanshu-jain-iit-ism"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://minimal-portfolio-shubhanshu-dark-l.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-111111?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/></a>
  <a href="mailto:shubhanshujain2233@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <a href="https://codeforces.com/profile/Tanjiro_cp"><img src="https://img.shields.io/badge/Codeforces-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" alt="Codeforces"/></a>
  <a href="https://leetcode.com/u/sj_33/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"/></a>
  <a href="https://www.codechef.com/users/shubh_jain_1"><img src="https://img.shields.io/badge/CodeChef-5B4638?style=for-the-badge&logo=codechef&logoColor=white" alt="CodeChef"/></a>
</p>

## 🧑‍💻 About Me

I'm a Full Stack Engineer at **GoPaisa** (fintech, Noida), working on backend performance, data pipelines and internal tooling. Some of that work:
- Cut a production query from **2+ min to under 3 s**.
- Reduced CSV export memory from **2.5 GB to 400 MB**.
- Built a campaign analytics platform covering **1.2M+ clicks**.

Before that, as an AI Intern at **IncNut Digital**, I built **multi-agent RAG customer-support agents** that cut support workload by **60%**. I graduated with a B.Tech from **IIT (ISM) Dhanbad** in 2025.

I'm competitive programmer: **CodeChef 5★ (2029)** · **LeetCode Knight (2010)** · **Codeforces Specialist (1527)**.

I'm open to **SDE / Full Stack / Agentic AI** roles.

## 🤖 AI Application Development

<details>
<summary><b>IncNut Digital</b> — multi-agent RAG for customer support (AI Intern, Jul – Oct 2025)</summary>

**Stack:** Python, LangGraph, Flowise, Google Gemini API, OpenAI API
- **Multi-agent RAG:** built customer-support agents for the D2C brands **Vedix** and **SkinKraft**, which answer customer queries from brand knowledge.
- **Orchestration:** agent workflows built with LangGraph and Flowise.
- **Cancellation handling:** refined agent prompt logic to resolve order-cancellation issues, cutting cancellation blockers for **35.7% of users**.
- **Automation:** automated routine customer queries, reducing support workload by **60%**.
</details>

**AI skills:** multi-agent orchestration (LangGraph, Flowise) · RAG pipelines · prompt engineering · LLM API integration (Gemini, OpenAI, OpenRouter, DeepSeek) · streaming responses · tool-calling coding agents · n8n workflow automation

## 🔥 Projects

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/folio">Folio</a></b> — no-code portfolio builder with zero-deploy publishing · <a href="https://folio-green-omega.vercel.app">live</a></summary>

**Stack:** Next.js 16, TypeScript, PostgreSQL, Drizzle ORM, Better Auth, Turborepo, Zod
- **Live-preview editor** with draft autosave; publishes to permanent public URLs with no deploy step.
- **Turborepo monorepo** with pluggable themes and light/dark colour "Looks".
- Imports **AI-generated JSON**, validated with Zod.
- **Immutable versioned snapshots** for instant rollback.
</details>

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/pm2-auto-recovery-alerts">Phoenix</a></b> — health monitoring and SSH auto-recovery for PM2 "zombie" processes</summary>

**Stack:** Node.js, Express 5, MongoDB, node-ssh, PM2, Winston, Docker
- **Catches zombie states:** detects blocked event loops, DB deadlocks and memory leaks where PM2 still reports `online`.
- **Priority-ordered polling** with jitter; separates 200 (healthy), 503 (dependency down) and timeout (down).
- **Auto-recovery:** after N consecutive failures it SSHs in, runs `pm2 describe` to choose start or restart, then re-verifies health and logs telemetry.
- **Pluggable alerts:** Flock, Slack or Telegram.
- **Secured CRUD API:** timing-safe API-key auth and path-traversal checks.
</details>

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/AI-Compare">AI Compare</a></b> — Gemini vs DeepSeek, streamed side by side · <a href="https://ai-compare-steel.vercel.app/">live</a></summary>

**Stack:** React, Gemini 2.5 Flash-Lite SDK, OpenAI SDK via OpenRouter (DeepSeek V3), react-markdown
- **Parallel streaming:** sends one prompt to both models and streams each answer token by token.
- **Failure isolation:** each model runs independently, so one provider failing doesn't block the other.
- **Per-model history:** keeps multi-turn history for each model, persisted in localStorage.
- **Extensible:** adding another provider is a config change through OpenRouter.
</details>

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/URL-shortner">URL Shortener</a></b> — link shortener with click analytics and role-based admin</summary>

**Stack:** Node.js, Express 5, MongoDB, EJS, JWT
- **Click analytics:** logs a visit timestamp on every redirect.
- **Auth:** JWT stored in cookies, with role-based `restrictTo(roles)` middleware guarding an admin view.
</details>

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/MegaBlog">MegaBlog</a></b> — blogging platform on React + Appwrite</summary>

**Stack:** React, Redux Toolkit, React Router, React Hook Form, TinyMCE, Appwrite, Tailwind
- **Core features:** auth, protected routes, slug-based post CRUD and draft/active status.
- **Editing:** rich-text editor with image uploads.
- **Swappable backend:** Appwrite sits behind service classes, so it can be replaced without UI changes.
</details>

<details>
<summary><b><a href="https://github.com/Shubhanshu-ism/trello-clone">StickIt</a></b> — Trello-style drag-and-drop board</summary>

**Stack:** React, react-beautiful-dnd, Tailwind
- **Board:** drag cards across lists, with editable lists and cards and a detail modal.
- **Persistence:** board saved in localStorage, with one-click reset.
</details>

**Building now:** AI GitLab Coding Agent (Next.js + Docker agent loop → MR → CI auto-repair) · a from-scratch dnd-kit-style drag-and-drop library

## 🛠️ Tech Stack

<p>
  <img src="https://skillicons.dev/icons?i=ts,js,python,cpp,nodejs,express,nextjs,react,redux,tailwind,postgresql,mongodb,docker,kubernetes,nginx,linux,git,vercel" alt="TypeScript, JavaScript, Python, C++, Node.js, Express, Next.js, React, Redux, Tailwind, PostgreSQL, MongoDB, Docker, Kubernetes, Nginx, Linux, Git, Vercel" />
</p>

**Also:** FastAPI · WebSockets · SSE · PM2 · Drizzle · Sequelize · Turborepo · LangGraph · LangChain · Flowise · Gemini API · OpenAI API · OpenRouter · Multi-Agent RAG · n8n

## 📈 GitHub Stats

<p align="center">
  <img height="170" src="https://github-readme-stats.shion.dev/api?username=Shubhanshu-ism&theme=dark&hide_border=false&include_all_commits=false&count_private=false&show_icons=true" alt="GitHub stats for Shubhanshu-ism" />
  <img height="170" src="https://github-readme-stats.shion.dev/api/top-langs/?username=Shubhanshu-ism&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact" alt="Top languages for Shubhanshu-ism" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Shubhanshu-ism&theme=dark&hide_border=false" alt="GitHub streak for Shubhanshu-ism" />
</p>
