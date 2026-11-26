

<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=30&center=true&vCenter=true&width=640&height=60&duration=3200&pause=900&color=58A6FF&lines=Hi%2C+I'm+Charlie+%F0%9F%91%8B;Backend+%26+distributed+systems;CS+%40+UWaterloo+%C2%B7+class+of+2028" alt="Hi, I'm Charlie. Backend and distributed systems. CS at UWaterloo, class of 2028." />
</h1>

<p align="center">
  <b>I build systems that stay correct under load, recover after crashes, and ship with numbers anyone can reproduce.</b>
</p>

<p align="center">
  <a href="https://linkedin.com/in/charliezhangck"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:c256zhan@uwaterloo.ca"><img src="https://img.shields.io/badge/Email-333333?style=for-the-badge&logo=gmail&logoColor=EA4335" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Open_to-Summer_2027_internships-2EA043?style=for-the-badge" alt="Open to Summer 2027 internships" />
</p>

---

### 👋 About me

- 🎓 **Computer Science @ University of Waterloo** (class of 2028)
- 💼 **Now: Software Developer Intern @ D2L.** Shipping LLM features to production
- 🧭 **Before: Full-stack @ The Traveller.** Generative-AI engine 
- 🎯 **Looking for:** Summer 2027 SWE internships in backend, infrastructure, or commerce
- 🏋️ **Off the keyboard:** powerlifting

---

### 🚀 Featured projects

#### ⚡ [Flashpoint](https://github.com/CharlieNotChilly/Flash-Point): a checkout engine that never oversells
`Ruby on Rails` `Redis Lua` `Sidekiq` `PostgreSQL` `k6` `Docker` `GitHub Actions`

- **Correctness:** 5,000 simultaneous buyers on 1,000 units → **exactly 1,000 orders, 0 oversold**, verified by an end-to-end stock invariant
- **Atomicity:** stock check, deduction, and hold creation happen in one Redis Lua call; 20 duplicate retries with the same idempotency key decrement stock once
- **Recovery:** confirmations stay in a Redis pending set until PostgreSQL commits; a reconciler re-queues lost jobs, and repeated delivery still produces **exactly one order**

<details>
<summary><b>How it works</b></summary>

```mermaid
flowchart LR
    Buyer[Buyer] --> API[Rails API]
    API -->|reserve / confirm in one Lua call| Redis[(Redis, AOF fsync always)]
    API -->|enqueue| Worker[Sidekiq writer]
    Worker -->|insert once per hold| PG[(PostgreSQL)]
    Sweeper[Sweeper] -->|expire holds, re-queue lost writes| Worker
```
</details>

#### 📦 [Shelfwise](https://github.com/CharlieNotChilly/Shelfwise): AI inventory forecasting for Shopify merchants
`Ruby on Rails` `Shopify GraphQL API` `Polaris` `Python` `LightGBM` `FastAPI`

- **Accuracy:** cut forecast error (WAPE) from **73.6% to 63.4%** vs. a moving-average baseline across 500 SKUs × 52 weeks, with rolling-origin refits and no future-data leakage
- **Product:** embedded Shopify app‡ that warns merchants before a SKU runs out, demoed on a dev store with **1,000‡** real orders
- **Integration:** syncs orders through GraphQL bulk operations and webhooks‡ with a cost-aware client that stays within Shopify's rate limits

<details>
<summary><b>How it works</b></summary>

```mermaid
flowchart LR
    Store[Shopify store] -->|bulk ops + orders/create webhook| App[Rails app]
    App -->|weekly sales per SKU| Model[FastAPI + LightGBM]
    Model -->|forecast| App
    App -->|stockout banner| Admin[Polaris admin UI]
```
</details>

#### 📈 [LineValue](https://github.com/CharlieNotChilly/Line-Value): real-time odds analytics & risk platform
`Python` `FastAPI` `asyncio` `Redis Streams` `PostgreSQL` `React` `Docker`

- **Ingestion:** at-least-once Redis Streams consumers with idempotent upserts normalize odds from **28‡ sportsbooks**: **4,800‡ quotes/s** in replay at **45 ms‡** p95
- **Serving:** de-vigged, leave-one-out pricing engine behind Redis-cached FastAPI at **38 ms‡** p99 under 200 concurrent clients
- **Evaluation:** with a frozen threshold, flagged prices beat the closing consensus **58%‡** of the time vs. **49%‡** for matched controls across **1,100‡** events

<details>
<summary><b>How it works</b></summary>

```mermaid
flowchart LR
    Odds[The Odds API] --> Poller[Async poller]
    Poller -->|raw corpus + XADD| Stream[(Redis Stream)]
    Stream --> Norm[Normalizers x4]
    Norm -->|idempotent upserts| PG[(PostgreSQL)]
    PG --> API[FastAPI + Redis cache] --> UI[React dashboard]
```
</details>

---

### 🛠️ Tech I use

**Languages & frameworks**<br/>
<img src="https://skillicons.dev/icons?i=ruby,rails,python,fastapi,ts,js,cs,cpp&perline=8" alt="Ruby, Rails, Python, FastAPI, TypeScript, JavaScript, C#, C++" />

**Backend, data & cloud**<br/>
<img src="https://skillicons.dev/icons?i=nodejs,redis,postgres,graphql,react,docker,aws,terraform&perline=8" alt="Node.js, Redis, PostgreSQL, GraphQL, React, Docker, AWS, Terraform" />

**DevOps & tools**<br/>
<img src="https://skillicons.dev/icons?i=grafana,githubactions,linux,git&perline=8" alt="Grafana, GitHub Actions, Linux, Git" />

---

### 📊 Activity

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=CharlieNotChilly&theme=github-dark-blue&hide_border=true&border_radius=10" alt="GitHub streak" />
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake-dark.svg" />
  <img alt="Snake eating my contributions" src="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake.svg" />
</picture>
