# Leetcode-Total-Clone

A **full-stack LeetCode-style platform** with integrated **AI assistance**, real-time judging, and an **admin panel** for complete problem lifecycle management.

- **React + Node.js/Express** with a clean REST API boundary  
- Modular folder structure, ESLint + Prettier enforced

*Authentication & Security*
- **JWT-based Signup / Login** with refresh tokens
- **Password hashing** (bcrypt), rate-limiting and CORS hardening

*Problem Management*
- **Admin Panel** to **add / edit / delete** problems, tags and hidden test-cases  
- Rich-text editor for descriptions and Markdown rendering

*Online Code Editor*
- **Monaco-based** editor with syntax highlighting for JS, Python, C++, Java & Go  
- Theme toggling, auto-save drafts, and custom input

*Judge System*
- **Sandboxed runner** (Docker + seccomp) that compiles, executes and compares output against **hidden test-cases**  
- Real-time status updates: *Queued → Running → Accepted / Wrong Answer / Runtime Error / TLE*

*AI Integration*
- GPT-powered **chatbot** that provides context-aware *hints, explanations & complexity analysis*  
- **Plagiarism detection** using code-embedding similarity

*Video Support*
- Inline **YouTube / self-hosted video** player for solution walkthroughs

*Error Handling & Debugging*
- Granular API error codes, stack-trace logging with Winston, and circuit-breaker middleware

*Deployment & Scalability*
- **Docker-Compose** for local dev; Helm charts for Kubernetes  
- Horizontal scaling with sticky-session support via Redis  
- CDN-cached assets and lazy-loaded React chunks

***

## 🛠️ Tech Stack

| Layer          | Technology                              |
| -------------- | --------------------------------------- |
| Frontend       | **React**, Redux Toolkit, Vite, Tailwind CSS |
| Backend        | **Node.js**, Express, Socket.io, Redis      |
| AI Services    | Python (FastAPI), **OpenAI API**, Scikit-learn |
| DevOps         | Docker, GitHub Actions, Nginx, Kubernetes |

***

## 📂 Project Structure
```text
Leetcode-Total-Clone/
├── frontend/          # React SPA
├── backend/           # Express API

```

***

## 🚀 Quick Start

1. **Clone & Install**
   ```bash
   git clone https://github.com/adarshshuklaas/Leetcode-Total-Clone.git
   cd Leetcode-Total-Clone && ./scripts/setup.sh   # installs Node, Python & Docker deps
   ```

2. **Environment Variables**
   ```env
   # Mongo
   MONGODB_URI=mongodb://localhost:27017/leetcode

   # Auth
   JWT_SECRET=super-secret
   JWT_REFRESH_SECRET=another-secret

   # Redis
   REDIS_URL=redis://localhost:6379

   # AI
   OPENAI_API_KEY=sk-...
   ```

3. **Run All Services**
   ```bash
   docker-compose up --build
   ```
   Services:  
   -  Frontend `localhost:3000`  
   -  API `localhost:5000`  
   -  AI `localhost:8000`  

***

## 🔧 Selected API Endpoints
```http
# Auth
POST /api/auth/register       Sign-up
POST /api/auth/login          Login & receive tokens
GET  /api/auth/me             Current user profile

# Problems
GET  /api/problems            Query / filter problems
POST /api/problems            (Admin) create
PUT  /api/problems/:id        (Admin) update

# Submissions
POST /api/submissions         Submit & judge code
GET  /api/submissions/:id     Verdict + execution stats

# AI
POST /api/ai/hints            Context-aware hints
POST /api/ai/plagiarism       Similarity score
```

***

## 🤝 Contributing

1. Fork → feature branch → PR  
2. Pre-commit hooks enforce lint & 90% test coverage  
3. Describe **what / why** in commit messages

***

## 🗺️ Roadmap

- [ ] Mobile (React Native)
- [ ] Live pair-coding interviews
- [ ] Subscription & Stripe payments
- [ ] Advanced analytics dashboard

***

## 📄 License
MIT © 2025 Adarsh Shukla

[1](https://www.enacton.com/leetcode-clone/)
[2](https://www.youtube.com/watch?v=GnodscC2p-A)
[3](https://www.scribd.com/document/465766175/Clone-Graph-LeetCode)
[4](https://algo.monster/templates)
[5](https://www.youtube.com/watch?v=aXXZwyeTJ98)
[6](https://www.youtube.com/watch?v=igqiduZR-Gg)
[7](https://github.com/jpoly1219/go-leetcode)
[8](https://www.reddit.com/r/leetcode/comments/11dd1bv/a_great_template_for_recording_your_leetcode/)
[9](http://codesandbox.io/p/github/ratribiana/leetclone-AI)
[10](https://www.linkedin.com/posts/tanu-bisui-318056306_project-leetcode-clone-i-made-a-clone-activity-7200193214484533248-jXN5)
