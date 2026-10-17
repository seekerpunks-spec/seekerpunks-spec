# Hi, I'm sha-256 👋

**Self-taught builder based in Melbourne, Australia.** I build AI agents, LLM-powered apps, scrapers and automation, mostly in **TypeScript** and **Python**, and I ship them end to end: data pipelines, backends, payments, desktop apps and bots.

I build with AI coding agents every day and check their work with tests, evaluation sets and runtime smoke tests.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat&logo=openai&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-47848F?style=flat&logo=electron&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat&logo=socketdotio&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)

## 🛠️ Featured projects

### Bushpass: job finder desktop app for Working Holiday backpackers *(code private, [architecture write-up public](https://github.com/seekerpunks-spec/bushpass-architecture))*
A product that collects farm and regional job ads across Australia and works out which ones count towards a Working Holiday visa extension.
- **Next.js + Prisma (Postgres)** app with **16 scraper adapters** behind one common interface, a scheduler that re-scrapes whichever source is most overdue, and URL + hash deduplication.
- **Rules engine with an LLM fallback.** Hard rules decide eligibility. An OpenAI model only proposes a category as structured JSON with a confidence score, results are cached and versioned, and the LLM can never override the rules.
- **Electron desktop app** for macOS and Windows with **signed (ed25519) update manifests**. Windows builds run on GitHub Actions, and a Cloudflare Worker in front of R2 serves updates.
- **Licence and payments API.** A Stripe webhook issues a licence key by email, activation is tied to one device, and an LLM proxy keeps API keys off client machines.

> The product is currently offline. Diagram, design decisions, code excerpts and real screenshots are in **[bushpass-architecture](https://github.com/seekerpunks-spec/bushpass-architecture)**. I'm happy to give a code walkthrough on request.

### [brAIm](https://github.com/seekerpunks-spec/braim-discord-voice-bot): real-time voice AI bot for Discord *(public)*
A Discord bot that joins a voice channel and talks through OpenAI's **real-time voice API**, but only answers when it is addressed by name. It also handles noise-gated interruptions, daily usage quotas, leaving automatically when the channel is empty, and web search plus image/video generation tools.
TypeScript · discord.js voice · vitest test suite (90 tests).

### Sales-agent message guard: ML allow/block filter *(private)*
A lightweight local classifier, **built for a client's WhatsApp AI sales agent**, that checks messages before and after the agent replies and blocks unsafe or off-policy content, including prompt-injection attempts.
Python · scikit-learn (TF-IDF + logistic regression) · evaluation sets and regression tests · dependency-free inference.

### [Punk City](https://github.com/seekerpunks-spec/punk-city): multiplayer isometric browser game *(public)*
A Habbo-style social game: an isometric world rendered with PixiJS, A* pathfinding, real-time multiplayer with Socket.io, chat, friends, private apartments, a shop and server-validated player trades, with PostgreSQL persistence.
React · TypeScript · PixiJS · Node.js · Socket.io · PostgreSQL.

### [Multi-agent Discord orchestrator](https://github.com/seekerpunks-spec/discord-agent-orchestrator) *(public, prototype, not tested live)*
A Discord bot that routes a request to planner, developer and reviewer sub-agents, then merges their answers. It has allow-listed access and asks for confirmation before any external action.
TypeScript · OpenAI API.

## 📫 Get in touch

Open to **junior AI / automation roles in Australia & remote**. Private repos can be walked through on a call.
