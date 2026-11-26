<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=30&center=true&vCenter=true&width=640&height=60&duration=3500&pause=800&color=58A6FF&lines=Hi%2C+I'm+Charlie+%F0%9F%91%8B;CS+%40+University+of+Waterloo;Building+systems+that+hold+up" alt="Typing intro" />
</h1>

<p align="center">
  <a href="https://linkedin.com/in/charliezhangck"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:c256zhan@uwaterloo.ca"><img src="https://img.shields.io/badge/Email-333333?style=for-the-badge&logo=gmail&logoColor=EA4335" alt="Email" /></a>
</p>

### About me

- 🎓 Computer Science at the **University of Waterloo** (class of 2028)
- 💼 Co-op at **D2L** on the Workforce / Learning Operations Hub team; previously full-stack at **The Traveller**, where I built a generative-AI proposal engine and Microsoft Entra ID SSO
- 🔧 I care about correctness under load: idempotency, crash recovery, and numbers I can reproduce
- 🏋️ Powerlifter outside of code

### Featured projects

#### ⚡ [Flashpoint](https://github.com/CharlieNotChilly/Flash-Point): flash-sale checkout engine
`Ruby on Rails` `Redis Lua` `Sidekiq` `PostgreSQL` `k6` `Docker`
- 5,000 simultaneous buyers on 1,000 units: **exactly 1,000 orders, 0 oversold**
- Atomic Lua reservations, idempotency keys, and a reconciler that recovers lost jobs, all tested in CI

#### 📦 [Shelfwise](https://github.com/CharlieNotChilly/Shelfwise): inventory forecasting for Shopify merchants
`Python` `LightGBM` `FastAPI` `Ruby on Rails`
- Cut forecast error (WAPE) from **73.6% to 63.4%** vs. a moving-average baseline on 500 SKUs × 52 weeks, with no future-data leakage
- Shopify app in progress

#### 📈 [LineValue](https://github.com/CharlieNotChilly/Line-Value): real-time odds analytics platform
`asyncio` `Redis Streams` `PostgreSQL` `React`
- 🚧 In design: at-least-once ingestion with idempotent writes and a leak-proof closing-line backtest (spec and build plan in the repo)

### Tech I use

<p>
  <img src="https://skillicons.dev/icons?i=ruby,rails,python,fastapi,ts,js,cs,cpp&perline=8" alt="Languages and frameworks" /><br/>
  <img src="https://skillicons.dev/icons?i=redis,postgres,react,docker,aws,githubactions,linux,git&perline=8" alt="Infrastructure and tools" />
</p>

### Activity

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=CharlieNotChilly&theme=github-dark-blue&hide_border=true&border_radius=10" alt="GitHub streak" />
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake-dark.svg" />
  <img alt="Snake eating my contributions" src="https://raw.githubusercontent.com/CharlieNotChilly/CharlieNotChilly/output/github-contribution-grid-snake.svg" />
</picture>
