
<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=30&center=true&vCenter=true&width=640&height=60&duration=3500&pause=800&color=58A6FF&lines=Hi%2C+I'm+Charlie+%F0%9F%91%8B;CS+%40+University+of+Waterloo;Building+systems+that+hold+up" alt="Typing intro" />
</h1>

<p align="center">
  <a href="https://linkedin.com/in/charliezhangck"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:c256zhan@uwaterloo.ca"><img src="https://img.shields.io/badge/Email-333333?style=for-the-badge&logo=gmail&logoColor=EA4335" alt="Email" /></a>
</p>

### About me

- 🎓 Computer Science at the **University of Waterloo** (class of 2028)
- 💼 Software Developer Intern, Generative AI\* at **D2L**: cut failed LLM generations by 60%‡, built a 221‡-case prompt-evaluation gate in CI, and led 6‡ co-ops taking a Grade Planner and Study Widgets to production for early 2027
- 🧭 Previously full-stack at **The Traveller**: a generative-AI proposal engine that cut drafting from 8 hours to 20 minutes, and Microsoft Entra ID SSO for 50+ staff
- 🔧 I care about correctness under load: idempotency, crash recovery, and numbers I can reproduce
- 🏋️ Powerlifter outside of code

### Featured projects

#### ⚡ [Flashpoint](https://github.com/CharlieNotChilly/Flash-Point): flash-sale checkout engine
`Ruby on Rails` `Redis Lua` `Sidekiq` `PostgreSQL` `k6` `Docker`
- 5,000 simultaneous buyers on 1,000 units: **exactly 1,000 orders, 0 oversold**
- Atomic Lua reservations, idempotency keys, and a reconciler that recovers lost jobs, all tested in CI

#### 📦 [Shelfwise](https://github.com/CharlieNotChilly/Shelfwise): AI inventory forecasting for Shopify
`Ruby on Rails` `Shopify GraphQL API` `Polaris` `Python` `LightGBM`
- Embedded Shopify app‡ that alerts merchants before stockouts, demoed on a dev store with 1,000‡ real orders
- Cut forecast error (WAPE) from **73.6% to 63.4%** vs. a moving-average baseline on 500 SKUs × 52 weeks, with no future-data leakage
- Syncs orders through GraphQL bulk operations and webhooks‡ within Shopify API rate limits

#### 📈 [LineValue](https://github.com/CharlieNotChilly/Line-Value): real-time odds analytics & risk platform
`Python` `FastAPI` `asyncio` `Redis Streams` `PostgreSQL` `React`
- At-least-once ingestion from **28‡ sportsbooks** with idempotent upserts: **4,800‡ quotes/s** in replay at **45 ms‡** p95
- De-vigged, leave-one-out pricing engine served at **38 ms‡** p99 under 200 concurrent clients
- Flagged prices beat the closing consensus **58%‡** of the time vs. **49%‡** for matched controls across 1,100‡ events

### Tech I use

<p>
  <img src="https://skillicons.dev/icons?i=ruby,rails,python,fastapi,ts,js,cs,cpp&perline=8" alt="Languages and frameworks" /><br/>
  <img src="https://skillicons.dev/icons?i=nodejs,redis,postgres,graphql,react,docker,aws,terraform&perline=8" alt="Backend, data, and cloud" /><br/>
  <img src="https://skillicons.dev/icons?i=grafana,githubactions,linux,git&perline=8" alt="DevOps and tools" />
</p>

### Activity

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=CharlieNotChilly&theme=github-dark-blue&hide_border=true&border_radius=10" alt="GitHub streak" />
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake-dark.svg" />
  <img alt="Snake eating my contributions" src="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake.svg" />
</picture>
